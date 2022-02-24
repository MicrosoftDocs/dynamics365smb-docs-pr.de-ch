---
title: Mithilfe von Fibu Buch.-Blätern direkt in die Finanzbuchhaltung buchen| Microsoft Docs
description: Mehr über die Nutzung von Buchungsblättern erfahren, um auf Fibukonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten zu buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/10/2020
ms.author: sgroespe
ms.openlocfilehash: 37a69940d6b449a779a6bf8fb9d9729c99aa9ea4
ms.sourcegitcommit: 0b5f8f68b1c9526288bfcce1a3bdc988d2910040
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454445"
---
# <a name="working-with-general-journals"></a>Arbeiten mit Fibu Buch.-Blättern

Die meisten Finanztransaktionen werden in den Fibuposten von Geschäftsbelegen wie Einkaufsrechnungen und Verkaufsaufträge gebucht. Sie können auch Geschäftsaktivitäten wie Einkauf, Zahlung oder Rückerstattung von Mitarbeiterausgaben verarbeiten, indem Sie Erfassungsjournalzeilen in den verschiedenen Erfassungsjournalzeilen in [!INCLUDE[d365fin](includes/d365fin_md.md)] buchen.  

Die meisten Erfassungsjournale basieren auf dem *Fibu Erf.-Journal*, und Sie können alle Transaktionen auf der Seite **Fibu Erf.-Journal** bearbeiten. Weitere Informationen finden Sie unter [Transaktionen direkt im Fibuposten buchen](finance-how-post-transactions-directly.md).  

Beispielsweise können Sie die Kosten der Mitarbeiter, die sie selber bezahlt haben, verwenden, um später zurückzuahlen. Weitere Informationen finden Sie unter [Erstatten Sie die Ausgaben der Mitarbeiter zurück](finance-how-record-reimburse-employee-expenses.md).

Aber in vielen Fällen sollten Sie Erf.-Journals verwenden, die für bestimmte Arten von Transaktionen optimiert sind, wie **Zahlungsausgangs Erf.-Journal** zum Erfassen von Zahlungen. Weitere Informationen finden Sie unter [Zahlungsbelege und Erstattungen im Zahlungsausgangs Erf.-Journal](payables-how-post-payments-refunds.md).  

Fibu Erfassungsjournale dienen zum Buchen auf Fibukonten sowie auf andere Konten wie Bank-, Debitoren-, Debitoren- oder Mitarbeiterkonten. Bei der Buchung mit einem Fibu Erf.-Journal werden immer Posten für Fibukonten erstellt. Dies gilt auch, wenn beispielsweise eine Erfassungsjournalzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird.

