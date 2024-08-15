---
title: Zahlungen auf nicht ausgeglichene Verkaufsbelege anwenden
description: 'Sie gleichen die Beträge aus, die von den Debitoren mit Bezug auf den entsprechenden Verkaufsbeleg bezahlt werden und buchen die Zahlungen, um den Debitor, die Fibuposten und die Bankposten zu aktualisieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 07/08/2024
ms.service: dynamics-365-business-central
---

# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Debitorenzahlungen aus einer Liste mit unbezahlten Verkaufsbelegen abstimmen

Nachdem Kunden elektronische Zahlungen auf Ihr Bankkonto getätigt haben, müssen Sie die folgenden Massnahmen ergreifen:

* Wenden Sie jede Zahlung auf den entsprechenden gebuchten Verkaufsbeleg an.
* Buchen Sie Zahlungseingänge, um die Debitoren-, Fibuposten- und Bankposten zu aktualisieren.

Abhängig von den Unternehmensanforderungen können Sie Zahlungen manuell, automatisch und durch Zahlungsverkehr registrieren.  

> [!NOTE]  
> Dieselben Aufgaben, einschliesslich Kreditorenzahlungen, können Sie auf der Seite **Zahlungsabstimmungs-Erf.-Journal** ausführen. Sie können beispielsweise Bankauszüge importieren, die automatische Anwendung verwenden und Bankkonten abstimmen. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

Verwenden Sie die Seite **Debirotenzahlungen registrieren**, um interne Konten auszugleichen, indem mithilfe von tatsächlichen Kassenzahlen sichergestellt wird, dass Zahlungen eingezogen werden. Sie können Einzel- oder Pauschalzahlungen schnell prüfen und buchen, Skontozahlungen verarbeiten und unbezahlte Belege finden.

Sie müssen Zahlungen für verschiedene Debitoren mit verschiedenen Fälligkeitsdaten als einzelne Zahlungen buchen. Zahlungen für denselben Debitor, der das gleiche Fälligkeitsdatum hat, können als Pauschalzahlung gebucht werden. Pauschalzahlungen sind beispielsweise dann nützlich, wenn ein Debitor eine einzelne Zahlung getätigt hat, die mehrere Verkaufsrechnungen umfasst.

## <a name="to-set-up-the-payment-registration-journal"></a>Zahlungsregistrierungserf.-Journal einrichten

Da Sie verschiedene Zahlungsarten auf verschiedene Gegenkonten buchen können, müssen Sie ein Gegenkonto auf der Seite **Zahlungsanmeldungs-Einrichtung** auswählen, bevor Sie die Bearbeitung von Debitorenzahlungen starten. Wenn Sie immer auf das gleiche Gegenkonto buchen, können Sie dieses Konto als Standardwert festlegen und diesen Schritt jedes Mal vermeiden, wenn Sie die Seite **Debitorenzahlung erfassen** öffnen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einrichtung der Zahlungsregistrierung** ein und wählen Sie dann den zugehörigen Link. Sie können auch auf der Seite **Debitorenzahlung erfassen** die Aktion **Einrichten** auswählen.
2. Füllen Sie die Felder auf der Seite **Zahlungserfassungseinrichtung** aus. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)].  

> [!TIP]
> Um später Buchungen, die über das Journal gebucht wurden, leichter identifizieren zu können, können Sie dem Erfassungsjournal eine bestimmte Nummernserie zuweisen. Die Nummernserie ist hilfreich, wenn Sie Zahlungsabstimmungs-Erfassungsjournale verwenden, um Zahlungen zu registrieren und anzuwenden.

## <a name="to-register-customer-payments-individually"></a>Um Debitorenzahlungen einzeln zu erfassen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Debitoren-Zahlungen registrieren** ein und wählen Sie dann den zugehörigen Link.  

    Die Seite **Debitorenzahlungen registrieren** werden alle gebuchten Belege angezeigt, für die eine Zahlung erfasst werden kann. Sie können die Seite auch über die Seiten **Debitoren** und **Debitorenkarte** öffnen, die für den angegebenen Debitoren gefiltert wird.  
