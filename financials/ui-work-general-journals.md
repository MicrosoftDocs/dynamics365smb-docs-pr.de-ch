---
title: "Mithilfe von Fibu Buch.-Blätern direkt in die Finanzbuchhaltung buchen| Microsoft Docs"
description: "Mehr über die Nutzung von Fibu Erf.-Journal erfahren, um auf Fibukonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten zu buchen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: fb1c3a7f209113f75d8cddc58985eb6a3f21e8ed
ms.contentlocale: de-ch
ms.lasthandoff: 07/07/2017


---
# <a name="working-with-general-journals"></a>Arbeiten mit Fibu Buch.-Blättern
Die meisten Finanztransaktionen werden in den Fibuposten von Geschäftsbelegen wie Einkaufsrechnungen und Verkaufsaufträge gebucht. Für Geschäftsaktivitäten, die nicht in einem Beleg in[!INCLUDE[d365fin](includes/d365fin_md.md)] festgehlaten sind, wie kleinere Aufwendungen oder Zahlungseingänge, können Sie die entsprechenden Transaktionen erstellen, indem Sie die Buch.-Blattzeilen im **Fibu Buch.-Blatt** buchen. Weitere Informationen finden Sie unter [So gehts: Transaktionen direkt in der Finanzbuchhaltung buchen.](finance-how-post-transactions-directly.md).

Fibu Erf.-Jounrale dienen zum Erfen auf Fibukonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten. Bei der Buchung mit einem Fibu Erf.-Journal werden immer Posten für Fibukonten erstellt. Dies gilt auch, wenn beispielsweise eine Erfassungsjournalzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird.

