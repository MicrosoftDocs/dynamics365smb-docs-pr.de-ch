---
title: Designdetails - Bestandbuchung | Microsoft Docs
description: Jede Bestandstransaktion, wie etwa eine Einkaufslieferung oder eine Verkaufslieferung, bucht zwei Posten unterschiedlichen Typs.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: dc3e997d0ca29c680cd6a915751a368dd77a5433
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880318"
---
# <a name="design-details-inventory-posting"></a>Designdetails: Bestandsbuchung
Jede Bestandstransaktion, wie etwa eine Einkaufslieferung oder eine Verkaufslieferung, bucht zwei Posten unterschiedlichen Typs.  

|Postenart|Description|  
|----------------|---------------------------------------|  
|Menge|Spiegelt die Menge im Bestand wider. Diese Informationen werden in Lagerposten gespeichert.<br /><br /> Begleitet von den Artikelausgleichsposten.|  
|Wert|Spiegelt die Änderung des Lagerwerts wider. Diese Informationen werden in Wertposten gespeichert.<br /><br /> Pro Lagerposten und pro Kapazitätsposten kann es einen oder mehrere Wertposten geben.<br /><br /> Informationen zu Kapazitätswertposten, die sich auf die Verwendung der Produktions- oder Montageressourcen beziehen, finden Sie unter [Designdetails: Produktionsauftragsbuchung](design-details-production-order-posting.md) .|  

 In Verbindung mit Mengenbuchungen gibt es Artikelausgleichsposten, um die Bestandserhöhung mit der Bestandsminderung zu verknüpfen. Dies ermöglicht dem Kalkulationsmodul, Kosten für Lagerzu- an die entsprechenden Abgänge weiterzuleiten und umgekehrt. [Weitere Informationen finden Sie unter "Designdetails: Artikelverfolgung".](design-details-item-application.md)  

 Lagerposten, Wertposten und Artikelausgleichsposten werden durch eine Artikel Erf.-Journalzeile erstellt, entweder indirekt durch Erfassen einer Auftragszeile oder direkt auf der Seite Fenster Artikel Erf.-Journal.  

 In regelmässigen dynamischen Abständen werden Wertposten, die im Bestandsposten erstellt werden, in die Finanzbuchhaltung gebucht, um die beiden Bücher aus Finanzkontrollgründen abzugleichen. Weitere Informationen finden Sie unter [Designdetails: Abstimmung mit der Fibu](design-details-reconciliation-with-the-general-ledger.md).  

 ![Eintragsfluss beim Abgleich des Lagerbestands mit dem Sachkonto](media/design_details_inventory_costing_1_entry_flow.png "Eintragsfluss beim Abgleich des Lagerbestands mit dem Sachkonto")  

## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie Lagerposten, Wertposten und Artikelausgleichsposten zu Fibuposten führen.  

 Sie buchen eine Einkaufsbestellung als erhalten und fakturiert für 10 Artikel mit einem EK-Preis von MW 7 und einem Gemeinkostensatz von MW 1. Das Buchungsdatum ist 01-01-20. Die folgenden Einträge werden folgendermassen erzeugt:  

 **Lagerposten**  

|Buchungsdatum|Postentyp|Einstandsbetrag (tatsächl.)|Menge|Laufnr.|  
|------------------|----------------|----------------------------|--------------|---------------|  
|01-01-20|Einkauf|80.00|10|1|  

 **Wertposten**  

|Buchungsdatum|Postentyp|Einstandsbetrag (tatsächl.)|Lagerposten Laufnr.|Laufnr.|  
|------------------|----------------|----------------------------|---------------------------|---------------|  
|01-01-20|EK-Preis|70.00|1|1|  
|01-01-20|Kosten|10,00|1|2|  

 **Artikelausgleichsposten**  

|Laufnr.|Lagerposten Laufnr.|Eingeh. Lagerposten Laufnr.|Ausgeh. Lagerposten Laufnr.|Menge|  
|---------------|---------------------------|----------------------------|-----------------------------|--------------|  
|1|1|1|0|10|  

 Als nächsten Schritt buchen Sie einen Verkauf mit 10 Stück des Artikels mit einem Buchungsdatum aus 01-15-20.  

 **Lagerposten**  

