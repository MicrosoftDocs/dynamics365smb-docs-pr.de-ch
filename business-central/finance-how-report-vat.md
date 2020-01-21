---
title: Übermitteln von MWST-Berichten an die Steuerbehörden | Microsoft Docs
description: Erfahren Sie, wie Sie Berichte erstellen, die die MWST aus Verkäufen in einer Periode bzw. aus Verkäufen und Einkäufen darstellt, und übermitteln Sie den Bericht an eine Steuerbehörde.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 01/13/2020
ms.author: bholtorf
ms.openlocfilehash: e7671e54f95a48322df186b5aed5a81552f9f91f
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953793"
---
# <a name="report-vat-to-tax-authorities"></a>Melden von MWST an die Steuerbehörden
Dieses Thema beschreibt die Berichte in [!INCLUDE[d365fin](includes/d365fin_md.md)], die Sie verwenden können, um MWST-Informationen über Einkäufe und Verkäufe an die Steuerbehörden in Ihrer Region zu senden.

Es können folgende Berichte verwendet werden:

* Der Verkaufslistenbericht **EU-Verkaufsliste** führt MWST-Beträge der Europäischen Union (EU) auf, die Sie für Verkäufe an für MWST registrierte Debitoren innerhalb der EU eingetrieben haben  
* Der Bericht **MWST-Rückgabe** enthält die MWST für Verkäufe und Einkäufe an Debitoren in allen Ländern, die MWST verwenden.

Wenn Sie den gesamten Verlauf von MWST-Posten anzeigen möchten, erstellt jede Buchung, die Mehrwertsteuer beinhaltet, einen Posten auf der Seite **MWST-Posten**. Diese Posten werden verwendet, um Ihren MWST.-Abrechnungsbetrag (Ihrer Zahlung oder Erstattung) für eine bestimmte Periode zu berechnen. Zum Anzeigen von MWST-Einträgen wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Kostenbudgeteinträge löschen** ein, und wählen Sie dann den zugehörigen Link.

