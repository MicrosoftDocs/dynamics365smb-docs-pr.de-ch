---
title: "Einrichten von Internetfavoriten für Kontaktunternehmen| Microsoft Docs"
description: "Sie können Internet oder Internetfavoriten definieren und diese einem Kontaktunternehmen zuordnen, die Ihnen helfen, zu identifizieren, wie Sie nach Informationen über die Kontakte suchen möchten."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b81deefcdf79a93cc988d216f80b08794efb8ab6
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-web-sources-for-contact-companies"></a>Vorgehensweise: Einrichten von Internetfavoriten für Kontaktunternehmen
Sie können Ihren Kontakten Internetfavoriten (z. B. Suchmaschinen und Websites) zuordnen, um anzuzeigen, wo Sie im Internet nach Informationen über die Kontakte suchen möchten. Wenn Sie Internetfavoriten zuordnen, legen Sie fest, welche Suchmaschine und welchen Suchbegriff die Anwendung bei der Suche nach der gewünschten Information verwendet.

Die Nutzung von Internetfavoriten zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Buchungsspurcode. Sie müssen diesen Schritt nur einmal für jeden Internetfavoriten ausführen. Sobald Sie einen Buchungsspurcode haben, können Sie den Code zu den Kontaktpersonen zuweisen.

## <a name="to-define-a-web-source-code"></a>um einen Internetfavoritencode zu definieren
1. Wählen Sie das Symbol ![Nach Seite oder Bericht] (media/ui-search/search_small.png "Nach Seite oder Bericht suche") und geben **Internetquellen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder **Code**, **Beschreibung** und **URL** aus.

    Geben Sie %1 im Feld **URL** ein, um einen Platzhalter für einen Suchbegriff in der URL einzufügen. Wenn Sie den Internetfavoriten von einer Kontaktkarte aus aktivieren, wird "%1" automatisch durch das Suchwort ersetzt (z. B. den Namen eines Unternehmens), das Sie in dem Fenster **Kontakt-Internetfavoriten** eingegeben haben.

Wiederholen Sie diese Schritte, um weitere Internetfavoriten einzurichten.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Um Internetfavoriten zu einem Kontaktunternehmen zuzuordnen
Wenn Sie Internetfavoriten zuordnen, legen Sie fest, welche Suchmaschine und welchen Suchbegriff die Anwendung bei der Suche nach der gewünschten Information verwendet.

1. Öffnen Sie den Kontakt.
2. Wählen Sie die Aktion **Unternehmen** und dann die **Internetfavoriten**-Aktion aus. Das Fenster **Kontakt Internetfavoriten** wird geöffnet.
3. Wählen Sie im Feld **Internetfavoritencode** den Internetfavoriten aus, den Sie zuordnen möchten.
4. Geben Sie im Feld **Suchbegriff** den Suchbegriff ein, der bei der Suche nach der Information verwendet werden soll.

Wiederholen Sie diese Schritte, um weitere Internetfavoriten zuzuordnen.

Außerdem können Sie Internetfavoriten auf die gleiche Art in dem Fenster **Kontaktliste** zuordnen.

## <a name="see-also"></a>Siehe auch
[Kontaktunternehmenerstellen](marketing-create-contact-companies.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

