---
title: Erstellen Sie einen Verkaufsauftrag, der mit einer Einkaufsbestellung für eine direkte Lieferung verknüpft ist | Microsoft Docs
description: Beschreibt, wie Sie einen Verkaufsauftrag erstellen, der mit einer Bestellung verknüpft ist, um sicherzustellen, dass die Artikel vom Kreditor direkt an den Debitor versendet werden
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c61f55701ecb07862f42d3cce242756001529588
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193697"
---
# <a name="make-drop-shipments"></a>Direktlieferungen machen
Eine Direktlieferung ist die Lieferung von Artikeln, von einem Ihrer Kreditoren direkt an einen Ihrer Debitoren.

Wenn ein Verkaufsauftrag für die Direktlieferung markiert ist und Sie einen Verkaufsauftrag erstellen, bei dem der Kunde im **Lief. an**-Feld, **Adresse Debitor** angegeben ist, können Sie die beiden Belege verknüpfen und so den Lieferanten anweisen, direkt an den Kunden zu senden.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>So erstellen Sie einen Verkaufsauftrag für eine Direktlieferung
Um eine Direktlieferung vorzubereiten, erstellen Sie einen normalen Verkaufsauftrag für einen Artikel, ausser dass Sie in der Verkaufsauftragszeile angeben müssen, dass für den Verkauf Direktlieferung benötigt wird.

1. Legen Sie einen Verkaufsauftrag für einen Artikel an. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
2. Aktivieren Sie in der Verkaufsauftragszeile für den Direktlieferungsartikel das Kontrollkästchen **Direktlieferung**. Verwenden Sie die Funktion **Spalten auswählen**, wenn das Feld nicht sichtbar ist. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>So erstellen Sie Bestellungen für Direktlieferungen:
Um eine Direktlieferung für den Artikel, der verkauft werden soll, vorzubereiten, erstellen Sie eine normale Bestellung, ausser dass Sie in der Bestellung angeben müssen, dass direkt an den Debitoren geliefert wird, nicht an Sie selbst.

1. Erstellen Sie eine Bestellung. Füllen Sie keines dieser Felder in den Zeilen aus. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).
2. Wählen Sie im Feld **Lief. an** **Adresse Debitor** aus.
3. Wählen Sie im Feld **Debitor** den Debitor aus, an den Sie verkaufen.
3. Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.
4. Auf der Seite **Verkaufsliste** wählen Sie den Auftrag, den Sie im Abschnitt [So erstellen Sie einen Verkaufsauftrag für Direktlieferung](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment) vorbereitet haben.
5. Wählen Sie die Schaltfläche **OK** aus.

Die Zeileninformation aus dem Auftrag werden in die Bestellzeile eingetragen.

Sie können nun den Kreditor anweisen, die Artikel an Ihren Kunden zu versenden, indem Sie ihm beispielsweise die Bestellung als PDF-Datei senden.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>So zeigen Sie den verknüpften Auftrag aus der Bestellung an
* Wählen Sie die Verkaufsauftragszeile der Direktlieferung aus, dann die Aktion **Bestellung**, die Aktion **Direktlieferung** und die Aktion **Bestellung**.

## <a name="to-post-a-drop-shipment"></a>So buchen Sie eine Direktlieferung:
Wenn der Kreditor die Artikel geliefert hat, können Sie den Verkaufsauftrag als geliefert buchen. Sie können auch die Bestellung buchen, aber nur mit der Option **Erhalten** bis der Verkaufsauftrag fakturiert wurde.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie den Verkaufsauftrag, den Sie in [So erstellen Sie einen Verkaufsauftrag für Direktlieferung]() erstellt haben.
3. Geben Sie im Feld **Zu liefernde Menge** an, wieviele der Bestellmengen geliefert werden sollen, die gesamte Menge oder eine Teilmenge.
4. Wählen Sie die Aktion **Buchen** oder **Buchen und Senden** aus.
5. Wählen Sie dann entweder die Option **Liefern**, um zu einem späteren Zeitpunkt zu fakturieren oder **Liefern und Fakturieren**, um sofort zu fakturieren.

## <a name="see-also"></a>Siehe auch
[Spezialaufträge erstellen:](sales-how-to-create-special-orders.md)  
[Einkauf von Artikeln für einen Verkauf](purchasing-how-purchase-products-sale.md)  
[Produkte verkaufen](sales-how-sell-products.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Verkauf](sales-manage-sales.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
