---
title: Mithilfe von Fibu-Erfassungsjournalen direkt in die Finanzbuchhaltung buchen
description: 'Mehr über die Nutzung von Erfassungsjournalen erfahren, um auf Fibukonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten zu buchen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 08/29/2023
ms.custom: bap-template
ms.search.keywords: 'journals, recurring, accrual, renumber, bulk-post'
ms.search.form: '39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
---
# <a name="work-with-general-journals"></a>Mit Fibu Erfassungsjournalen arbeiten

Die meisten finanziellen Transaktionen werden über Belege wie Einkaufsrechnungen und Verkaufsaufträge im Fibu verbucht. Sie können jedoch auch geschäftliche Aktivitäten verarbeiten, wie z.B.:

* Einkauf
* Zahlungen
* Verwendung wiederkehrender Erfassungsjournale zum Buchen von Zugängen
* Rückerstattung von Mitarbeiterausgaben durch Buchung von Erfassungsjournalzeilen in Journalen  

Die meisten Journale basieren auf dem Fibu Erfassungsjournal, und Sie können alle Transaktionen auf der Seite **Fibu Erf.-Journal** verarbeiten. Mehr dazu erfahren Sie unter [Transaktionen direkt im Fibu buchen](finance-how-post-transactions-directly.md).  

Sie können zum Beispiel Spesen von Mitarbeitern zur Erstattung buchen. Erfahren Sie mehr unter [Datensätze für die Erstattung von Ausgaben der Mitarbeiter erfassen](finance-how-record-reimburse-employee-expenses.md).

[!INCLUDE [prod_short](includes/prod_short.md)] bietet jedoch auch Erfassungsjournale, die für bestimmte Arten von Transaktionen optimiert sind, wie z. B. das **Zahlungsausgangs Erf.-Journal** zum Erfassen von Zahlungen. Weitere Informationen finden Sie unter [Zahlungsbelege und Erstattungen im Zahlungsausgangs Erf.-Journal](payables-how-post-payments-refunds.md).  

Mit den Fibu-Erfassungsjournalen buchen Sie finanzielle Transaktionen auf Fibukonten und verschiedenen anderen Konten. Zu den anderen Konten gehören Bank-, Debitor-, Kreditor- und Mitarbeiterkonten. Die Buchung mit Fibu-Erfassungsjournal erstellt Belege auf Fibukonten, auch wenn Sie beispielsweise eine Journalzeile auf ein Debitorenkonto buchen. Der Posten wird über eine Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht.

