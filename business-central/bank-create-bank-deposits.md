---
title: Bankeinlagen erstellen
description: 'Sie können Einzahlungen vornehmen, um einen Transaktionsdatensatz zu pflegen, der Informationen enthält, die auf ausstehende Rechnungen und Gutschriften angewendet werden können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'bank, deposit'
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 08/29/2024
ms.custom: bap-template
---

# Bankeinlagen erstellen

> [!NOTE]
> Die Möglichkeit, Bankeinlagen zu erstellen, ist in [!INCLUDE [prod_short](includes/prod_short.md)] 2022 Veröffentlichungszyklus 1 für viele Länder-/Regionalversionen neu. Wenn Sie [!INCLUDE [prod_short](includes/prod_short.md)] vor dieser Version in den USA, Kanada oder Mexiko waren, nutzen Sie möglicherweise die früheren Funktionen. Sie können fortfahren, die neuen Funktionen werden die alten jedoch in einer zukünftigen Version ersetzen. Ihr Administrator kann zur Seite **Funktionsverwaltung** navigieren und die Option **Funktionsupdate: Standardisierte Bankabstimmung und Einzahlungen** aktivieren, um die in diesem Artikel beschriebenen neuen Funktionen zu verwenden.  

Verwenden Sie die Seite **Bankeinzahlungen**, um Einzahlungen als einzelnes Dokument zu registrieren, das einen oder mehrere Posten auf einem Bankkonto bucht. Bankeinzahlung werden in der Regel verwendet, um Bareinzahlungen zu registrieren. Die Seite „Bankeinzahlungen“ ist im Menü **Zahlungsmanagement** im Rollencenter „Geschäftsführer“ und in anderen Rollencentern verfügbar, die sich auf das Zahlungsmanagement beziehen.

Beträge auf Bankeinlagen können aus mehreren Quellen stammen:

* Verkäufe unter Verwendung eines Fibukontos für Umsätze
* Debitorenzahlungen
* Barrückerstattungen von Kreditoren oder Barzahlungen an sie 

Bankeinzahlungszeilen enthalten Informationen zu einzelnen Einzahlungen, z. B. Schecks von Debitoren. Die Summe der Beträge in den Zeilen muss den Gesamtbetrag der Einzahlung ergeben.

Nachdem Sie die Einzahlungsinformationen und -zeilen ausgefüllt haben, müssen Sie sie buchen. Durch die Buchung werden die entsprechenden Bücher aktualisiert, darunter das Hauptbuch sowie die Bank-, Debitoren- und Kreditorenbücher. Gebuchte Einzahlungen werden zur späteren Referenz auf der Seite **Gebuchte Bankeinzahlungen** gespeichert.

Der Bericht **Bankeinzahlung** zeigt Debitoren- und Kreditoreneinzahlungen mit dem ursprünglichen Einzahlungsbetrag, dem noch offenen Einzahlungsbetrag und dem angewendeten Betrag an. Der Bericht zeigt auch den gesamten gebuchten Einzahlungsbetrag an, der abgestimmt werden soll.

## Bevor Sie beginnen

Bevor Sie Bankeinzahlungen verwenden können, müssen einige Dinge eingerichtet werden. Sie müssen eine Nummernserien- und Fibu Erf.-Journalvorlage bereithalten. Sie sollte ausserdem angeben, ob Bankeinzahlungsbeträge als Abschlag gebucht werden sollen. D. h. als Summe aller Beträge in den Einzahlungszeilen. Andernfalls wird jede Zeile als einzelner Posten gebucht. Das Buchen einer Einzahlung als einzelner Bankposten kann den Bankabgleich vereinfachen.

### Nummernserien und Abschlagseinzahlungen

Sie müssen eine Nummernserie für Bankeinzahlungen einrichten und dann die Serie im Feld **Bankeinzahlungsnr.** auf der Seite **Debitoren & Verkauf Einr.** angeben. Weitere Informationen über Nummernserien finden Sie unter [Erstellen von Nummernserien](ui-create-number-series.md)

Um zudem Einzahlungen als Abschläge und nicht als einzelne Positionen zu buchen, aktivieren Sie auf der Seite zur **Einrichtung von Verkäufen und Forderungen** die Umschaltfläche **Bankeinzahlungen als Abschlag buchen**. Wird die Buchung einer Einzahlung als Abschlag gebucht, wird ein Bankposten für den vollen Betrag der Einzahlung erstellt, wodurch der Bankabgleich vereinfacht werden kann.

