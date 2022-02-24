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
ms.date: 05/05/2020
ms.author: edupont
ms.openlocfilehash: 236cb83e99c2385edc09622255037a152bf41e6e
ms.sourcegitcommit: 57e31a8b92feeaf8c6c63eba147f36b38eee7679
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 05/06/2020
ms.locfileid: "3339936"
---
# <a name="send-remittance-advice"></a>Rimesseavis senden

Wenn Zahlungsanzeigen verwendet werden, um Kreditoren über die Zahlungen zu benachrichtigen, die erstellt werden, können Sie Zahlungsanzeige als Massenvorgang aus dem Zahlungsausgangs-Erf.-Journal buchen und erneut senden, nachdem die Zahlungen von Kreditorenposten getätigt werden, indem Sie Belegsendeprofile verwenden.

> [!NOTE]
> Diese Funktionalität wird nur in Business Central online und lokal in folgenden Ländern unterstützt: Grossbritannien, USA, Kanada, Australien Neuseeland, und Südafrika.  

Sie können Zahlungsanzeigen auf zwei verschiedene Arten senden:

* Auf der Seite **Zahlungsausgangs-Erf.-Journal** wählen Sie **Navigieren**, **Zahlungen**, **Senden der Zahlungsanzeige**, um die Zahlungsanzeige für eine oder mehrere Erfassungsjournalzeilen zu buchen
* Wählen Sie auf der Seite **Kreditorenposten** **Aktionen**, **Funktionen**, **Überweisungsbescheid senden** aus, um einen Überweisungsbescheid per E-Mail zu senden, nachdem die Kreditorenzahlungen für einen von mehreren Kreditorenposten gebucht wurden.

## <a name="see-also"></a>Siehe auch

[Zahlungsvorschlag](payables-how-suggest-vendor-payments.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
