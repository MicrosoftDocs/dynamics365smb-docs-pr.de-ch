---
title: Zahlungsabstimmung mit der Envestnet Yodlee Bank Feeds Erweiterung
description: Beschreibt die Erweiterung „Envestnet Yodlee Bank Feeds“, die Verknüpfungen zu Bankkonten herstellt, sodass Sie Zahlungen schnell abstimmen können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d8a04218e44c4a40d96f5e84677434c51f6ef5f3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757406"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Die Envestnet Yodlee Bank Feeds-Erweiterung

Um die Zahlungen schnell abzustimmen, die an Ihre Bankkonten getätigt werden, kann der Dienst „Envestnet Yodlee Bank Feeds“ Ihre Systembankkonten mit Ihrem Online-Bankkonto verknüpfen. Das bedeutet, dass der letzte Bankkontoauszug automatisch oder manuell in Ihr Abstimmungs-Erfassungsjournal gespeist wird und stellt sicher, dass immer die aktuelle Zahlungen mit minimalem Fehlerrisiko verarbeitet werden.

Der Envestnet Yodlee Bank Feeds Service wird nur in den USA und in Kanada unterstützt.

> [!NOTE]
> Der Envestnet Yodlee Bank Feeds Service wird nur in der Online-Version von Business Central unterstützt. Um diese Funktionalität lokal nutzen zu können, müssen Sie ein Co-Brand-Konto von Envestnet Yodlee erhalten.<br /><br />
> Der Envestnet Yodlee Bank Feeds Service wird nur in den USA und in Kanada unterstützt.
> Es werden nur Banken mit Wohnsitz in diesen Ländern unterstützt, auch wenn Banken aus anderen Ländern im Bankenauswahlfenster Envestnet Yodlee Bank Feeds unter [!INCLUDE[prod_short](includes/prod_short.md)] erscheinen können.

> [!IMPORTANT]
> Aufgrund der neuen Zahlungsdiensterichtlinie in Europa (PSD2) können Sie nach dem 14. September 2019 nicht mehr automatisch Kontoauszüge von Banken in Grossbritannien importieren in [!INCLUDE[prod_short](includes/prod_short.md)]. Wir prüfen, ob wir dieses Funktion in Zukunft wieder anbieten können.

Der Envestnet Yodlee Bank Feeds-Service bietet die folgenden Vorteile:

* Entfernt die Anforderung zur manuellen Eingabe.
* Verbessert Effektivität und die Genauigkeit, wenn die Zahlungsabstimmung erfolgt.
* Unterstützt viele Banken.
* Hier aktuelle Informationen über Banktransaktionen in [!INCLUDE[prod_short](includes/prod_short.md)]
* Unterstützt manuelle sowie automatische Bankfeeds.
* Aktiviert das Outsourcing der Zahlungsabstimmung zu einem Buchhalter, indem das Bieten des Lagerzugang zu den Bankkontoauszügen bereitgestellt wird.

## <a name="available-bank-feeds"></a>Verfügbare Bankfeeds
Sie können prüfen, ob eine Bank unterstützt wird, indem Sie den Dienst Envestnet Yodlee Bank Feeds einrichten und sich mit ihm verbinden. Die Bank wird in der Liste angezeigt, wenn sie von Envestnet Yodlee unterstützt wird.

Weitere Informationen finden Sie unter [Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Siehe auch
[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)    
[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]