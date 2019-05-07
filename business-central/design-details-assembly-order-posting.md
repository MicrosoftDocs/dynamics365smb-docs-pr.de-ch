---
title: 'Designdetails: Montageauftragsbuchung | Microsoft Docs'
description: Die Montageauftragsbuchung basiert auf demselben Prinzip wie das Buchen ähnlicher Aktivitäten von Verkaufsaufträgen und von Produktionsverbrauch/-aushabe. Die Prinzipien werden jedoch insofern kombiniert, als Montageaufträge ihre eigene Buchungsbenutzeroberfläche, wie für Verkaufsaufträge, haben, während die tatsächliche Postenbuchung im Hintergrund als direkte Artikel- und Ressourcen Erf.-Journalbuchung, wie für den Fertigungsverbrauch, Ausgabe und Kapazität geschieht.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a26cafc11479d7065645947f63fa93d28ddb824f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "941787"
---
# <a name="design-details-assembly-order-posting"></a>Designdetails: Montageauftragsbuchung
Die Montageauftragsbuchung basiert auf demselben Prinzip wie das Buchen ähnlicher Aktivitäten von Verkaufsaufträgen und von Produktionsverbrauch/-aushabe. Die Prinzipien werden jedoch insofern kombiniert, als Montageaufträge ihre eigene Buchungsbenutzeroberfläche, wie für Verkaufsaufträge, haben, während die tatsächliche Postenbuchung im Hintergrund als direkte Artikel- und Ressourcen Erf.-Journalbuchung, wie für den Fertigungsverbrauch, Ausgabe und Kapazität geschieht.  

Ähnlich wie bei der Fertigungsauftragsbuchung werden die verbrauchten Komponenten und die verwendeten Ressourcen konvertiert und als Montageartikel ausgegeben, wenn der Montageauftrag gebucht wird. Weitere Informationen finden Sie unter [Designdetails: Produktionsauftragsbuchung](design-details-production-order-posting.md). Der Kostenfluss für Montageaufträge ist jedoch weniger Komplex, insbesondere da die Buchung der Montagekosten nur einmal geschieht und daher keinen WIP-Bestand generiert.  

Die folgenden Erf.-Journalbuchungen treten während der Montageauftragsbuchung auf:  

-   Das Artikel Erf.-Journal bucht die positiven Lagerposten, die Ausgabe des Montageartikels repräsentieren, aus dem Montageauftragskopf.  
-   Das Artikel Erf.-Journal bucht die negativen Lagerposten, die den Verbrauch von Montagekomponenten repräsentieren, aus Montageauftragszeilen.  
-   Das Ressourcen-Erf.-Journal bucht den Verbrauch von Montageressourcen (Zeiteinheiten) aus den Montageauftragszeilen.  
-   Das Kapazitäts Erf.-Journal bucht Wertposten bezüglich des Ressourcenverbrauchs, aus den Montageauftragszeilen.  

Das folgende Diagramm zeigt die Struktur von Artikel- und Ressourcenposten, die aus der Montageauftragsbuchung resultieren.  

![Artikel, Ressource und Kapazitätsposten, die sich aus der Montageauftragsbuchung ergeben](media/design_details_assembly_posting_1.png "Artikel, Ressource und Kapazitätsposten, die sich aus der Montageauftragsbuchung ergeben")  

> [!NOTE]  
>  Arbeitsplätze und Arbeitsplatzgruppen sind enthalten, um zu veranschaulichen, dass Kapazitätsposten aus der Produktion sowie aus der Montage erstellt werden.  

Die folgenden Diagramm zeigt, wie Montagedaten bei der Buchung in Buchungsposten eingehen.  

![Montage-verknüpfter Postenfluss bei der Buchung](media/design_details_assembly_posting_2.png "Montage-verknüpfter Postenfluss bei der Buchung")  

## <a name="posting-sequence"></a>Buchen der Sequenz  
Die Buchung eines Montageauftrags erfolgt in der folgenden Reihenfolge:  

1.  Die Montageauftragszeilen werden gebucht.  
2.  Der Montageauftragskopf wird gebucht.  

In der folgenden Tabelle wird die Aktionsfolge illustriert.  

