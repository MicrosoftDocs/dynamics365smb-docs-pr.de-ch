---
title: 'QR-Bill Management [CH]'
description: 'Dieser Artikel beschreibt die Verbesserungen an der QR-Bill Management-Erweiterung und wie Sie Business Central zum einfachen Generieren, Senden und Importieren Ihrer QR-Rechnungen verwenden können.'
author: sorenfriisalexandersen
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'QR-bill, invoice, incoming documents, payment reference'
ms.search.form: '11502, 11510, 11511, 11512, 11513, 11514, 11515, 11516, 11517, 11518'
ms.date: 04/05/2023
ms.author: soalex
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="qr-bill-management-in-the-swiss-version-of-business-central"></a>QR-Bill Management in der Schweizer Version von Business Central

Seit 1. Juli 2020 müssen Unternehmen in der Schweiz QR-Rechnungen empfangen können. QR-Rechnungen sind Zahlungsscheine für Rechnungen und Teil einer landesweiten Initiative zur Optimierung von Zahlungsprozessen. QR-Rechnungen ersetzen alle vorhandenen Zahlungsscheine und ESR-bezogene Funktionen. Sie enthalten alle erforderlichen Informationen zum Vornehmen von Zahlungen. Ein QR-Code auf dem Zahlungsschein erleichtert das Importieren der Informationen in [!INCLUDE[prod_short](../../includes/prod_short.md)]. Alle relevanten Informationen werden importiert und zum Generieren von Zahlungen für den Kreditor verwendet, der die QR-Rechnung gesendet hat, einschliesslich der Zahlungsreferenz, die automatisch in Kreditorenposten eingefügt und in Zahlungsdateien an die Bank exportiert wird.

## <a name="get-started-with-the-qr-bill-management-extension"></a><a name="get-started"></a>Erste Schritte mit der QR-Bill Management-Erweiterung

Die QR-Bill Management-Erweiterung ist in [!INCLUDE[prod_short](../../includes/prod_short.md)] enthalten und automatisch installiert. Für die ersten Schritte mit der Erweiterung müssen Sie ein paar Konfigurationsänderungen in [!INCLUDE[prod_short](../../includes/prod_short.md)] vornehmen. Eine einfache Möglichkeit dazu ist die Auswahl des Symbols ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"). Geben Sie **Einrichtung der QR-Rechnung** ein, und wählen Sie dann den zugehörigen Link. Die Anleitung hilft Ihnen bei der Eingabe von Informationen, wie etwa:

* Angeben, ob Ihre IBAN oder QR-IBAN verwendet werden soll. QR-IBAN ist eine IBAN, die eine Zahl zwischen 30000 und 31999 an den Positionen 5 bis 9 enthält, wie etwa *CH55 30024 123456789012*.
* Definieren, wie Namen und Adressen auf QR-Rechnungen angezeigt werden und wie die Codierung für deutsche Umlaute verwendet werden soll. (Wir empfehlen, dass Sie die Standardwerte verwenden.)
* Wählen Sie **Standardmässiges QR-Rechnungslayout** aus. Das Layout bestimmt, ob IBAN oder QR-IBAN verwendet werden soll, ob der Referenztyp Kreditor oder QR-Referenz ist und ob die Abrechnungsinformationen im SWICO-Format enthalten sein sollen.
* Aktivieren Sie Verkaufs- und Servicerechnungstypen sowie Zahlungsmethoden für QR-Rechnungen.
* Geben Sie die Erf.-Journalvorlage und das Erfassungsjournal an, die verwendet werden sollen, wenn Einkaufserfassungsjournale aus gescannten oder importierten QR-Rechnungen generiert werden.

Bei Bedarf können Sie die Layouteinstellungen auf der Seite **QR-Rechnungslayout** ändern.

## <a name="issuing-qr-bills"></a>Ausstellen von QR-Rechnungen

Sie können QR-Rechnungen für Verkaufs- und Servicerechnungen aktivieren. Durch diese Option wird ein Eintrag zur Seite **Berichtsauswahl - Verkauf** hinzugefügt, der beim Generieren der Rechnungen eine zusätzliche PDF-Datei mit der QR-Rechnung generiert. Zur Aktivierung der Funktion wählen Sie das Feld **Belegtypen für QR-Rechnungen aktiviert** auf der Seite **Einrichtung der QR-Rechnung** aus und aktivieren Sie die gewünschten Dokumenttypen, indem Sie das entsprechende Feld in der Spalte **Aktiviert** auswählen.

