---
title: Zusätzliche Währungen festlegen
description: 'In der Anwendung wird der Fibuposten in der Mandantenwährung (MW) eingerichtet. Eine weitere Währung, der ein aktueller Wechselkurs zugewiesen ist, wird als zusätzliche Währung eingerichtet.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 07/23/2021
ms.author: bholtorf
---
# Einrichten einer zusätzlichen Berichtswährung

Da die Anzahl der Länder, in denen Unternehmen Geschäftsbeziehungen unterhalten, ständig wächst, wird es immer wichtiger, dass Finanzdaten in mehreren Währungen erfasst und angezeigt werden können.

> [!NOTE]  
> Wenn Sie in [!INCLUDE[prod_short](includes/prod_short.md)] nach Echtzeitinformationen zu Wechselkursen (FX) oder älteren Kursen suchen, werden diese als Währung bezeichnet. Siehe neben diesem Artikel auch [Währungswechselkurse aktualisieren](finance-how-update-currencies.md).


In der Anwendung wird der Fibuposten in der Mandantenwährung (MW) eingerichtet, aber eine weitere Währung, der ein aktueller Wechselkurs zugewiesen ist, kann als zusätzliche Währung eingerichtet werden. Wird eine zweite Währung als [!INCLUDE[prod_short](includes/prod_short.md)] Berichtswährung festgelegt, werden Beträge automatisch für jeden Fibuposten und weitere Posten, wie zum Beispiel MWST-Posten, in der Mandantenwährung und der Berichtswährung erfasst.

> [!Warning]
> Die Funktion Zusätzliche Berichtswährung sollte nicht als Grundlage für die Umrechnung von Abschlüssen verwendet werden, wenn Sie die Einschränkungen nicht verstehen. Es handelt sich dabei nicht um ein Tool, mit dem Finanzauswertungen von Niederlassungen im Rahmen einer Unternehmenskonsolidierung durchgeführt werden können. Die zusätzliche Berichtswährung kann nur verwendet werden, um Berichte in einer anderen Währung zu erstellen, so als ob diese Währung die Hauswährung der Firma wäre.
>
> Sie haben z.B. eine grosse Menge an Debitoren in Britischen Pfund (GBP) und Sie haben Ihre zusätzliche Berichtswährung (ACY) auf GBP festgelegt. In diesem Szenario werden die Beträge in den Debitoren, die GBP verwenden, nicht um Wechselkursgewinne/-verluste im ACY bereinigt, sondern nur die Beträge in den Debitoren, die in anderen Währungen sind. Das bedeutet, dass, wenn Sie ACY verwenden, um Ihren Jahresabschluss zu erstellen, dies zu unter- oder überbewerteten ausstehenden Salden der Debitoren führen kann.

## Anzeigen von Berichten und Beträgen in der Berichtswährung
Eine Berichtswährung kann in folgenden Fällen für das Berichtswesen eines Unternehmens hilfreich sein:

- Unternehmen in Nicht-EU-Ländern/-Regionen mit einem hohen Anteil von Transaktionen mit Unternehmen in EU-Ländern/-Regionen. In diesem Fall möchte das nicht-EU-Unternehmen seine Berichte möglicherweise ebenfalls in Schweizer Franken erstellen, damit diese für die Handelspartner in der EU besser nutzbar sind.
- Unternehmen, die Berichte in einer international gehandelten Währung anzeigen möchte, wenn dies auf deren Landeswährung nicht zutrifft.

Einige Finanzberichte basieren auf Fibuposten. Um die Finanzdaten in dem Bericht in der zusätzlichen Berichtswährung anzuzeigen, aktivieren Sie einfach das Feld **In Zusatzwährung anzeigen** im Inforegister **Optionen** für den entsprechenden Sachkontobericht.

## Regulieren von Wechselkursen

Da sich Wechselkurse ständig ändern, müssen weitere Währungsentsprechungen im System in regelmässigen Abständen reguliert werden. Werden diese Regulierungen nicht durchgeführt, sind Beträge, die aus fremden (oder zusätzlichen) Währungen umgerechnet und in der Mandantenwährung in der Finanzbuchhaltung gebucht wurden, möglicherweise irreführend. Darüber hinaus müssen Tagesposten, die vor der Eingabe eines Tageswechelkurses in der Anwendung gebucht werden, aktualisiert werden, nachdem der Tageswechselkurs eingegeben wurde. Die Stapelverarbeitung  **Wechselkurse** regulieren dient zur Regulierung der Wechselkurse gebuchter Kreditoren-, Debitoren- und Bankkontoposten. Berichtswährungsbeträge in Fibuposten können hiermit ebenfalls aktualisiert werden. Weitere Informationen finden Sie unter [Stapelverarbeitungsauftrag "Wechselkurse regulieren"](finance-how-update-currencies.md).

