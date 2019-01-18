---
title: "Vorbereiten zur Einrichtung von Geschäftsbeziehungscodes für Kontakte | Microsoft Docs"
description: "Geschäftsbeziehungen in Business Central werden verwendet, um das Marketing zu erleichtern und um die Geschäftsbeziehung anzuzeigen, die Sie mit Ihren Interessenten, Debitoren und Debitoren haben, wie z. B. Bank oder Dienstleister."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-marketing
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 33743655f682aae9e02393aa68d04dffd334357b
ms.contentlocale: de-ch
ms.lasthandoff: 11/26/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Einrichten von Geschäftsbeziehungen für Kontaktunternehmen
Sie können Geschäftsbeziehungen verwenden, um die Geschäftsbeziehung anzuzeigen, die Sie mit Ihren Kontakten haben wie z. B. Interessent, Bank, Berater und Dienstleister usw. pflegen.

Die Nutzung von Geschäftsbeziehungen zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Geschäftsbeziehungscode. Sie müssen diesen Schritt nur einmal für jede Geschäftsbeziehung ausführen. Sobald Sie einen Geschäftsbeziehungscode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.

> [!NOTE]  
>   Wenn Sie planen, Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten in anderen Teilen der Anwendung zu synchronisieren, können Sie für sie eine Geschäftsbeziehung erstellen.

## <a name="to-define-a-business-relation-code"></a>Definieren eines Geschäftsbeziehungscodes
Der Geschäftsbeziehungscode definiert eine Kategorie oder einen Typ von Geschäftsbeziehung wie BANK oder Gesetz. Sie können mehrere Geschäftsbeziehungscodes haben. Um die Geschäftsbeziehung zu definieren, verwenden Sie die Seite **Geschäftsbeziehungen**.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Geschäftsbeziehung** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein. Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.

## <a name="AssignBusRelContact">Um Kontakten Geschäftsbeziehungen zuzuordnen:</a>
Sie können Geschäftsbeziehungen nicht zu Personen zuordnen – nur zu Unternehmen.

1. Öffnen Sie den Kontakt.
2. Wählen Sie die Aktion **Unternehmen** und dann die **Geschäftsbeziehungen**-Aktion aus.

    Die Seite **Kontakt Geschäftsbeziehungen** wird angezeigt.
3. Wählen Sie im Feld **Geschäftsbeziehungscode** die Geschäftsbeziehung aus, die Sie zuordnen möchten.

Wiederholen Sie diese Schritte, um beliebig viele Geschäftsbeziehungen zuzuordnen. Ausserdem können Sie Geschäftsbeziehungen auf die gleiche Art in dem Fenster Kontaktliste zuordnen.

Die Anzahl der Geschäftsbeziehungen, die Sie dem Kontakt auf der Kontaktkarte zugeordnet haben, wird im Feld **Anzahl Geschäftsbeziehungen** im Abschnitt **Segmentierung** auf der Seite **Kontakt** angezeigt.

Nachdem Sie Ihren Kontakten Geschäftsbeziehungen zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen. Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).

## <a name="see-also"></a>Siehe auch
[Kontaktunternehmenerstellen](marketing-create-contact-companies.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