Die in ein Erf.-Journal eingegebenen Informationen sind temporär und können geändert werden, solange sie sich im Erf.-Journal befinden. Durch Buchen des Erf.-Journals werden die Informationen in Posten auf Konten übertragen und können nicht mehr geändert werden. Der Ausgleich gebuchter Posten kann jedoch aufgehoben werden, und Sie haben die Möglichkeit zum Buchen von Storno- oder Korrekturposten. Weitere Informationen finden Sie unter [Erf.-Journalbuchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Buch-Blattvorlagen und Stapel nutzen

Es gibt mehrere Fibu Erfassungsjournalvorlagen. Jede Erf.-Journalvorlage wird durch eine spezifisches Seite mit bestimmten Funktionen und den Feldern dargestellt, die benötigt werden, um diese Funktionen zu unterstützen, wie die Seite **Zahlungs-Abstimmungs-Erf.-Journal**, um Bankzahlungen zu verarbeiten, und die Seite **Zahlungsausgangs Erf.-Journal**, um Ihre Mitarbeiter zu bezahlen. Weitere Informationen finden Sie unter [Zahlungen vornehmen](payables-make-payments.md) und [Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Erf.-Journal oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md).

Sie können zu jeder Erfassungsjournalvorlage mehrere Erfassungsjournalnamen als Journal-Stapel erstellen. Beispielsweise können Sie Ihre eigenen Buch-Stapel für das Zahlungserfassungsjournal erstellen, das Ihr persönliches Layout und Ihre Einstellungen hat. Der nächste Tipp ist ein Beispiel, wie Sie ein Erf.-Journal anpassen.

> [!TIP]  
> Wenn Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel auf der Seite **Fibu Erf.-Journalnamen**-Seite auswählen, dann werden das Feld **Betrag**, beispielsweise Fibu Erfassungsjournalzeilen für dieselbe Belegnummer automatisch mit dem Wert, der zum Ausgleichen des Belegs erforderlich ist, ausgefüllt. Weitere Informationen finden Sie unter[[!INCLUDE[d365fin](includes/d365fin_md.md)]Werte Vorschlagen](ui-let-system-suggest-values.md).

> [!TIP]
> Verwenden Sie zum Hinzufügen oder Entfernen von Feldern in Erfassungsjournalen das Banner **Personalisieren**. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Hauptkonten und Gegenkonten und Saldokonten verstehen
Wurden auf der Seite **Erfassungsjournale** Standardgegenkonten für die Erf.-Journalnamen eingerichtet, wird das Gegenkonto beim Ausfüllen des Felds **Kontonr.** automatisch ausgefüllt. Andernfalls müssen die Felder **Kontonr.** und **Gegenkontonr.** manuell ausgefüllt werden. Bei einem positiven Betrag im Feld **Betrag** wird das Hauptkonto belastet, und auf dem Gegenkonto erfolgt eine Gutschrift. Bei einem negativen Betrag erfolgt eine Gutschrift auf dem Hauptkonto, und das Gegenkonto wird entsprechend belastet.

> [!NOTE]  
>   Die MWST für Haupt- und Gegenkonto wird getrennt berechnet, damit für die Konten unterschiedliche MWST-Prozentsätze verwendet werden können.

## <a name="working-with-recurring-journals"></a>Arbeiten mit wiederkehrenden Erfassungsjournalen
Bei einem wiederkehrenden Erf.-Journal handelt es sich um ein Fibu Erf.-Journal mit speziellen Feldern für die Verwaltung von Transaktionen, die häufig und ohne oder und mit geringen Änderungen gebucht werden. Mithilfe dieser speziellen Felder für wiederkehrende Transaktionen können Sie feste und variable Beträge buchen. Sie können auch ein automatisches Storno für den Tag nach dem Buchungsdatum festlegen und wiederkehrende Posten zusammen mit Verteilungsschlüsseln verwenden. Sie können auch Umlageschlüssel verwenden, um wiederkehrende Posten mit einem einzigen Vorgang zwischen verschiedenen Konten aufteilen zu können. Weitere Informationen finden Sie unter [Zuordnung von Beträgen des wiederkehrenden Erf.-Journals auf mehrere Konten](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).

Regelmässig gebuchte Transaktionen müssen in einem wiederkehrenden Erf.-Journal nur einmal eingegeben werden. Das bedeutet, dass Einträge wie Konten, Dimensionen oder Dimensionswerte nach der Buchung im Erfassungsjournal verbleiben. Eventuelle Änderungen können Sie bei jeder Buchung vornehmen.

### <a name="recurring-method-field"></a>Feld Wiederholungsmethode
Dieses Feld legt fest, wie der in der Erf.-Journalzeile angegebene Betrag nach der Erfassung bearbeitet werden soll. Wenn Sie z. B. bei jeder Buchung der Zeile den gleichen Betrag verwenden, können Sie den Betrag unverändert lassen. Wenn Sie dagegen immer den Betrag ändern, jedoch Konto und Text unverändert lassen, können Sie den Betrag nach der Buchung löschen lassen.

| Bis | Informationen |
| --- | --- |
|Fixiert|Der Betrag in der Erf.-Journalzeile wird nach der Buchung nicht geändert.|
|Variabel|Der Betrag wird nach dem Buchen aus der Erf.-Journalzeile gelöscht.|
|Saldo|Der gebuchte Betrag des Kontos in der Zeile wird Konten zugewiesen, die für die Zeile in der Tabelle Gen angegeben werden. Fibu Erf.-Jrn. Tabelle. Der Saldo auf dem Konto beträgt somit Null. Denken Sie daran, das Feld **Verteilung %** auf der Seite **Verteilungsübersicht** auszufüllen. Weitere Informationen finden Sie unter [Zuordnung von Beträgen des wiederkehrenden Erf.-Journals auf mehrere Konten](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).|
|Umgekehrt fix|Der Betrag in der Erf.-Journalzeile bleibt nach der Buchung erhalten und für den folgenden Tag wird ein Gegenposten gebucht.|
|Umgekehrt variabel|Der Betrag in der Erf.-Journalzeile wird nach der Buchung gelöscht und für den folgenden Tag wird ein Gegenposten gebucht.|
|Umgekehrt Ausgleich|Der gebuchte Betrag des Kontos in der Zeile wird Konten zugewiesen, die für die Zeile auf der Seite **Zuweisungen** angegeben werden. Der Saldo auf dem Konto wird auf Null gesetzt, und ein Gegenposten wird am folgenden Tag gebucht.|

> [!NOTE]  
>  Sie können die Mehrwertsteuerfelder entweder in der wiederkehrenden Erfassungsjournalzeile oder in der Verteilungs Erf.-Journalzeile, aber niemals in beiden gleichzeitig, ausfüllen. Das heisst, sie können auf der Seite **Zuweisungen** nur passende Zeilen eintragen, wenn die entsprechenden Zeilen nicht im wiederkehrenden Erf.-Journal eingetragen werden.

### <a name="recurring-frequency-field"></a>Feld Wiederholungsrate
Das Feld legt fest, wie oft der Posten in der Erf.-Journalzeile gebucht wird. Das ist ein Datumsformelfeld, und es muss für andere Zeilen des wiederkehrenden Erf.-Journals ausgefüllt werden. Weitere Informationen zu finden Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Beispiele
Wenn die Erf.-Journalzeile z. B. monatlich gebucht werden soll, geben Sie "1M" ein. Nach jeder Buchung wird dann das Datum im Feld **Buchungsdatum** auf dasselbe Datum im nächsten Monat aktualisiert.

Wenn Sie immer am Letzten des Monats buchen möchten, können Sie nach einem der folgenden Beispiele vorgehen:

- Sie können die erste Buchung am letzten Tag eines Monats buchen und die Wiederholungsrate 1T + 1M – 1T (1 Tag + 1 Monat –1 Tag) eingeben. Mit dieser Formel wird immer das richtige Datum berechnet, unabhängig davon, wie viele Tage der Monat hat.

- Sie können die erste Buchung an einem beliebigen Tag eines Monats buchen und dann die Formel eingeben: 1M+CM. Diese Formel addiert einen ganzen Monat plus die verbleibenden Tage bis zum Letzten des Monats.

### <a name="expiration-date-field"></a>Ablaufdatumsfeld
Das Feld bestimmt das Datum, an dem die Zeile letztmalig gebucht werden soll. Nach dem im Feld angegebenen Datum wird die Zeile nicht mehr gebucht.

Dieses Feld bietet den Vorteil, dass die Zeile nicht sofort aus dem Erf.-Journal gelöscht wird und Sie jederzeit das Ablaufdatum durch ein späteres Datum ersetzen können, so dass Sie die Zeile noch länger verwenden können.

Wenn das Feld leer ist, wird die Zeile bei jeder Buchung mitgebucht, bis sie aus dem Erfassungsjournal gelöscht wird.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Zuordnung von Beträgen des wiederkehrenden Erf.-Journals auf mehrere Konten
Auf der Seite **Wiederk. Fibu Erf.-Journal** können Sie die **Verteilungen** Aktion auswählen, anzeigen oder verwalten und bestimmen, wie Beträge der Zeile des wiederkehrenden Erf.-Journals auf mehrere Konten und Dimensionen zugeordnet werden. Das heisst, die Verteilung ist eine Gegenkontozeile für die Zeile des wiederkehrenden Erf.-Journals.

Genau wie in einem wiederkehrenden Erfassungsjournal müssen Sie die Angaben für eine Verteilung nur einmal eingeben. Nach der Buchung verbleibt die Verteilung im Erf.-Journal, so dass Sie die Beträge und Verteilungen nicht bei jeder Buchung der wiederkehrenden Erfassungsjournalzeile erneut eingeben müssen.

Wenn die Wiederholungsart im Wiederk. Erf.-Journal auf **Ausgleich** oder **Umgekehrt Ausgleich** gesetzt ist, werden keine Dimensionswertcodes im Wiederk. Erf.-Journal berücksichtigt, wenn das Konto auf Null gesetzt ist. Anders ausgedrückt, wenn Sie auf der Seite **Zuordnungen** eine wiederkehrende Zeile auf die verschiedenen Dimensionswerte verteilen, wird nur eine Umkehrbuchung erstellt. Wenn Sie also im Verteilungsbuch eine Zeile des wiederkehrenden Erf.-Journals zuordnen, die einen Wertcode der Dimension enthält, dürfen Sie denselben Code nicht auf der Seite **Zuordnungen** eingeben. Andernfalls sind die Zahlen für die Dimensionswerte falsch.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Beispiel: Zuordnen von Mietzahlungen auf verschiedene Abteilungen
Sie zahlen jeden Monat Miete, daher haben Sie den Vertragsrabattbetrag auf das Kassenkonto in einer Zeile des wiederkehrenden Erfassungsjournals eingegeben. Auf der Seite **Zuordnungen** können Sie die Kosten auf die Kostenstellen entsprechend der jeweils belegten Quadratmeterzahlen aufteilen. Die Berechnung erfolgt aufgrund der Verteilungsprozente für jede Verteilungs-Buch.-Blattzeile. Sie können verschiedene Konten für jede Zeile des Buch.-Blattes Verteilungen eingeben (wenn die Miete auch auf verschiedene Konten aufgeteilt werden soll) oder Sie können dasselbe Konto mit verschiedenen Dimensionswertcodes für die Dimension "Kostenstelle" auf jeder Zeile eingeben.

## <a name="working-with-standard-journals"></a>Arbeiten mit Standard-Buchblättern
Wenn Sie Erfassungsjournalzeilen erstellt haben, die Sie wahrscheinlich zu einem späteren Zeitpunkt erneut erstellen werden, können Sie sich entscheiden, diese als Standard Erfassungsjournal zu speichern, bevor Sie das Erfassungsjournal buchen. Diese Funktionalität wird in Artikel Buch.-Blätter und Buch.-Blätter angewendet.

> [!NOTE]  
>   Das folgende Verfahren bezieht sich auf das Artikel Erf.-Journal, die Informationen betreffen jedoch auch das Standard Erf.-Journal.

### <a name="to-save-a-standard-journal"></a>Ein Standard-Erfassungsjournal speichern:
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Artikel Erfassungsjournale** ein und wählen Sie dann den entsprechenden Link.
2. Geben Sie in mindestens eine Erfassungsjournalzeile ein.
3. Wählen Sie die Buch.-Blattzeilen aus, die Sie wieder verwenden möchten.
4. Wählen Sie die **Als Standard Buch.-Blatt speichern** Aktion aus.
5. Auf der Anforderungsseite **Als Standard Artikel Erf.-Journal speichern** müssen Sie ein neues oder vorhandenes Standard Erf.-Journal eingeben, in dem die Zeilen gespeichert werden sollen:

    Wenn Sie bereits mindestens ein Standard-Artikel Erfassungsjournal erstellt haben und es durch eine neue Zusammenstellung von Artikel Erfassungsjournalzeilen ersetzen möchten, können Sie Feld Code den gewünschten Code auszuwählen.
6. Wählen Sie die Schaltfläche **OK**, um zu bestätigen, dass Sie das vorhandene Standard-Artikel-Erfassungsjournal überschreiben und seinen gesamten Inhalt ersetzen möchten.
7. Wählen Sie das Feld **Stückpreis speichern** aus, wenn Sie die Werte im Feld **Stückpreis** im Standard Artikel Erfassungsjournal speichern möchten.
8. Wählen Sie das Feld **Menge speichern** aus, wenn die Anwendung die Werte im Feld **Menge** speichern muss.
9. Wählen Sie **OK** aus, um das Standard Artikel Erfassungsjournal zu speichern.

Wenn Sie das Standard-Artikel-Erf.-Journal gespeichert haben, wird die Seite "Artikel Erf.-Journal" angezeigt, so dass Sie mit der Erfassung fortfahren können. Diesen Vorgang können Sie beim Erfassen dieser oder einer ähnlichen Zeile einfach wiederholen.

### <a name="to-reuse-a-standard-journal"></a>Standard Erf.-Journale wieder nutzen
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Artikel Erfassungsjournale** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die **Standard Buch.-Blatt abrufen** Aktion aus.

    Die Seite "Standard Artikel Buch.-Blätter" wird geöffnet und zeigt Codes und Beschreibungen für alle vorhandenen Standard Artikel Buch.-Blätter an.
3. Zum Überprüfen eines Standard Artikel Buch.-Blatts vor dem Auswählen für die Wiederverwendung klicken Sie auf **Buch.-Blatt anzeigen**.

    Alle Änderungen, die an einem Standard Artikel Erfassungsjournal vorgenommen werden, werden sofort implementiert. Sie sind beim nächsten Mal, wenn Sie das betreffenden Standard Artikel Erfassungsjournal öffnen oder verwenden. Daher sollten Sie sicher sein, dass die Änderung gewichtig genug ist, um sie allgemein zu übernehmen. Nehmen Sie andernfalls die spezifische Änderung am Artikel Erf.-Journal vor, nachdem die Zeilen im Standard Artikel Erf.-Journal eingefügt wurden. Siehe dazu auch Schritt 4 unten.
4. Auf der Seite **Standard Artikel Erf.-Journals** wählen Sie das Standard Artikel Erf.-Journal aus, das Sie erneut verwenden möchten, und klicken Sie auf **OK**.

    Jetzt wird das Artikel Erf.-Journal mit den Zeilen aufgefüllt, die Sie als Standard Artikel Erf.-Journal gespeichert haben. Wenn Erf.-Journalzeilen bereits im Artikel Erf.-Journal vorhanden sind, werden die eingefügten Zeilen unterhalb der vorhandenen Erf.-Journalzeilen eingefügt.

    Normalerweise, d.h., wenn das Feld **Stückpreis speichern** während der Funktion **Als Standard Buch.-Blatt speichern** nicht markiert war, wird das Feld **Stückpreis** in den eingefügten Zeilen automatisch mit dem aktuellen Wert des Artikels gefüllt (der aus dem Feld **Einstandspreis** auf der Artikelkarte kopiert wird).

    > [!NOTE]  
    >   Wenn Sie eines der Felder **Stückzahl speichern** oder **Menge speichern** ausgewählt haben, sollten Sie jetzt überprüfen, ob die eingefügten Werte für diese bestimmte Lagerregulierung richtig sind, bevor Sie das Artikelprotokoll speichern.

    Wenn die eingefügten Artikel Erf.-Journalzeilen gespeicherte Stückpreise enthalten, die Sie nicht buchen möchten, können Sie sie schnell an den aktuellen Artikelwert anpassen:

6. Wählen Sie den Artikel, für den Sie den Lagerbestand anpassen möchten, und wählen Sie dann die Aktion **Einheitsbetrag neu berechnen** aus. Dadurch wird das Feld Stückpreis mit dem aktuellen Einstandspreis des Artikels aktualisiert.
7. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-renumber-document-numbers-in-journals"></a>Belegnummern in Erf.-Journalen neu nummerieren
Um sicherzustellen, dass Sie keine Buchungsfehler aufgrund der Reihenfolge der Belegnummern erhalten, können Sie die Funktion **Belegnummern neu nummerieren** verwenden, bevor Sie ein Erfassungsjournal buchen.

In allen Erf.-Journalen, die auf dem Fibu-Erf.-Journal basieren, kann das Feld **Belegnr.** bearbeitet werden, so dass Sie unterschiedliche Belegnummern für verschiedene Erfassungsjournalzeilen oder die gleiche Belegnummer für die zugehörigen Erfassungsjournalzeilen angeben können.

Wenn das Feld **Serien-Nr.** auf dem Buch.-Blatt ausgefüllt ist, erfordert die Buchungsfunktion in Fibu Buch.-Blättern, dass die Belegnummern auf einzelnen oder gruppierten Buch.-Blattzeilen sequenziell angeordnet sind. Um sicherzustellen, dass Sie keine Buchungsfehler aufgrund der Reihenfolge der Belegnummern erhalten, können Sie die Funktion **Belegnummern neu nummerieren** verwenden. Wenn verwandte Erf.-Journalzeilen nach Belegnummern gruppiert wurden, bevor Sie die Funktion verwendet haben, bleiben sie gruppiert, können aber eine andere Belegnummer erhalten.

Diese Funktion funktioniert auch bei gefilterten Ansichten.

Jede Neunummerierung der Belegnummern berücksichtigt verwandte Anwendungen, wie etwa eine Zahlungsanwendung, die von dem Beleg auf der Erf.-Journalzeile an ein Kreditorenkonto durchgeführt wurde. Entsprechend werden die Felder **Ausgleichs-ID** und **Ausgleich mit Belegnr.** in den betroffenen Posten aktualisiert.

Die folgende Prozedur basiert auf der Seite **Fibu Erf.-Journal**, gilt aber für alle anderen Erf.-Journals, die auf dem Hauptbuch basieren, wie etwa die Seite **Zahlungs Erf.-Journal**.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Fibu Erfassungsjournale** ein und wählen Sie dann den entsprechenden Link.
2. Wenn Sie zum Buchen des Buchs bereit sind, wählen Sie auf der Registerkarte Aktionen, in der Gruppe Funktionen, die Option **Belegnummern neu nummerieren**.

Werte im Feld **Belegnr.** werden geändert, wo erforderlich, sodass die Belegnummern auf einzelnen oder gruppierten Erfassungsjournalzeilen in sequenzieller Reihenfolge stehen. Nach der Neunummerierung der Belege können Sie mit der Buchung des Erf.-Journals fortfahren.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Buchen von Transaktionen direkt im Fibuposten](finance-how-post-transactions-directly.md)  
[Erf.-Journalbuchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md)  
[Kosten und Einkünfte zuteilen](year-allocate-costs-income.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Schliessen von offenen Lagerposten aus einem festen Ausgleich im Artikel Erf.-Journal](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Lager im Neubewertungsjournal neu bewerten](inventory-how-revalue-inventory.md)  
[Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md)  
[Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Erf.-Journal oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md)  
[Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten](payables-how-apply-purchase-transactions-manually.md)  
[Arbeiten mit Intercompany-Belegen und -Erfassungsjournalen](intercompany-how-work-documents-journals.md)  