## Einrichten einer Berichtswährung

Folgen Sie diesen Schritten, um die zusätzliche Berichtswährung einzurichten:

- Legen Sie Fibukonten für die Buchung von Kursregulierungen fest.  
- Legen Sie Kursregulierungsart für alle Fibukonten fest.  
- Legen Sie die Kursregulierungsmethode für MWST.-Posten fest.  
- Aktivieren Sie die Berichtswährung.  

### Fibukonten für die Buchung von Kursregulierungen festlegen:  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Währungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Im Fenster **Währungen** geben Sie die folgenden Felder für die zusätzliche Berichtswährung an.  

|Feld|Description|  
|---------------------------------|---------------------------------------|  
|**Sachkto. Kursgewinn real. Kto**|Das Fibukonto, auf das Kursgewinne aus Wechselkursregulierungen zwischen der Mandantenwährung und der Berichtswährung gebucht werden sollen.|  
|**Sachkto. Kursverlust real. Kto**|Das Fibukonto, auf das Kursverluste aus Wechselkursregulierungen zwischen der Mandantenwährung und der Berichtswährung gebucht werden sollen.|  
|**Rundungsgewinn Konto**|Das Fibukonto, auf das Rundungsgewinne gebucht werden, wenn in der Anwendungsregion «Finanzbuchhaltung» Buchungen sowohl in der Mandantenwährung als auch in einer Berichtswährung durchgeführt werden.|  
|**Rundungsverlust Konto**|Das Fibukonto, auf das Rundungsverluste gebucht werden, wenn in der Anwendungsregion «Finanzbuchhaltung» Buchungen sowohl in der Mandantenwährung als auch in einer Berichtswährung durchgeführt werden.|

> [!NOTE]  
>  Rundungsbeträge können entstehen, wenn [!INCLUDE[prod_short](includes/prod_short.md)] Soll- und Habenbeträge rundet, die aus der Mandantenwährung in eine Berichtswährung umgerechnet wurden.  

Für jedes Fibukonto müssen Sie angeben, wie Beträge für dieses Konto hinsichtlich der Wechselkursschwankungen zwischen der Mandantenwährung und der Berichtswährung reguliert werden.  

### So geben Sie die Kursregulierungsmethode für alle Fibukonten an

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Kontenplan** wählen Sie das gewünschte Konto aus, und wählen Sie die **Bearbeiten** Aktion aus.  
3. Wählen Sie auf dem Inforegister **Berichtswesen** die richtige Methode im Feld **Kursregulierung** aus.  

    Wenn Sie Buchungen in einer Berichtswährung durchführen, geben Sie im Feld **Kursregulierung** an, wie dieses Fibukonto bei Wechselkursschwankungen zwischen der Mandantenwährung und der Berichtswährung ausgeglichen wird. Die folgende Tabelle enthält die Optionen, die Sie auswählen können.  

    |Feld|Beschreibung|  
    |----------------------------------|---------------------------------------|  
    |**Keine Regulierung**|Es wird keine Wechselkursregulierung auf das Fibukonto gebucht. Diese Option wird standardmässig verwendet.<br /><br /> **HINWEIS:** Die Option sollte ausgewählt werden, wenn der Wechselkurs zwischen der Mandantenwährung und der Berichtswährung immer fest ist.|  
    |**Betrag regulieren**|Der MW-Betrag wird gemäss der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Fibukonto im Feld **Betrag** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Fibukto. Kursgewinn real. Kto.** und **Fibukto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  
    |**Betrag (BW) regulieren**|Die zusätzliche Berichtswährung wird gemäss der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Fibukonto im Feld **Betrag (BW)** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Fibukto. Kursgewinn real. Kto.** und **Fibukto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  

    Wechselkursgewinne und -verluste werden erstmals bei Ausführung der Stapelverarbeitung **Wechselkurse regulieren** gebucht. In diesem Batchauftrag wird der regulierte Wechselkurs im Fenster **Währungswechselkurs** gefunden, und die Beträge in den Feldern **Betrag** und **Betrag (BW)** des Fibupostens werden anschliessend verglichen, um zu ermitteln, ob ein Kursgewinn oder -verlust vorliegt. Im Batchauftrag wird mithilfe der im Feld **Kursregulierung** ausgewählten Option bestimmt, ob Wechselkursgewinne oder -verluste für Fibukonten berechnet und gebucht werden.  

