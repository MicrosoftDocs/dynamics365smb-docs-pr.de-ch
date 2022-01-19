---
title: Nutzung von Business Central with Outlook| Microsoft Docs
description: Dieser Dienst hat eine starke Integration in Microsoft 365 und macht es möglich, dass Sie Ihre Geschäftsaktivitäten und E-Mails mit Debitoren und Kreditoren direkt in Outlook verwalten können.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: 5de1ae4dc96419d848103a8b4ea9e11113793242
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589683"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Nutzen Sie Business Central als Ihr Unternehmenspostfach in Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] bietet ein Add-In, mit dem Sie die geschäftlichen Interaktionen mit Ihren Kunden und Kreditoren direkt in Microsoft Outlook verwalten können. Mit dem [!INCLUDE[prod_short](includes/prod_short.md)]-Add-in für Outlook können Sie Finanzdaten zu Kunden und Kreditoren einsehen und Finanzbelege wie Offerten und Rechnungen erstellen und versenden.

Das Add-In [!INCLUDE[prod_short](includes/prod_short.md)] besteht aus zwei separaten Add-Ins, die die folgenden Funktionalitäten bieten:

- Contact Insights

   Mit diesem Add-In können Sie [!INCLUDE[prod_short](includes/prod_short.md)] Kunden- oder Kreditor-Informationen in Outlook-E-Mails und Kalenderterminen nachschlagen. Ausserdem können Sie damit [!INCLUDE[prod_short](includes/prod_short.md)]-Geschäftsbelege erstellen und an einen Kontakt senden, z.B. eine Verkaufsofferte oder eine Rechnung.

- Beleg-Ansicht

   Wenn ein Geschäftsdokument in einer E-Mail versendet wird, stellt das Add-In einen direkten Link von der E-Mail zu dem eigentlichen Geschäftsdokument in [!INCLUDE[prod_short](includes/prod_short.md)] her.

## <a name="get-started"></a>Erste Schritte

