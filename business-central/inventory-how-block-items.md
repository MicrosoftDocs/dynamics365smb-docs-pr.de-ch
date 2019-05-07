---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: In Business Central kann ein Artikel als für Verkäufe, Einkäufe oder alle Verwendungszwecke gesperrt gekennzeichnet werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e13d59e939e71a252e08afc26d2fb1ec76b247c9
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "917540"
---
# <a name="block-items-from-sales-or-purchasing"></a>Artikel vom Verkauf oder Einkauf sperren
Sie können einen Artikel sperren, damit er nicht auf Verkaufs- oder Einkaufszeilen eingetragen werden kann, und Sie können ihn sperren, damit er nicht in einer Transaktion gebucht werden kann.  

In der folgenden Tabelle wird veranschaulicht, was beim Sperren von Artikeln passiert.  

|Option|Description|  
|--------------------|------------|  
|**Vertrieb gesperrt**|Der Artikel kann nicht in einem Verkaufsbeleg oder einem Erf.-Journal für Verkaufsartikel eingegeben werden.|  
|**Einkauf gesperrt**|Der Artikel kann nicht in einem Einkaufsbeleg, einem Erf.-Journal für Einkaufsartikel oder in Einkaufsplanungsprozessen eingegeben werden.|  
|**Gesperrt**|Der Artikel kann für keine Artikeltransaktion verwendet werden. Weitere Informationen zum Sperren eines Artikels für alle Zwecke erhalten Sie unter "Artikelkarte".|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>So sperren Sie einen Artikel vom Eintrag auf Verkaufszeilen  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.  

Wenn Sie versuchen, den Artikel in ein Verkaufsdokument oder eine Erf.-Journalzeile einzutragen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.  

Wenn Sie versuchen, den Artikel in ein Einkaufsdokument oder eine Erf.-Journalzeile einzutragen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.

## <a name="to-block-an-item-from-being-posted"></a>So sperren Sie einen Artikel vor der Buchung
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.

Wenn Sie versuchen, irgendeine Transaktion für den Artikel zu buchen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.

## <a name="see-also"></a>Siehe auch  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