4.  Schliessen Sie das Fenster**Fibukontokarte**.  

### Die Kursregulierungsmethode für MWST.-Posten festlegen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Fibuposten Einrichtung** die richtige Methode im Feld **MWST-Kursregulierung** aus.  
3. Wenn Sie die Buchung in einer Berichtswährung durchführen, können Sie im Feld **MWST-Kursregulierung** angeben, wie die im Fenster **MWST Buchungsmatrix Einr.** für die Buchung der MWST eingerichteten Konten bei Wechselkursschwankungen zwischen der Mandantenwährung und der Berichtswährung reguliert werden.  

    Wenn Sie die Stapelverarbeitung **Wechselkurse regulieren** aufrufen, wird im Fenster **Währungswechselkurs** der regulierte Wechselkurs gefunden, und die Beträge in den Feldern **Betrag** und **Betrag (BW)** im MWST-Posten werden verglichen, um zu ermitteln, ob ein Kursgewinn oder -verlust vorliegt. Der Batchauftrag verwendet die von Ihnen gewählte Option zur Buchung von Wechselkursgewinnen oder -verlusten für MWST.-Konten.  

    Ihnen stehen dieselben Optionen wie bei Fibuposten zur Verfügung. Bei den regulierten Posten handelt es sich jedoch um MWST.-Posten. Die folgende Tabelle enthält die Optionen, die Sie auswählen können.

    |Feld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Keine Regulierung**|Es wird keine Wechselkursregulierung auf das Fibukonto gebucht. Diese Option wird standardmässig verwendet.|  
    |**Betrag regulieren**|Der MW-Betrag wird gemäss der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Fibukonto im Feld **Betrag** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Fibukto. Kursgewinn real. Kto.** und **Fibukto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  
    |**Betrag (BW) regulieren**|Die zusätzliche Berichtswährung wird gemäss der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Fibukonto im Feld **Betrag (BW)** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Fibukto. Kursgewinn real. Kto.** und **Fibukto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  

### Berichtswährung aktivieren:  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Fibuposten Einrichtung** das Feld **Berichtswährung**, um die Berichtswährung auszuwählen, in der Sie Daten erfassen möchten.  
3. Beim Verlassen des Felds zeigt [!INCLUDE[prod_short](includes/prod_short.md)] eine Bestätigungsmeldung an, die Sie über die Auswirkungen der Aktivierung der Berichtswährung informiert.  
4. Wählen Sie die Schaltfläche **Ja** aus, um zu bestätigen, dass Sie die Währung aktivieren möchten.  
5. Der Batchauftrag **Berichtswährung regulieren** wird geöffnet.

    Für die Stapelverarbeitung wird ein Standardwechselkurs verwendet. Dies ist der am Arbeitsdatum gültige Wechselkurs aus dem Fenster **Währungswechselkurse**. Rundungsbeträge, die bei der Umrechnung der Mandantenwährung in die Berichtswährung entstehen, werden auf die im Fenster **Währungen** angegebenen Differenzkonten für Gewinne und Verluste gebucht. Das Buchungsdatum und die Belegnummer dieser Posten ist mit denen des ursprünglichen Fibupostens identisch. Nachdem sämtliche Rundungsposten gebucht wurden, wird bei der Stapelverarbeitung ein Rundungsposten am Ultimodatum jedes abgeschlossenen Jahres auf das Abschlusskonto für die GuV gebucht. Hierdurch wird sichergestellt, dass der Endsaldo der GuV-Konten für alle abgeschlossenen Jahre in der Mandantenwährung und der Berichtswährung 0 ist.
6. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Wählen Sie die Schaltfläche **OK**, um den Batchauftrag zu starten.  

Nach die Stapelverarbeitung ausgeführt wurde, sind die Beträge in den folgenden bereits vorhandenen Posten in der Mandantenwährung und der Berichtswährung angegeben:  

- Fibuposten  
- Artikelausgleichsposten  
- MWST.-Posten  
- Projektposten  
- Wertposten  
- Fertigungsauftragszeilen  
- Fertigungsauftragsposten  

Darüber hinaus werden die Beträge für alle zukünftigen Posten desselben Typs sowohl in der Mandantenwährung als auch in der Berichtswährung erfasst.  

> [!NOTE]  
> Das Feld **Berichtswährung** wird erst aktiviert, nachdem Sie im Batchauftrag **Berichtswährung regulieren** die Schaltfläche **OK** gewählt haben.  

## Siehe verwandte [Microsoft Schulungen](/training/paths/use-multiple-currencies-dynamics-365-business-central/)

## Siehe auch

[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)  
[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
