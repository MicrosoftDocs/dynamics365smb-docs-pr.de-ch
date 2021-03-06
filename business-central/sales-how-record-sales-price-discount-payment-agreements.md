---
title: Besondere Verkaufspreise und Rabatte aufzeichnen| Microsoft Docs
description: Beschreibt, wie Preise die alternative und Rabattvereinbarungen definiert, die Sie zu Verkaufsbelegen beim Verkauf an verschiedene Debitoren gelten sollen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0873c45262dd9606ac187f5aab07b09677f6c1c8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035620"
---
# <a name="record-special-sales-prices-and-discounts"></a>Spezielle Verkaufspreise und Rabatte aufzeichnen

Die unterschiedlichen Preis- und Zahlungsrichtlinien, die beim Verkauf an verschiedene Debitoren gelten, müssen so definiert werden, dass die vereinbarten Regeln und Werte für Verkaufsbelege übernommen werden, die für den Debitor erstellt werden.

Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[prod_short](includes/prod_short.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Erf.-Journalzeilen berechnet. Weitere Informationen finden Sie unter [Beste Preisberechnung](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Für die Preise können Sie besondere auf den Verkaufszeilen verschiedene Verkaufspreise einfügen, wenn eine bestimmte Kombination aus Debitor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist. Weitere Informationen finden Sie unter [So legen Sie einen Verkaufspreis für einen Kunden fest](#to-set-up-a-sales-price-for-a-customer) und [Beste Preisberechnung](#best-price-calculation).  

Für die Rabatte können Sie zwei Arten von Verkaufsrabatten einrichten und verwenden:

| Rabattart | Beschreibung |
| --- | --- |
| **Verkaufszeilenrabatt** |Ein Betrag mit Rabatt wird auf den Verkaufszeilen eingefügt, wenn eine bestimmte Kombination aus Debitor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist. Diese Funktionalität gilt auf gleiche Weise für Verkaufsbelege. |
| **Rechnungsrabatt** |Ein prozentualer Rabatt, der gewährt wird, wenn der Wertbetrag aller Zeilen eines Verkaufsbelegs einen bestimmten Mindestwert übersteigt. |

Da Verkaufszeilenrabatte und Verkaufspreise auf einer Kombination aus Artikel und Debitor bestehen, können Sie diese Konfiguration auch auf der Artikelkarte des Artikels eingerichtet werden, für den die Regeln und Werte gelten.

> [!NOTE]  
> Wenn Sie einen Artikel nicht zu einem verbilligten Preis verkaufen möchten, lassen Sie einfach Skontofelder auf der Artikelkarte leer und schliessen Sie den Artikel nicht in einer Zeilenrabatteinrichtung ein.

## <a name="sales-invoice-discounts-and-service-charges"></a>Verkaufsrechnungsrabatte und Servicegebühren

Wenn Sie Rechnungsrabatte verwenden, bestimmt die Höhe des Rechnungsbetrages die Höhe des Rabattes, der gewährt wird.  

Auf der Seite **Debitorenrechnungsrabatte** können Sie einen Zuschlag für Rechnungen über einem bestimmten Betrag einrichten.  

Bevor Sie Rechnungsrabatte mit Verkäufen verwenden können, müssen Sie einige Informationen in der Anwendung definieren. Sie müssen Folgendes entscheiden:  

- Welchen Debitoren diese Art von Rabatt gewährt wird  
- Welche Rabattprozentsätze Sie verwenden möchten  

Wenn Sie Rechnungsrabatte automatisch berechnen möchten, können Sie dies auf der Seite **Debitoren und Verkauf einrichten** tun.  

Sie können für jeden Debitor angeben, ob Sie Rechnungsrabatte gewähren möchten, wenn die Anforderungen erfüllt sind (d. h. der Rechnungsbetrag gross genug ist). Sie können die Bedingungen für Rechnungsrabatte für inländische Debitoren in der Mandantenwährung und für ausländische Debitoren in Fremdwährung festlegen.  

Sie verknüpfen Rabattprozentsätze mit bestimmten Rechnungsbeträgen auf den Seiten **Debitorenrechnungsrabatte** für jeden Debitor. Sie können eine beliebige Anzahl von Prozentsätzen auf jeder Seite eingeben. Jeder Debitor kann eine eigene Seite haben, oder Sie können verschiedene Debitoren mit der gleichen Seite verknüpfen.  

Zusätzlich (oder anstatt) eines Rabattprozentsatzes können Sie einen Zuschlag mit einem bestimmten Rechnungsbetrag verknüpfen.  

> [!TIP]  
> Bevor Sie diese Informationen eingeben, ist es sinnvoll, eine Skizze der Rabattstruktur vorzubereiten, die Sie verwenden möchten. Dadurch wird es Ihnen erleichtert, zu erkennen, welche Debitoren mit derselben Rechnungsrabattseite verknüpft werden können. Wenn Sie weniger Seiten einrichten müssen, können Sie die Basisinformationen schneller eingeben.

Weitere Informationen zur Schulung für Rabatte bei Verkäufen finden Sie unter [Einrichten von Rabatten für Ihre Kunden](/learn/modules/customer-discounts-dynamics-365-business-central/index) unter Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Rechnungsrabatte bei Verkäufen berechnen

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>So erstellen Sie Verkaufszeilenrabatte für einen Debitor:

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Zeilenrabatte**.

    Auf der Seite **Verkaufszeilenrabatte** ist das Feld **Verkaufsart** mit **Debitor** vorausgefüllt und das Feld **Verkaufscode** ist mit der Debitorennummer vorausgefüllt.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

> [!Note]
> Wenn Sie die Fenster **Verkaufspreise** und **Verkaufszeilenrabatte** von einem bestimmten Debitoren öffnen, werden die Felder **Verkaufsartfilter** und **Verkaufscodefilter** für den Debitor festgelegt und können nicht geändert oder entfernt werden. Dies wird durch den grau unterlegten Wert im Feld **Verkaufscodefilter** angezeigt.
>
> Um Preise oder Zeilenrabatte für alle Debitoren, eine Debitorenpreisgruppe oder Kampagne einzurichten, müssen Sie die Fenster von einer Artikelkarte aus öffnen. Verwenden Sie alternativ für Verkaufspreise die Seite **Verkaufspreis-Arbeitsblatt**. Weitere Informationen finden Sie unter [So führen Sie eine Sammelaktualisierung von Artikelpreisen durch](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Um Rechnungsrabattkonditionen für Einkäufe einzurichten:

Nachdem Sie sich entschieden haben, welche Debitoren für Rechnungsrabatte in Frage kommen, geben Sie die Rechnungsrabattcodes auf den Debitorenkarten ein, und richten Sie die Bedingungen für die einzelnen Codes ein.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Debitorenkarte für einen Debitor, der für Rechnungsrabatte in Frage kommt.
3. Geben Sie im Feld **Rechnungsrabattcode** einen Code für das jeweilige Rechnungsrabattfenster ein, das die Anwendung verwenden soll, um Rechnungsrabatte für den Debitor zu berechnen.

    > [!NOTE]  
    > Rechnungsrabattcodes werden durch Bestandskundenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt.. Um kundenspezifische Rechnungsrabattbedingungen einzurichten, setzen Sie das Feld **Rechnungs-Rabatt-Code** auf den Kundencode des Kunden und fahren Sie dann mit dem nächsten Schritt fort.

4. Auf der Seite **Debitorenkarte** wählen Sie die Aktion **Rechnungsrabatt** aus. Die Seite **Debitorenrechnungsrabatte** wird geöffnet.
5. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in EUR einrichten möchten, dann lassen Sie das Feld leer.
6. Optional geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
7. Geben Sie im Feld **Rabatt** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
8. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Debitor einen Rechnungsrabatt erhält.

Der Rechnungsrabatt wird jetzt eingerichtet und dem fraglichen Debitor zugewiesen. Wenn Sie den Debitorencode im Feld **Rechnungs-Rabattcode** für andere Debitorenkarten auswählen, wird derselbe Rechnungsrabatt diesen Kunden zugewiesen.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Um Verkaufspreise für einen Debitor zu erstellen:

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Preise**.

    Auf der Seite **Verkaufspreise** ist das Feld **Verkaufsart** mit **Debitor** vorausgefüllt und das Feld **Verkaufscode** ist mit der Debitorennummer vorausgefüllt.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

## <a name="to-copy-sales-prices"></a>Verkaufspreise kopieren

Falls Sie Verkaufspreise kopieren möchten, wie z. B. den Preis eines einzelnen Debitors, um ihn in einer Debitorengruppe zu verwenden, müssen Sie die Stapelverarbeitung **VK-Preis vorschlagen** ausführen. Batchauftrag, den Sie von der Seite **Verkaufspreis-Arbeitsblatt** aus starten.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Verkaufspreisarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den **Vorgeschlagenen Verkaufspreis auf dem Arbeitsblatt.** Aktion  
3. Füllen Sie im Inforegister **Verkaufspreis** die Felder mit der **Verkaufsart** und dem **Verkaufscode** der ursprünglichen Preise aus, die Sie kopieren möchten.  
4. Füllen Sie im oberen Bereich der Anforderungsseite die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.  
5. Wenn Sie mit dem Batchauftrag neue Preise erstellen wollen, wählen Sie in das Feld **Neue Preise generieren**.  
6. Wählen Sie die Schaltfläche **OK** , um die Zeilen auf der Seite **VK-Preisvorschläge** mit den neuen Preisvorschlägen auszufüllen, und geben Sie an, dass diese für die gewählte Verkaufsart gültig sind.  

> [!NOTE]  
> Die Stapelverarbeitung erzeugt nur Vorschläge, implementiert die vorgeschlagenen Änderungen aber nicht. Falls Sie die Vorschläge annehmen möchten, d. h. sie auf der Seite **VK-Preise** übernehmen möchten, können Sie die Aktion **Preisvorschlag übernehmen** verwenden, die Sie auf der Seite **VK-Preisvorschläge** finden.

## <a name="to-bulk-update-item-prices"></a>So aktualisieren Sie Debitorenartikelpreise auf einmal

Wenn Sie Artikelpreise, wie alle Lagerzugangs-Artikelpreise durch einen Prozentsatz auf einmal aktualisieren möchten, müssen Sie **Artikelpreis vorschlagen** auswählen.  Batchauftrag. Sie finden den Link zur Stapelverarbeitung auf der Seite **VK-Preisvorschläge**.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Verkaufspreisarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den **Vorgeschlagenen Verkaufspreis auf dem Arbeitsblatt.** Aktion  
3. Geben Sie auf dem Inforegister **Zeilen** im Feld **Artikelnummer** oder **Bestand-Buchungsgruppe** oder andere Felder mit den ursprünglichen Artikelpreisen aus, die Sie aktualisieren möchten ein.  
4. Füllen Sie im oberen Bereich der Anforderungsseite die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.
5. Wenn Sie möchten, dass die Stapelverarbeitung automatisch eingegeben wird, geben Sie Artikelpreise anpassen ein im Feld **Korrekturfaktor**. Beispielsweise geben Sie entsprechend 1.15 unter **Korrekturfaktor** für die Preiserhöhung für den Artikelpreis um 15% ein.  
6. Wenn Sie mit dem Batchauftrag neue Preise erstellen wollen, wählen Sie in das Feld **Neue Preise generieren**.  
7. Wählen Sie die Schaltfläche **OK** , um die Zeilen auf der Seite **VK-Preisvorschläge** mit den neuen Preisvorschlägen auszufüllen, und geben Sie an, dass diese für die gewählte **Verkaufsart** gültig sind.  

> [!NOTE]
> Die Stapelverarbeitung erzeugt nur Vorschläge, implementiert die vorgeschlagenen Änderungen aber nicht. Wenn Sie mit den Vorschlägen zufrieden sind und sie annehmen möchten, d. h. sie in die Tabelle **Verkaufspreise** übernehmen möchten, können Sie den Batchauftrag **Preisvorschlag übernehmen** verwenden, den Sie im Register **Aktionen**, in der Gruppe **Funktionen** auf der Seite **VK-Preisformular** finden.

## <a name="best-price-calculation"></a>Beste Preisberechnung

Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[prod_short](includes/prod_short.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Erf.-Journalzeilen berechnet.

Der beste Preis ist der niedrigste mögliche Preis mit dem höchsten möglichen Zeilenrabatt an einem bestimmten Datum. [!INCLUDE[prod_short](includes/prod_short.md)] berechnet diesen, wenn Sie den Verkaufspreis und den prozentualen Zeilenrabatt für Artikel auf neuen Beleg und Buch.-Blattzeilen eingefügt haben.

> [!NOTE]  
> Nachfolgend wird erläutert, wie die besten Preise für Verkäufe berechnet werden. Die Berechnung ist die gleiche wie für Einkäufe.

1. [!INCLUDE[prod_short](includes/prod_short.md)] prüft die Kombination aus Rechnungsempfänger und Artikel und wählt den entsprechenden Preis/Rabatt unter Verwendung der folgenden Kriterien:

    - Hat dieser Debitor eine spezielle Vereinbarung für Preise oder Zeilenrabatte oder gehört der Debitor zu einer Gruppe, die solche Vereinbarungen hat?
    - Ist der Artikel oder die Artikelrabattgruppe in der Zeile in einer dieser Vereinbarungen enthalten?
    - Liegt das Auftragsdatum (oder das Buchungsdatum für die Rechnung und Gutschrift) innerhalb des Start- und Enddatums der Preis-/Zeilenrabatt-Vereinbarung?
    - Wurde ein Einheitencode angegeben? Falls dies der Fall ist, prüft [!INCLUDE[prod_short](includes/prod_short.md)] Preise/Rabatte mit dem gleichen Einheitencode und die Preise und Rabatte, bei denen kein Einheitencode angegeben wurde.

2. [!INCLUDE[prod_short](includes/prod_short.md)] überprüft, ob Preis-/Rabattvereinbarungen für Informationen für die Beleg- oder die Buch.-Blattzeile gilt und fügt dann den gültigen Einheitspreis und den prozentualen Zeilenrabatt, unter Verwendung der folgenden Kriterien ein:

    - Gibt es eine Mindestanzahl in der Preis-/Rabattvereinbarung, die erfüllt ist?
    - Gibt es eine Währungsanforderung in der Preis-/Rabattvereinbarung, die erfüllt ist? In diesem Fall werden der niedrigste Preis und der höchsten Zeilenrabatt für diese Währung eingefügt, selbst wenn lokale Währung einen besseren Preis liefern würde. Falls es für den angegebenen Währungscode keine Preis-/Zeilenrabatte gibt, verwendet [!INCLUDE[prod_short](includes/prod_short.md)] den niedrigsten Preis und den höchsten Zeilenrabatt in Ihrer lokalen Währung.

Wenn keine Spezialpreise für die Artikel in der Zeile gefunden werden, werden entweder letzte Einkaufspreis oder der VK-Preis von der Artikelkarte oder der Lagerhaltungsdatenkarte verwendet.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]