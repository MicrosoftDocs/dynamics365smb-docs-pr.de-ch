---
title: Anzahl und Anpassen Inventar
description: 'Beschreibt, wie Sie den physischen Bestand zählen und mit Hilfe von Belegen den Lagerbestand anpassen können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 04/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="count-and-adjust-inventory-using-documents"></a>Erfassung und Regulierung des Lagerbestand mithilfe von Belegen

Sie können mithilfe der Inventurauftrags- und Inventurerfassungsbelege eine Inventur der Artikel durchführen. Die Seite **Inventurauftrag** wird verwendet, um das vollständige Inventurerfassungsprojekt zu organisieren, zum Beispiel eines pro Standort. Die Seite **Inventurerfassung** wird verwendet, um die tatsächliche Zählung von Artikeln zu erfassen und mitzuteilen. Sie können mehrere Aufzeichnungen für einen Auftrag erstellen, z. B. das Verteilen von Artikelgruppen an verschiedene Mitarbeitende.

Sie können den Bericht **Inventurerfassung** aus jeder Erfassung drucken und er enthält leere Mengenfelder zur Eingabe des gezählten Lagerbestands. Wenn Sie fertig mit der Erfassung sind und die Mengen auf der Seite **Inventurerfassung** eingegeben haben, wählen Sie die Schaltfläche **Fertigstellen** aus. Durch diese Aktion werden die Mengen an die entsprechenden Zeilen der Seite **Inventurauftrag** übertragen. [!INCLUDE [prod_short](includes/prod_short.md)] stellt sicher, dass Sie eine Artikelanzahl nicht doppelt erfassen können.  

> [!NOTE]
> Die Verwendung von Belegen für eine Inventurerfassung bietet eine grössere Kontrolle und unterstützt die Verteilung der Erfassung auf mehrere Mitarbeitende. Sie können die Aufgabe auch mithilfe von Erfassungsjournalen durchführen, wie auf den Seiten **Lagererfassungsjournale** und **Logistik-Lagererfassungsjournale**. Weitere Informationen finden Sie unter [Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Erfassungsjournalen](inventory-how-count-adjust-reclassify.md). Dieser Artikel beschreibt, wie eine Inventurerfassung mithilfe von Belegen durchgeführt wird.
>
> Wenn Sie Zonen in Ihrem Lager verwenden, können Sie keine Inventuraufträge verwenden. Verwenden Sie stattdessen die Seite **Logistik-Inventur-Erf.-Journal**, um Ihre Lagerposten zu zählen, bevor Sie sie mit den Lagerposten synchronisieren.

Das Erfassen des Lagerbestands mithilfe von Belegen besteht aus den folgenden Gesamtschritten:

1. Erstellen Sie einen Inventurauftrag mit den erwarteten vorab ausgefüllten Artikelmengen.
2. Generieren Sie eine oder mehrere Inventurerfassungen aus dem Auftrag.
3. Geben Sie die gezählten Artikelmengen zu den Erfassungen ein, wie beispielsweise auf den Ausdrucken erfasst, und legen Sie sie auf **Beendet** fest.
4. Schliessen Sie den Inventurauftrag ab und buchen Sie ihn.

## <a name="to-create-a-physical-inventory-order"></a>So erstellen Sie einen Inventurauftrag

Auf Anwendungsebene ist ein Inventurauftrag ein vollständiger Beleg, der aus einem Inventurauftragskopf und Auftragspositionen besteht. Die Informationen im Inventurauftragskopf geben an, wie die Inventur durchgeführt werden soll. Die Auftragspositionen enthalten Informationen über die Artikel und deren Lagerorte.