1. Als Erstes müssen Sie das [!INCLUDE[prod_short](includes/prod_short.md)]-Add-In in Outlook installieren. Möglicherweise hat Ihr Administrator das Add-in bereits für Sie installiert. Wenn Sie sich also nicht sicher sind, fragen Sie Ihren Administrator oder lesen Sie den nächsten Schritt, um zu überprüfen, ob es installiert ist.

    Wenn das Add-In nicht für Sie installiert wurde, lesen Sie [Installieren Sie das Add-In für Ihren eigenen Gebrauch](admin-outlook.md#install). 

2. Wenn das Add-In installiert ist, können Sie auf das **[!INCLUDE[prod_short](includes/prod_short.md)]** Add-In von jeder neuen oder bestehenden E-Mail Nachricht oder jedem Kalendertermin in Outlook aus zugreifen.

    Beginnen Sie damit, sich bei Outlook anzumelden und eine E-Mail-Nachricht zu öffnen. Wenn Sie dann die Outlook App verwenden, gehen Sie zum Menüband und suchen Sie nach **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Oder wenn Sie Outlook im Web verwenden, suchen Sie oben oder unten in der Nachricht nach dem Symbol ![Business Central-Add-in in Outlook.](media/outlook-business-central-icon.png) oder gehen Sie zu den weiteren Aktionen ![Weitere Aktionen für eine E-Mail in Outlook anzeigen.](media/outlook-more-actions-button.png) Schaltfläche enthält.

    ![Zugriff auf Business Central-Add-Ins in Outlook.](media/outlook-business-central-addin.png)

   Wenn Sie das Add-In selbst installiert haben und sich für eine Beispiel-E-Mail entschieden haben, suchen Sie in Ihrem Posteingang nach der Willkommens-E-Mail. Diese E-Mail enthält Informationen, die Ihnen die ersten Schritte erleichtern.

Wenn Sie das Add-In zum ersten Mal verwenden, werden Sie im Add-In-Fenster [!INCLUDE[prod_short](includes/prod_short.md)] möglicherweise aufgefordert, sich anzumelden. Wählen Sie in diesem Fall **Jetzt anmelden** und folgen Sie den Anweisungen auf dem Bildschirm, um sich bei Business Central mit Ihrem Konto anzumelden.

> [!TIP]
> Wenn Sie das neue Outlook im Web verwenden, können Sie **[!INCLUDE[prod_short](includes/prod_short.md)]** anheften, sodass es immer sofort sichtbar ist, anstatt zur Schaltfläche „Weitere Aktionen“ gehen zu müssen. So können Sie bequem die Contact Insights einsehen, während Sie durch verschiedene E-Mails blättern.

Weitere Informationen finden Sie unter [Verwenden von Add-Ins in Outlook im Web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in"></a>Arbeiten Sie mit Kontakten und Belegen mit dem Contact Insights-Add-in

Angenommen  Sie erhalten eine E-Mail von einem Debitor, der für einige Artikel ein Offerte möchte. Sie können direkt in Outlook das [!INCLUDE[prod_short](includes/prod_short.md)]-Add-In öffnen, das den Sender als Debitoren identifiziert und die Debitorenkarte für dieses Unternehmen öffnet. Auf diesem Dashboard sehen Sie die Übersichtsinformationen für den Kunden und können Detailinformationen zu bestimmten Belegen anzeigen. Sie können sich auch die Verkaufshistorie für den Debitor anzeigen lassen. Wenn es ein neuer Kontakt ist, können Sie ihn als neuen Debitor in Outlook erstellen in [!INCLUDE[prod_short](includes/prod_short.md)] ohne Outlook zu verlassen.  

Im Add-In können Sie eine Verkaufsofferte erstellen und sie diesem Kunden zusenden, ohne Outlook zu verlassen. Alle Informationen, die Sie zum Versenden der Verkaufsofferte benötigen, sind in Ihrem Geschäftseingang in Outlook verfügbar. Sobald Sie die Daten eingegeben haben, posten Sie die Offerte und versenden sie per E-Mail. [!INCLUDE[prod_short](includes/prod_short.md)] erstellt eine .PDF-Datei mit dem Verkaufsangebot und fügt sie der E-Mail-Nachricht hinzu, deren Entwurf Sie im Add-In erstellt haben.  

Möchten Sie eine E-Mail von einem Kreditor erhalten, können Sie das Add-In verwenden, um mit Kreditoren und Einkaufsrechnungen zu arbeiten.  

Manchmal möchten Sie mehr Felder sehen, als im Add-In angezeigt werden, z.B.wenn Sie Zeilen in einer Rechnung ausfüllen möchten. Um Ihnen mehr Platz zum Arbeiten zu geben, können Sie das Add-In in einer separaten Seite aufklappen. Es ist immer noch ein Teil von Outlook, aber Sie haben mehr Platz. Wenn Sie Daten für den Beleg in der Popup-Ansicht eingeben, werden die Änderungen automatisch gespeichert. Die folgenden Abschnitte führen Sie durch einige grundlegende Aufgaben, um Ihnen ein allgemeines Verständnis für die Verwendung zu vermitteln.

> [!TIP]
> Die Aufgaben erläutern, wie Sie das Add-In aus einer E-Mail-Nachricht heraus verwenden können. Aber Sie können dasselbe auch von einem Kalendertermin in Outlook aus tun.

### <a name="look-up-a-business-contact-when-composing-an-email"></a>Nachschlagen eines Geschäftskontakts beim Verfassen einer E-Mail

1. Erstellen Sie eine neue E-Mail-Nachricht.
2. Gehen Sie im Menüband auf **[!INCLUDE[prod_short](includes/prod_short.md)]** und wählen Sie **Contact Insights**. Oder wenn Sie Outlook im Web verwenden, gehen Sie zum Ende der Nachricht und wählen Sie ![Business Central-Add-in Symbol in Outlook.](media/outlook-business-central-icon.png) > **Contact Insights**.
3. In dem sich öffnenden **[!INCLUDE[prod_short](includes/prod_short.md)]** Add-In-Fenster suchen Sie den gewünschten Kontakt und wählen ihn aus.

    Eine Übersicht des Kontakts wird in dem Fenster angezeigt und der Kontakt wird in der **An** Zeile der E-Mail hinzugefügt.

### <a name="view-and-change-the-contact-details-or-switch-company"></a>Anzeigen und Ändern der Kontaktdetails oder Wechseln der Firma

Die Aktionsleiste am oberen Rand des Add-In-Fensters [!INCLUDE[prod_short](includes/prod_short.md)] enthält mehrere Aktionen, mit denen Sie die Details des Kontakts einsehen und ändern können.

![Business Central-Add-in-Aktionsleiste in Outlook.](media/outlook-addin-action-bar.png)

So können Sie beispielsweise die vollständigen Kontaktdetails öffnen, wie Sie sie in [!INCLUDE[prod_short](includes/prod_short.md)] sehen würden. Wenn Sie mit mehr als einer [!INCLUDE[prod_short](includes/prod_short.md)]-Firma arbeiten, können Sie ganz einfach zwischen den Firmen wechseln.

### <a name="track-incoming-documents"></a>Eingehende Belege verfolgen 

Vielleicht verwenden Sie die Liste **Eingehende Belege** in [!INCLUDE[prod_short](includes/prod_short.md)], um Belege zur Verarbeitung zu verfolgen, die Ihnen von Einkäufern zugeschickt werden, z.B. eine Einkaufsrechnung, die bezahlt werden muss. In diesem Fall können Sie Datensätze für Eingehende Belege ganz einfach über das Outlook-Add-In erstellen und die E-Mail-Anhänge hinzufügen.

1. Wenn Sie eine E-Mail von einem Kreditor erhalten, die einen Anhang enthält, wählen Sie das Symbol ![Business Central-Add-in für Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Contact Insights**. 

2. Wählen Sie in der Aktionsleiste des Add-Ins die Option **Weitere Aktionen anzeigen** und dann die Option **Senden an Eingehende Belege...**. 

### <a name="create-and-send-new-document-to-a-contact"></a>Neues Dokument erstellen und an einen Kontakt senden

1. Wählen Sie im Menüband oder am unteren Rand der Nachricht ![Business Central-Add-in Symbol in Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Neu**, und wählen Sie dann die Art des Belegs, den Sie erstellen möchten, z. B. **Verkaufsofferte**.
2. Nehmen Sie die Änderungen an dem Beleg im Bereich **[!INCLUDE[prod_short](includes/prod_short.md)]** Add-In vor.
3. Wenn der Beleg zum Versenden an den Kontakt bereit ist, wählen Sie in der Aktionsleiste **Weitere Aktionen anzeigen** und dann die Aktion **Senden per E-Mail**.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in"></a>Anzeigen eines Belegs aus einer E-Mail mit dem Add-In Dokumentenansicht

Unabhängig davon, ob es sich um eine gesendete oder empfangene E-Mail handelt, können Sie jeden [!INCLUDE[prod_short](includes/prod_short.md)]-Beleg, wie z.B. eine Verkaufsofferte, direkt in Outlook anzeigen. Von dort aus können Sie Änderungen vornehmen und zu verwandten Informationen navigieren &mdash;, genauso wie Sie es von [!INCLUDE[prod_short](includes/prod_short.md)] aus tun würden.

Wenn Sie die Outlook App verwenden, wählen Sie einfach **Dokumentenlink** am Anfang der Nachricht. Wenn Sie Outlook im Internet verwenden, suchen Sie in der Nachricht nach dem Link zu einem Beleg. Der Text des Referenzlinks enthält die Belegnummer, die auf der in [!INCLUDE[prod_short](includes/prod_short.md)] verwendeten Zahlenreihe basiert. Der Link für eine Verkaufsofferte würde zum Beispiel so aussehen: **Sales Quote S-QUO1000**.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Weitere Informationen

[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Abrufen von Business Central auf meinem mobilen Gerät](install-mobile-app.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Finanzen](finance.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Mindestanforderungen für Outlook](product-requirements.md#outlook)  
[Verwenden von Add-Ins für Outlook online](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]