Die in ein Erf.-Journal eingegebenen Informationen sind temporär und können geändert werden, solange sie sich im Erf.-Journal befinden. Wenn Sie das Journal buchen, werden die Informationen in Erfassungen auf einzelnen Konten übertragen, wo sie nicht geändert werden können. Der Ausgleich gebuchter Posten kann jedoch aufgehoben werden, und Sie haben die Möglichkeit zum Buchen von Storno- oder Korrekturposten. Erfahren Sie mehr unter [Erf.-Journal-Buchungen stornieren und Rückgängigmachung von Eingängen/Versendungen](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="add-context-to-general-journal-transactions"></a>Fibu Erf.-Journal-Transaktionen Kontext hinzufügen

Wenn Sie ein Erfassungsjournal erstellen, können Sie Links mit Kontext zu seinen Transaktionen hinzufügen. Wenn Sie das Erfassungsjournal buchen, kopiert [!INCLUDE [prod_short](includes/prod_short.md)] die Links zu dem gebuchten Erfassungsjournal und den Posten, die das Erfassungsjournal erstellt. Die Bereitstellung von Links kann beispielsweise Ihrem Wirtschaftsprüfer das Leben erleichtern. Wenn Sie Bilder Ihrer Ausgabenbelege auf der Sharepoint-Website Ihres Unternehmens speichern, können Sie Links zu den Dateien hinzufügen. Wenn Sie das Erfassungsjournal veröffentlichen, um Ihre Ausgaben einzureichen, kann Ihr Wirtschaftsprüfer schnell auf die Belegdateien zugreifen.

## <a name="use-journal-templates-and-batches"></a>Erf.-Journalvorlagen und -namen verwenden

Es gibt mehrere Fibu Erfassungsjournalvorlagen. Jede Erf.-Journalvorlage wird durch eine spezifisches Seite mit bestimmten Funktionen und den Feldern dargestellt, die benötigt werden, um diese Funktionen zu unterstützen, wie die Seite **Zahlungs-Abstimmungs-Erf.-Journal**, um Bankzahlungen zu verarbeiten, und die Seite **Zahlungsausgangs Erf.-Journal**, um Ihre Mitarbeiter zu bezahlen. Weitere Informationen finden Sie unter [Zahlungen vornehmen](payables-make-payments.md) und [Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Erf.-Journal oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md).

Sie können zu jeder Erfassungsjournalvorlage mehrere Erfassungsjournalnamen als Journal-Stapel erstellen. Beispielsweise können Sie Ihre eigenen Buch-Stapel für das Zahlungserfassungsjournal erstellen, das Ihr persönliches Layout und Ihre Einstellungen hat. Der nächste Tipp ist ein Beispiel, wie Sie ein Erf.-Journal anpassen.

> [!TIP]  
> Wenn Sie auf der Seite **Erf.-Journalnamen** in der Zeile für Ihren Batch das Kontrollkästchen **Ausgleichsbetrag vorschlagen** aktivieren, wird das Feld **Betrag** z. B. in den Erfassungsjournalzeilen für dieselbe Belegnummer automatisch mit dem Wert vorausgefüllt, der zum Ausgleich des Belegs erforderlich ist. Weitere Informationen finden Sie unter [[!INCLUDE[prod_short](includes/prod_short.md)] Werte vorschlagen lassen](ui-let-system-suggest-values.md).

> [!TIP]
> Sie können Felder in Erfassungsjournalen hinzufügen oder entfernen, indem Sie sie personalisieren. Erfahren Sie mehr unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a>Fibu Erf.-Journal-Stapelverarbeitungen überprüfen

Sie können eine Hintergrundprüfung einschalten, um Verzögerungen beim Buchen zu vermeiden. Bei der Prüfung werden Sie benachrichtigt Sie, wenn ein Fehler in dem Finanz Erf.-Journal, an dem Sie gerade arbeiten, das Buchen des Journals verhindert. Auf der Seite **Fibu Erf.-Journal** können Sie **Hintergrundfehlerprüfung** wählen, damit [!INCLUDE[prod_short](includes/prod_short.md)] Finanz Erfassungsjournale überprüft, wie z. B. Fibu Erfassungsjournale oder Zahlungsausgangs Erfassungsjournale, während Sie an ihnen arbeiten.

Wenn Sie die Prüfung aktivieren, werden in der Infobox **Erf.-Journal-Prüfung** Probleme in der aktuellen Zeile und im gesamten Batch angezeigt. Die Überprüfung erfolgt, wenn Sie einen Finanz-Erf.-Journalnamen laden und eine andere Erf.-Journalzeile auswählen. Die Kachel **Probleme insgesamt** in der Infobox zeigt die Gesamtanzahl von Problemen, die [!INCLUDE[prod_short](includes/prod_short.md)] gefunden hat, und Sie können sie auswählen, um eine Übersicht über die Probleme zu öffnen.

Mit den Aktionen **Zeilen mit Problemen anzeigen** und **Alle Zeilen anzeigen** können Sie zwischen Erfassungsjournalzeilen mit und ohne Probleme hin- und herschalten. Die Infobox **Erfassungsjournalzeilendetails** bietet einen schnellen Überblick und Zugriff auf die Daten der Erfassungsjournalzeilen, wie z.B. das Fibukonto, den Debitor oder Kreditor und die Buchungseinrichtung für bestimmte Konten.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Hauptkonten und Gegenkonten und Saldokonten verstehen

Wurden auf der Seite **Erfassungsjournale** Standardgegenkonten für die Erf.-Journalnamen eingerichtet, wird das Gegenkonto beim Ausfüllen des Felds **Kontonr.** automatisch ausgefüllt. Andernfalls müssen die Felder **Kontonr.** und **Gegenkontonr.** manuell ausgefüllt werden. Bei einem positiven Betrag im Feld **Betrag** wird das Hauptkonto belastet, und auf dem Gegenkonto erfolgt eine Gutschrift. Bei einem negativen Betrag erfolgt eine Gutschrift auf dem Hauptkonto, und das Gegenkonto wird entsprechend belastet.

> [!NOTE]  
> Die MWST für Haupt- und Gegenkonto wird getrennt berechnet, damit für die Konten unterschiedliche MWST-Prozentsätze verwendet werden können.

## <a name="work-with-recurring-journals"></a>Mit wiederkehrenden Erfassungsjournalen arbeiten

Ein wiederkehrendes Erfassungsjournal ist ein allgemeines Journal mit spezifischen Feldern zur Verwaltung von Transaktionen, die Sie häufig mit wenigen oder gar keinen Änderungen buchen. Zum Beispiel Transaktionen für Ausgaben wie Miete, Abonnements, Strom und Heizung. Mit wiederkehrenden Erfassungsjournalen können Sie feste und variable Beträge buchen und automatische Stornoposten für den Tag nach dem Buchungsdatum festlegen. Mit Verteilungsschlüsseln können Sie die wiederkehrenden Posten auf verschiedene Konten aufteilen. Weitere Informationen finden Sie unter [Zuordnung von Beträgen des wiederkehrenden Erf.-Journals auf mehrere Konten](#allocating-recurring-journal-amounts-to-several-accounts).

Mit einem wiederkehrenden Erfassungsjournal erstellen Sie die Posten, die regelmässig nur einmal gebucht werden. So bleiben beispielsweise die Konten, Dimensionen, Dimensionswerte usw. nach der Buchung im Journal erhalten. Falls Änderungen erforderlich sind, können Sie diese bei jeder Buchung vornehmen.

### <a name="recurring-method-field"></a>Feld Wiederholungsmethode

Das Feld **Wiederkehrende Methode** ist wichtig. Es bestimmt, wie der Betrag in der Erfassungsjournalzeile nach der Buchung behandelt werden soll. Wenn Sie z.B. bei jeder Buchung der Zeile den gleichen Betrag verwenden, können Sie den Betrag beibehalten. Wenn Sie dieselben Konten und denselben Text in der Zeile verwenden, der Betrag aber bei jeder Buchung variiert, können Sie den Betrag nach der Buchung löschen.

| Bis | Siehe |
| --- | --- |
|F Fest|Der Betrag in der Erf.-Journalzeile wird nach der Buchung nicht geändert.|
|V Variabel|Der Betrag wird nach dem Buchen aus der Erf.-Journalzeile gelöscht.|
|B Saldo|Der gebuchte Betrag des Kontos in der Zeile wird Konten zugewiesen, die für die Zeile in der Tabelle Gen angegeben werden. Fibu Erf.-Jrn. Tabelle. Der Saldo des Kontos wird auf Null festgelegt. Denken Sie daran, das Feld **Verteilung %** auf der Seite **Verteilungsübersicht** auszufüllen. Weitere Informationen finden Sie unter [Zuordnung von Beträgen des wiederkehrenden Erf.-Journals auf mehrere Konten](#allocating-recurring-journal-amounts-to-several-accounts).|
|RF Umgekehrt fix|Der Betrag in der Erf.-Journalzeile bleibt nach der Buchung erhalten und für den folgenden Tag wird ein Gegenposten gebucht.|
|RV Umgekehrt variabel|Der Betrag in der Erf.-Journalzeile wird nach der Buchung gelöscht und für den folgenden Tag wird ein Gegenposten gebucht.|
|RB Umgekehrt Ausgleich|Der gebuchte Betrag des Kontos in der Zeile wird Konten zugewiesen, die für die Zeile auf der Seite **Zuweisungen** angegeben werden. Der Saldo auf dem Konto wird auf Null gesetzt, und ein Gegenposten wird am folgenden Tag gebucht.|
|Saldo nach Dimension|Die Erf.-Journalzeile ordnet die Kosten basierend auf dem Saldo eines Fibukontos nach Dimensionen zu. Sie werden aufgefordert, die Dimensionsfilter festzulegen, die zur Berechnung des Kontostands des Fibukontos nach Dimension verwendet werden sollen, aus der Sie die Kosten zuordnen möchten. Alternativ können Sie später die Aktion **Dimensionsfilter festlegen** wählen.|
|Rückbuchungssaldo nach Dimension|Die Erf.-Journalzeile ordnet die Kosten basierend auf dem umgekehrten Ausgleich eines Fibukontos nach Dimensionen zu. Sie werden aufgefordert, die Dimensionsfilter festzulegen, die zur Berechnung des Kontostands des Fibukontos nach Dimension verwendet werden sollen, aus der Sie die Kosten zuordnen möchten. Sie können auch die Aktion **Dimensionsfilter festlegen** später wählen.|

> [!NOTE]  
> Sie können die Mehrwertsteuerfelder entweder in der wiederkehrenden Erfassungsjournalzeile oder in der Verteilungs Erf.-Journalzeile, aber niemals in beiden gleichzeitig, ausfüllen. Das heisst, sie können auf der Seite **Zuweisungen** nur passende Zeilen eintragen, wenn die entsprechenden Zeilen nicht im wiederkehrenden Erf.-Journal eingetragen werden.

### <a name="recurring-frequency-field"></a>Feld Wiederholungsrate

Dieses Feld für die Datumsformel bestimmt, wie oft der Eintrag in der Erfassungsjournalzeile gebucht werden soll, und muss ausgefüllt werden. Mehr dazu erfahren Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#use-date-formulas).

#### <a name="examples"></a>Beispiele

Wenn die Erf.-Journalzeile z. B. monatlich gebucht werden soll, geben Sie "1M" ein. Nach jeder Buchung wird dann das Datum im Feld **Buchungsdatum** auf dasselbe Datum im nächsten Monat aktualisiert.

Wenn Sie immer am Letzten des Monats buchen möchten, können Sie nach einem der folgenden Beispiele vorgehen:

* Sie können die erste Buchung am letzten Tag eines Monats buchen und die Wiederholungsrate 1T + 1M – 1T (1 Tag + 1 Monat –1 Tag) eingeben. Mit dieser Formel wird immer das richtige Datum berechnet, unabhängig davon, wie viele Tage der Monat hat.

* Buchen Sie den ersten Eintrag an einem beliebigen Tag des Monats, indem Sie 1M+CM eingeben. Diese Formel addiert einen ganzen Monat plus die verbleibenden Tage bis zum Letzten des Monats.

### <a name="expiration-date-field"></a>Ablaufdatumsfeld

Das Feld bestimmt das Datum, an dem die Zeile letztmalig gebucht werden soll. Die Zeile wird nach diesem Datum nicht mehr gebucht.

Die Verwendung des Feldes Ablaufdatum hat den Vorteil, dass die Zeile nicht sofort aus dem Erfassungsjournal gelöscht wird. Sie können ein späteres Datum eingeben, so dass Sie die Zeile auch in der Zukunft verwenden können.

Wenn das Feld leer ist, wird die Zeile jedes Mal gebucht, bis sie aus dem Journal gelöscht wird.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Zuordnung von Beträgen des wiederkehrenden Erf.-Journals auf mehrere Konten

Auf der Seite **Wiederk. Fibu Erf.-Journal** können Sie die Aktion **Verteilungen** auswählen und bestimmen, wie Beträge der Zeile des wiederkehrenden Erf.-Journals auf mehrere Konten und Dimensionen zugeordnet werden. Die Zuordnung dient als Ausgleichskontozeile für die Erfassungsjournalzeile.

Wie bei einem wiederkehrenden Erfassungsjournal geben Sie eine Zuweisung einmalig ein. Diese bleibt nach der Buchung im Verteilungs Erf.-Journal erhalten. Sie müssen nicht jedes Mal Beträge und Verteilungen eingeben, wenn Sie die Erfassungsjournalzeile buchen.

Falls die wiederkehrende Methode im wiederkehrenden Erfassungsjournal auf **Saldo** oder **Rückbuchungssaldo** festgelegt ist, werden Dimensionswertcodes im diesem Journal nicht berücksichtigt, wenn das Konto auf Null gesetzt ist. Wenn Sie eine wiederkehrende Zeile auf der Seite **Zuordnungen** den Dimensionenwerten zuordnen, wird nur ein Storno erstellt.

> [!NOTE]
> Wenn Sie eine wiederkehrende Erfassungsjournalzeile zuweisen, die einen Code für Dimensionswerte enthält, geben Sie denselben Code nicht auf der Seite **Verteilungen** ein. Andernfalls sind die Zahlen für die Dimensionswerte falsch.  

Um wiederkehrende Journalbeträge basierend auf Dimensionen zuzuweisen, legen Sie das Feld **Wiederkehrende Methode** auf **Saldo nach Dimension** oder **Umkehren des Gleichgewichts nach Dimension** fest. Wenn die wiederkehrende Methode im wiederkehrenden Erfassungsjournal auf **Saldo nach Dimension** oder **Rückbuchungssaldo nach Dimension** festgelegt ist, werden Dimensionswertcodes im wiederkehrenden Erfassungsjournal berücksichtigt, wenn das Konto auf Null gesetzt wird. Wenn Sie eine wiederkehrende Zeile auf der Seite **Zuordnungen** den Dimensionswerten zuordnen, werden Stornobuchungen erstellt, die der Anzahl der Dimensionswertkombinationen entsprechen, aus denen sich der Saldo zusammensetzt. Wenn Sie einen Kontensaldo über ein wiederkehrendes Erfassungsjournal zuweisen, das einen Dimensionswertcode enthält, denken Sie daran, **Saldo nach Dimension** oder **Rückbuchungssaldo nach Dimension** zu verwenden, um sicherzustellen, dass die Dimensionswerte korrekt aus dem Quellkonto ausgeglichen oder storniert werden.  

Ihr Unternehmen verfügt beispielsweise über einige Geschäftsbereiche und eine Handvoll Abteilungen, die Ihre Controller als Dimensionen eingerichtet haben. Um den Prozess der Buchungserfassung zu beschleunigen, müssen die Sachbearbeiter nur die Dimensionen der Geschäftsbereiche eingeben. Da jede Unternehmenseinheit über spezifische Verteilungsschlüssel für die Dimension Abteilung verfügt, z. B. basierend auf der Anzahl der Mitarbeiter, können Sie die wiederkehrenden Methoden **Saldo nach Dimension** oder **Rückbuchungssaldo nach Dimension** verwenden, um die Ausgaben für jede Unternehmenseinheit auf der Grundlage der Verteilungsschlüssel den richtigen Abteilungen zuzuordnen.  

> [!NOTE]
> Bemassungen, die Sie in Zuordnungszeilen festlegen, werden nicht automatisch berechnet, und Sie müssen angeben, welche Bemassungswerte in den Zuordnungskonten festgelegt werden müssen. Wenn Sie die Verknüpfung zwischen der Quellkontodimension und der Zuordnungskontodimension beibehalten möchten, empfehlen wir die Verwendung der Funktionen [Kostenrechnung](finance-about-cost-accounting.md).

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Beispiel: Zuordnen von Mietzahlungen auf verschiedene Abteilungen

Sie zahlen monatlich Miete, also haben Sie den Betrag auf dem Kassenkonto in einer wiederkehrenden Erfassungsjournalzeile erfasst. Auf der Seite **Zuweisungen** können Sie die Dimension Abteilung verwenden, um die Ausgaben auf mehrere Abteilungen aufzuteilen. Zum Beispiel nach der Anzahl der Quadratmeter, die jede Abteilung belegt. Die Berechnung erfolgt aufgrund der Verteilungsprozente für jede Verteilungs-Buch.-Blattzeile. Sie können die Aufteilung auf verschiedene Arten vornehmen:

* Geben Sie verschiedene Konten in verschiedenen Zuordnungszeilen ein, um die Mietkosten auf mehrere Konten aufzuteilen.
* Geben Sie dasselbe Konto ein, verwenden Sie aber in jeder Zeile unterschiedliche Dimensionswertcodes für die Dimension Abteilung.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### <a name="calculate-the-reversal-date"></a>Stornierungsdatum berechnen

Wenn Sie wiederkehrende Fibu Erfassungsjournale verwenden, um Abgrenzungen am Ende einer Periode zu buchen, ist es wichtig, die volle Kontrolle über Stornierungsposten zu haben. Auf der Seite **Wiederkehrende Fibu Erfassungsjournale** können Sie mithilfe des Felds **Stornierungsdatumsberechnung** das Datum steuern, an dem Stornierungsposten gebucht werden, wenn wiederkehrende Stornierungsmethoden verwendet werden.

#### <a name="example"></a>Beispiel

Zugänge werden in der Regel mit den wiederkehrenden Methoden **Fest**, **Variabel** oder **Saldo** in der Erfassungsjournalzeile gebucht. Das Buchungsdatum des gebuchten Betrags auf dem Konto in der Erf.-Journalzeile wird anhand der wiederkehrenden Häufigkeit berechnet. Das Buchungsdatum für die Gegenposten wird mithilfe des Felds **Stornierungsdatumsberechnung** wie folgt berechnet:

* Wenn das Feld leer ist, wird der Gegenposten am nächsten Tag gebucht.
* Wenn das Feld eine Datumsformel enthält (z. B. **5D** für fünf Tage) wird der Gegenposten mit einem Buchungsdatum gebucht, das anhand der Stornierungsdatumberechnung berechnet wird.

> [!NOTE]
> Standardmässig ist das Feld **Stornierungsdatumsberchnung** auf der Seite **Wiederkehrende Fibu Erfassungsjournale** nicht verfügbar. Um das Feld zu verwenden, müssen Sie es hinzufügen, indem Sie die Seite personalisieren. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="work-with-standard-journals"></a>Mit Standard-Erfassungsjournalen arbeiten

Wenn Sie Erfassungsjournalzeilen erstellt haben, von denen Sie wissen, dass Sie sie wahrscheinlich später noch einmal erstellen werden, können Sie sie als Standard Erfassungsjournal speichern, bevor Sie das Journal buchen. Dasselbe gilt für Artikel Erfassungsjournale und Fibu Erfassungsjournale.

> [!NOTE]
> Standard-Erfassungsjournale enthalten möglicherweise nicht alle Felder, die Sie in die resultierenden Fibukontoeinträge aufnehmen möchten. Wenn Sie z. B. eine allgemeine Standard Fibu Erf.-Journal zum Erfassen einer Zahlung verwenden, enthalten die Sachkontoeinträge das Feld „Zahlungsformencode“ nicht.

> [!NOTE]  
> Das folgende Verfahren bezieht sich auf das Artikel Erf.-Journal, die Informationen betreffen jedoch auch das Standard Erf.-Journal.

### <a name="to-save-a-standard-journal"></a>Ein Standard-Erfassungsjournal speichern:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Element Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.
2. Geben Sie in mindestens eine Erfassungsjournalzeile ein.
3. Wählen Sie die Buch.-Blattzeilen aus, die Sie wieder verwenden möchten.
4. Wählen Sie die **Als Standard Buch.-Blatt speichern** Aktion aus.
5. Auf der Anforderungsseite **Als Standard Artikel Erf.-Journal speichern** müssen Sie ein neues oder vorhandenes Standard Erf.-Journal eingeben, in dem die Zeilen gespeichert werden sollen:

    Wenn Sie bereits ein oder mehrere Artikel Erfassungsjournale erstellt haben und eines davon durch die neuen Artikel Erfassungsjournalzeilen ersetzen möchten, wählen Sie im Feld **Code** das Artikel Erf.-Journal aus.
6. Wählen Sie **OK**, um zu bestätigen, dass Sie den Inhalt des vorhandenen Standard Artikel Erf.-Journals ersetzen möchten.
7. Um die Werte im Feld **Stückpreis** des Standard Erf.-Journals zu speichern, wählen Sie das Feld **Stückpreis speichern**.
8. Um die Werte im Feld **Menge** zu speichern, wählen Sie das Feld **Menge speichern**.
9. Wählen Sie **OK**, um das Standard Artikel Erf.-Journal zu speichern.

Wenn Sie das Standard-Artikel Erf.-Journal speichern, wird die Seite Artikel Erf.-Journal angezeigt, auf der Sie die Buchung vornehmen können.

### <a name="to-reuse-a-standard-journal"></a>Standard Erf.-Journale wieder nutzen

> [!NOTE]
> Standard-Erfassungsjournale haben nicht immer die gleichen Felder wie allgemeine Erfassungsjournale. Wenn Sie die Aktion „Standard-Erfassungsjournale abrufen“ verwenden, um die Felder in das allgemeine Erfassungsjournal zu kopieren, enthält das allgemeine Erfassungsjournal möglicherweise weniger Informationen als bei der manuellen Erstellung. 

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Element Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die **Standard Buch.-Blatt abrufen** Aktion aus.
3. Zum Überprüfen eines Standard Artikel Buch.-Blatts vor dem Auswählen für die Wiederverwendung klicken Sie auf **Buch.-Blatt anzeigen**.

    Änderungen, die Sie in einem Standard Artikel Erf.-Journal vornehmen, werden sofort implementiert und sind beim nächsten Öffnen oder Wiederverwenden des Standard Artikel Erf.-Journales wieder vorhanden. Vergewissern Sie sich, dass die Änderung wichtig genug ist, um sie allgemein anzuwenden. Andernfalls nehmen Sie die spezifische Änderung im Artikel Erfassungsjournal vor, nachdem die Zeilen des Standard Artikel Erfassungsjournals hinzugefügt wurden. Siehe dazu auch Schritt 4.
4. Wählen Sie auf der Seite **Standard Artikel Erfassungsjournale** das Journal aus, das Sie wiederverwenden möchten, und wählen Sie dann **OK**.

    Das Artikel Erf.-Journal enthält die von Ihnen gespeicherten Zeilen. Wenn das Artikel Erf.-Journal bereits Zeilen enthält, erscheinen die neuen Zeilen nach diesen.

    Wenn Sie den Schalter **Betrag pro Einheit speichern** beim Speichern des Erfassungsjournals nicht aktivieren, enthält das Feld **Betrag pro Einheit** in den Zeilen, die aus dem Standardjournal hinzugefügt werden, den Wert aus dem Feld **Kosten pro Einheit** auf der Artikelkarte.

    > [!NOTE]  
    > Wenn Sie die Schalter **Einheit speichern** oder **Menge speichern** beim Speichern des Erfassungsjournals aktiviert haben, stellen Sie sicher, dass die neuen Werte korrekt sind, bevor Sie das Artikel Erf.-Journal buchen.
    >
    > Wenn die eingefügten Artikel Erfassungsjournalzeilen gespeicherte Einheitsbeträge enthalten, die Sie nicht buchen möchten, können Sie sie an den aktuellen Wert des Artikels anpassen.

5. Wählen Sie den Artikel, für den Sie den Lagerbestand anpassen möchten, und wählen Sie dann die Aktion **Einheitsbetrag neu berechnen** aus. Durch diese Aktion wird das Feld Betrag pro Einheit mit den aktuellen Kosten pro Einheit des Artikels aktualisiert.
6. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-renumber-document-numbers-in-journals"></a>Belegnummern in Erf.-Journalen neu nummerieren

Um durch die Belegnummer verursachte Buchungsfehler zu vermeiden, können Sie die Aktion **Belegnummern neu nummerieren** verwenden, bevor Sie ein Journal buchen.

In allen Erf.-Journalen, die auf dem Fibu-Erf.-Journal basieren, kann das Feld **Dokumentennr.** bearbeitet werden, so dass Sie unterschiedliche Belegnummern für verschiedene Erfassungsjournalzeilen oder die gleiche Belegnummer für die zugehörigen Erfassungsjournalzeilen angeben können.

Wenn das Feld **Serien-Nr.** auf dem Buch.-Blatt ausgefüllt ist, erfordert die Buchungsfunktion in Fibu Buch.-Blättern, dass die Belegnummern auf einzelnen oder gruppierten Buch.-Blattzeilen sequenziell angeordnet sind. Wählen Sie einfach die Aktion **Belegnummern neu nummerieren** aus, und relevante **Belegnr.**-Felder werden anschliessend aktualisiert. Wenn zusammengehörige Erfassungsjournalzeilen nach Belegnummern gruppiert waren, bevor Sie die Funktion verwendet haben, bleiben sie gruppiert, erhalten aber möglicherweise eine andere Belegnummer.  

Diese Funktion funktioniert auch bei gefilterten Ansichten.

Bei einer Neunummerierung der Belegnummern werden zusammenhängende Anwendungen berücksichtigt, z. B. ein Zahlungsausgleich, der von dem Beleg in der Erfassungsjournalzeile auf ein Kreditorenkonto gestellt wurde. Dementsprechend werden die Felder **Antrags-ID** und **Antrags-Dok. Nr.** in den Sachkontoeinträgen aktualisiert werden.

### <a name="to-renumber-documents-in-journals"></a>Belege in Erfassungsjournalen neu nummerieren

Die folgende Prozedur basiert auf der Seite**Fibu Erf.-Journal**, gilt aber für alle anderen Erf.-Journals, die auf dem Hauptbuch basieren, wie etwa die Seite **Zahlungs Erf.-Journal**.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Allgemeine Erfassungen** ein, und wählen Sie dann den entsprechenden Link.
2. Wenn Sie bereit sind, das Journal zu buchen, wählen Sie die Aktion **Belegnummern neu nummerieren**.

Werte im Feld **Dokumentennr.** werden geändert, wo erforderlich, sodass die Belegnummern auf einzelnen oder gruppierten Erfassungsjournalzeilen in sequenzieller Reihenfolge stehen. Nachdem die Belege neu nummeriert wurden, können Sie das Journal buchen.

## <a name="see-also"></a>Siehe auch

[Transaktionen direkt in der Finanzbuchhaltung buchen](finance-how-post-transactions-directly.md)  
[Erf.-Journal-Buchungen stornieren und Eingänge/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md)  
[Kosten und Einkünfte zuteilen](year-allocate-costs-income.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Schliessen von offenen Lagerposten aus einem festen Ausgleich im Artikel Erf.-Journal](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Lager im Neubewertungsjournal neu bewerten](inventory-how-revalue-inventory.md)  
[Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md)  
[Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Erf.-Journal oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md)  
[Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten](payables-how-apply-purchase-transactions-manually.md)  
[Arbeiten mit Intercompany-Belegen und -Erfassungsjournalen](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
