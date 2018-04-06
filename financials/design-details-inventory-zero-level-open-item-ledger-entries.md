---
title: "Lagerposten öffnen"
description: Erfahren, warum der Lagerbestand Null ist, obwohl offene Lagerposten vorhanden sind.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 5ca7f39425ebbfa741b464f7421d798ee2d88bbd
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-known-item-application-issue"></a>Designdetails: Bekannte Artikelanwendungsprobleme
Dieser Artikel adressiert ein Problem, bei dem der Lagerebene Null ist, obwohl offene Lagerposten in existieren [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Der Artikel beginnt, indem die typischen Symptomen des Problems aufgeführt werden, gefolgt von den Grundlagen der Artikelanwendung bis hin zur Unterstützung der beschriebenen Gründen für dieses Problem. Am Ende des Artikels finden Sie eine Problemumgehung, um solche offenen Lagerposten zu adressieren.  

## <a name="symptoms-of-the-issue"></a>Symptome des Problems  
 Übliche Symptome des Problems mit Null Lagerbestand, obwohl offene Lagerposten vorhanden sind, sind die folgenden:  

-   Die folgende Nachricht, wenn Sie versuchen, eine Lagerbuchungsperiode abzuschliessen: "Das Lager kann nicht geschlossen werden, da es negativen Lagerbestand für einen oder mehrere Artikel gibt."  

-   Eine Lagerpostensituation, wo ein ausgehender Lagerposten und sein verwandter eingehender Lagerposten offen sind.  

     Siehe das nachfolgende Beispiel einer Lagerpostensituation.  

     |Postennr.|Buch. Datum|Postenart |Belegtyp|Belegnummer|Artikelnr.|Lagerortcode |Menge|Einstandsbetrag (tatsächl.)|Fakturierte Menge|Restmenge|Öffnen|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |333|01 28 2018|Verkauf|Verkaufslieferung|102043|TEST|BLAU|-1|-10|-1|-1|Ja|  
     |334|01 28 2018|Verkauf|Verkaufslieferung|102043|TEST|BLAU|1|10|1|1|Ja|  

<!--![Why is inventory zero 1](media/helene/TechArticleInventoryZero1.png "Whyisinventoryzero\_1")-->

## <a name="basics-of-item-application"></a>Vorgaben des Artikelausgleichs  
 Es wird ein Artikelausgleichsposten für jede Lagertransaktion erstellt, um den Empfänger mit Kosten auf seine Herkunftsbelege mit Kosten zu verknüpfen, sodass die Kosten gemäss der Lagerabgangsmethode weitergeleitet werden können. [Weitere Informationen finden Sie unter "Designdetails: Artikelverfolgung".](design-details-item-application.md)  

-   Für einen eingehenden Lagerposten wird der Artikelausgleichsposten erstellt, wenn der Lagerposten erstellt wurde.  

-   Für einen ausgehenden Lagerposten wird der Artikelausgleichsposten erstellt, wenn der Lagerposten gebucht wird, WENN es einen offenen eingehenden Lagerposten mit verfügbarer Menge gibt, auf den er angewendet werden kann. Wenn es keinen offenen eingehenden Lagerposten gibt, für den er gelten soll, bleibt der ausgehende Lagerposten offen, bis ein eingehender Lagerposten, auf den er angewendet werden kann, für die Buchung angewendet werden kann.  

 Es gibt zwei Arten von Artikelausgleich:  

-   Mengenausgleich  

-   Ausgleich Lagerwert reguliert  

### <a name="quantity-application"></a>Mengenausgleich  
 Mengenanträge werden für alle Lagertransaktionen gesetzt und werden automatisch oder manuell in den Systemprozessen erstellt. Wenn sie manuell gesetzt werden, werden Mengenanwendungen als fester Ausgleich behandelt.  

 Das folgende Diagramm zeigt, wie Mengenanträge gemacht werden.  

![Warum der Lagerbestand Null 2 ist](media/helene/TechArticleInventoryZero2.png "Whyisinventoryzero\_2")

 Beachten Sie weiter, dass Lagerposten 1 (Einkauf) sowohl Lieferant des Artikels und die Kostenquelle für den ausgeglichenen Lagerposten, Lagerposten 2 (Verkauf) ist.  

> [!NOTE]  
>  Wenn der ausgehende Lagerposten zum durchschnittlichen Einstandspreis bewertet wird, dann ist der eingehende Lagerposten nicht der einzigartige Kostenursprung. Es gibt nur einer Rolle in der Berechnung des durchschnittlichen Einstandspreises der Periode wieder.  

### <a name="cost-application"></a>Ausgleich Lagerwert reguliert  
Der Kostenausgleich tritt nur in eingehenden Transaktionen auf, bei denen das Feld **Ausgegl. von Artikelposten** ausgefüllt ist, um einen festen Ausgleich zu erstellen. Das erfolgt in der Regel in Verbindung mit einer Verkaufsgutschrift oder einem Lieferungsszenario, das rückgängig gemacht wird. Die Kostenanwendung stellt sicher, dass der Artikel des Lagerbestands mit dem gleichen Einstandspreis erneut eingeben wird, wie als er geliefert wurde.  

Das folgende Diagramm zeigt, wie Kostenanträge gemacht werden.  

|Postennr.|Buch. Datum|Postenart |Belegtyp|Belegnummer|Artikelnr.|Lagerortcode |Menge|Einstandsbetrag (tatsächl.)|Fakturierte Menge|Restmenge|Öffnen|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|333|01 28 2018|Verkauf|Verkaufslieferung|102043|TEST|BLAU|-1|-10|-1|-1|Ja|  
|334|01 28 2018|Verkauf|Verkaufslieferung|102043|TEST|BLAU|1|10|1|1|Ja|  
<!--![Why is inventory zero 3](media/helene/TechArticleInventoryZero3.png "Whyisinventoryzero\_3")-->

 Beachten Sie darüber hinaus, dass eingehender Lagerposten 3 (Rücklieferung) ein Kostenempfänger für den ursprünglichen ausgehenden Lagerposten 2 (Verkauf) ist.  

## <a name="illustration-of-a-basic-cost-flow"></a>Abbildung eines grundlegenden Kostenflusses  
 Buchen Sie einen vollständigen Kostenfluss annehmen, in den ein Artikel geliefert wird, geliefert und fakturiert wird und mit der gleichen \-Kostenstornierung wieder geliefert wird.  

 Das folgende Diagramm zeigt den Kostenfluss.  

![Warum der Lagerbestand Null 4 ist](media/helene/TechArticleInventoryZero4.png "Whyisinventoryzero\_4")

 Beachten Sie darüber hinaus, dass die Kosten an Lagerposten 2 (Verkauf), dann an Lagerposten 3 (Rücklieferung) und zum Schluss an Lagerposten 4 weitergeleitet werden (Verkauf 2).  

## <a name="reasons-for-the-issue"></a>Gründe für das Problem  
 Übliche Symptome des Problems mit Null Lagerbestand, obwohl offene Lagerposten vorhanden sind, können wie folgt sein:  

-   Szenario 1: Eine Lieferung und eine Rechnung wird gebucht, obwohl der Artikel nicht verfügbar ist. Die Buchung wird dann mit den selben Kosten mit einer Verkaufsgutschrift storniert.  

-   Szenario 2: Eine Lieferung wird gebucht, obwohl der Artikel nicht verfügbar ist. Die Buchung wird dann mit der Lieferungsfunktion rückgängig gemacht.  

 Das folgende Diagramm zeigt, wie Artikelausgleiche in beiden Szenarien gemacht werden.  

![Warum der Lagerbestand Null 6 ist](media/helene/TechArticleInventoryZero6.png "Whyisinventoryzero\_6")  

 Beachten Sie darüber hinaus, dass ein Ausgleich mit Kosten (angezeigt durch die blauen Pfeile) sicherstellt, dass Lagerposten 2 (Rücklieferung) die gleichen Einstandspreis wie der Lagerposten hat, den er storniert, d.h. Lagerposten 1 zugeordnet ist (Verkauf 1). Es wird jedoch kein Mengenantrag (angezeigt durch die roten Pfeile) vorgenommen.  

 Lagerposten 2 (Rücklieferung) kann nicht gleichzeitig Kostenempfänger des Ursprungseintrags und Lieferant des Artikels und der Ursprung der Kosten sein. Daher bleibt der Lagerposten des ursprünglichen Verkaufs (Verkauf 1) offen, bis eine gültige Herkunft erscheint.  

## <a name="identifying-the-issue"></a>Festlegung des Ergebnisses  
 Um herauszufinden, wann die offenen Lagerposten erstellt werden, können Sie folgendermassen für das jeweilige Szenario vorgehen:  

 Für Szenario 1, können Sie das jeweilige Problem wie folgt erkennen:  

-   Im **Geb. Verkaufsgutschrift** oder **Gebuchte Rücksendung** Fenster suchen Sie im Feld **Ausgleich.\-vom Lagerposten**, um festzulegen, ob das Feld ausgefüllt ist, und in diesem Fall auf welche Lagerposten die Rücksendung angewendet wird.  

 Für Szenario 2 können Sie das jeweilige Problem in einer der folgenden Arten erkennen:  

-   Suchen Sie einen offenen ausgehenden Lagerposten und einen eingehenden Lagerposten mit derselben Nummer im Feld **Belegnr.** Feld und nach "Ja" in dem Feld **Korrektur**. Siehe das nachfolgende Beispiel einer solchen Lagerpostensituation.  

|Postennr.|Buch. Datum|Postenart |Belegtyp|Belegnummer|Artikelnr.|Lagerortcode |Menge|Einstandsbetrag (tatsächl.)|Fakturierte Menge|Restmenge|Öffnen|Storno|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|333|01 28 2018|Verkauf|Verkaufslieferung|102043|TEST|BLAU|-1|-10|-1|-1|Ja|Nr.|  
|334|01 28 2018|Verkauf|Verkaufslieferung|102043|TEST|BLAU|1|10|1|1|Ja|**Ja**|  
<!--![Why is inventory zero 7](media/helene/TechArticleInventoryZero7.png "Whyisinventoryzero\_7")-->

-   Im **Geb. Verkaufsgutschrift** suchen Sie im Feld **Ausgleich.vom Lagerposten**, um festzulegen, ob das Feld ausgefüllt ist, und in diesem Fall auf welche Lagerposten die Rücksendung angewendet wird.  

> [!NOTE]  
>  Anwendungen mit Kosten können nicht im Fenster **Ausgeglichene Artikelposten** identifiziert werden, da dieses Fenster nur Mengen-Anwendungen anzeigt.  

 Für beide Szenarien können Sie die beteiligte Anwendung mit Kosten, wie folgt erkennen:  

1.  Öffnen Sie die **Artikelausgleichsposten** - Tabelle.  

2.  Filtern im Feld **Lagerposten Laufnr.** anhand des Rücklieferungsartikelpostens.  

3.  Analysieren Sie den Artikelausgleichspostens und nehmen Sie folgendes zur Kenntnis:  

     Wenn das **Ausgeh. Lagerposten Laufnr.** Feld für einen eingehenden Lagerposten (positiv) erstellt wird, dann bedeutet dies, dass die eingehenden Lagerposten der Empfänger mit Kosten des ausgehenden Lagerpostens sind.  

     Siehe das nachfolgende Beispiel einer Artikelpostenanwendung.  

     |Postennr.|Lagerposten Laufnr.|Eingeh. Lagerposten Laufnr.|Ausgeh. Lagerposten Laufnr.|Menge|Buch. Datum|Ausgleich Lagerwert reguliert|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |299|334|334|333|1|01 28 2018|Ja|  
<!--![Why is inventory zero 8](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 Beachten Sie darüber hinaus, dass der eingehende Lagerposten 334 auf den ausgehenden Lagerposten 333 angewendet wird.  

## <a name="workaround-for-the-issue"></a>Gründe für das Problem  
 Im Fenster **Artikel Erf.-Journal** buchen Sie die folgenden Zeilen für den fraglichen Artikel:  

-   Ein positiver Zugang, um den offenen ausgehenden Lagerposten zu schliessen.  

-   Ein Abgang mit derselben Menge.  

     Diese Anpassung gleicht den Lagerbestand aus, der vom Lagerzugang verursacht wird und beendet den offenen eingehenden Lagerposten.  

 Das Ergebnis ist, dass der Lagerbestand Null ist und alle Lagerposten geschlossen werden.  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Artikelausgleich](design-details-item-application.md)   
[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)  