Die in ein Erf.-Journal eingegebenen Informationen sind temporär und können geändert werden, solange sie sich im Erf.-Journal befinden. Durch Buchen des Erf.-Journals werden die Informationen in Posten auf Konten übertragen und können nicht mehr geändert werden. Der Ausgleich gebuchter Posten kann jedoch aufgehoben werden, und Sie haben die Möglichkeit zum Buchen von Storno- oder Korrekturposten. Weitere Informationen finden Sie unter [Stornieren von Buch.-Blattbuchungen](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Buch-Blattvorlagen und Stapel nutzen
Es gibt mehrere Fibu Erfassungsjournalvorlagen. Jede Erfassungsjournalvorlage wird durch ein spezifisches Fenster mit bestimmten Funktionen und den Feldern dargestellt, die benötigt werden, um diese Funktionen zu unterstützen, wie das Fenster **Zahlungsabstimmungs-Erfassungsjournal**, um Bankzahlungen und das Fenster **Zahlungsausgangs-Erfassungsjournal** zu verarbeiten, um Ihre Kreditoren zu bezahlen. Weitere Informationen finden Sie unter [Anwenden von Zahlungen](payables-make-payments.md) und [Vorgehensweise: Ausgleichen Debitoren-Zahlungen manuell aus](receivables-how-apply-sales-transactions-manually.md).

Sie können zu jeder Erfassungsjournalvorlage mehrere Erfassungsjournalnamen als Journal-Stapel erstellen. Beispielsweise können Sie Ihre eigenen Buch-Stapel für das Zahlungserfassungsjournal erstellen, das Ihr persönliches Layout und Ihre Einstellungen hat. Der nächste Tipp ist ein Beispiel, wie Sie ein Erf.-Journal anpassen.

> [!TIP]  
> Wenn Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu Erfassungsjournalnamen** auswählen, dann werden das Feld **Betrag**, beispielsweise Fibu Erfassungsjournalzeilen für dieselbe Belegnummer automatisch mit dem Wert, der zum Ausgleichen des Belegs erforderlich ist, ausgefüllt. Weitere Informationen finden Sie unter[[!INCLUDE[d365fin](includes/d365fin_md.md)]Werte Vorschlagen](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Hauptkonten und Gegenkonten und Saldokonten verstehen
Wurden Standardgegenkonten für die Erfassungsjournalnamen eingerichtet, wird das Gegenkonto beim Ausfüllen des Felds **Kontonr.** automatisch ausgefüllt. Feld Sie müssen auch das Feld **Kontonr.**ausfüllen, Feld und **Gegenkonto-Nummer** Feld manuell. Bei einem positiven Betrag im Feld **Betrag** wird das Hauptkonto belastet, und auf dem Gegenkonto erfolgt eine Gutschrift. Bei einem negativen Betrag erfolgt eine Gutschrift auf dem Hauptkonto, und das Gegenkonto wird entsprechend belastet.

> [!NOTE]  
>   Die MWST für Haupt- und Gegenkonto wird getrennt berechnet, damit für die Konten unterschiedliche MWST-Prozentsätze verwendet werden können.

## <a name="working-with-recurring-journals"></a>Arbeiten mit wiederkehrenden Erfassungsjournalen
Bei einem wiederkehrenden Erfassungsjournal handelt es sich um ein Fibu Erfassungsjournal mit speziellen Feldern für die Verwaltung von Transaktionen, die häufig mit geringen oder keinen Änderungen gebucht werden. Mithilfe dieser speziellen Felder für wiederkehrende Transaktionen können Sie feste und variable Beträge buchen. Sie können auch ein automatisches Storno für den Tag nach dem Buchungsdatum festlegen und wiederkehrende Posten zusammen mit Verteilungsschlüsseln verwenden.

## <a name="working-with-standard-journals"></a>Arbeiten mit Standard-Buchblättern
Wenn Sie Erfassungsjournalzeilen erstellt haben, die Sie wahrscheinlich zu einem späteren Zeitpunkt erneut erstellen werden, können Sie sich entscheiden, diese als Standard Erfassungsjournal zu speichern, bevor Sie das Erfassungsjournal buchen. Diese Funktionalität wird in Artikel Buch.-Blätter und Buch.-Blätter angewendet.

> [!NOTE]  
>   Das folgende Verfahren bezieht sich auf das Artikel Erf.-Journal, die Informationen betreffen jedoch auch das Standard Erf.-Journal.

### <a name="to-save-a-standard-journal"></a>Ein Standard-Erfassungsjournal speichern:
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buchblatt** ein und wählen den zugehörenden Link aus.
2. Geben Sie in mindestens eine Erfassungsjournalzeile ein.
3. Wählen Sie die Buch.-Blattzeilen aus, die Sie wieder verwenden möchten.
4. Wählen Sie die **Als Standard Buch.-Blatt speichern** Aktion aus.
5. Im Anforderungsfenster **Als Standard Artikel Buch.-Blatt speichern** müssen Sie ein neues oder vorhandenes Standard Buch.-Blatt eingeben, in dem die Zeilen gespeichert werden sollen:

    Wenn Sie bereits mindestens ein Standard-Artikel Erfassungsjournal erstellt haben und es durch eine neue Zusammenstellung von Artikel Erfassungsjournalzeilen ersetzen möchten, können Sie Feld Code den gewünschten Code auszuwählen.
6. Wählen Sie die Schaltfläche **OK**, um zu bestätigen, dass Sie das vorhandene Standard-Artikel-Erfassungsjournal überschreiben und seinen gesamten Inhalt ersetzen möchten.
7. Wählen Sie das Feld **Stückpreis speichern** aus, wenn Sie die Werte im Feld **Stückpreis** im Standard Artikel Erfassungsjournal speichern möchten.
8. Wählen Sie das Feld **Menge speichern** aus, wenn die Anwendung die Werte im Feld **Menge** speichern soll.
9. Wählen Sie **OK** aus, um das Standard Artikel Erfassungsjournal zu speichern.

Wenn Sie das Standard-Artikel-Erfassungsjournal gespeichert haben, wird das Fenster Artikel Erfassungsjournal angezeigt, so dass Sie mit der Buchung fortfahren können. Diesen Vorgang können Sie beim Buchen dieser oder einer ähnlichen Zeile einfach wiederholen.

### <a name="to-reuse-a-standard-journal"></a>Standard Erf.-Journale wieder nutzen
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buchblatt** ein und wählen den zugehörenden Link aus.
2. Wählen Sie die **Standard Buch.-Blatt abrufen** Aktion aus.

    Das Fenster Standard-Artikelprotokolle wird geöffnet und zeigt Codes und Beschreibungen für alle vorhandenen Standard-Artikelprotokolle an.
3. Zum Überprüfen eines Standard Artikel Buch.-Blatts vor dem Auswählen für die Wiederverwendung klicken Sie auf **Buch.-Blatt anzeigen**.

    Alle Änderungen, die an einem Standard Artikel Erfassungsjournal vorgenommen werden, werden sofort implementiert. Sie sind beim nächsten Mal, wenn Sie das betreffenden Standard Artikel Erfassungsjournal öffnen oder verwenden. Daher sollten Sie sicher sein, dass die Änderung gewichtig genug ist, um sie allgemein zu übernehmen. Nehmen Sie andernfalls die spezifische Änderung am Artikel Erf.-Journal vor, nachdem die Zeilen im Standard Artikel Erf.-Journal eingefügt wurden. Siehe dazu auch Schritt 4 unten.
4. Im Fenster **Standard Artikel Buch.-Blätter** wählen Sie das Standard Artikel Buch.-Blatt aus, das Sie erneut verwenden möchten, und klicken Sie auf **OK**.

    Jetzt wird das Artikel Erf.-Journal mit den Zeilen aufgefüllt, die Sie als Standard Artikel Erf.-Journal gespeichert haben. Wenn Erf.-Journalzeilen bereits im Artikel Erf.-Journal vorhanden sind, werden die eingefügten Zeilen unterhalb der vorhandenen Erf.-Journalzeilen eingefügt.

    Normalerweise, d.h., wenn das Feld **Stückpreis speichern** während der Funktion **Als Standard Buch.-Blatt speichern** nicht markiert war, wird das Feld **Stückpreis** in den eingefügten Zeilen automatisch mit dem aktuellen Wert des Artikels gefüllt (der aus dem Feld **Einstandspreis** auf der Artikelkarte kopiert wird).

    > [!NOTE]  
>   Wenn Sie eines der Felder **Stückzahl speichern** oder **Menge speichern** ausgewählt haben, sollten Sie jetzt überprüfen, ob die eingefügten Werte für diese bestimmte Lagerregulierung richtig sind, bevor Sie das Artikelprotokoll speichern.

    Wenn die eingefügten Artikel Erf.-Journalzeilen gespeicherte Stückpreise enthalten, die Sie nicht buchen möchten, können Sie sie schnell an den aktuellen Artikelwert anpassen:

6. Wählen Sie den Artikel, für den Sie den Lagerbestand anpassen möchten, und wählen Sie dann die Aktion **Einheitsbetrag neu berechnen** aus. Dadurch wird das Feld Stückpreis mit dem aktuellen Einstandspreis des Artikels aktualisiert.
7. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-renumber-document-numbers-in-journals"></a>Belegnummern in Erf.-Journalen neu nummerieren
Um sicherzustellen, dass Sie keine Buchungsfehler aufgrund der Reihenfolge der Belegnummern erhalten, können Sie die Funktion **Belegnummern neu nummerieren** verwenden, bevor Sie ein Erfassungsjournal buchen.

In allen Buch.-Blättern, die anhand das Fibu Buch.-Blatt handelt, ist das **Belegnr.** Feld manuell bearbeitbar, so dass Sie verschiedene Belegnummern für verschiedene Erf.-Journalzeilen oder eine einzige Belegnummer für gruppierte Erf.-Journalzeilen angeben können.

Wenn das Feld **Serien-Nr.** auf dem Buch.-Blatt ausgefüllt ist, erfordert die Buchungsfunktion in Fibu Buch.-Blättern, dass die Belegnummern auf einzelnen oder gruppierten Buch.-Blattzeilen sequenziell angeordnet sind. Um sicherzustellen, dass Sie keine Buchungsfehler aufgrund der Reihenfolge der Belegnummern erhalten, können Sie die Funktion **Belegnummern neu nummerieren** verwenden. Wenn verwandte Erf.-Journalzeilen nach Belegnummern gruppiert wurden, bevor Sie die Funktion verwendet haben, bleiben sie gruppiert, können aber eine andere Belegnummer erhalten.

Diese Funktion funktioniert auch bei gefilterten Ansichten.

Jede Neunummerierung der Belegnummern berücksichtigt verwandte Anwendungen, wie etwa eine Zahlungsanwendung, die von dem Beleg auf der Erf.-Journalzeile an ein Kreditorenkonto durchgeführt wurde. Entsprechend werden die **Auf ID anwenden** und **Auf Dok.Nr. anwenden** Felder in den betroffenen Posten werden aktualisiert werden.

Die folgende Prozedur basiert auf dem Fenster **Fibu Buch.-Blatt**, gilt aber für alle anderen Buch.-Blätter, die auf dem Hauptbuch basieren, wie etwa das Fenster **Zahlungs Buch.-Blatt**.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wenn Sie zum Buchen des Buchs bereit sind, wählen Sie auf der Registerkarte Aktionen, in der Gruppe Funktionen, die Option **Belegnummern neu nummerieren**.

Werte in **Dokumentennummer** Feld werden geändert, wo erforderlich, sodass die Belegnummern auf einzelnen oder gruppierten Erf.-Journalzeilen in sequenzieller Reihenfolge stehen. Nach der Neunummerierung der Belege können Sie mit der Buchung des Erf.-Journals fortfahren.


## <a name="see-also"></a>Siehe auch
[Vorgehensweise: Transaktionen direkt in die Finanzbuchhaltung buchen](finance-how-post-transactions-directly.md)  
[So geht's: Buch.-Blatt-Buchungen stornieren](finance-how-reverse-journal-posting.md)  
[Erklärt, wie Kosten und Einnahmen zugewiesen werden.](year-allocate-costs-income.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