Um die Inventurauftragspositionen zu erstellen, verwenden Sie üblicherweise die Aktion **Zeilen berechnen**, um den aktuellen Lagerbestand als Positionen auf dem Auftrag hinzuzufügen. Sie können auch die Aktion **Aus Dokument kopieren** verwenden, um die Positionen mit dem Inhalt aus einem anderen offenen oder gebuchten Inventurauftrag ausfüllen zu lassen. Nachfolgend wird nur beschrieben, wie Sie die Aktion **Zeilen berechnen** verwenden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Physikalische Inventuraufträge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die erforderlichen Felder auf dem Inforegister **Allgemein** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie auf der Registerkarte  **Aktionen**  in der Gruppe  **Funktionen**  die Option  **Sonstige** und anschließend  **Zeilen berechnen aus**.
5. Wählen Sie die Optionen nach Bedarf aus.
6. Richten Sie die Filter beispielsweise so ein, dass nur eine Teilmenge der Artikel bei der ersten Erfassung gezählt wird.

    > [!TIP]
    > Um mehrere Mitarbeitende für die Erfassung des Lagerbestands einzuplanen, legen Sie jedes Mal verschiedene Filter fest, wenn Sie die Aktion **Zeilen berechnen** verwenden, damit der Auftrag mit der Teilmenge von Lagerartikeln eingegeben wird, den der jeweilige Benutzende erfasst. Wenn Sie mehrere Inventurerfassungen für mehrere Mitarbeitende generieren, minimieren Sie das Risiko, dass Artikel zweimal gezählt werden. Weitere Informationen finden Sie unter [So erstellen Sie eine Inventurerfassung](#to-create-a-physical-inventory-recording).

7. Wählen Sie die Schaltfläche **OK** aus.

Eine Position für jeden Artikel, der im ausgewählten Lagerort und entsprechend der festgelegten Filter und Optionen vorhanden ist, wird dem Auftrag hinzugefügt. Für Artikel, die im Artikeltracking eingerichtet sind, wird das Kontrollkästchen **Artikeltracking verwenden** ausgewählt. Informationen über die erwartete Menge von Serien- und Chargennummern sind verfügbar, indem Sie **Positionen** und dann **Artikeltrackingzeilen** auswählen. Weitere Informationen finden Sie unter [Verarbeitung des Artikeltrackings beim Erfassen des Lagerbestands](#handle-item-tracking-when-counting-inventory).

Sie können jetzt mindestens eine Erfassung erstellen. Dabei handelt es sich um Anweisungen für die Mitarbeitenden, die die Inventur durchführen.  

> [!NOTE]
> Wenn Sie das paketspezifische Tracking nutzen, können Sie auch Belege verwenden, um den Lagerbestand mit Paketnummern zu zählen und anzupassen. Um diese Funktion nutzen zu können, müssen Sie **Funktionsupdate: Verwendung des Pakettrackings in Inventuraufträgen aktivieren** auf der Seite **Funktionsverwaltung** aktivieren. Bestehende Inventuraufträge werden jedoch aktualisiert. [!INCLUDE [prod_short](includes/prod_short.md)] kann die **Paketnr.** nicht ausfüllen Feld Sie müssen diese Positionen mit der Aktion **Zeilen berechnen** auf der Seite **Inventurauftrag** neu erstellen.
>
> Sie können die Paketnummer für Artikel eingeben, bei denen ein Pakettracking erforderlich ist, und zwar auf der Seite **Inventurerfassungszeilen**. Wählen Sie **Beenden** aus, um die Erfassung abzuschliessen.
>
> Nachdem Sie auf der Seite **Inventurauftrag** die Option **Beenden** ausgewählt haben, berechnet [!INCLUDE [prod_short](includes/prod_short.md)] Differenzen hinsichtlich der Verpackung und anderer Artikeltrackingdetails und nimmt positive oder negative Anpassungen vor.

## <a name="to-create-a-physical-inventory-recording"></a>So erstellen Sie eine Inventurerfassung

Für jeden Inventurauftrag können Sie eine oder mehrere Inventurerfassungsbelege erstellen, auf denen die Mitarbeitenden die gezählten Mengen erfassen können. Mitarbeitende können Mengen entweder manuell oder mit einem Scanner eingeben.

Standardmässig wird die Erfassung aller Zeilen im zugehörigen Inventurauftrag erstellt. Um zu vermeiden, dass zwei Mitarbeitende dieselben Artikel zählen, wenn Sie die Zählung verteilen, füllen Sie den Inventurauftrag nach und nach aus, indem Sie Filter für den Batchauftrag **Zeilen berechnen** festlegen. Erstellen Sie dann die Inventurerfassung mit aktiviertem Kontrollkästchen **Nur nicht erfasste Zeilen**. Durch diese Einstellung wird sichergestellt, dass jede neue Erfassung andere als die in anderen Aufzeichnungen enthaltenen Artikel aufweist.

Im Falle der manuellen Zählung können Sie den Bericht **Inventurerfassung** ausdrucken, der eine leere Spalte enthält, in der Lagermitarbeitende die gezählten Mengen aufschreiben können. Wenn die Zählung abgeschlossen ist, geben Sie die erfassten Mengen in die entsprechenden Zeilen auf der Seite **Inventurerfassung** ein. Zuletzt übertragen Sie die erfassten Mengen in den zugehörigen Inventurauftrag, indem Sie den Status auf **Beendet** setzen.

1. Auf einer Seite  **Inventurauftrag**, die Zeilen für die in einer Aufzeichnung zu zählenden Artikel enthält, müssen Sie die Aktion  **Neue Aufzeichnung erstellen**  auswählen.
1. Wählen Sie auf der Registerkarte  **Aktionen**  in der Gruppe  **Funktionen**  die Option  **Sonstige** und anschließend  **Neue Aufnahme erstellen**.
1. Wählen Sie die Optionen und Filter nach Bedarf aus.
1. Wählen Sie die Schaltfläche **OK** aus.
1. Jede Gruppe von Artikeln, die gezählt wird, laden Sie in den zugehörigen Inventurauftrag. Dann wiederholen Sie die Schritte 1 bis 3 bei aktiviertem Kontrollkästchen **Nur nicht erfasste Zeilen**.
1. Wählen Sie auf der Registerkarte  **Verwandte** die Option  **Bestellung** und anschließend die Aktion  **Aufzeichnungen**  aus, um die Seite  **Liste der physischen Bestandsaufzeichnungen**  zu öffnen.
1. Öffnen Sie die entsprechende Erfassung.
1. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.
1. Bei Artikeln, die das Artikeltracking verwenden, erstellen Sie eine weitere Zeile für jeden Chargen- oder Seriennummerncode, indem Sie die Aktion **Funktionen** und dann die Aktion **Zeile kopieren** auswählen. Weitere Informationen finden Sie unter [Verarbeitung des Artikeltrackings beim Erfassen des Lagerbestands](#handle-item-tracking-when-counting-inventory).  
1. Wählen Sie die Aktion **Drucken** aus, um den Beleg vorzubereiten, den Mitarbeitende verwenden, um die von ihnen gezählten Mengen aufzuschreiben.

## <a name="to-finish-a-physical-inventory-recording"></a>So schliessen Sie eine Inventurerfassung ab

Nachdem die Mitarbeitenden die Mengen gezählt haben, erfassen Sie die Mengen in [!INCLUDE [prod_short](includes/prod_short.md)].

1. Wählen Sie auf der Seite **Inventurerfassungsübersicht** die Inventurerfassung aus, die Sie abschliessen möchten, und wählen Sie dann die Aktion **Bearbeiten** aus.
2. Füllen Sie dann im Inforegister **Zeilen** die tatsächlich gezählte Menge im Feld **Menge** für jede Zeile aus.
3. Für Artikel mit Serien- oder Chargennummern (bei ausgewähltem Kontrollkästchen **Artikeltracking verwenden**) geben Sie die gezählten Mengen in den Zeilen für die betreffenden Serien- und Chargennummern der Artikel ein. Weitere Informationen finden Sie unter [Verarbeitung des Artikeltrackings beim Erfassen des Lagerbestands](#handle-item-tracking-when-counting-inventory).
4. Aktivieren Sie in jeder Zeile das Kontrollkästchen **Erfasst**.
5. Wenn Sie alle Daten für eine Inventurerfassung eingegeben haben, wählen Sie die Aktion **Fertig stellen** aus. Beachten Sie, dass bei allen Zeilen das Kontrollkästchen **Erfasst** ausgewählt sein muss.

    > [!NOTE]
    > Wenn Sie eine Inventurerfassung abschliessen, wird jede Zeile in die Zeile des zugehörigen Inventurauftrags übertragen, mit der sie genau übereinstimmt. Damit sie übereinstimmen, müssen die Werte in den Feldern **Artikelnr.**, **Variantencode**, **Lagerortcode** und **Lagerplatzcode** mit der Erfassung und den Auftragszeilen übereinstimmen.>
    > 
    > Wenn keine übereinstimmende Inventurauftragszeile vorhanden ist und das Kontrollkästchen **Erfassung ohne Auftrag erlauben** aktiviert ist, wird eine neue Zeile eingefügt und das Kontrollkästchen **Ohne Auftrag erfasst** in der entsprechenden Inventurauftragszeile aktiviert. Andernfalls wird eine Fehlermeldung angezeigt und der Vorgang wird abgebrochen.> Wenn mehr als eine Zeile einer Inventurerfassung mit einer Zeile eines Inventurauftrags übereinstimmt, wird eine Meldung angezeigt und der Vorgang abgebrochen. Wenn aus irgendwelchen Gründen zwei identische Inventurerfassungszeilen im Inventurauftrag landen, können Sie eine Aktion verwenden, um das Problem zu lösen. Weitere Informationen finden Sie unter [So finden Sie doppelte Inventurauftragszeilen](#to-find-duplicate-physical-inventory-order-lines).

## <a name="to-complete-a-physical-inventory-order"></a>So schliessen Sie einen Inventurauftrag ab

Nachdem Sie eine physische Bestandserfassung abgeschlossen haben, wird das Feld  **Menge erfasst (Basis)**  im zugehörigen Inventurauftrag mit den gezählten (erfassten) Werten aktualisiert und das Kontrollkästchen  **In Erfassungszeilen**  wird aktiviert. Wenn eine gezählte Menge von der erwarteten Menge abweicht, wird die Differenz in den Feldern  **Pos. Menge (Basis)**  und  **Neg. Menge (Basis)**  angezeigt.

Um auf die erwarteten Mengen und alle erfassten Differenzen für Artikel mit Artikeltracking zuzugreifen, wählen Sie die Aktion **Zeilen** und dann **Artikeltrackingzeilen** aus, um verschiedene Ansichten für Serien- und Chargennummern in der Inventur auszuwählen.

Sie können auch die **Phys. Inventory Order Diff.** Aktion auswählen, um Unterschiede zwischen der erwarteten und der gezählten Menge anzuzeigen.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>So finden Sie doppelte Inventurauftragszeilen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Physikalische Inventuraufträge** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie den Inventurauftrag, für den Sie doppelte Zeilen anzeigen möchten.
1. Wählen Sie auf der Registerkarte  **Verwandte**  die Option  **Sonstiges** und anschließend  **Doppelte Zeilen anzeigen**.

Doppelte physische Lagerauftragszeilen anzeigen, sodass Sie sie löschen und nur eine Zeile mit eindeutigem Satz von Werten in den Feldern **Artikelnr.**, **Variantencode**, **Lagerortcode** und **Lagerplatzcode** behalten können.

### <a name="to-post-a-physical-inventory-order"></a>So buchen Sie einen Inventurauftrag

Nach dem Fertigstellen eines Inventurauftrags und Ändern des Status in **Beendet** können Sie ihn buchen. Der Status eines Inventurauftrags kann unter folgenden Bedingungen nur auf **Beendet** festgelegt werden:

- Alle zugehörigen Inventurerfassungen weisen den Status **Beendet** auf.
- Jede Inventurauftragszeile wird in mindestens einer Inventurerfassungszeile erfasst.
- Die Kontrollkästchen **In Erfassungszeilen enthalten** und **Berechnete erw. Menge** werden für alle Inventurauftragszeilen aktiviert.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Physikalische Inventuraufträge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Inventurauftrag aus, den Sie fertig stellen möchten, klicken Sie auf **Bearbeiten**.

    Auf der Seite **Inventurauftrag** kann die Menge angezeigt werden, die im Feld **Erfasste Menge (Basis)** angezeigt wird.
3. Wählen Sie die Schaltfläche **Fertigstellung** aus.

    Der Wert im Feld **Status** ist **Beendet**. Eine Änderung des Auftrags ist jetzt nur noch durch Auswahl der Aktion **Erneut öffnen** möglich.
4. Um den Auftrag zu buchen, wählen Sie dann die Aktion **Buchen** und dann die Schaltfläche **OK** aus.

    Die Lagerposten werden zusammen mit allen verknüpften Artikeltrackingposten aktualisiert.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

### <a name="to-view-posted-physical-inventory-orders"></a>So zeigen Sie gebuchte Inventuraufträge an

Nach dem Buchen wird der Inventurauftrag gelöscht, und der Beleg kann als gebuchter Inventurauftrag angezeigt und ausgewertet werden. Der gebuchte Auftrag umfasst die darin enthaltenen Inventurerfassungen sowie ggf. Bemerkungen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Gebuchte Phys. Orders** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Geb. Inventuraufträge** den gebuchten Inventurauftrag aus, den Sie anzeigen möchten, und wählen Sie dann die Aktion **Anzeigen** aus.
3. Wählen Sie auf der Registerkarte  **Verwandte** die Option  **Bestellung** und anschließend die Aktion  **Aufzeichnungen**, um eine Liste der zugehörigen physischen Bestandsaufzeichnungen anzuzeigen.  

## <a name="handle-item-tracking-when-counting-inventory"></a>Verarbeitung des Artikeltrackings beim Erfassen des Lagerbestands

Das Artikeltracking gehört zu den Serien- oder Chargennummern, die Artikeln zugeordnet sind. Beim Erfassen eines Artikels, der im Bestand zum Beispiel unter zehn verschiedenen Chargennummern gespeichert wird, muss der Mitarbeitende erfassen, welche und wie viele Einheiten einer Chargennummer im Lager vorhanden sind. Weitere Informationen finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).

Das Kontrollkästchen **Artikeltracking verwenden** für Inventurauftragszeilen wird automatisch aktiviert, wenn für den Artikel ein Artikeltrackingcode eingerichtet ist. Sie können das Kontrollkästchen manuell aktivieren oder deaktivieren.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Beispiel – Vorbereiten einer Inventurerfassung für einen Artikel mit Artikelverfolgung

Berücksichtigen Sie eine Inventur für Artikel A, der im Lagerbestand unter zehn verschiedene Seriennummern gespeichert wird.

1. Wählen Sie in der Erfassungszeile für den Artikel das Kontrollkästchen **Artikeltracking verwenden** aus.
2. Wählen Sie das Feld **Seriennr.** aus, die erste Seriennummer, die im Lagerbestand für den Artikel existiert, und wählen Sie dann die Schaltfläche **OK** aus.

    Kopieren Sie die Zeile für den ersten Artikel mit Artikelverfolgung, um zusätzliche Zeilen entsprechend der Anzahl von Seriennummern einzufügen, die im Bestand gespeichert sind.

3. Wählen Sie die Aktion **Funktionen** und dann **Zeile kopieren** aus.
4. Geben Sie auf der Seite **Inventurerfassungszeile kopieren** **9** in das Feld **Anzahl Kopien** ein und wählen Sie dann die Schaltfläche **OK** aus.
5. Wählen Sie in der ersten Zeile im Feld **Seriennr.** die nächste Seriennummer für den Artikel aus.
6. Wiederholen Sie Schritt 5 für die verbleibenden acht Seriennummern. Stellen Sie sicher, dass Sie nicht zweimal dieselbe Nummer auswählen.
7. Wählen Sie die Aktion **Drucken** aus, um den Beleg vorzubereiten, den Mitarbeitende verwenden, um die gezählten Artikel und Serien-/Chargennummern aufzuschreiben.

Beachten Sie, dass der Bericht **Inventurerfassung** zehn Zeilen für Artikel A enthält, einen für jede Seriennummer.

### <a name="example---record-and-post-counted-lot-number-differences"></a>Beispiel – Erfassen und Buchen von erfassten Chargennummer-Differenzen

Ein Artikel mit Chargennummern wird im Bestand mit der Lager mit der CHARGEN-Nummernserie gespeichert.

**Voraussichtlich verfügbar**:

|Chargennr.|Menge|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Summe|120|

**Erfasste Mengen**:

|Chargennr.|Menge|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|20|
|LOT1006|10|
|Summe|112|

**Zu buchende Mengen**:

|Chargennr.|Erwartete Menge|Erfasste Menge|Zu buchende Menge|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|20|-10|
|LOT1006|10|0|-10|
|Summe|120|112|-8|

Auf der Seite **Inventurauftrag** enthält das Feld **Negative Menge (Basis)** die Zahl **8**. Für die Auftragszeile zeigt die Seite **Inventurtracking-Liste** die positiven oder negativen Mengen für die einzelnen Chargennummern an.

## <a name="inventory-documents"></a>Inventurbelege

Die folgenden Arten von Belegen sind nützlich für die Verwaltung Ihres Lagers:

* Benutzen Sie **Inventarbelege**, um positive Anpassungen von Artikeln basierend auf Qualität, Quantität und Kosten zu registrieren.
* Benutzen Sie **Inventursendungen**, um fehlende oder beschädigte Waren abzuschreiben.

Sie können diese Dokumente jederzeit ausdrucken, freigeben, erneut öffnen und ihnen in der Kopfzeile gemeinsame Werte, wie beispielsweise Abmessungen, zuweisen. Wenn Sie die Belege nach dem Posten erneut drucken möchten, verwenden Sie die Seiten **Gebuchte Lagerzugänge** und **Gebuchte Lagerabgänge**.

> [!NOTE]
> Bevor Sie diese Belege verwenden können, müssen Sie eine Nummernserie angeben, um ihre Bezeichner zu erstellen. Weitere Informationen finden Sie unter [Nummerierung von Inventurbelegen einrichten](#to-set-up-numbering-for-inventory-documents).

### <a name="to-set-up-numbering-for-inventory-documents"></a>Nummerierung von Inventurbelegen einrichten

Der folgende Ablauf zeigt, wie die Nummerierung von Inventurbelegen eingerichtet wird.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Lagerbestandseinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Im Inforegister **Nummerierung** geben Sie in den folgenden Feldern die Zahlenreihe für Belege an:

   - **Inv.-Quittungsnummern**  
   - **Gebuchte Zahlungseingangsnummern**  
   - **Invt. Sendungsnummern**  
   - **Gebuchte Invt.-Sendungsnummern**  

### <a name="to-create-and-post-an-inventory-document"></a>Erstellen und Buchen eines Inventurbelegs

Das folgende Verfahren zeigt, wie Sie einen Inventarbeleg erstellen, drucken und buchen. Die Schritte sind ähnlich wie für eine Inventursendungen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Lagerzugänge** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie in der Kopfzeile der Seite  **Lastschriftbeleg**  den Standort im Feld  **Standortcode**  aus und füllen Sie dann die restlichen Felder nach Bedarf aus.
3. Wählen Sie im Inforegister **Zeilen** im Feld **Artikel** den Lagerartikel aus. Geben Sie in dem Feld **Menge** die Anzahl des Artikels an, der hinzugefügt werden soll.
4. Um einen  **Lagerbeleg** Bericht von der Seite  **Lagerbeleg**  auszudrucken, wählen Sie die Aktion  **Drucken** .

Auf der Seite  **Lastschriftbeleg**  stehen Ihnen folgende Funktionen zur Verfügung:

- Wählen Sie die Aktionen **Veröffentlichen** oder **Wieder öffnen** zum Festlegen des Status für die nächste Verarbeitungsstufe aus.  
- Wählen Sie die Aktion **Buchen** aus, um den Lagereingang zu buchen, oder wählen Sie **Veröffentlichen und drucken** aus, um den Beleg zu buchen und den Testbericht auszudrucken.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="printing-inventory-documents"></a>Drucken von Inventurbelegen

Sie können die Berichte angeben, die in verschiedenen Phasen gedruckt werden müssen, indem Sie eine der folgenden Optionen im Feld **Benutzung** für die Seite **Berichtsauswahl – Lagerbestand** auswählen:

* Lagerzugang
* Warenausgang
* Geb. Lagerzugang
* Geb. Lagerabgang

> [!NOTE]
> Die verfügbaren Berichte können je nach Lokalisierung für Ihr Land bzw. Ihre Region variieren. Die Basisanwendung enthält keine Layouts.

## <a name="see-also"></a>Siehe auch

[Zählen, Anpassen und Inventar mithilfe von Journalen neu klassifizieren](inventory-how-count-adjust-reclassify.md)    
[Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md)    
[Lagerbest.](inventory-manage-inventory.md)    
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)    
[Verkauf](sales-manage-sales.md)    
[Einkauf](purchasing-manage-purchasing.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
