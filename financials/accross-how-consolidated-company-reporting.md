---
title: Konsolidieren Sie Daten aus mehreren Unternehmen | Microsoft Docs
description: "Verschaffen Sie sich die Zusammenfassungsansicht des Finanzstatus über Ihr Unternehmen."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 07/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 9739f89c45dd63d03235fef4204b2adeb48ac4d3
ms.contentlocale: de-ch
ms.lasthandoff: 12/14/2017

---

# <a name="how-to-work-with-the-consolidated-trial-balance-report"></a>Vorgehensweise: Arbeiten mit dem konsolidierten Bilanz-Bericht
Wenn Sie mehr als einen Mandanten haben [!INCLUDE[d365fin](includes/d365fin_md.md)], kann der konsolidierte Bilanz-Bericht im Buchhalter Rollen-Center Ihnen einen Überblick über den Finanzstatus Ihres Gesamtgeschäfts geben.  

Der Bericht Fibuposten (Fibu) kombiniert aus jedem Ihrer Mandanten in einem neuen Mandanten, den erstellen, um die konsolidierten Daten zu berücksichtigen. Dieses Unternehmen wird in der Regel als "konsolidiertes Unternehmen" bezeichnet. Der Konsolidierungsmandant ist einfach ein Container für die konsolidierten Daten und hat keine Verbindung zu den aktuellen Geschäftsdaten. Die Unternehmen, die Sie im konsolidierten Unternehmen einschliessen, wird zur **Geschäftseinheit** im Bericht.

Konsolidierungen können wie folgt und für Folgendes durchgeführt werden:  

* Die Mandanten, die verschiedene Kontenpläne haben.  
* Unternehmen, die verschiedene Geschäftsjahre und verschiedene Währungen verwenden.  
* Entweder den vollständigen Betrag oder einen angegebenen Prozentsatz der Finanzdaten eines bestimmten Mandanten
* Mittels der Wechselkurse der anderen Währung in den einzelnen Fibukonten

Je nach Komplexität Ihrer Unternehmen, gibt es zwei Arten, den Bericht einrichten:

* Wenn Sie nicht erweiterte Einstellungen benötigen, wie Einschliessen eines Unternehmens, dessen Sie nur ein Teil anlegen, können Sie die Felder **Mandanten-Konsolidierung** unterstützer Setup um raschen Einrichten einer Konsolidierung nutzen. Der Leitfaden führt Sie durch die grundlegenden Schritte durch.
* Wenn Sie erweitertere Einstellungen benötigen, können Sie den Konsolidierungsmandanten und die Konzernmandanten einrichten.

## <a name="to-do-a-simple-consolidation-setup"></a>Eine einfache Konsolidierungseinrichtung tun
Wenn die Konsolidierung einfach ist, weil Sie beispielsweise die Geschäftseinheit als Ganzes besitzen, führt Sie der unterstützte Setup **Mandanten-Konsolidierung** durch die folgenden Schritte:

* Wählen Sie aus, ob einen neuen Konsolidierungsmandanten erstellen oder ob die Daten in einem Mandanten konsolidiert werden, den Sie bereits für die Konsolidierung erstellt haben. Der Mandant sollte keine Transaktionen beinhalten.
* Ergebnisse in Vorschau anzeigen. [!INCLUDE[d365fin](includes/d365fin_md.md)] überprüft, dass die Masterdaten und die Transaktionen in den Konsolidierungsmandanten erfolgreich übertragen werden können.

Um die unterstützte Einrichtung zu starten, gehen Sie folgendermassen vor:

1. Im Feld **Buchhalter** wählen Sie Rollencenter **Unterstützte Einrichtung** Aktion aus.
2. Wählen Sie **Einrichten Konsolidierungsberichterstellung** und schliessen Sie dann jeden Schritt im unterstützten Setup ab.

## <a name="to-do-an-advanced-consolidation-setup"></a>Um eine erweiterte Konsolidierungseinrichtung zu tun
Wenn Sie erweitertere Einstellungen für die Konsolidierung benötigen, können Sie die Konsolidierung manuell einrichten. Wenn Sie Unternehmen haben, die Sie nur teilweise besitzen, oder Sie haben Mandanten, die nicht in der Konsolidierung enthalten sein soll. Die Einrichtung des konsolidierten Mandanten erfolgt auf die gleiche Weise wie die Einrichtung anderer Mandanten. Weitere Informationen finden Sie unter [Vorbereitungen für das Ausführen von Geschäften](ui-get-ready-business.md).  

[!INCLUDE[d365fin](includes/d365fin_md.md)]Mithilfe der Konsolidierungsfunktionen der Anwendung können Sie eine Liste der zu konsolidierenden Mandanten erstellen, die Buchhaltungsdaten vor der Konsolidierung überprüfen, Daten aus Dateien und Datenbanken importieren und die Konsolidierungsberichte generieren.  

1. Melden Sie sich im Konsolidierungsmandanten an.
2. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Geschäftseinheit** ein und wählen Sie den zugehörigen Link aus.  
3. Wählen Sie Aktion **Neu** aus, und füllen Sie die relevanten Felder aus.  