|Aktion|Description|  
|------------|-----------------|  
|Buchung initialisieren|1.  Führen Sie Vorprüfungen durch.<br />2.  Fügen Sie die Buchungsnummer hinzu, und ändern Sie den Montageauftragskopf.<br />3.  Geben Sie den Montageauftrag frei.|  
|Buchung|<ol><li>Erstellen Sie den gebuchten Montageauftragskopf.</li><li>Kommentarzeilen kopieren.</li><li>Beitragsmontageauftragszeilen (Verbrauch):<br /><br /> <ol><li>Erstellen Sie ein Statusfenster, um den Montageverbrauch zu berechnen.</li><li>Erhalten Sie die Restmenge, auf der die Artikel Erf.-Journalzeile basiert.</li><li>Setzen Sie die verbrauchten und die verbleibenden Mengen zurück.</li><li>Für Montageauftragszeilen des Typs Artikel:<br /><br /> <ol><li>Füllen Sie die Felder in der Erf.-Journalzeile aus.</li><li>Übertragen Sie Reservierungen die Artikel Erf.-Journalzeile.</li><li>Buchen Sie die Artikel Erf.-Journalzeilen, um die Lagerposten zu erstellen.</li><li>Erstellen Sie Logistik Buch.-Blattzeilen, und buchen Sie sie.</li></ol></li><li>Für Montageauftragszeilen des Typs Ressource:<br /><br /> <ol><li>Füllen Sie die Felder in der Erf.-Journalzeile aus.</li><li>Buchen des Artikels Erf.-Journalzeile. Dies erstellt Kapazitätsposten.</li><li>Erstellen und buchen Sie Ressourcen-Erf.-Journalzeilen.</li></ol></li><li>Übertragen Sie Feldwerte aus der Montageauftragszeile in eine neu erstellte gebuchte Montageauftragszeile.</li></ol></li><li>Buchen Sie den Montageauftragskop (Ausgang):<br /><br /> <ol><li>Füllen Sie die Felder in der Erf.-Journalzeile aus.</li><li>Übertragen Sie Reservierungen die Artikel Erf.-Journalzeile.</li><li>Buchen Sie die Artikel Erf.-Journalzeilen, um die Lagerposten zu erstellen.</li><li>Erstellen Sie Logistik Buch.-Blattzeilen, und buchen Sie sie.</li><li>Setzen Sie die Montagemengen und die verbleibenden Mengen zurück.</li></ol></li></ol>|  

> [!IMPORTANT]  
>  Anders als für fertiggestellte Artikel, die zu den Soll-Kosten gebucht werden, wird Montageausstoß zu den Ist-Kosten gebucht.  

## <a name="cost-adjustment"></a>Regulierung Kosten  
 Sobald ein Montageauftrag gebucht wird, in der Bedeutung, dass Komponenten (Material) und Ressourcen in einen neuen Artikel montiert werden, soll die Bestimmung der Ist-Kosten dieses Montageartikels und die Kosten des aktuellen Lagerstatus der betroffenen Komponenten möglich sein. Dies wird durch Weiterleitung von Kosten von den gebuchten Posten der Quelle (den Komponenten und Ressourcen) an die gebuchten Posten des Ziels (die Montageartikel) erreicht. Die Weiterleitung der Kosten wird ausgeführt, indem neue Posten berechnet und generiert werden; diese werden als Regulierungsposten bezeichnet und den Zielposten zugeordnet.  

 Die weiterzuleitenden Montagekosten werden mithilfe des Auftragsebenenerkennungsmechanismus erkannt. Informationen über andere Ausgleichserkennungsmechanismen, siehe [Designdetails: Kostenanpassung](design-details-cost-adjustment.md)  

### <a name="detecting-the-adjustment"></a>Erkennen der Regulierung  
Die Entdeckungsfunktion auf Auftragsebene wird in Konvertierungsszenarien, der Produktion und bei der Montage verwendet. Die Feldfunktionen funktionieren wie folgt:  

-   Kostenregulierung wird erkannt, indem der Auftrag markiert wird, sobald eine Ressource oder ein Werkstoff als verbraucht/verwendet gebucht wird.  
-   Die Kostenweiterleitung entsteht durch Anwenden der Kosten aus dem Werkstoff oder der Ressource auf die Ausstoßposten, die mit dem Auftrag verknüpft sind.  

Die folgende Grafik zeigt die Regulierungspostenstruktur und die Regulierung der Montagekosten.  

![Montage-verknüpfter Postenfluss bei der Kostenanpassung](media/design_details_assembly_posting_3.png "Montage-verknüpfter Postenfluss bei der Kostenanpassung")  

### <a name="performing-the-adjustment"></a>Preiskorrektur durchführen  
Die Verteilung erkannter Regulierungen von Material- und Ressourcenkosten zu den Montageausgabeposten geschieht durch die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise**. Enthält die Funktion „Mehrstufiger Ausgleich“, die aus den folgenden zwei Elementen besteht:  