## <a name="adding-billing-information-to-qr-bills"></a>Hinzufügen von Abrechnungsinformationen zu QR-Rechnungen

Beim Erstellen einer QR-Rechnung können Sie Abrechnungsinformationen im SWICO-Format einfügen, wie von SIX, dem Schweizer Anbieter für Zahlungsinfrastruktur, empfohlen. Im Idealfall können Geschäftsanwendungen, die QR-Rechnungen erstellen oder importieren, Informationen, wie den MWST-Betrag, die Rechnungsnummer des Kreditors usw., verarbeiten, weil diese für die zu zahlende Rechnung wertvoll sein können. In [!INCLUDE[prod_short](../../includes/prod_short.md)] importieren wir diese Informationen, verwenden allerdings nur die Rechnungsnummer des Kreditors. Falls Sie die weitere Informationen einbeziehen möchten, müssen Sie dies anpassen.

## <a name="understanding-the-payment-reference"></a>Informationen über die Zahlungsreferenz

Bei Zahlungsprozessen geht es um das Bezahlen des richtigen Betrags an die richtige Partei. Dadurch können sie Zahlungen leichter abstimmen und ausstehende Konten schliessen. Die QR-Bill Management-Erweiterung wickelt diese Prozesse durch Generieren einer Zahlungsreferenz für QR-Rechnungen ab, die für Rechnungen in einem bestimmten Unternehmen eindeutig ist. Dies bedeutet, dass dieselbe Zahlungsreferenz nicht mehrmals ausgestellt werden kann.  