2. Wählen Sie das Kontrollkästchen **Zahlung erfolgt** in der Zeile, die den gebuchten Beleg darstellt, für den eine Zahlung geleistet wurde.
3. Geben Sie im Feld **Empfangsdatum** das Datum ein, an dem die Zahlung gemacht wurde. Dieses Datum kann vom Arbeitsdatum abweichen.  

   Wenn das Kontrollkästchen **Automatische Datumseingabe** auf der Seite **Einrichtung der Zahlungserfassung** aktiviert ist, enthält das Feld **Empfangsdatum** das Arbeitsdatum.  
4. In dem Feld **Betrag erhalten** geben Sie den Betrag ein, der bezahlt wurde.

    Für gesamte Zahlungen ist dies der gleiche Betrag wie der Betrag im Feld **Verbleibender Betrag** in der Zeile. Für Teilzahlungen ist dieser Betrag niedriger als der Betrag im Feld **Verbleibender Betrag** in der Zeile.
5. Wiederholen Sie die Schritte 2 bis 4 für gebuchte Belege, für die Zahlungen getätigt wurden.  
6. Wählen Sie die Aktion **Zahlung buchen** aus.  

Die eingegebene Zahlungsinformation wird für Belege in Zeilen gebucht, in denen das Kontrollkästchen **Zahlung erhalten** aktiviert ist. Zahlungsposten werden im Fibuposten, Bank und in Debitorenkonten gebucht.

## <a name="to-reconcile-lump-sum-payments"></a>Pauschalzahlungen verarbeiten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Debitoren-Zahlungen registrieren** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Kontrollkästchen **Zahlung erfolgt** in den Zeilen der gebuchten Belege für denselben Debitor, für die eine Pauschalzahlung geleistet wurde.  

    > [!NOTE]  
    > Der Debitor im Feld **Name** muss der Gleiche in allen Zeilen sein, die in die Pauschalzahlung einbezogen werden sollen.  

    Wenn das Kontrollkästchen **Automatische Datumseingabe** auf der Seite **Einrichtung der Zahlungserfassung** aktiviert ist, enthält das Feld **Empfangsdatum** das Arbeitsdatum.  
3. Geben Sie im Feld **Empfangsdatum** das Datum ein, an dem die Zahlung gemacht wurde. Dieses Datum kann vom Arbeitsdatum abweichen.  

    > [!NOTE]  
    > Dieses Datum muss das gleiche in allen Zeilen sein, die als Pauschalzahlung gebucht werden.  
4. Geben Sie im Feld **Betrag erhalten** die Beträge in mehreren Zeilen ein, die den einmaligen Zahlungsbetrag zusammenfassen.  

    > [!TIP]  
    > Versuchen Sie, mit dem Pauschalbetrag so viele volle Zahlungen wie möglich zu buchen. Geben Sie Beträge auf so viele Zeilen wie möglich ein, die dieselben sind, wie der Betrag im Feld **Verbleibender Betrag**.  
5. Wiederholen Sie die Schritte 2 bis 4 für andere Zeilen, die für gebuchte Belege für denselben Debitor stehen, für den eine Pauschalzahlung geleistet wurde.  
6. Wählen Sie die Aktion **Als einmalige Zahlung buchen** aus.

   Die eingegebene Zahlungsinformation wird für Belege in Zeilen gebucht, in denen das Kontrollkästchen **Zahlung erhalten** aktiviert ist. Zahlungseingänge werden in Fibuposten, Bank und in Debitorenkonten gebucht. Jede Zahlung wird für den entsprechenden gebuchten Verkaufsbeleg angewandt.  

