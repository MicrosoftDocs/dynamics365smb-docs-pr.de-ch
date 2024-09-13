---
title: Tätigen Sie Zahlungen per AMC Banking (USA) oder SEPA-Überweisung (EU).
description: 'Verarbeiten Sie Zahlungen an Ihre Kreditoren, indem Sie eine Datei (EFT) zusammen mit den Zahlungsinformationen aus den Erfassungsjournalzeilen exportieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 08/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer"></a>Tätigen Sie Zahlungen mit der AMC Banking 365 Fundamentals-Erweiterung oder der SEPA-Überweisung

Auf der Seite  **Zahlungsjournale**  können Sie Zahlungen an Ihre Lieferanten verarbeiten, indem Sie eine Datei zusammen mit den Zahlungsinformationen aus den Journalzeilen exportieren. Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten. [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt das SEPA-Überweisungsformat, aber in Ihrem Land/Ihrer Region sind möglicherweise andere Formate für elektronische Zahlungen verfügbar.

> [!NOTE]
> In der generischen Version von [!INCLUDE[prod_short](includes/prod_short.md)]  wird ein globaler Diensteanbieter eingerichtet und verbunden, der Bankdaten in das Dateiformat konvertiert, das Ihre Bank verlangt. In den nordamerikanischen Versionen kann derselbe Dienst verwendet werden, um Zahlungsdateien als Electronic Funds Transfer (EFT) zu senden, z.B. über das allgemein verwendete Automated Clearing House (ACH) Netzwerk, allerdings mit einem etwas anderen Verfahren. Siehe Schritt 6 unter [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Um SEPA-Banküberweisungen zu aktivieren, müssen Sie zunächst ein Bankkonto, einen Kreditor und das Fibu Erf.-Journal anlegen, auf dem das Zahlungsausgangs Erf.-Journal basiert. Anschließend bereiten Sie die Zahlungen an Lieferanten vor, indem Sie die Seite  **Zahlungsjournale**  automatisch mit fälligen Zahlungen mit angegebenen Buchungsdaten füllen.  

Nachdem Sie überprüft haben, dass die Bank die Zahlungen verarbeitet hat, können Sie die Zahlungsjournalzeilen buchen.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension"></a>Einrichten der AMC Banking 365 Fundamentals Erweiterung

Aktivieren Sie die AMC Banking 365 Fundamentals Erweiterung, um:

* Konvertieren Sie Kontoauszugsdateien in ein importierbares Format.
* Konvertieren Sie Ihre exportierten Zahlungsdateien in das von Ihrer Bank benötigte Format.

Weitere Informationen finden Sie unter [Die AMC Banking 365 Fundamentals-Erweiterung verwenden](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer"></a>SEPA-Überweisung einrichten

Auf der Seite  **Zahlungsjournale**  können Sie Zahlungen in eine Datei exportieren und sie zur Verarbeitung der entsprechenden Geldüberweisungen in Ihre elektronische Bank hochladen. [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt das SEPA-Überweisungsformat, aber in Ihrem Land/Ihrer Region sind möglicherweise andere Formate für elektronische Zahlungen verfügbar.  

Um ein Bankdateiformat exportieren zu können, das in  [!INCLUDE[prod_short](includes/prod_short.md)] nicht standardmäßig unterstützt wird, können Sie eine Datenaustauschdefinition einrichten. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).  

Bevor Sie Zahlungen elektronisch durch den Export von Zahlungszeilen im SEPA-Banküberweisungsformat verarbeiten können, müssen Sie die folgenden Einrichtungsschritte ausführen:  

* Richten Sie das Bankkonto ein, um mit dem SEPA-Banküberweisungsformat umzugehen  
* Einrichten von Lieferantenkarten, um Zahlungen zu verarbeiten, indem Dateien im SEPA-Banküberweisungsformat exportiert werden.  
* Richten Sie den zugehörigen Hauptbuchstapel ein, um den Zahlungsexport von der Seite  **Zahlungsjournale**  aus zu ermöglichen.  
* Verbindung der Datenaustauschdefinition für eine oder mehrere Zahlungsarten mit den relevanten Zahlungsverfahren  

> [!NOTE]
> Business Central unterstützt sowohl das SEPA-Format CT pain.001.001.03 als auch CT pain.001.001.09. Sie können auf der Seite  **Bankkontonummer Karte**  ein beliebiges Format auswählen.  

> [!TIP]
> Dieser Artikel gilt für die generische Version von [!INCLUDE [prod_short](includes/prod_short.md)]. In Ihrem Land oder Ihrer Region wurden möglicherweise zusätzliche Pflichtfelder zu den verschiedenen Seiten hinzugefügt. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Ein Bankkonto für SEPA-Banküberweisung einrichten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das Bankkonto aus, von dem Sie Zahlungsdateien im SEPA-Überweisungsformat exportieren.
3. Wählen Sie auf dem Inforegister **Allgemein** im Feld **Kreditübertragung Nachr.-IDs** eine Nummernserie aus, aus der den SEPA-Banküberweisungsposten Nummern zugewiesen werden.
4. Geben Sie auf der Registerkarte  **Kommunikation**  die Adresse und Kontaktinformationen der Bank ein. 

   > [!NOTE]
   > Sie müssen das Feld  **Länder-/Regionscode**  ausfüllen. Wenn das Feld leer ist, können Sie keine Zahlungen für das Konto exportieren. Außerdem muss das Land/die Region über einen gültigen ISO-Code verfügen.

5. Geben Sie auf der Registerkarte  **Buchung**  im Feld  **Währungscode**  die Währung für das Bankkonto an.  

   > [!NOTE]  
   > Das Feld **Währungscode** muss auf **EUR** festgelegt werden, da SEPA-Banküberweisungen nur in der Schweizer Franken-Währung gebucht werden können.  

6. Wählen Sie auf der Registerkarte  **Überweisung**  im Feld  **Zahlungsexportformat**  das SEPA-Format aus, das Sie verwenden möchten.  
7. Geben Sie im Feld  **IBAN**  die internationale Bankkontonummer für das Konto an.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Eine Kreditorenkarte für SEPA-Banküberweisung einrichten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **Kreditoren** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie die Karte des Lieferanten, den Sie elektronisch bezahlen, indem Sie Exportzahlungsdateien im SEPA-Überweisungsformat verwenden.  
3. Wählen Sie auf der Registerkarte  **Zahlungen**  im Feld  **Zahlungsmethodencode**  die Option  **BANK** aus.  
4. Wählen Sie im Feld  **Bevorzugtes Bankkonto**  die Bank aus, an die das Geld überwiesen wird, wenn es von Ihrer elektronischen Bank verarbeitet wird.  

    Wenn Sie für diesen Anbieter noch kein Bankkonto Auswählen eingerichtet haben, können Sie dies jetzt tun. Weitere Informationen finden Sie unter [Einrichten von Kreditorbankkonten für den Export von Bankdateien](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). Der Wert im Feld **Bevorzugtes Bankkonto** wird aus dem Feld **Bankkonto Empfänger** auf der Seite **Zahlungsausgangs Erf.-Journal** kopiert.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Das Zahlungsausgangs Erf.-Journal für den Export von Zahlungsdateien festlegen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Zahlungsausgangs Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Feld **Stapelname** die \-Dropdownschaltfläche aus.  
3. Wählen Sie auf der Seite **Erf.-Journalnamen** die Aktion **Liste bearbeiten**.  
4. Aktivieren Sie in der Zeile des Zahlungsjournals, das Sie zum Exportieren von Zahlungen verwenden, das Kontrollkästchen  **Zahlungsexport zulassen** .  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Verbindung der Datenaustauschdefinition für eine oder mehrere Zahlungsarten mit den relevanten Zahlungsverfahren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Zahlungsformen** ein, und wählen Sie dann den entsprechenden Link.  
2. Auf der **Zahlungsformen**-Seite wählen Sie die Zahlungsform, die verwendet wird, um Zahlungen zu exportieren, und wählen Sie dann das Feld **Definition der Zahlungsexportzeile** aus.  
3. Auf der Seite **Pmt. Export-Zeilen-Definitionen** wählen Sie den Code, den Sie im Feld **Code** im Inforegister **Zeilendefinitionen** in Schritt 4 im Bereich „Formatierung aus Zeilen und Spalten von in der Datei beschreiben“ im Vorgang [Atenaustauschdefinition einrichten](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="preparing-the-payment-journal"></a>Zahlungsjournal vorbereiten

Füllen Sie das Zahlungsausgangs Erf.-Journal mit Zeilen für fällige Zahlungen an Kreditoren, mit der Option, Buchungsdaten basierend auf dem Fälligkeitsdatum der zugehörigen Einkaufsbelege einzufügen. Weitere Informationen finden Sie unter [Kreditoren verwalten](payables-manage-payables.md).

## <a name="exporting-payments-to-a-bank-file"></a>Zahlungen in eine Bankdatei exportieren

Wenn Sie bereit sind, Zahlungen an Ihre Lieferanten oder Rückerstattungen an Ihre Mitarbeiter zu leisten, können Sie eine Datei mit den Zahlungsinformationen in den Zeilen auf der Seite  **Zahlungsjournale**  exportieren. Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten.

In der generischen Version von [!INCLUDE[prod_short](includes/prod_short.md)] ist die AMC Banking 365 Fundamentals-Erweiterung verfügbar. In den nordamerikanischen Versionen kann die gleiche Erweiterung verwendet werden, um Zahlungsdateien wie beim elektronischen Zahlungsverkehr (EFT) zu versenden, allerdings mit einem etwas anderen Prozess. Siehe Schritt 6 unter [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Bevor Sie Zahlungsdateien aus dem Zahlungsausgangs Erf.-Journal exportieren können, müssen Sie das elektronische Format für das betreffende Bankkonto angeben und die AMC Banking 365 Fundamentals-Erweiterung aktivieren. Weitere Informationen finden Sie unter [Bankkonten einrichten](bank-how-setup-bank-accounts.md) und [Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md). Darüber hinaus müssen Sie das Kontrollkästchen **Zahlungsexport erlauben** auf der Seite **Fibu Erf.-Journalnamen** auswählen. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md).  

Verwenden Sie die Seite  **Gutschriftsübertragungsregister**, um die Zahlungsdateien anzuzeigen, die aus dem Zahlungsjournal exportiert wurden. Von dieser Seite aus können Sie Zahlungsdateien auch erneut exportieren, wenn technische Fehler oder Dateiänderungen aufgetreten sind. Beachten Sie jedoch, dass exportierte EFT-Dateien auf dieser Seite nicht angezeigt werden und nicht erneut exportiert werden können.  

### <a name="to-export-payments-to-a-bank-file"></a>Zahlungen in eine Bankdatei exportieren

Die folgenden Schritte beschreiben, wie Sie einen Lieferanten per Scheck bezahlen. Die Schritte sind ähnlich, wie wenn sie Ihren Debitoren Scheck zurückerstatten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Zahlungsausgangs Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Zahlungsausgangs-Erfassungsjournalzeilen aus. Weitere Informationen finden Sie unter [Zahlungen und Rückerstattungen aufzeichnen](payables-how-post-payments-refunds.md)

    > [!NOTE]
    > Wenn Sie EFT verwenden, müssen Sie entweder **Elektronische Zahlung** oder **Elektronische Zahlung-IAT** im Feld **Bankkontozahlungsart** auswählen. Verschiedene Dateiexportdienste und deren Formaten benötigen verschiedene Einrichtungswerte auf den Seiten **Bankkontokarte** und **Kreditor-Bankkontokarte**. Sie werden über die falschen oder fehlende Einrichtungswerte informiert, wenn Sie versuchen, die Datei zu exportieren.
    >
    > Die EFT-Funktion kann nur für Bankkonten in der Mandantenwährung verwendet werden. Es kann nicht mit einer Fremdwährung verwendet werden, die durch einen Wert im Feld **Währungscode** angezeigt ist. (Leerer Feldwert bedeutet Mandantenwährung.)

3. Nachdem Sie alle Zahlungsjournalzeilen ausgefüllt haben, wählen Sie die Aktion  **Exportieren** .
4. Füllen Sie auf der Seite **Elektronische Zahlungen exportieren** die Felder nach Bedarf aus.

    Fehlermeldungen werden in der Infobox  **Zahlungsdateifehler**  angezeigt. Dort können Sie auch eine Fehlermeldung auswählen, um auf weitere Details zuzugreifen. Sie müssen alle Fehler beheben, bevor Sie die Zahlungsdatei exportieren können.

    > [!TIP]  
    > Wenn Sie die AMC Banking 365 Fundamentals-Erweiterung verwenden, wird in einer häufigen Fehlermeldung angezeigt, dass der Bankkontoauszug nicht die Länge hat, die Ihre Bank benötigt. Um den Fehler zu vermeiden oder zu beheben, müssen Sie den Wert im **IBAN**-Feld auf der Seite **Bank** entfernen, und dann im **Kontokarten**-Feld eine Kontonummer in dem Format eingeben, das Ihre Bank erfordert.

5. Geben Sie auf der Seite **Speichern unter** den Speicherort an, zu dem die Datei exportiert werden soll, und wählen Sie dann **Speichern**.

    > [!NOTE]  
    > Wenn Sie EFT verwenden, speichern Sie die resultierenden Kreditorenüberweisungsformulare als Word-Dokument ab oder wählen Sie aus, diese direkt per E-Mail an den Kreditor zu senden. Die Zahlungen werden jetzt auf die Seite **EFT-Datei generieren** hinzugefügt, aus der Sie mehrere Zahlungsaufträge erstellen können, um Übertragungskosten zu sparen. Weitere Informationen finden Sie unter den folgenden Themen:
6. Wählen Sie auf der Seite  **Zahlungsjournale**  die Aktion  **EFT-Datei generieren**  aus.

    Auf der Seite  **EFT-Datei generieren**  werden im Inforegister  **Zeilen**  alle EFT-Zahlungen angezeigt, die Sie aus dem Zahlungsjournal für ein Bankkonto exportiert haben, aber noch nicht generiert wurden.
7. Wählen Sie die **EFT-Datei generieren** Aktion aus, um eine Datei für alle EFT-Zahlungen zu exportieren.
8. Geben Sie auf der Seite **Speichern unter** den Speicherort an, zu dem die Datei exportiert werden soll, und wählen Sie dann **Speichern**.

Die Bankzahlungsdatei wird an den von Ihnen angegebenen Speicherort exportiert. Sie können es auf Ihr elektronisches Bankkonto hochladen und die tatsächlichen Zahlungen vornehmen. Dann können Sie die Buch.-Blattzeilen der exportierten Zahlung buchen.

### <a name="to-plan-when-to-post-exported-payments"></a>Um die Buchung von exportierten Zahlungen zu planen

Wenn Sie für eine exportierte Zahlung keine Zahlungsjournalzeile buchen möchten, können Sie die Journalzeile einfach löschen. Zum Beispiel, weil Sie auf die Bestätigung warten, dass die Bank die Transaktion verarbeitet hat. Wenn Sie später eine Zahlungsjournalzeile erstellen, um den Restbetrag zu bezahlen, wird im Feld  **Gesamtexportierter Betrag**  angezeigt, wie viel des Zahlungsbetrags bereits exportiert wurde. Detaillierte Informationen über die exportierte Summe können Sie auch finden, indem Sie die Schaltfläche **Posten im Kreditübertragungsjournal** auswählen, um Einzelheiten zu Dateien der exportierten Zahlung anzuzeigen.

Wenn Sie Zahlungen erst buchen möchten, wenn die Bank deren Verarbeitung bestätigt hat, haben Sie folgende Möglichkeiten:

* In einem Zahlungsjournal mit vorgeschlagenen Zahlungszeilen können Sie entweder nach **In Zahlungsdatei exportiert**  Spalte oder die **Gesamte exportierte Menge**  und löschen Sie anschließend Zahlungsvorschläge für offene Rechnungen, für die bereits Zahlungen geleistet wurden.
* Auf der **Lieferantenzahlungen vorschlagen**  Seite, auf der Sie angeben, welche Zahlungen in das Zahlungsjournal eingefügt werden sollen, können Sie Auswählen die **Exportierte Zahlungen überspringen**  Kontrollkästchen, wenn Sie keine Journalzeilen für bereits exportierte Zahlungen einfügen möchten.

Um Informationen über exportierte Zahlungen anzuzeigen, wählen Sie die Aktion **Zahlungs-Export-Verlauf**.

### <a name="to-re-export-payments-to-a-bank-file"></a>Um Zahlungen erneut in eine Bankdatei zu exportieren

Sie können Zahlungsdateien aus der **Kreditübertragungsjournale**-Seite exportieren. Bevor Sie Zahlungsjournalzeilen löschen oder buchen, können Sie die Zahlungsdatei auch erneut aus dem **Zahlungsjournale**  Seite, indem Sie sie erneut exportieren. Wenn Sie die Zahlungsjournalzeilen nach dem Export löschen oder buchen, können Sie dieselbe Zahlungsdatei erneut exportieren. **Überweisungsregister**  Seite. Wählen Sie die Zeile für den Stapelauftrag für Gutschriftübertragungen aus, die Sie erneut exportieren möchten, und verwenden Sie dann die Aktion **Zahlungen erneut in Datei exportieren**.

> [!NOTE]  
> Beachten Sie, dass die exportierten EFT-Dateien nicht auf der Seite **Kreditübertragungsjournale** angezeigt werden und nicht wieder exportiert werden können.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Überweisungsjournale** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie einen Zahlungsexport, den Sie erneut exportieren möchten, und wählen die Aktion **Erneuter Zahlungsexport in Datei** aus.

## <a name="posting-the-payments"></a>Verbuchung der Zahlungen

Nachdem Ihre Bank die elektronische Zahlung verarbeitet hat, buchen Sie die Zahlungen. Weitere Informationen finden Sie unter [Zahlungen durchführen](payables-make-payments.md).

## <a name="see-also"></a>Siehe auch

[AMC Banking 365 Fundamentals-Erweiterung verwenden](ui-extensions-amc-banking.md)  
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Mit Fibu Erfassungsjournalen arbeiten](ui-work-general-journals.md)  
[Zahlungen per SEPA-Lastschriftverfahren erfassen](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
