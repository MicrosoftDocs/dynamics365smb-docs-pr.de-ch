---
title: Abschreibungsverwaltung einrichten| Microsoft Docs
description: "Um Anlagenreparaturen und -Dienst zu verwalten, geben Sie allgemeine Wartungsinformationen, Codes für die Art der Arbeit und eine Buchung für Kosten an."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cdf1183fb5383311dc34d8c2c619a1eddf7e8851
ms.contentlocale: de-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-fixed-asset-maintenance"></a>So geht's: Einrichten der Anlagenwartung
Um die Anlagenwartung zu verwalten, müssen Sie erst einige allgemeine Wartungsinformationen einrichten, ein Buchungskonto für Wartungskosten und Wartungscodes für die Arten von Arbeit, beispielsweise Instandhaltung oder Reparatur.

## <a name="to-set-up-general-maintenance-information"></a>So richten Sie allgemeine Wartungsinformationen ein:
Wenn Sie die Felder für Wartung eingerichtet haben, können Sie Wartungsausgaben aus einem Erf.-Journal buchen.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Anlage, für die Sie den Versicherungsposten festlegen wollen, und wählen die Aktion **Bearbeiten** aus.
3. Füllen Sie auf dem Inforegister **Wartung** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>So richten Sie Wartungscodes ein
Wenn Sie Wartungskosten aus einem Fibu Buch.-Blatt buchen, füllen Sie das Feld **Wartungscode** aus. So erfassen Sie, welche Art von Wartung durchgeführt wurde, beispielsweise Instandhaltung oder Reparatur.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Wartung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Legen Sie im Fenster **Wartung** Codes für unterschiedliche Arten von Wartungsarbeiten fest.

## <a name="to-set-up-maintenance-expense-accounts"></a>So richten Sie Aufwandskonten für die Wartung ein
Um Wartungskosten zu buchen, müssen Sie erst eine Kontonummer im Fenster **Anlagenbuchungsgruppen** eingeben.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen-Buchungsgruppe** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie das Feld **Aufwandskto. Wartung** für jede einzelne Buchungsgruppe aus.

> [!NOTE]  
>   Um festzulegen, ob Wartungskosten auf Kostenstellen und/oder Kostenträger verteilt werden, müssen Sie einen Verteilungsschlüssel einrichten. Weitere Informationen finden Sie unter [So geht's: Allgemeine Anlagenfeatures einrichten](fa-how-setup-general.md).

## <a name="see-also"></a>Siehe auch
[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Finanzen](finance.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

