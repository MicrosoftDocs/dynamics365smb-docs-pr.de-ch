---
title: Abschließen der Buchhaltungsperioden für ein Geschäftsjahr | Microsoft Docs
description: Beschreibt, wie Sie die Buchhaltungsperioden schliessen, die das Geschäftsjahr ausmachen.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: e51d25b90a3f51953479906a35380541e02d7380
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "922925"
---
# <a name="close-accounting-periods"></a>Schliessen von Buchhaltungsperioden
Wenn ein Geschäftsjahr vorbei ist, müssen die Perioden, aus denen es besteht, geschlossen werden.

## <a name="to-close-accounting-periods"></a>Buchhaltungsperioden schliessen:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Buchhaltungsperioden** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie auf der Seite **Buchhaltungsperioden** die Aktion **Jahr auswählen** aus.

    Sind mehrere Geschäftsjahre offen, wird angenommen, dass das früheste automatisch abgeschlossen werden soll. Ein Mitteilungsfenster wird angezeigt, in dem das zu schliessende Jahr angegeben wird und die Konsequenzen erklärt werden.
3. Wählen Sie die Schaltfläche **Ja** aus, um das Jahr zu schliessen.

Das Geschäftsjahr ist geschlossen und die Felder **Abgeschlossen** und **Datum gesperrt** werden für alle Perioden des Jahres aktiviert. Das Geschäftsjahr kann nicht erneut geöffnet werden und Sie können das Häkchen aus den Feldern **Abgeschlossen** oder **Datum gesperrt** nicht mehr entfernen.

> [!NOTE]  
>   Sie können ein Geschäftsjahr erst abschliessen, wenn Sie ein neues erstellt haben. Beachten Sie, dass Sie nach dem Abschluss eines Geschäftsjahres das Startdatum des folgenden Geschäftsjahres nicht mehr ändern können.

Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Fibuposten gebucht werden. In diesen Fällen wird in den Posten vermerkt, dass die Buchung in einem abgeschlossenen Geschäftsjahr erfolgte, d. h., das Feld **Nachbuchung** wird mit einem Häkchen versehen.

Nachdem ein Geschäftsjahr abgeschlossen wurde, müssen Sie die Erfolgsrechnungsnullstellung durchführen und das Ergebnis auf ein Bilanzkonto übertragen lassen. Dies können das jedes Mal wiederholen, wenn Sie in ein abgeschlossenes Geschäftsjahr gebucht haben.

## <a name="see-also"></a>Siehe auch
[Schliessen der Bücher](year-close-books.md)  
[So buchen Sie den Jahresabschlussposten](year-how-post-year-end-close-entry.md)  
[Ein neues Geschäftsjahres eröffnen](finance-how-open-new-fiscal-year.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