Wenn der Konzernmandant eine Fremdwährung verwendet, müssen Sie  den Wechselkurs angeben, der in der Konsolidierung verwendet werden soll. Sie müssen auch Konsolidierungdaten über die Sachkonten der Konzernmandanten angeben. In den folgenden Abschnitten werden diese Prozesse erläutert.

### <a name="to-prepare-general-ledger-accounts-for-consolidation"></a>Um die Fibuposten manuell für die Konsolidierung vorzubereiten
Wenn der Kontenplan des Konzernmandanten aus dem Konsolidierungsmandanten abweicht, müssen Sie die Fibukonten vorbereiten für die Konsolidierung. Sie können Konten definieren, um Soll- und Habenposten zu buchen und die Methode festlegen, die verwendet wird, um Währungen im Konsolidierungsmandanten zu übersetzen. Dies ist beispielsweise dann nützlich, wenn Sie häufig den Bericht ausführen.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben **Kontenplan** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie die Karte für das Konto, und füllen Sie dann die Felder im Inforegister **Konsolidierung** aus.

### <a name="to-specify-exchange-rates-for-consolidations"></a>Wechselkurse für Konsolidierungen angeben:
Richten Sie Wechselkurse für die Konsolidierung ein, wenn für die Finanzauswertungen eines Konzernmandanten nicht die Währung des konsolidierten Mandanten verwendet wird. Für jedes Konto bestimmt der Inhalt des Feldes **Konsol. Umrechnungsmethode** den Wechselkurses. Geben Sie auf jeder Konzernmandantenkarte im Feld **Währungswechselkurs** an, ob bei der Konsolidierung Wechselkurse des Konzernmandanten oder Wechselkurse des konsolidierten Mandanten verwendet werden sollen. Bei Verwendung von Wechselkursen des konsolidierten Mandanten können die Wechselkurse für einen Konzernmandanten geändert werden. Enthält bei einer Geschäftseinheit das Feld **Wechselkurstabelle** (auf der Konzernmandantenkarte) den Wert **Lokal**, kann der Wechselkurs auf der Konzernmandantenkarte geändert werden. Zwar werden die Wechselkurse aus der Tabelle **Währungswechselkurs** kopiert, Sie haben jedoch die Möglichkeit, diese Wechselkurse vor der Konsolidierung zu ändern.

Die folgende Tabelle beschreibt die Wechselkursmethoden, die Sie für Konten verwenden können.

|Wechselkurs | Typische Nutzung |
|---|---|
|Durchschnittskurs (manuell) | Der Durchnittskurs für den zu konsolidierenden Zeitraum berechnen Sie manuell. Sie berechnen den Durchschnitt entweder als arithmetisches Mittel oder als bestmögliche Schätzung und geben ihn für jeden Konzernmandanten ein. Für Erfolgsrechnung-Konten verwendet.|
|Ultimokurs | Für Kontenschema für Bilanz verwendet.|
|Letzter Ultimokurs | Schlusskurs: Der Schlusskurs am Devisenmarkt für den Tag, für den die Bilanz oder Erfolgsrechnung erstellt wird. Sie geben diesen Kurs für jeden Konzernmandanten ein. Für Kontenschema für Bilanz verwendet.|
|Historischer Kurs | Der Wechselkurs, der galt, als die Transaktion erfolgte.|
|Gemischter Wechselkurs | Mischkurs: Die Beträge der laufenden Periode werden zum Durchschnittskurs umgerechnet und zum zuvor erfassten Saldo für den konsolidierten Mandanten addiert. Diese Methode wird meistens für Gewinn- und Verlustkonten verwendet, da diese Beträge aus unterschiedlichen Perioden umfassen und daher mit verschiedenen Umrechnungskursen bestimmte Beträge vereinen.|
|Eigenkapitalkurs | Dieses ist ähnlich wie der **Mischkurs**. Differenzen werden gebucht, um Fibukonten zu trennen.|   

Um Wechselkurse für Konzernmandanten anzugeben, gehen Sie folgendermassen vor:

1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Geschäftseinheit** ein und wählen Sie den zugehörigen Link aus.  
2. Auf der Seite **Konzernmandantenliste** wählen Sie die Konzernmandanten aus, und wählen Sie die **Durchschnittskurs (manuell)** Aktion aus.   
3. Der Inhalt des Felds **Bezug auf Wechselkursbetrag** (im Fenster **Wechselkurs ändern**) wurde aus der Tabelle **Währungswechselkurs** kopiert, kann jedoch geändert werden. Schliessen Sie die Seite.  
4. Wählen Sie die **Ultimokurs**-Aktion aus.  
5. In dem Feld **Kurs** geben Sie den Wechselkurs ein.

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### <a name="to-exclude-a-company-from-consolidation"></a>Um einen Mandanten aus der Konsolidierung auszuschliessen
Wenn Sie keinen Konzernmandanten in die Konsolidierung einbeziehen, können Sie sie ausschliessen. Um das zu tun, wechseln Sie zur Konzernmandantenkarte, und löschen Sie das  Kontrollkästchen **Konsolidieren**.

