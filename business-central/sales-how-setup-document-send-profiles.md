---
title: Bevorzugte Methoden der Übermittlung von Verkaufsbelegen einrichten | Microsoft Docs
description: Beschreibt, wie Sie für jeden Debitor die bevorzugte Methode zum Versenden von Verkaufsbelegen, z.B. E-Mail, PDF, elektronischer Beleg usw., einrichten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1ec87cbf0885b392dc92bbd9a25fca81db38c5a1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758156"
---
# <a name="set-up-document-sending-profiles"></a>Belegsendeprofile einrichten
Sie können jeden Debitor mit einer bevorzugten Methode der Übermittlung von Verkaufsbelegen einrichten, sodass Sie nicht jedes Mal eine Sendeoptionen auswählen müssen, wenn Sie die Schaltfläche **Buchen und senden** auswählen.

Auf der Seite **Belegsendeprofile** richten Sie verschiedene **Belegsendeprofile** ein, die Sie aus dem Feld von einer Debitorenkarte auswählen können. Im Kontrollkästchen **Standard** geben Sie an, dass das Belegsendprofil das Standardprofil für alle Debitoren gilt, ausser Debitoren, bei denen das Feld **Belegsendeprofil** mit einem anderen Sendeprofil ausgefüllt ist.

Wenn Sie die Schaltfläche **Buchen und senden** für einen Verkaufsbeleg auswählen, wird im Dialogfeld **Buchungs- und Sendebestätigung** das verwendete Sendeprofil angezeigt. Dabei handelt es sich entweder um das für den Debitor eingerichtete oder um Standardprofil für alle Debitoren. In diesem Dialogfeld können Sie das Sendeprofil für den Verkaufsbeleg ändern. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## <a name="to-set-up-a-document-sending-profile"></a>Einrichten von Belegsendeprofilen
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Belegsendeprofil** ein und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Belegsendeprofile** wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Sendeprofil für eine Debitorenkarte festlegen
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte des Debitors, für den ein Sendeprofil eingerichtet werden soll.
3. Wählen Sie im Inforegister **Belegsendeprofil** ein Profil aus, das sie eingerichtet haben wie im vorigen Verfahren beschrieben.

## <a name="see-also"></a>Siehe auch
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]