Falls Ihr Kunde zudem [!INCLUDE[prod_short](../../includes/prod_short.md)] verwendet, wird die Zahlungsreferenz importiert, wenn Sie QR-Rechnungen erhalten, an die Seite **Kreditorenposten** übertragen und als Referenz beim Erstellen von Kreditorenzahlungen verwendet. Weitere Informationen finden Sie unter [Empfang von QR-Rechnungen](ui-extensions-qr-bill-management.md#receiving-qr-bills).

Der Ablauf ist ähnlich wie bei der vorherigen ESR-Referenzfunktion, die die QR-Rechnungen ersetzen. Schliesslich werden die Zahlungsdateien (pain.001) von der Geschäftsanwendung des Kunden mit der Nachricht an seine Bank gesendet, die Beträge an das Konto des Kreditors zu überweisen. Die Bank erstellt eine Kontoauszugsdatei (camt.054), die der Kreditor importieren kann, um die Konten abzustimmen. Diese Datei enthält die Zahlungsreferenz und wird über das Datenaustauschframework importiert, das von der QR-Bill Management-Erweiterung aktualisiert wird, um camt.054-Dateien zu importieren.

Für ESR-Referenzen können Sie Informationen konfigurieren, damit sie beispielsweise die Kundennummer und Rechnungsnummer enthalten. Sie können in QR-Rechnungen die Zahlungsreferenz nicht konfigurieren. Es besteht immer eine direkte Relation zwischen ausgestellter QR-Rechnung und einer Zahlung. Dadurch wird die Abstimmung erleichtert und die Zahlungsreferenz muss auf QR-Rechnungen nicht mehr konfiguriert werden. Stattdessen verwendet [!INCLUDE[prod_short](../../includes/prod_short.md)] einen eindeutigen Zähler für die Zahlungsreferenz. Außerdem ist eine Logik implementiert, die den zweimaligen Import oder Scan derselben Zahlungsreferenz sperrt.

### <a name="formats-for-qr-references-and-creditor-references"></a><a name="formats"></a>Formate für QR-Referenzen und Kreditorreferenzen

Die QR-Referenz besteht aus 26 numerischen Positionen zzgl. einer Prüfziffer.  

Die ISO-Kreditorreferenz (ISO 11649) ermöglicht dem Kreditor automatische Vergleiche zwischen ihren Rechnungen und den eingehenden Zahlungen. Sie muss den Wert *RF* an den Positionen 1-2 und ein korrektes Testzeichen an den Positionen 3-4 sowie höchstens 25 Zeichen enthalten.  

## <a name="using-multiple-bank-accounts-as-issuers-of-qr-bills"></a><a name="multiplebankaccounts"></a>Verwendung mehrerer Bankkonten als Ersteller von QR-Rechnungen

Die Ersteller von QR-Rechnungen können mehrere Bankkonten verwenden, um Zahlungen auf verschiedene Bankkonten umzuleiten. Dies steht mit der Zahlungsform in Verbindung, in der Sie die **QR-Rechnung Bankkontonr.** angeben können. Wenn angegeben, werden die IBAN/QR-IBAN-Informationen von diesem Bankkonto auf QR-Rechnungen verwendet, die die angegebene Zahlungsform verwenden. Auf diese Weise können Sie eingehende Zahlungen auf das gewünschte Bankkonto leiten. Falls Sie nicht mehrere Bankkonten verwenden und die **QR-Rechnung Bankkontonr.** auf der Registerkarte **Zahlungsformen** angeben, werden die QR-IBAN/IBAN-Informationen von der Seite **Unternehmensinformationen** stattdessen auf QR-Rechnungen verwendet. Stellen Sie sicher, dass zumindest die Informationen für Ihr primäres Bankkonto dort eingerichtet sind. Weitere Informationen finden Sie unter [Bankkonten festlegen](../../bank-how-setup-bank-accounts.md).

> [!NOTE]
> Ersteller von QR-Rechnungen müssen ihre Bankkonten so einrichten, dass sie ihren Kunden die richtigen Konten zeigen, je nachdem, ob sie QR-IBANs oder gewöhnliche IBANs verwenden. Empfängern und Zahlern von QR-Rechnungen empfehlen wir, Bankkonten für Zahlung und Überweisung an andere Konten ordnungsgemäss mit gewöhnlichen oder QR-IBANs einzurichten.

### <a name="adding-a-qr-iban-to-a-new-or-existing-bank-account"></a>Hinzufügen einer QR-IBAN zu einem neuen oder bestehenden Bankkonto

Um eine andere als die auf der Seite **Unternehmensinformationen** festgelegte QR-IBAN zu verwenden, geben Sie die Bankkontoinformationen auf der **Bankkontokarte** an:

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Liste **Zahlungsformen** die Aktion **Neu** oder **Bearbeiten**.
3. Geben Sie im Inforegister **Umlagerung** im Feld **QR-IBAN** das Bankkonto ein.

## <a name="scanning-and-importing-qr-bills"></a>Scannen und Importieren von QR-Rechnungen

Zum Scannen oder Importieren einer QR-Rechnung müssen Sie einen der folgenden Typen von Scangeräten verwenden:

* Ein Eingangsscanner, der den QR-Code entschlüsselt und die Tastatur simuliert, um den entschlüsselten Wert direkt in ein Feld in [!INCLUDE[prod_short](../../includes/prod_short.md)] einzugeben.
* Ein Scanner, der den QR-Code entschlüsseln und in einer TXT-Datei speichern kann, die Sie in [!INCLUDE[prod_short](../../includes/prod_short.md)] importieren. 

> [!NOTE]
> Sie können keine QR-Rechnungen, die Sie als PDF-Dateien erhalten haben, direkt in [!INCLUDE[prod_short](../../includes/prod_short.md)] importieren, weil [!INCLUDE[prod_short](../../includes/prod_short.md)] keine QR-Codes interpretieren kann. Sie müssen eine der oben angegebenen Scanmethoden verwenden.

## <a name="receiving-qr-bills"></a>Empfang von QR-Rechnungen

Sie können QR-Rechnungen an mehreren Orten in [!INCLUDE[prod_short](../../includes/prod_short.md)] empfangen:

* **Eingehende Belege**, wenn eine QR-Rechnung das Erstellen eines neuen Kaufbelegs oder eines Einkauf Erf.-Journals initiieren soll.
* **Einkaufsbestellungen und Einkaufsrechnungen**, wenn Sie Informationen aus einer QR-Rechnung in einen vorhandenen Einkaufsbeleg importieren und zur Überprüfung von Betrag und Währung sowie zum Aufbewahren der Zahlungsreferenz verwenden möchten.
* **Einkaufserfassungsjournale**, wenn Sie neue Einkaufserfassungsjournalzeilen auf Grundlage von QR-Rechnungen erstellen möchten. 

### <a name="receiving-a-qr-bill-through-an-incoming-document"></a>Empfangen einer QR-Rechnung über einen eingehenden Beleg

Der Empfang einer QR-Rechnung über eingehende Belege ist insbesondere hilfreich, wenn der Prozess automatisiert ist. Sie können QR-Rechnungen durch eingehende Belege allerdings auch manuell empfangen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **Eingehende Belege** ein, und wählen Sie dann den zugehörigen Link aus.
2. Erstellen Sie in der Liste **Eingehende Belege** einen neuen Eintrag, indem Sie **Neu** und dann **Neu** wählen.
3. Geben Sie auf der Seite **Eingehender Beleg** eine Beschreibung in das Feld **Beschreibung** ein.
4. Zum Importieren der QR-Rechnung wählen Sie eine der folgenden Aktionen aus:
   * **QR-Rechnung scannen**, um eine QR-Rechnung in den eingehenden Belegposten zu scannen.
   * **Gescannte QR-Rechnungsdatei importieren**, um eine vom zweiten Scannertyp generierte Datei wie im Abschnitt [Scannen und Importieren von QR-Rechnungen](#scanning-and-importing-qr-bills) beschrieben zu verwenden.

> [!TIP]
> Nach dem Importieren der QR-Rechnung können Sie sie im Inforegister **Detailabgleich** auf Fehler überprüfen.

Im eingehenden Beleg können Sie ein Einkauf Erf.-Journal oder eine Einkaufsrechnung erstellen und die Zahlungsreferenz von der QR-Rechnung wird beiden zugeordnet. Weitere Informationen finden Sie unter [Arbeiten mit eingehenden Belegen](../../across-income-documents.md).

> [!NOTE]
> Beim Importieren von QR-Rechnungen sucht [!INCLUDE[prod_short](../../includes/prod_short.md)] nach einem Kreditorenbankkonto mit übereinstimmender IBAN oder QR-IBAN. Beim Importieren von QR-Rechnungen in eingehenden Belegen und damit verbundenen Erstellen eines Belegs oder Einkauf Erf.-Journals bestimmt das Kreditorenbankkonto den zu verwendenden Kreditor. Der Ansatz mit dem eingehenden Beleg hilft zu gewährleisten, dass der richtige Kreditor zugewiesen ist. 

#### <a name="receiving-through-the-kofax-ocr-service"></a>Eingang über den Kofax OCR-Dienst

> [!NOTE]
> Falls vorhandene Unternehmen in [!INCLUDE[prod_short](../../includes/prod_short.md)] die Rückgabe einer QR-Referenz wünschen, wenn sie den Kofax OCR-Dienst verwenden, müssen sie die vorhandene Datenaustauschsdefinition aktualisieren, die als **Datenaustauschart** für die Verarbeitung von Rechnungen in eingehenden Belegen verwendet wird.  

Führen Sie die folgenden Schritte aus, um eine bestehende Datenaustauschdefinition zu aktualisieren. 

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Tell Me-Funktion") Geben Sie im Symbol **Data Exchange Definitions** ein und wählen Sie dann den zugehörigen Link. 
2. Suchen Sie in der Liste **Datenaustauschdefinitionen** die Zeile, die Sie aktualisieren möchten, und öffnen Sie die Karte. 
3. Wählen Sie auf dem Inforegister **Zeilendefinitionen** **OCRINVHEADER** aus.  
4. Erstellen Sie im Inforegisterkarte **Spaltendefinitionen** eine neue Zeile, und geben Sie die folgenden Werte ein.

    | Feld | Wert |
    |-------|-------|
    | **Spaltennr.** | 11513 |
    | **Name** | Schweizer QR-Rechnung Referenznummer |
    | **Beschreibung** | Schweizer QR-Rechnung Referenznummer |
    | **Pfad** | /Document/HeaderFields/HeaderField\[Type\[text()='qrreference'\]\]/Text |
    
5. Wählen Sie auf dem Inforegister **Zeilendefinitionen** **Feldzuordnung** aus.  
6. Erstellen Sie auf der Seite **Feldzuordnung** eine neue Position, und geben Sie die folgenden Werte ein.

    | Feld | Wert |
    |-------|-------|
    | **Spaltennr.** | 11513 |
    | **Zieltabellen-ID** | 38 |
    | **Zielfeld-ID** | 171 |
    | **Nur überprüfen** | False |

7. Schliessen Sie die Seiten.  

### <a name="receiving-a-qr-bill-through-purchase-orders-or-purchase-invoices"></a>Empfang einer QR-Rechnung über Einkaufsbestellung oder Einkaufsrechnung

Beim Empfang einer QR-Rechnung über eine Einkaufsbestellung oder eine Einkaufsrechnung wird der Rechnungsbetrag überprüft und die Zahlungsreferenz zu den Posten hinzugefügt. Sie können eine QR-Rechnung wie eingehende Belege scannen oder in eine vorhandene Einkaufsbestellung oder eine Einkaufsrechnung importieren. Dieser Prozess verwendet die QR-IBAN oder IBAN aus der QR-Rechnung, um den Kreditor mit einer übereinstimmenden Nummer zu finden. Falls keine Übereinstimmung gefunden wird, können Sie die QR-Rechnung scannen oder importieren. Daher müssen Sie das Kreditoren-Bankkonto erstellen und dann das Hinzufügen der QR-Rechnung zum Kaufbeleg erlauben.

* Zum Hinzufügen einer QR-Rechnung zu einem vorhandenen Kaufbeleg wählen Sie den Zielbeleg und dann entweder die Aktion **QR-Rechnung scannen** oder **Gescannte QR-Rechnungsdatei importieren** auf der Seite **Bestellungen** oder **Einkaufsrechnungen**.

Wenn die QR-Rechnung gescannt oder in den Kaufbeleg importiert wird, werden der Betrag, die Zahlungsreferenz und weitere Informationen aus der QR-Rechnung hinzugefügt. Diese Daten werden zur Überprüfung verwendet, bevor der Kaufbeleg gebucht wird. Die Buchung wird gesperrt, wenn der Betrag der Bestellung oder der Rechnung nicht mit dem Betrag der QR-Rechnung übereinstimmt. Die Überprüfung erfolgt ebenso, wenn Sie die QR-Rechnung scannen oder importieren. Falls Sie die QR-Rechnung hochladen, die den **Betrag** nicht enthält, beispielsweise, wenn die entschlüsselte QR-Rechnung nach dem Hochladen eine leere Zeile aufweist, in der der Betrag stehen sollte, wird der Abschnitt **QR-Rechnung** auf der Seite **Einkaufsrechnung** angezeigt. Das Feld **Betrag** im Abschnitt **QR-Rechnung** kann bearbeitet werden. Sie können den entsprechenden Betrag diesem Feld hinzufügen. Falls eine hochgeladene QR-Rechnung einen Wert im Feld **Betrag** hat, wird er automatisch im Feld **Betrag** im Abschnitt **QR-Rechnung** festgelegt, das Feld kann aber dennoch bearbeitet werden.  

Falls die Zahlungsreferenz bereits in einem Kreditorenposten für einen Kreditor verwendet wird, tritt ein Fehler auf. Kreditoren können nicht mehrere QR-Rechnungen mit derselben Zahlungsreferenz ausstellen. Entsprechend tritt ein Fehler auf, wenn die QR-Rechnung und die Zahlungsreferenz bereits in einen offenen Kaufbeleg importiert wurden.

### <a name="receiving-a-qr-bill-through-a-purchase-journal"></a>Empfang einer QR-Rechnung über ein Einkauf Erf.-Journal

Sie können QR-Rechnungen direkt in ein Einkauf Erf.-Journal scannen oder importieren. Diese Option ist hilfreich, wenn Sie neue Einkauf Erf.-Journale auf Grundlage einer QR-Rechnung erstellen möchten. Durch direktes Scannen oder Importieren in ein Einkauf Erf.-Journal wird eine neue **Einkaufserfassungsjournalzeile** mithilfe des Kreditors und des Betrags aus der QR-Rechnung erstellt. Zudem wird versucht, den Kreditor zu erkennen, indem ein **Kreditor Bankkonto** mit übereinstimmender IBAN oder QR-IBAN gesucht wird. Beispiel: Die Verwendung von Einkaufserfassungsjournalen ist hilfreich, wenn Sie keine Einkaufsbestellungen oder Einkaufsrechnungen verwenden möchten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Tell Me-Funktion") Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Erstellen Sie in der Liste **Einkaufserfassungsjournale** einen neuen Eintrag, indem Sie eine der folgenden Aktionen wählen:
   * **QR-Rechnung scannen**, um eine QR-Rechnung in den eingehenden Belegposten zu scannen.
   * **Gescannte QR-Rechnungsdatei importieren**, um eine vom zweiten Scannertyp generierte Datei wie im Abschnitt [Scannen und Importieren von QR-Rechnungen](#scanning-and-importing-qr-bills) beschrieben zu verwenden.

## <a name="reconciliation"></a>Abstimmen

Beim Importieren von Banktransaktionen (camt) auf der Seite **Zahlungsabstimmungserfassungsjournale** wird angenommen, dass die Datei die Zahlungsreferenz enthält und dass automatisch die entsprechenden **Debitorenposten** gesucht werden, um die Transaktion auszugleichen.

## <a name="see-also"></a>Siehe auch

[Elektronische Zahlungen (Schweiz)](swiss-electronic-payments.md)  
[Lokale Funktion (Schweiz)](switzerland-local-functionality.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