-   Nehmen Sie einen Montageauftrags-Ausgleich vor, welcher die Kosten aus dem Material- und Ressourcenverbrauch an den Montageausgangsposten weiterleitet. Zeilen 5 und 6 im nachstehenden Algorithmus sind dafür zuständig.  
-   Nehmen Sie Ein-Niveau-Anpassungen vor, welche die Kosten für einzelne Artikel mithilfe ihrer Lagerabgangsmethode weiterleiten. Rubriken 9 und 10 im nachstehenden Algorithmus sind für dafür zuständig.  

![Zusammenfassung des Kostenanpassungsregulierungsalgorithmus für Montagebuchung](media/design_details_assembly_posting_4.jpg "Zusammenfassung des Kostenanpassungsregulierungsalgorithmus für Montagebuchung")  

> [!NOTE]  
>  Das Element „WIP-Regulierungen“ auf den Zeilen 7 und 8 ist für die Weiterleitung von Produktionsmaterial und Kapazitätsnutzung an die Ausgabe nicht abgeschlossener Fertigungsaufträge verantwortlich. Dies wird nicht verwendet, wenn Montageauftragskosten reguliert werden, da der Begriff WIP nicht auf Montage angewendet wird.  

Weitere Informationen darüber, wie Kosten aus der Montage und aus der Produktion in die Fibu gebucht werden, finden Sie unter [Designdetails: Bestandesbuchung](design-details-inventory-posting.md).  

## <a name="assembly-costs-are-always-actual"></a>Montagekosten sind immer Ist-Kosten  
 Das Umlaufbestand- (WIP) Konzept gilt nicht in der Montageauftragsbuchung. Montagekosten werden nur als Ist-Kosten gebucht, nie als erwartete Kosten. Weitere Informationen finden Sie unter [Designdetails: Erwartete Kostenbuchung](design-details-expected-cost-posting.md).  

Dies wird durch die folgende Datenstruktur ausgeführt.  

-   Im Feld **Art** der Artikel Buch.-Blattzeilen in den Tabellen **Kapazitätsposten** und **Wertposten** Tabellen, wird *Ressource* verwendet, um Montageressourcenposten zu identifizieren.  
-   Im Feld **Lagerpostenart** der Artikel Erf.-Journalzeilen, in den Tabellen **Kapazitätsposten** und **Wertposten** Tabellen, werden *Montageausgabe* und *Montageverbrauch* verwendet, um die AusgabemontageLagerposten und verbrauchte Montagekomponentenposten zu identifizieren.  

Darüber hinaus werden Produktbuchungsgruppen im Montageauftragskopf und in den Montageauftragszeilen standardmäßig wie folgt ausgefüllt.  

|Einheit|Typ|Buchungsgruppe|Produktbuchungsgruppe|  
|------------|----------|-------------------|------------------------------|  
|Montageauftragskopf|Artikel|Lagerbuchungsgruppe|Produktbuchungsgruppe|  
|Montageauftragszeile|Artikel|Lagerbuchungsgruppe|Produktbuchungsgruppe|  
|Montageauftragszeile|Ressource||Produktbuchungsgruppe|  

Entsprechend werden nur Ist-Kosten in der Finanzbuchhaltung gebucht, und keine Interimskonten werden aus der Montageauftragsbuchung eingegeben. Weitere Informationen finden Sie unter [Designdetails: Konten in der Fibu](design-details-accounts-in-the-general-ledger.md).  

## <a name="assemble-to-order"></a>Auftragsmontage  
Der Lagerposten, der aus der Buchung eines Auftragsmontageverkaufs resultiert, wurde für den entsprechenden Lagerposten für die Montageausgabe fest angewendet. Entsprechend werden die Kosten eines Auftragsmontageverkaufs aus dem Montageauftrag abgeleitet, mit dem er verknüpft wurde.  

Lagerposten des Typs Verkauf, die aus dem Buchen von Auftragsmontagemengen resultieren, werden mit **Ja** im Feld **Auftragsmontage** markiert.  

Das Buchen von Verkaufsauftragszeilen, bei denen ein Teil eine Lagermenge und ein anderer Teil eine Auftragsmontagemenge darstellt, führt zu separaten Lagerposten, einer für die Lagermenge und einer für die Auftragsmontagemenge.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Designdetails: Fertigungsauftragsbuchung](design-details-production-order-posting.md)   
 [Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)  
 [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