## <a name="about-the-ec-sales-list-report"></a>Info über den Bericht „EU-Verkaufsliste“
In Grossbritannien müssen alle Unternehmen, die Waren und Dienstleistungen an für Mehrwertsteuer registrierte Debitoren verkaufen, einschliesslich Debitoren in anderen Ländern der Europäischen Union (EU), eine elektronische Version des Verkaufslistenberichts der MWST-Beträge der Europäischen Union (EU) im XML-Format an die HMRC-Website (Her Majesty's Revenue and Customs) senden. Der EU-Verkaufslistenbericht passt nur für Länder in der EU.

Der Bericht enthält eine Zeile für jede Art Transaktion mit dem Debitor und zeigt den Gesamtbetrag für jede Art von Transaktionen an. Es gibt drei Arten von Transaktionen, die der Bericht enthalten kann:  

* B2B-Waren  
* B2B-Dienste  
* Triangulierte Waren B2Bs  

B2B-Waren und Dienste geben an, ob Sie eine Ware oder einen Dienst verkauften, und werden durch die **EU-Service** in der MWST Buchungsmatrix-Einrichtung gesteuert. Triangulierte Waren B2Bs geben an, ob Sie sich im Einzelhandel mit einem Kreditor engagierten und durch die Einstellung **EU-Dreiecksgeschäft** in Verkaufsbelegen, wie Aufträge, Rechnungen, Gutschriften, usw. gesteuert werden.  

Nachdem die Steuerbehörden den Bericht erneut erstellen, senden Sie eine E-Mail an die Kontaktperson des Unternehmens. In [!INCLUDE[d365fin](includes/d365fin_md.md)], wird die Kontaktperson auf der Seite **Firmendaten** angegeben. Bevor Sie den Bericht senden, prüfen Sie, ob eine Kontaktperson ausgewählt ist.

## <a name="about-the-vat-return-report"></a>Über den MWST-Rückgabebericht
Verwenden Sie diesen Bericht, um MWST für Einkaufs- und Verkaufsbelege zu senden, wie Bestellungen und Verkaufsaufträge, Rechnungen und Gutschriften. Die Informationen dieses Berichts haben dabei dasselbe Format wie die Formulare der Finanz- und Steuerbehörden.  

Die Mehrwertsteuer wird auf Basis der MWST-Buchungsmatrix-Einr. und der MWST-Buchungsgruppen berechnet, die Sie eingerichtet haben.

Für die Mehrwertsteuerrückgabe können Sie die Posten angeben, die berücksichtigt werden sollen:

* Buchen Sie nur offene Transaktionen oder geöffnete und geschlossene. Dies ist beispielsweise dann nützlich, wenn Sie die abschliessende jährliche Mehrwertsteuerrückgabe vorbereiten.
* Buchen Sie nur Posten aus den angegebenen Zeiträumen, oder aktualisieren Sie auch Posten aus den vorherigen Perioden. Dies dient zum Aktualisieren der Mehrwertsteuerrückgabe, die Sie bereits gebucht haben, wenn zum Beispiel ein Kreditor eine verspätete Rechnung sendet.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Um sich mit der Webdienst Ihrer Steuerbehörde zu verbinden
[!INCLUDE[d365fin](includes/d365fin_md.md)] stellt die Dienst-Verbindungen für Steuerbehördenwebsites bereit. Wenn Sie beispielsweise in Grossbritannien sind, können Sie die **GovTalk**-Dienst-Verbindung ausführen, um die EU-Verkaufsliste und MWST-Rückgabeberichte elektronisch zu senden. Wenn Sie den Bericht manuell buchen möchten, indem Sie z. B. die Daten auf der Website der Steuerbehörden eingeben, ist dies nicht erforderlich.   

Um MwSt an eine Steuerbehörden zu übermitteln, müssen Sie den [!INCLUDE[d365fin](includes/d365fin_md.md)] mit der Steuerbehörde verbinden. Dazu ist es erforderlich, dass Sie ein Konto mit Ihrer Steuerbehörden einrichten. Wenn Sie ein Konto haben, können Sie eine Dienst-Verbindung ausführen, die wir in [!INCLUDE[d365fin](includes/d365fin_md.md)] voraussetzen.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Serviceverbindungen** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die entsprechenden Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >   Es ist empfehlenswert, die Verbindung zu testen. Um dies zu tun, aktivieren Sie das Kontrollkästchen **Testmodus**, bereiten den MWST-Bericht vor und senden ihn wie im Abschnitt _Vorbereiten und Übermitteln eines MWST-Berichts_ beschrieben. Im Testmodus testet der Dienst, ob die Steuerbehörden den Bericht erhalten, und der Status des Berichts gibt an, ob die Testübermittlung erfolgreich war. Denken Sie daran, dass dies keine tatsächliche Datenübermittlung ist. Um den tatsächlichen Bericht zu senden, müssen Sie das Feld **Testmodus** deaktivieren und dann den Übermittlungsvorgang wiederholen.

## <a name="to-set-up-vat-reports-in-included365finincludesd365fin_mdmd"></a>Einrichten von MWST-Berichten in [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **MWST-Berichtsservice** ein und wählen Sie dann den entsprechenden Link.  
2. Wenn Sie Benutzer diesen Bericht ändern und erneut senden lassen möchten, wählen Sie das Kontrollkästchen **Übermittelte Berichte ändern**.  
3. Wählen Sie die Nummernserie für jeden Bericht.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Vorbereiten und Übermitteln eines MWST-Berichts
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **EU-Verkaufsliste** oder **MWST-Rückgabe** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie Aktion **Neu** aus, und füllen Sie die relevanten Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um den Inhalt des Berichts zu erstellen, wählen Sie die **Vorschlagszeilen** Aktion.  

    > [!NOTE]  
    >   Für den EU-Verkaufslistenbericht können Sie Transaktionen überprüfen, die in den Berichtszeilen enthalten sind, bevor Sie den Bericht senden. Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **MwSt-Einträge anzeigen** aus.  
4. Um einen Bericht für die Übermittlung zu überprüfen und vorzubereiten, wählen Sie die **Freigabe**-Aktion.  

    > [!NOTE]  
    >   [!INCLUDE[d365fin](includes/d365fin_md.md)] prüft, ob der Bericht korrekt eingerichtet ist. Wenn die Prüfung fehlschlägt, werden die Fehler im Fenster **Fehler und Warnungen**  angezeigt, sodass Sie entsprechende Änderungen vornehmen können. Wenn die Meldung zu einer fehlenden Einstellung in [!INCLUDE[d365fin](includes/d365fin_md.md)] erfolgt, können Sie auf die Nachricht klicken, um die Seite zu öffnen, die die Informationen zur Korrektur enthält.  
5. Um den Bericht zu buchen, wählen Sie die **Übermitteln** Aktion.  

Nachdem Sie den Bericht gesendet haben, überwacht [!INCLUDE[d365fin](includes/d365fin_md.md)] den Service und bewahrt einen Datensatz Ihrer Kommunikation auf. Das Feld **Status** gibt an, wo der Bericht in Bearbeitung ist. Beispielsweise wenn die Behörden Ihren Bericht verarbeiten, ändert sich der Status des Berichts auf **Erfolgreich**. Wenn die Steuerbehörde Fehler im Bericht finden, erhält der Bericht den Status **Fehler**. Sie können die Fehler unter **Fehler und Warnungen** anzeigen, korrigieren und den Bericht erneut senden. Um eine Liste Ihrer EU-Verkaufsübersichts-Berichte anzuzeigen, wechseln Sie zur Seite **EU-Verkaufsübersichts-Berichte**.  

## <a name="viewing-communications-with-your-tax-authority"></a>Zeigt den Verlauf der Kommunikation mit der Steuerbehörde an
In einigen Ländern tauschen Sie Meldungen mit Steuerbehörden aus, wenn Sie Berichte senden. Sie können die erste und letzte Meldung anzeigen, die Sie gebucht oder erhalten haben, indem Sie die Aktionen **Übermittlungsnachricht herunterladen** und **Antwornachricht herunterladen** gewählt haben.  

## <a name="submitting-vat-reports-manually"></a>Manuelles Senden von MWST-Berichten
Wenn Sie eine andere Methode verwenden, um den Bericht zu buchen, indem Sie beispielsweise die XML exportieren und sie in eine Steuerbehördenwebsite, können Sie sie danach **als übermittet markieren**, um den Berichtszeitraum zu schliessen. Wenn Sie den Bericht als freigegeben kennzeichnen, ist er nicht mehr editierbar. Wenn Sie die Erklärung ändern müssen, nachdem Sie sie als freigegeben gekennzeichnet haben, müssen Sie sie zuerst erneut öffnen.

## <a name="vat-settlement"></a>MWST-Abrechnung
Die Netto-MWST muss in regelmässigen Abständen an die Steuerbehörden überwiesen werden. Bei häufigen MWST-Abrechnungen können Sie die Stapelverarbeitung **MWST abrechnen und buchen** ausführen, um die offenen MWST-Posten abzuschliessen und die MWST-Beträge für Einkäufe und Verkäufe an das MWST-Abrechnungskonto zu übertragen.

Die Übertragung von MWST-Beträgen auf Abrechnungskonten bedeutet, dass das Vorsteuerkonto im Haben und das Umsatzsteuerkonto im Soll mit den für die angegebene Abrechnungsperiode berechneten Beträge bebucht wird. Der Nettobetrag wird als Haben auf das MWST-Ausgleichskonto gebucht (oder als Soll, wenn der Einkaufs-MWST-Betrag grösser ist). Sie können die Abrechnung unmittelbar buchen oder erst einen Testbericht ausdrucken.  

> [!Note]
> Wenn Sie die Stapelverarbeitung **MWST abrechnen und buchen** verwenden und keine **MWST-Geschäftsbuchungsgruppe** und **MWST-Produktbuchungsgruppe** angeben, werden Posten mit den Geschäftsbuchungsgruppen und Produktbuchungsgruppencodes einbezogen.

## <a name="configuring-your-own-vat-reports"></a>MwSt-Bericht konfigurieren
Sie können den EU-Verkaufslistenberichtsstandard verwenden, aber Sie können auch eigene Berichte erstellen. Dazu ist es erforderlich, dass Sie mehrere Codeunits erstellen. Wenn Sie Hilfe benötigen, kontaktieren Sie einen Microsoft Partner.  

Die folgende Tabelle beschreibt Codeunits, die Sie für den Bericht erstellen müssen.

| Codeunit | Was sie tun müssen |
|----|-----|
|Vorschlagszeilen| Abrufen von Informationen aus der Tabelle MWST-Posten und sie in den Zeilen des MWST-Berichts anzeigen|
|Inhalt | Kontollieren Sie das Format des Berichts. Beispielsweise ob es XML oder JSON ist. Das Format, das zu verwenden ist, hängt von den Anforderungen des Webdiensts Ihrer Steuerbehörden ab. |
|Übermittlung | Steuern Sie, wie und wann Sie den Bericht basierend auf den Anforderungen Ihrer Steuerbehörden senden. |
|Antwort-Handler | Bearbeit die Antwort der Steuerbehörden. Beispielsweise sendet sie eine E-Mail an die Kontaktperson Ihres Mandanten. |
|Abbrechen | Senden Sie eine Stornierung eines MwSt-Berichts, der zuvor zu Ihrer Steuerbehörden gesendet wurde. |  

> [!Note]
> Wenn Sie Codeunits für den Bericht erstellen, passen Sie auf den Wert im Feld **MwSt Berichts-Version** auf. Dieses Feld muss der Version des Berichts entsprechen, der von der Steuerbehörde verlangt wurde oder verlangt wird. Beispielsweise können Sie**2017** in dieses Feld eingeben, um anzugeben, dass der Bericht der Anforderungen entspricht, die im letzten Jahr verlangt wurden. Um die aktuellen Version zu finden, setzen Sie sich mit den Steuerbehörden in Verbindung.

## <a name="see-related-training-at-microsoft-learnlearnpathsprocess-vat-dynamics-365-business-central"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch
[Methoden für die Berechnung und Buchung von Mehrwertsteuer einrichten](finance-setup-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