Wenn eine Zahlung in der Bank nicht durch eine Zeile auf der Seite **Debitoren-Zahlungen registrieren** dargestellt wird, liegt das möglicherweise daran, dass der zugehörige Beleg noch nicht gebucht wurde. In diesem Fall können Sie eine Suchfunktion verwenden, um den Beleg zu buchen und schnell zu suchen, um die Zahlung zu verarbeiten. Weitere Informationen finden Sie unter [Bestimmten Verkaufsbeleg suchen, der nicht vollständig fakturiert wurde](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Wenn eine Zahlung in der Bank nicht durch einen Beleg dargestellt wird, können Sie ein ausgefülltes Fibu-Erfassungsjournal über die Seite **Debitorenzahlungen registrieren** öffnen, um die Zahlung direkt auf das Gegenkonto zu buchen, ohne die Zahlung auf einen Beleg anzuwenden. Alternativ können Sie die Zahlung im Erfassungsjournal buchen, bis der Ursprung der Zahlung gelöst wurde. Weitere Informationen finden Sie im Abschnitt [Zahlung ohne zugehörigen Beleg erfassen oder buchen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Vorgehensweise: Manuelle Verarbeitung von Zahlungen mit Rabatten

Wenn Sie ein Skonto mit dem Debitor vereinbart haben, können die Zahlungsbeträge niedriger als die fakturierten Beträge sein, wenn die Zahlung vor dem vereinbarten Skontodatum auftritt.  

Dieses Thema erläutert Verfahren zum Buchen von verbilligten Zahlungen auf der Seite **Zahlungserfassung**.  

* Der Zahlungsbetrag entspricht dem diskontierten Betrag und dessen Zahlungsdatum liegt vor dem Rabattdatum. Sie buchen die Zahlung, wie sie ist.  
* Der Zahlungsbetrag entspricht dem diskontierten Betrag, aber dessen Zahlungsdatum liegt nach dem Skontodatum. Sie buchen die Zahlung als Teilzahlung. Der Beleg bleibt offen, um den Restbetrag einzufordern/zu bezahlen. Sie können das Skontodatum später festlegen, um die vollständige Bezahlung zu ermöglichen.  
* Die Zahlungssumme ist niedriger als der verbleibende diskontierte Betrag. Sie buchen die Zahlung als Teilzahlung. Der Beleg bleibt offen, um den Restbetrag einzufordern/zu bezahlen.  
* Die Zahlungssumme ist höher als der verbleibende diskontierte Betrag. Sie buchen die Zahlungen, wie sie sind. Nur der Restbetrag wird gebucht. Der extra Betrag wird dem Debitor gutgeschrieben.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Zahlungsbetrag verarbeiten, der dem diskontierten Betrag entspricht und dessen Zahlungsdatum vor dem Skontodatum liegt

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Debitoren-Zahlungen registrieren** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie den Zahlungsbetrag im Feld **Betrag erhalten** ein. Der Betrag ist gleich wie der Betrag im Feld **Restbetrag inkl. Rabatt**.

    Das Kontrollkästchen **Zahlung erfolgt** wird automatisch aktiviert und das Feld **Empfangsdatum** mit dem Arbeitsdatum ausgefüllt.
3. Geben Sie im Feld **Datum erhalten** das Zahlungsdatum ein. Das Datum steht vor dem Datum im Feld **Skontodatum**.
4. Vergewissern Sie sich, dass das Feld **Restbetrag** den Wert Null (0) enthält.  
5. Wählen Sie auf der Registerkarte **Zahlung buchen**, um den Gesamtbetrag auf Sach-, Bank- und Debitorenkonten zu buchen.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Zahlungsbetrag verarbeiten, der dem diskontierten Betrag entspricht, dessen Zahlungsdatum jedoch nach dem Rabattdatum liegt

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Debitoren-Zahlungen registrieren** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie den Zahlungsbetrag im Feld **Betrag erhalten** ein. Der Betrag ist gleich wie der Betrag im Feld **Restbetrag inkl. Rabatt**.

    Das Kontrollkästchen **Zahlung erfolgt** wird automatisch aktiviert und das Feld **Empfangsdatum** mit dem Arbeitsdatum ausgefüllt.
3. Geben Sie im Feld **Eingangsdatum** ein Zahlungsdatum an, das nach dem Datum im Feld **Skontodatum** liegt.

   Datumsfelder ändern zu roter Schrift, und eine Fehlermeldung wird unten auf der Seite angezeigt. Das Problem wird mit den nächsten beiden Schritte behoben.
4. Wählen Sie die Aktion **Details** aus.  
5. Geben Sie auf der Seite  **Zahlungsregistrierungsdetails**  im Feld  **Zahlungsrabattdatum**  auf dem Inforegister  **Zahlungsrabatt**  ein Datum ein, das nach dem Datum im Feld  **Empfangsdatum**  auf der Seite  **Zahlungsregistrierungseinrichtung**  liegt.  

    Die Fehlermeldung und die rote Schriftart verschwinden, und Sie können fortfahren, die verbilligte Zahlung zu bearbeiten.
6. Vergewissern Sie sich, dass das Feld **Restbetrag** den Betrag enthält, der verbleibt, um den vollständigen Rechnungsbetrag zu bezahlen.  
7. Wählen Sie die Aktion **Zahlung buchen**, um den Teilbetrag auf Sach-, Bank- und Debitorenkonten zu buchen.  

Der zugehörige Beleg bleibt offen.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Zahlung verarbeiten, die niedriger als der verbleibende diskontierte Betrag ist

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Debitoren-Zahlungen registrieren** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie den Zahlungsbetrag im Feld **Betrag erhalten** ein. Der Betrag ist kleiner als der Betrag im Feld **Restbetrag inkl. Rabatt**.

    Das Kontrollkästchen **Zahlung erfolgt** wird automatisch aktiviert und das Feld **Empfangsdatum** mit dem Arbeitsdatum ausgefüllt.  
3. Geben Sie im Feld **Datum erhalten** das Zahlungsdatum ein. Das Datum steht vor dem Datum im Feld **Skontodatum**.
4. Vergewissern Sie sich, dass das Feld **Restbetrag** den Betrag enthält, der verbleibt, um den rabattierten Rechnungsbetrag zu bezahlen.  
5. Wählen Sie die Aktion **Zahlung buchen**, um den Teilbetrag auf Sach-, Bank- und Debitorenkonten zu buchen.  

Der zugehörige Beleg bleibt offen.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Zahlung verarbeiten, die höher als der verbleibende diskontierte Betrag ist

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Debitoren-Zahlungen registrieren** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie den Zahlungsbetrag im Feld **Betrag erhalten** ein. Der Betrag ist grösser als der Betrag im Feld **Restbetrag inkl. Rabatt**.  

    Das Kontrollkästchen **Zahlung erfolgt** wird automatisch aktiviert und das Feld **Empfangsdatum** mit dem Arbeitsdatum ausgefüllt.
3. Geben Sie im Feld **Datum erhalten** das Zahlungsdatum ein. Das Datum steht vor dem Datum im Feld **Skontodatum**.
4. Vergewissern Sie sich, dass das Feld **Restbetrag** den Wert Null (0) enthält.  
5. Wählen Sie auf der Registerkarte **Zahlung buchen**, um den Gesamtbetrag auf Sach-, Bank- und Debitorenkonten zu buchen.  

Der zugehörige Beleg ist abgeschlossen, und dem Debitor wird der Überzahlungsbetrag gutgeschrieben.  

## <a name="to-find-a-specific-sales-document-that-isnt-fully-invoiced"></a>Bestimmten Verkaufsbeleg suchen, der nicht vollständig fakturiert wurde

Die Seite **Debitoren-Zahlungen registrieren** unterstützt Sie bei Aufgaben, die interne Konten mit tatsächlichen Bargeldabbildungen ausgleichen müssen, um die effektive Sammlung von Debitoren sicher zu stellen. Es zeigt ausstehende eingehende Zahlungen als Zeilen an, welche Verkaufsbelege darstellen, in denen ein Betrag zur Zahlung fällig ist.  

Wenn eine Zahlung erfolgt oder bei der Bank oder auf andere Weise erfasst wird, wird der Verkaufs- oder Einkaufsbeleg in der Regel als Zeile auf der Seite **Debitoren-Zahlungen registrieren** dargestellt. Der Beleg wartet auf Ihre Buchung der Zahlung des ausstehenden Betrags. Manchmal wird jedoch eine Zahlung, die geleistet wurde, nicht durch eine Zeile auf der Seite **Debitoren-Zahlungen registrieren** dargestellt, da der Beleg in der Regel nich vollständig fakturiert ist.

Verwenden Sie die Aktion **Belege durchsuchen**, um nach Belegen zu suchen, die nicht vollständig fakturiert wurden. Sie können basierend auf einer oder mehrerer der folgenden Kriterien suchen:  

* Belegnummer  
* Betrag oder Betragsbereich  

Nachfolgend wird erklärt, wie man einen bestimmten Beleg findet, indem man beide Suchkriterien verwendet.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Debitoren-Zahlungen registrieren** ein und wählen Sie dann den zugehörigen Link.
2. Zeigen Sie mit dem Mauszeiger auf eine beliebige Zeile und wählen Sie **Beleg suchen**.
3. Auf der Seite **Belegsuche** geben Sie einen Suchwert im Feld **Belegnummer** ein.  

    > [!NOTE]  
    > Der Wert, den Sie hier eingeben, ist in den ausgeblendeten Platzhalterzeichen enthalten. Das bedeutet, dass die Aktion in allen Belegnummern sucht, die den eingegebenen Wert enthalten.
4. Geben Sie in dem Feld **Betrag** den entsprechenden Betrag auf dem Beleg ein, den Sie suchen möchten.  
5. Geben Sie im Feld **Betragsabwicklung in %** einen Prozentwert ein, um den Bereich von Beträgen zu definieren, die Sie sehen möchten, um den offenen Beleg zu finden.  

    Wenn Sie den Wert „10“ eingeben, sucht die Aktion nach Beträgen in einem Bereich von plus oder minus 10 Prozent des Werts im Feld **Betrag**.
6. Wählen Sie die Aktion **Suchen** aus.  

Wenn ein oder mehrere Belege mit den Suchkriterien im Feld **Ergebnis Belegsuche** übereinstimmen, wird die Seite geöffnet, um Zeilen anzuzeigen, die diese Belege darstellen. Jede Zeile enthält eine Belegnummer, eine Beschreibung und einen Betrag.

Wenn eine Zahlung in der Bank nicht durch einen Beleg dargestellt wird, können Sie ein ausgefülltes Fibu-Erfassungsjournal über die Seite **Debitorenzahlungen registrieren** öffnen, um die Zahlung direkt auf das Gegenkonto zu buchen, ohne die Zahlung auf einen Beleg anzuwenden. Alternativ können Sie die Zahlung im Erfassungsjournal buchen, bis der Ursprung der Zahlung gelöst wurde.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Zahlung ohne zugehörigen Beleg erfassen oder buchen

Wenn eine Zahlung in der Bank nicht durch einen Beleg dargestellt wird, können Sie mit der Aktion **Fibu-Erfassungsjournal** eine ausgefüllte Fibu-Erfassungsjournal-Zeile über die Seite **Debitorenzahlungen registrieren** öffnen. Verwenden Sie das Erfassungsjournal, um die Zahlung direkt auf das Gegenkonto zu buchen, ohne die Zahlung einem Beleg zuzuordnen. Alternativ können Sie die Zahlung im Erfassungsjournal buchen, bis der Ursprung der Zahlung gelöst wurde.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Debitoren-Zahlungen registrieren** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Fibu Erf.-Journal** aus.  

    Die Seite **Fibu Erf.-Journal** wird mit einer Zeile geöffnet, die das Saldokonto des Erf.-Journals enthält, das auf der Seite **Zahlungserfassungs-Einrichtung** festgelegt ist.  
3. Füllen Sie die übrigen Felder jeder Fibu Erf.-Journalzeile aus. Geben Sie beispielsweise den Betrag, die Debitorennummer oder Informationen aus dem Kontoauszug an. Weitere Informationen finden Sie unter [Transaktionen direkt im Fibuposten buchen](finance-how-post-transactions-directly.md).  

Sie können die Erf.-Journalzeile buchen, um die Summe in dem Gegenkonto zu aktualisieren. Alternativ können Sie die Erfassungsjournalzeile ungebucht lassen und ggf. mit einer Notiz anfügen, dass die Zahlung mehr Analyse benötigt.  

Wenn Sie die Erfassungsjournalzeile nicht buchen, wird ihr Wert dem Wert im Feld **Restbetrag inkl. Rabatt** auf der Seite **Zahlungserfassung** hinzugefügt.  

## <a name="see-also"></a>Siehe auch

[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