### <a name="to-include-a-partially-owned-company-in-consolidation"></a>Um einen teilweis-eigenen Mandant in die Konsolidierung einzubeziehen
Wenn Sie nur einen Teil des Unternehmen anlegen, können Sie einen Prozentsatz jeder Transaktion einschliessen, der dem Prozentsatz des Mandanten entspricht, den Sie besitzen. Wenn beispielsweise 70% des Unternehmen anlegen, enthält $70 Konsolidierung einer Rechnung für $100. Um den Prozentsatz des Unternehmens anzugeben, den Sie anlegen, wechseln Sie zur Konzernmandantenkarte, und geben Sie den Prozentsatz im Feld **Konsolidierung %** ein.  

### <a name="to-test-the-data-before-you-consolidate"></a>Prüfen von Datenbanken vor der Konsolidierung
Sie können Ihre Daten testen, bevor Sie sie an den Konsolidierungsmandanten übertragen. [!INCLUDE[d365fin](includes/d365fin_md.md)]So überprüfen Sie Unterschiede zwischen den Informationen in den Konzernmandanten und dem Konsolidierungsmandanten Beispielsweise ob Kontonummern oder Dimensionscodes abweichen. Sie müssen Fehler korrigieren, bevor Sie den Bericht ausführen können. Sie können prüfen, die Datenbank oder, wenn Sie Daten einer XML-Datei importiert, können Sie testen die Datei.   

1. Öffnen Sie den Konsolidierungsmandanten.  
2. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Geschäftseinheit** ein und wählen Sie den zugehörigen Link aus.  
3. Führen Sie einen der folgenden Schritte aus:  

    * Um eine Datei zu testen, wählen Sie die **Datei prüfen** Aktion, geben Sie den Namen der Datei an zum Testen ein, und wählen Sie dann **Drucken** aus.  
    * Um die Datenbank zu testen, wählen Sie **Datenbank prüfen**.  

## <a name="to-run-the-consolidation"></a>Die Konsolidierung wird ausgeführt.
Nachdem Sie Ihre Daten geteste haben, können Sie diese an den Konsolidierungsmandanten übertragen.  

1. Melden Sie sich im Konsolidierungsmandanten an.  
2. Im Feld **Buchhalter-Rollencenter** wählen Sie Rollencenter **Konsolidierung ausführen** Aktion aus.  
3. Füllen Sie die entsprechenden Felder aus.  
4. Wählen Sie im Feld **Won**, in der Spalte **Unternehmensnamen.** wählen Sie das konsolidierte Unternehmen im Feld **ist** aus.  

## <a name="to-export-data-from-dynamics-nav-and-import-it-in-included365finincludesd365finmdmd"></a>Um Daten zu exportiern und Dynamics NAV in zu importieren[!INCLUDE[d365fin](includes/d365fin_md.md)]
Wenn sich ein Konzernmandant in einer anderen Datenbank befindet, müssen Sie die  Konsolidierungsdaten in eine Datei exportieren, bevor diese konsolidiert werden können. Jeder Mandant muss separat konsolidiert werden. Zu diesem Zweck wird in der Anwendung die Stapelverarbeitung **Konsolidierung exportieren** verwendet.  

Nachdem der Batchauftrag ausgeführt wurde, sind alle Posten in den einzelnen Fibukonten verarbeitet. Für jede Kombination aus ausgewählten Dimensionen und Datum wird der Inhalt des Felds **Betrag** der Posten summiert und exportiert. Die nächste Kombination aus ausgewählten Dimensionen und Datum mit derselben Kontonummer verarbeitet, danach die Kombinationen in der nächsten Kontonummer, usw.  

Die exportierten Posten enthalten die folgenden Felder: **Kontonr.**, **Buchungsdatum** und **Betrag**. Wenn auch Dimensionsdaten exportiert wurden, sind ebenfalls Dimensionscodes und Dimensionswerte enthalten.  

1. Für jede exportierte Zeile wird, sofern die Summe des **Betrag**-Felds ein Sollbetrag ist, die im **Konsol. Sollkonto** des Konzernmandanten eingerichtete Kontonummer in die Zeile exportiert. Ist die Summe ein Habenbetrag, wird die entsprechende Nummer im Feld **Konsol. Habenkonto** in die Zeile exportiert.  
2. Das für jede exportierte Zeile verwendete Datum ist entweder das Enddatum der Periode oder, wenn die Übertragung täglich erfolgt, das genaue Berechnungsdatum.  
3. Bei dem für den Posten exportierten Dimensionswert handelt es sich um den Dimensionswert des Konsolidierungsmandanten, der im Feld **Konsolidierungscode** für diesen Dimensionswert eingerichtet ist. Wurde im Feld **Konsolidierungscode** für diesen Dimensionswert kein Dimensionswert des Konsolidierungsmandanten eingerichtet, wird der Dimensionswert selbst in die Zeile exportiert.   
4. Die XML-Dateien enthalten auch die Währungswechselkurse innerhalb der Konsolidierungsperiode. Diese Wechselkurse sind in einem eigenen Abschnitt zu Beginn der Datei aufgeführt.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md)

