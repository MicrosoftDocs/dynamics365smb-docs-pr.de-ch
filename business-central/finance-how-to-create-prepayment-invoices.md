---
title: 'Gewusst wie: Vorauszahlungsrechnungen erstellen | Microsoft Docs'
description: Erfahren Sie, wie Sie Situationen bearbeiten, in denen Vorauszahlung gefordert wird, oder Ihr Kreditor dies fordert.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5f227cc73531111ae15f69d6fba5ac541e28560c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746880"
---
# <a name="create-prepayment-invoices"></a>Vorauszahlungsrechnungen erstellen

Wenn Sie von Ihren Debitoren erwarten, dass diese vor der Lieferung eines Auftrags eine Vorauszahlung leisten, können Sie die Funktion „Vorauszahlung“ verwenden. Dies gilt auch, wenn Ihr Verkäufer erwartet, dass Sie die Zahlung übermitteln, bevor er eine Bestellung an Sie versendet.  

Sie können den Vorauszahlungsprozess starten, wenn Sie eine Einkaufsbestellung oder einen Verkaufsauftrag erstellen. Wenn Sie für diesen Debitor oder Kreditor einen standardmässigen Vorauszahlungsprozentsatz haben, wird dieser automatisch in die resultierende Vorauszahlungsrechnung aufgenommen. Sie können auch einen Vorauszahlungsprozentsatz für das gesamte Dokument angeben.

Nachdem Sie einen Auftrag oder eine Bestellung angelegt haben, können Sie eine Vorauszahlungsrechnung erstellen. Sie können für Verkaufs- oder Einkaufszeile die Standardprozentsätze verwenden, oder Sie können den Betrag den Anforderungen entsprechend anpassen. So können Sie beispielsweise den Gesamtbetrag für den gesamten Auftrag angeben.  

Im Folgenden wird beschrieben, wie eine Vorauszahlung für einen Verkaufsauftrag fakturiert wird. Die Schritte sind für eine Bestellung ähnlich.  

## <a name="to-create-a-prepayment-invoice"></a>So erstellen Sie eine Vorauszahlungsrechnung

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie einen neuen Verkaufsauftrag für den relevanten Debitor. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)  

    Auf dem Inforegister **Vorauszahlung** gibt das Feld **Vorauszahlung %** den Prozentsatz an, der zur Berechnung des Vorauszahlungsbetrags verwendet werden soll. Wenn auf der Debitorenkarte ein standardmässiger Vorauszahlungsprozentsatz angegeben ist, wird das Feld automatisch ausgefüllt. Sie können den Prozentsatz ändern. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Wählen Sie das Feld **Vorauszahlung komprimieren** aus, falls Sie auf der Vorauszahlungsrechnung Zeilen erstellen möchten, die Zeilen aus dem Kundenauftrag zusammenfassen, wenn folgende Bedingungen zutreffen:  

    - Es wird das gleiche Fibukonto für Vorauszahlungen verwendet, wie unter "Buchungsmatrix Einrichtung" festgelegt.  
    - Es werden die gleichen Dimensionen verwendet.  

    Wenn Sie eine Vorauszahlungsrechnung angeben möchten, die für jede Auftragszeile mit einem Vorauszahlungsprozentsatz eine Zeile enthält, wählen Sie nicht das Feld **Vorauszahlung komprimieren** aus.  

    Das Fälligkeitsdatum für die Vorauszahlung wird automatisch basierend auf dem Wert für **Zlg.-Bedingungscode Vorauszahlung** berechnet.

3. Füllen Sie die Verkaufszeilen aus.  

    Wenn Sie einen standardmässigen Vorauszahlungsprozentsatz für den Debitor oder auf dem Inforegister **Vorauszahlung** in diesem Dokument festgelegt haben, wird dieser Wert in jede Zeile kopiert. Sie können den Inhalt des Felds  in der Zeile **Vorauszahlung %** ändern.  

4. Um den gesamten Vorauszahlungsbetrag anzuzeigen, wählen Sie die Aktion **Statistik**.

    Wenn Sie den gesamten Vorauszahlungsbetrag für den Auftrag anpassen möchten, können Sie den Inhalt des Feldes **Vorauszahlungsbetrag** auf der Seite **Verkaufsauftragsstatistik** ändern.  

    Wenn das Feld **Preise inkl. MwSt** aktiviert ist, kann das Feld **Vorauszahlungsbetrag einschl. MwSt**. geändert werden.  

    Wenn Sie den Inhalt des Felds **Vorauszahlungsbetrag** ändern, wird der Betrag proportional auf alle Zeilen aufgeteilt, mit Ausnahme der Felder, bei denen im Feld **Vorauszahlung** der Wert **0** angegeben ist.  

5. Wählen Sie zum Drucken eines Testberichtes vor der Buchung der Vorauszahlungsrechnung die Aktion **Vorauszahlung** und dann die Aktion **Vorauszahlungstestbericht**.  
6. Wählen Sie zum Buchen der Vorauszahlungsrechnung die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsrechnung**.  

    Klicken Sie zum Buchen und Drucken der Vorauszahlungsrechnung die Aktion **Vorauszahlungsrechnung buchen und drucken**.  

Es können weitere Vorauszahlungsrechnungen für den Auftrag ausgegeben werden. Erhöhen Sie hierzu den Vorauszahlungsbetrag für eine oder mehrere Zeilen, passen Sie im Bedarfsfall das Belegdatum an, und buchen Sie die Vorauszahlungsrechnung. Für die Differenz zwischen den bisher fakturierten Vorauszahlungsbeträgen und dem neuen Vorauszahlungsbetrag wird eine neue Rechnung erstellt.  

> [!NOTE]  
> Wenn Sie in Nordamerika sind, können Sie den Prozentsatz nicht ändern, nachdem die Vorauszahlungsrechnung gebucht wurde. Dieses wird in der nordamerikanischen Version von [!INCLUDE[prod_short](includes/prod_short.md)] verhindert, da die Berechnung der Salestax ansonsten falsch ist.  

 Wenn Sie bereit zum Buchen des verbleibenden Rechnungsbetrags sind, buchen Sie diesen auf die gleiche Weise, wie Sie jede andere Rechnung buchen. Der Vorauszahlungsbetrag wird automatisch vom fälligen Betrag abgezogen.  

## <a name="see-also"></a>Siehe auch

[Fakturieren von Vorauszahlungen](finance-invoice-prepayments.md)  
[Exemplarische Vorgehensweise: Einrichten und Fakturieren von Verkaufsvorauszahlungen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]