|Buchungsdatum|Postentyp|Einstandsbetrag (tatsächl.)||Menge|Laufnr.|  
|------------------|----------------|----------------------------|-|--------------|---------------|  
|01-15-20|Verkauf|-80.00||-10|2|  

 **Wertposten**  

|Buchungsdatum|Postentyp|Einstandsbetrag (tatsächl.)|Lagerposten Laufnr.|Laufnr.|  
|------------------|----------------|----------------------------|---------------------------|---------------|  
|01-15-20|EK-Preis|-80.00|2|3|  

 **Artikelausgleichsposten**  

|Laufnr.|Lagerposten Laufnr.|Eingeh. Lagerposten Laufnr.|Ausgeh. Lagerposten Laufnr.|Menge|  
|---------------|---------------------------|----------------------------|-----------------------------|--------------|  
|2|2|1|2|-10|  

 Am Ende der Buchhaltungsperiode führen Sie die Stapelverarbeitung **Lagerreg. buchen** aus, um diese Lagertransaktionen mit der Fibu abzustimmen.  

 Weitere Informationen finden Sie unter [Designdetails: Konten in der Fibu](design-details-accounts-in-the-general-ledger.md).  

 Die folgenden Tabellen zeigen das Ergebnis der Abstimmung der Lagertransaktionen in diesem Beispiel mit der Finanzbuchhaltung.  

 **Wertposten**  

|Buchungsdatum|Postentyp|Einstandsbetrag (tatsächl.)|Gebuchte Lagerregulierung an G/L|Lagerposten Laufnr.|Laufnr.|  
|------------------|----------------|----------------------------|-------------------------|---------------------------|---------------|  
|01-01-20|EK-Preis|70.00|70.00|1|1|  
|01-01-20|Kosten|10,00|10,00|1|2|  
|01-15-20|EK-Preis|-80.00|-80.00|2|3|  

 **Fibuposten**  

|Buchungsdatum|Fibukonto|Kontonr. (En-US-Demo)||Betrag|Laufnr.|  
|------------------|------------------|---------------------------------|-|------------|---------------|  
|01-01-20|[Lagerkonto]|2130||70.00|1|  
|01-01-20|[Direkte Kosten Verrech.-Konto]|7291||-70.00|2|  
|01-01-20|[Lagerkonto]|2130||10,00|3|  
|01.01.07|[Gemeinkostenverrechnungskonto]|7292||-10.00|4|  
|01-15-20|[Lagerkonto]|2130||-80.00|5|  
|01-15-20|[COGS-Konto]|7290||80.00|6|  

> [!NOTE]  
>  Das Buchungsdatum der Fibuposten ist das gleiche wie für die zugehörigen Wertposten.  
>   
>  Das Feld Im S**achbuch gebuchte Kosten** in der Tabelle **Wertposten** wird ausgefüllt.  

 Die Beziehung zwischen Wertposten und Fibuposten wird in der Tabelle **Fibuposten - Lagerpostenverbindung** gespeichert.  

 **Relationsposten im Sachkonto – Tabelle Artikelpostenrelation**  

|Fibuposten Laufnr.|Wertposten Lfd. Nr.|Fibujournalnr.|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## <a name="assembly-and-production-posting"></a>Montage- und Produktions-Buchung  
Kapazitäts- und Ressourcenposten repräsentieren die Zeit, die als bei Produktion oder Montage verbraucht gebucht wird. Diese Prozesskosten werden als Wertposten in der Finanzbuchhaltung zusammen mit den entsprechenden Materialkosten in einer ähnlichen Struktur gebucht, wie für Lagerposten in diesem Thema beschrieben.  

Weitere Informationen finden Sie unter [Designdetails: Montageauftragsbuchung](design-details-assembly-order-posting.md).  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Designdetails: Konten in der Finanzbuchhaltung](design-details-accounts-in-the-general-ledger.md)   
 [Designdetails: Kostenkomponenten](design-details-cost-components.md) [Verwalten der Lagerkosten](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
