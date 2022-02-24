---
title: Regulieren von Wechselkursen
description: Wenn Sie steuerpflichtige Umsätze in Fremdwährung abrechnen, müssen die offiziellen Kurse der Eidg. Steuerverwaltung zur MWST-Kursumrechnung verwendet werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a2ac0ae057f13bb3ab522bd9c542b66bba1d5304
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301061"
---
# <a name="adjust-exchange-rates"></a>Wechselkurse regulieren
Wenn Sie steuerpflichtige Umsätze in Fremdwährung abrechnen, müssen die offiziellen Kurse der Eidg. Steuerverwaltung zur MWST-Kursumrechnung verwendet werden.  

Wenn diese Kurse nicht mit den Währungskursen in den Einkaufs- oder Verkaufsrechnungen übereinstimmen, müssen Sie die MWST-Sätze später mit einer Stapelverarbeitung regulieren. Diese Regulierungen können nur mit einem autorisierten MWST-Satz durchgeführt werden.  

Sie können diese Stapelverarbeitung beliebig oft ausführen. Achten Sie aber darauf, sie immer vor der Erstellung einer MWST-Abrechnung auszuführen.  

> [!NOTE]  
>  Bei Verwendung einer Berichtswährung müssen Sie sicherstellen, dass das Feld **MWST-Kursregulierung** auf der Seite **Finanzbuchhaltung Einrichtung** auf **Keine Regulierung** gesetzt ist.  

Weitere Informationen über MWST und Fremdwährungen finden Sie auf der [ESTV](https://go.microsoft.com/fwlink/?LinkId=285999)-Website.  

## <a name="to-adjust-an-exchange-rate"></a>So regulieren Sie einen Wechselkurs  

1.  Wählen Sie ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") ein und wählen **Währungswechselkurs-Dienste** und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Wechselkurse** aus.  
3.  Geben Sie auf der Seite **Währungswechselkurse** den offiziellen MWST-Satz pro Periode für die jeweilige Währung in die Felder **Anzahl MWST-Einheiten** und **MWST-Kurs** ein.  
4.  Wählen Sie die Schaltfläche **OK** aus.  
5.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen"), öffnen Sie **Wechselkurse regulieren**, und wählen Sie dann den zugehörigen Link aus.  
6.  Füllen Sie auf dem Inforegister **Optionen** die Felder wie in der folgenden Tabelle beschrieben aus.   

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Startdatum**|Geben Sie ein Datum ein, um den Anfang der Periode festzulegen, für die Posten reguliert werden.|  
    |**Enddatum**|Geben Sie hier das letzte Datum ein, bis zu dem Posten reguliert werden sollen. Dieses Datum entspricht normalerweise dem Buchungsdatum im Feld **Buchungsdatum**.|  
    |**MWST-Kurs für Steuerverw. regulieren**|Geben Sie an, ob Sie den MWST-Wechselkurs regulieren möchten.|  

7.  Wählen Sie die Schaltfläche **Drucken**, um den Batchauftrag zu starten. Diese Stapelverarbeitung legt fest, ob MWST-Posten reguliert werden müssen. Ausserdem bereitet sie einen Regulierungsposten für jeden dieser Posten für die Fibukonten "Unrealisierte/realisierte Kursregulierung" vor. Die vorhandenen MWST-Posten werden ebenfalls korrigiert.  

## <a name="see-also"></a>Siehe auch  
 [Mehrwertsteuer (Schweiz)](swiss-value-added-tax.md)   
 [MWST-Sätze für die Schweiz](vat-rates-for-switzerland.md)   
[Währungswechselkurse aktualisieren](../../finance-how-update-currencies.md)  
[Einrichten einer Berichtswährung](../../finance-how-setup-additional-currencies.md)
