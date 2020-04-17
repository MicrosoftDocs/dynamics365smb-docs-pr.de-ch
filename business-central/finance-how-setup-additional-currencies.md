---
title: Richten von zusätzlichen Währungen| Microsoft Docs
description: In der Anwendung wird der Fibuposten in der Mandantenwährung (MW) eingerichtet. Eine weitere Währung, der ein aktueller Wechselkurs zugewiesen ist, wird als zusätzliche Währung eingerichtet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9802821985550668d460aa3213c9fb64764169c0
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183562"
---
# <a name="set-up-an-additional-reporting-currency"></a>Einrichten einer zusätzlichen Berichtswährung
Da die Anzahl der Länder, in denen Unternehmen Geschäftsbeziehungen unterhalten, ständig wächst, wird es immer wichtiger, dass Finanzdaten in mehreren Währungen erfasst und angezeigt werden können.

In der Anwendung wird der Fibuposten in der Mandantenwährung (MW) eingerichtet, aber eine weitere Währung, der ein aktueller Wechselkurs zugewiesen ist, kann als zusätzliche Währung eingerichtet werden. Wird eine zweite Währung als [!INCLUDE[d365fin](includes/d365fin_md.md)] Berichtswährung festgelegt, werden Beträge automatisch für jeden Fibuposten und weitere Posten, wie zum Beispiel MWST-Posten, in der Mandantenwährung und der Berichtswährung erfasst.

> [!Warning]
> Die Funktion "Berichtswährung" sollte nicht als Grundlage für die Umrechnung von Finanzauswertungen verwendet werden. Es handelt sich dabei nicht um ein Tool, mit dem Finanzauswertungen von Niederlassungen im Rahmen einer Unternehmenskonsolidierung durchgeführt werden können. Die Berichtswährungsfunktion bietet lediglich die Möglichkeit, Berichte so in anderen Währungen vorzubereiten, als handelte es sich dabei um die Mandantenwährung des Unternehmens.

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Anzeigen von Berichten und Beträgen in der Berichtswährung
Eine Berichtswährung kann in folgenden Fällen für das Berichtswesen eines Unternehmens hilfreich sein:

- Unternehmen in Nicht-EU-Ländern/-Regionen mit einem hohen Anteil von Transaktionen mit Unternehmen in EU-Ländern/-Regionen. In diesem Fall möchte das nicht-EU-Unternehmen seine Berichte möglicherweise ebenfalls in Euro erstellen, damit diese für die Handelspartner in der EU besser nutzbar sind.
- Unternehmen, die Berichte in einer international gehandelten Währung anzeigen möchte, wenn dies auf deren Landeswährung nicht zutrifft.

Einige Finanzberichte basieren auf Fibuposten. Um die Finanzdaten in dem Bericht in der zusätzlichen Berichtswährung anzuzeigen, aktivieren Sie einfach das Feld **In Zusatzwährung anzeigen** im Inforegister **Optionen** für den entsprechenden Sachkontobericht.

## <a name="adjusting-exchange-rates"></a>Regulieren von Wechselkursen
Da sich Wechselkurse ständig ändern, müssen weitere Währungsentsprechungen im System in regelmässigen Abständen reguliert werden. Werden diese Regulierungen nicht durchgeführt, sind Beträge, die aus fremden (oder zusätzlichen) Währungen umgerechnet und in der Mandantenwährung in der Fibuposten gebucht wurden, möglicherweise irreführend. Darüber hinaus müssen Tagesposten, die vor der Eingabe eines Tageswechelkurses in der Anwendung gebucht werden, aktualisiert werden, nachdem der Tageswechselkurs eingegeben wurde. Die Stapelverarbeitung  **Wechselkurse** regulieren dient zur Regulierung der Wechselkurse gebuchter Kreditoren-, Debitoren- und Bankkontoposten. Berichtswährungsbeträge in Fibuposten können hiermit ebenfalls aktualisiert werden. Weitere Informationen finden Sie unter [Stapelverarbeitungsauftrag "Wechselkurse regulieren"](finance-how-update-currencies.md).

## <a name="setting-up-an-additional-reporting-currency"></a>Einrichten einer Berichtswährung
Folgen Sie diesen Schritten, um die zusätzliche Berichtswährung einzurichten:

-   Legen Sie Sachkonten für die Buchung von Kursregulierungen fest.  
-   Legen Sie Kursregulierungsart für alle Sachkonten fest.  
-   Legen Sie die Kursregulierungsmethode für MWST.-Posten fest.  
-   Aktivieren Sie die Berichtswährung.  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments"></a>Sachkonten für die Buchung von Kursregulierungen festlegen:  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Währungen** ein und wählen Sie dann den entsprechenden Link.  
2. Im Fenster **Währungen** geben Sie die folgenden Felder für die zusätzliche Berichtswährung an.  

|Feld|Description|  
|---------------------------------|---------------------------------------|  
|**Sachkto. Kursgewinn real. Kto**|Das Sachkonto, auf das Kursgewinne aus Wechselkursregulierungen zwischen der Mandantenwährung und der Berichtswährung gebucht werden sollen.|  
|**Sachkto. Kursverlust real. Kto**|Das Sachkonto, auf das Kursverluste aus Wechselkursregulierungen zwischen der Mandantenwährung und der Berichtswährung gebucht werden sollen.|  
|**Rundungsgewinn Konto**|Das Fibukonto, auf das Rundungsgewinne gebucht werden, wenn im Anwendungsbereich "Finanzbuchhaltung" Buchungen sowohl in der Mandantenwährung als auch in einer Berichtswährung durchgeführt werden.|  
|**Rundungsverlust Konto**|Das Fibukonto, auf das Rundungsverluste gebucht werden, wenn im Anwendungsbereich "Finanzbuchhaltung" Buchungen sowohl in der Mandantenwährung als auch in einer Berichtswährung durchgeführt werden.|

> [!NOTE]  
>  Rundungsbeträge können entstehen, wenn [!INCLUDE[d365fin](includes/d365fin_md.md)] Soll- und Habenbeträge rundet, die aus der Mandantenwährung in eine Berichtswährung umgerechnet wurden.  

Für jedes Sachkonto müssen Sie angeben, wie Beträge für dieses Konto hinsichtlich der Wechselkursschwankungen zwischen der Mandantenwährung und der Berichtswährung reguliert werden.  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts"></a>So geben Sie die Kursregulierungsmethode für alle Sachkonten an  
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Kontenplan** wählen Sie das gewünschte Konto aus, und wählen Sie die **Bearbeiten** Aktion aus.  
3. Wählen Sie auf dem Inforegister **Berichtswesen** die richtige Methode im Feld **Kursregulierung** aus.  

    Wenn Sie Buchungen in einer Berichtswährung durchführen, geben Sie im Feld **Kursregulierung** an, wie dieses Fibukonto bei Wechselkursschwankungen zwischen der Mandantenwährung und der Berichtswährung ausgeglichen wird. Die folgende Tabelle enthält die Optionen, die Sie auswählen können.  

    |Feld|Beschreibung|  
    |----------------------------------|---------------------------------------|  
    |**Keine Regulierung**|Es wird keine Wechselkursregulierung auf das Sachkonto gebucht. Diese Option wird standardmässig verwendet.<br /><br /> **HINWEIS:** Die Option sollte ausgewählt werden, wenn der Wechselkurs zwischen der Mandantenwährung und der Berichtswährung immer fest ist.|  
    |**Betrag regulieren**|Der MW-Betrag wird gemäss der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Fibukonto im Feld **Betrag** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Fibukto. Kursgewinn real. Kto.** und **Fibukto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  
    |**Betrag (BW) regulieren**|Die zusätzliche Berichtswährung wird gemäss der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Fibukonto im Feld **Betrag (BW)** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Fibukto. Kursgewinn real. Kto.** und **Fibukto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  

    Wechselkursgewinne und -verluste werden erstmals bei Ausführung der Stapelverarbeitung **Wechselkurse regulieren** gebucht. In diesem Batchauftrag wird der regulierte Wechselkurs im Fenster **Währungswechselkurs** gefunden, und die Beträge in den Feldern **Betrag** und **Betrag (BW)** des Fibupostens werden anschliessend verglichen, um zu ermitteln, ob ein Kursgewinn oder -verlust vorliegt. Im Batchauftrag wird mithilfe der im Feld **Kursregulierung** ausgewählten Option bestimmt, ob Wechselkursgewinne oder -verluste für Fibukonten berechnet und gebucht werden.  

