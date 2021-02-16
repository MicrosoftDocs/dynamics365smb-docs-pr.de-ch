---
title: Buchen Sie Zahlungsanzeige-Erweiterung | Microsoft Docs
description: Beschreibt das Senden der Zahlungsanzeigeerweiterung, die das Buchen und das Neuversenden der Zahlungsanzeige aus dem Zahlungsausgangs Erf.-Journal und den Kreditorenposten zulassen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3ae8d131b714b0d7ffb60727d1a991cd6e4ab692
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757081"
---
# <a name="send-remittance-advice"></a>Rimesseavis senden

Wenn Zahlungsanzeigen verwendet werden, um Kreditoren über die Zahlungen zu benachrichtigen, die erstellt werden, können Sie Zahlungsanzeige als Massenvorgang aus dem Zahlungsausgangs-Erf.-Journal buchen und erneut senden, nachdem die Zahlungen von Kreditorenposten getätigt werden, indem Sie Belegsendeprofile verwenden.

> [!NOTE]
> Diese Funktionalität wird nur in Business Central online und lokal in folgenden Ländern unterstützt: Grossbritannien, USA, Kanada, Australien Neuseeland, und Südafrika.  

Sie können Zahlungsanzeigen auf zwei verschiedene Arten senden:

* Auf der Seite **Zahlungsausgangs Erf.-Journal** wählen Sie **Zugehörig**, **Zahlungen**, **Überweisungsbescheid senden**, um den Überweisungsbescheid für eine oder mehrere Zahlungsausgangs Erfassungsjournalzeilen per E-Mail zu senden.
* Wählen Sie auf der Seite **Kreditorenposten** **Aktionen**, **Funktionen**, **Überweisungsbescheid senden** aus, um einen Überweisungsbescheid per E-Mail zu senden, nachdem die Kreditorenzahlungen für einen von mehreren Kreditorenposten gebucht wurden.

## <a name="see-also"></a>Siehe auch

[Zahlungsvorschlag](payables-how-suggest-vendor-payments.md)  
[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