### Fibu Erf.-Journalvorlagen für Bankeinzahlungen

Sie müssen auch eine Fibu Erf.-Journalvorlage für Einzahlungen erstellen. Fibu Erfassungsjournale werden verwendet, um Posten auf Bank-, Debitoren-, Kreditoren-, Anlagen- und Hauptbuchkonten zu buchen. Die Erf.-Journalvorlagen passen das Fibu Erf.-Journal an Ihren Arbeitszweck an. Das heisst, die Erf.-Journalvorlage enthält genau die Felder, die Sie benötigen.

Bei den Einzahlungen handelt es sich um Bareinnahmen. Daher möchten Sie Ihre Nummernserie möglicherweise für Bareinnahmenjournale wiederverwenden. Wenn Sie zwischen Einträgen von Bankeinzahlungen und Zahlungseingangs Erf.-Journalen unterscheiden müssen, verwenden Sie alternativ eine andere Nummernserie.

Sie müssen außerdem einen Batch-Job für die Vorlage erstellen. Um einen Batchauftrag zu erstellen, wählen Sie auf der Seite **Fibu Erf.-Journalvorlagen** die Aktion **Chargen** aus. Weitere Informationen zu Stapeln finden Sie unter [Buch-Blattvorlagen und Stapel nutzen](ui-work-general-journals.md#use-journal-templates-and-batches).

## Dimensionen in Bankeinzahlungszeilen

Die Zeilen der Bankeinzahlung verwenden die Standarddimensionen, die Sie in den Feldern  **Abteilungscode**  und  **Kundengruppencode**  angegeben haben. Wenn Sie im Feld  **Kontotyp** die Option  **Kunde** oder  **Lieferant**  auswählen, werden die Standardwerte durch die Dimensionen für den Kunden bzw. Lieferanten ersetzt. Die Dimensionen in den Zeilen können bei Bedarf geändert werden.

> [!TIP]
> Dimensionen in Zeilen werden gemäss „Standarddimension Prioritäten“ festgelegt. Zeilendimensionen haben Vorrang vor Kopfzeilendimensionen. Um Konflikte zu vermeiden, können Sie Regeln erstellen, die die Verwendung einer Dimension in Abhängigkeit von der Quelle priorisieren. Wenn Sie die Priorisierung von Dimensionen ändern möchten, können Sie ihre Prioritäten auf der Seite **Standarddimensionsprioritäten** ändern. Weitere Informationen finden Sie unter [Prioritäten für Standarddimensionen einrichten](finance-dimensions.md#to-set-up-default-dimension-priorities).

## Bankeinzahlung erstellen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Bankeinzahlungen** ein und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie **Neu** aus, um die Seite **Bankdepot** zu öffnen.
3. Wählen Sie die Fibu Erf.-Journalvorlage aus, die Sie für Bankeinzahlungen erstellt haben.  

    > [!NOTE]
    > Wenn die Fibu Erf.-Journalvorlage mehr als einen Stapel enthält, werden Sie aufgefordert, einen auszuwählen.

4. Wählen Sie im Feld **Bankkontonr.** das Bankkonto aus, auf das Sie den Betrag einzahlen möchten.

    > [!TIP]
    > Sie können überprüfen, ob Sie die Einzahlung auf das richtige Konto erfolgt, indem Sie die Hauptbucheinträge für das ausgewählte Bankkonto mithilfe der Aktionen **Kontokarte** und **Bankposten** suchen. Zum Beispiel, um zu überprüfen, ob ähnliche Einzahlungen auf das Konto getätigt wurden.

5. Geben Sie im Feld **Einzahlungsgesamtbetrag** den Gesamtbetrag der Einzahlung ein. Diese Summe muss die Summe der Beträge aller Zeilen sein.
6. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    Das Datum im Feld  **Buchungsdatum**  und die Dimensionen in den Feldern  **Abteilungscode**  und  **Kundengruppencode**  werden den Zeilen zugewiesen, die Sie für die Bankeinzahlung erstellen. Diese können bei Bedarf geändert werden.

7. Je nachdem, ob Sie das Bankguthaben pauschal oder jede Zeile einzeln ins Bank-/Sachkonto buchen möchten, aktivieren oder deaktivieren Sie den Umschalter **Als Abschlag buchen**. Die Standardeinstellung erfolgt über denselben Umschalter auf der Seite **Einkäufe und Verkäufe einrichten**.

    > [!NOTE]
    > Das Feld **Währungscode** zeigt die Währung an, die für das von Ihnen ausgewählte Bankkonto festgelegt ist. Sie können keine andere Währung auswählen.

8. Erstellen Sie im Inforegister **Zeilen** für jede Barzahlung, die Sie tätigen möchten, eine neue Zeile.
9. Geben Sie im Feld **Kontotyp** an, woher die Zahlung stammt. Für Bankeinzahlungen lautet der Typ in der Regel **Debitor** oder **Kreditor**.

    > [!NOTE]
    > Sie können auch eine Barzahlung an einen Kreditor registrieren. Wählen Sie dazu **Kreditor** aus, und geben Sie dann den Zahlungsbetrag als negative Zahl im Feld **Habenbetrag** der Zeile ein.

10. Geben Sie im Feld **Belegnr.** die Belegnummer der Rechnung ein, aus der der Habenbetrag stammt. Sie können für jede Zeile eine Belegnummer oder für alle Zeilen dieselbe Nummer verwenden.

    > [!TIP]
    > In der Regel müssen Sie das Feld **Belegtyp** für Finanzbuchungen nicht ausfüllen. Wenn Sie beispielsweise Bargeld aus einem Tagesverkauf einzahlen, lassen Sie das Feld leer. Wenn Sie Bargeld aus einer Debitorenzahlung einzahlen, wählen Sie **Zahlung** aus.

11. Wenn Sie eine Barzahlung für eine bestimmte Debitorenrechnung tätigen, wählen Sie die Aktion **Einträge anwenden** aus, und geben Sie dann im Feld **Ausgleichs-ID** die Rechnungsnummer ein.
12. Wenn Sie bereit sind, die Bankeinzahlung zu buchen, wählen Sie die Aktion **Buchen** aus.

    > [!NOTE]
    > Wenn das Bankkonto Standarddimensionen hat, bei denen das Feld  **Wertbuchung** die Optionen  **Code obligatorisch**,  **Gleicher Code** oder  **Kein Code** enthält, müssen Sie die Einzahlung als Pauschalbetrag buchen. Wenn Sie nicht als Pauschalbetrag buchen, kann die Buchung fehlschlagen, weil die Dimensionswerte der Konten in den Bankeinzahlungszeilen die Wertbuchungsregeln des Bankkontos verletzen.

    > [!TIP]
    > Bevor Sie die Einzahlung verbuchen, können Sie mit der Aktion  **Testbericht**  Ihre Angaben überprüfen. Der Bericht zeigt, ob Probleme vorliegen, beispielsweise fehlende Daten, die eine Buchung verhindern könnten.  

## Gebuchte Bankeinzahlungen finden

Auf der Seite **Gebuchte Bankeinzahlungen** sind die bisherigen Einzahlungen Ihres Unternehmens aufgelistet. In der Liste können Sie die Kommentare und Dimensionen überprüfen, die für die Einzahlungen angegeben wurden. Sie können die Bankeinzahlung öffnen, um weitere Details anzuzeigen, und von dort aus weitere Untersuchungen durchführen. Sie können beispielsweise die Aktion **Posten suchen** auswählen, um die gebuchten Bankposten anzuzeigen. Über den Bankposten können Sie den entsprechenden Hauptbucheintrag suchen.

Wenn Sie alle Hauptbucheinträge für die gebuchten Einzahlungszeilen suchen möchten, wechseln Sie zur Seite **Fibujournal**, und verwenden Sie die Aktion **Fibuposten**. Die Aktion zeigt alle Hauptbucheinträge an, einschließlich der Einträge für Debitoren und Kreditoren.

## Gebuchte Bankeinzahlung stornieren

Es gibt mehrere Möglichkeiten, eine gebuchte Bankeinzahlung rückgängig zu machen:

* Auf der Seite **Gebuchte Bankeinzahlungen** wählen Sie die Einzahlung und dann die Aktion **Buchung stornieren** aus.
* Suchen Sie auf der Seite **Fibujournale** das Journal für die Einzahlung, und wählen Sie dann die Aktion **Journal stornieren** aus.

> [!NOTE]
> Sie können nur ein Journal stornieren, das einen einzelnen Postentyp enthält. Das heisst, das Journal darf nur Debitorenposten oder Kreditorenposten enthalten, jedoch nicht beides. Wenn ein Journal beides enthält, müssen Sie die Einzahlung manuell stornieren.

## Weitere Informationen

[Finanzen](finance.md)  
[Einrichten von Finanzen](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]