4.  Schliessen Sie das Fenster**Fibukontokarte**.  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries"></a>Die Kursregulierungsmethode für MWST.-Posten festlegen:  
1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Fibuposteneinrichtung** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Fibuposten Einrichtung** die richtige Methode im Feld **MWST-Kursregulierung** aus.  
3. Wenn Sie die Buchung in einer Berichtswährung durchführen, können Sie im Feld **MWST-Kursregulierung** angeben, wie die im Fenster **MWST Buchungsmatrix Einr.** für die Buchung der MWST eingerichteten Konten bei Wechselkursschwankungen zwischen der Mandantenwährung und der Berichtswährung reguliert werden.  

    Wenn Sie die Stapelverarbeitung **Wechselkurse regulieren** aufrufen, wird im Fenster **Währungswechselkurs** der regulierte Wechselkurs gefunden, und die Beträge in den Feldern **Betrag** und **Betrag (BW)** im MWST-Posten werden verglichen, um zu ermitteln, ob ein Kursgewinn oder -verlust vorliegt. Der Batchauftrag verwendet die von Ihnen gewählte Option zur Buchung von Wechselkursgewinnen oder -verlusten für MWST.-Konten.  

    Ihnen stehen dieselben Optionen wie bei Fibuposten zur Verfügung. Bei den regulierten Posten handelt es sich jedoch um MWST.-Posten. Die folgende Tabelle enthält die Optionen, die Sie auswählen können.

    |Feld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Keine Regulierung**|Es wird keine Wechselkursregulierung auf das Sachkonto gebucht. Diese Option wird standardmässig verwendet.|  
    |**Betrag regulieren**|Der MW-Betrag wird gemäss der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Fibukonto im Feld **Betrag** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Fibukto. Kursgewinn real. Kto.** und **Fibukto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  
    |**Betrag (BW) regulieren**|Die zusätzliche Berichtswährung wird gemäss der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Fibukonto im Feld **Betrag (BW)** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Fibukto. Kursgewinn real. Kto.** und **Fibukto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  

### <a name="to-activate-the-additional-reporting-currency"></a>Berichtswährung aktivieren:  
1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Fibuposteneinrichtung** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Fibuposten Einrichtung** das Feld **Berichtswährung**, um die Berichtswährung auszuwählen, in der Sie Daten erfassen möchten.  
3. Beim Verlassen des Felds zeigt [!INCLUDE[d365fin](includes/d365fin_md.md)] eine Bestätigungsmeldung an, die Sie über die Auswirkungen der Aktivierung der Berichtswährung informiert.  
4. Wählen Sie die Schaltfläche **Ja** aus, um zu bestätigen, dass Sie die Währung aktivieren möchten.  
5. Der Batchauftrag **Berichtswährung regulieren** wird geöffnet.

    Für die Stapelverarbeitung wird ein Standardwechselkurs verwendet. Dies ist der am Arbeitsdatum gültige Wechselkurs aus dem Fenster **Währungswechselkurse**. Rundungsbeträge, die bei der Umrechnung der Mandantenwährung in die Berichtswährung entstehen, werden auf die im Fenster **Währungen** angegebenen Differenzkonten für Gewinne und Verluste gebucht. Das Buchungsdatum und die Belegnummer dieser Posten ist mit denen des ursprünglichen Fibupostens identisch. Nachdem sämtliche Rundungsposten gebucht wurden, wird bei der Stapelverarbeitung ein Rundungsposten am Ultimodatum jedes abgeschlossenen Jahres auf das Abschlusskonto für die GuV gebucht. Hierdurch wird sichergestellt, dass der Endsaldo der GuV-Konten für alle abgeschlossenen Jahre in der Mandantenwährung und der Berichtswährung 0 ist.
6. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
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
>  Das Feld **Berichtswährung** wird erst aktiviert, nachdem Sie im Batchauftrag **Berichtswährung regulieren** die Schaltfläche **OK** gewählt haben.  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch
[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)  
[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
