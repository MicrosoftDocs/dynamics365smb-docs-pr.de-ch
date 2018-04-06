---
title: 'Vorgehensweise: Verwalten von Benachrichtigungsvorlagen | Microsoft Docs'
description: "Benachrichtigungen werden an Workflowbenutzer gesendet, um ihnen mitzuteilen, welche Schritte sie ausführen müssen, oder sie über den Status von Workflowschritten zu informieren. Sie legen fest, wer wann Benachrichtigungen erhält, indem Sie Genehmigungsbenutzer, einen Benachrichtigungsplan für Benutzer und die entsprechenden Workflowantworten einrichten, um den Benachrichtigungsempfänger zu definieren. Weitere Informationen finden Sie unter  [Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 67db510085c5a858c88565087683ffeeb4f77bd1
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="manage-notification-templates"></a>Verwalten von Benachrichtigungsvorlagen
Benachrichtigungen werden an Workflowbenutzer gesendet, um ihnen mitzuteilen, welche Schritte sie ausführen müssen, oder sie über den Status von Workflowschritten zu informieren. Sie legen fest, wer wann Benachrichtigungen erhält, indem Sie Genehmigungsbenutzer, einen Benachrichtigungsplan für Benutzer und die entsprechenden Workflowantworten einrichten, um den Benachrichtigungsempfänger zu definieren. Weitere Informationen finden Sie unter  [Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md).  

 Benachrichtigungen basieren auf Vorlagen, die den Inhalt und das Layout der Benachrichtigung definieren. Sie können den Inhalt einer Benachrichtigungsvorlage exportieren, bearbeiten und dann in dieselbe oder eine neue Benachrichtigungsvorlage importieren. Dies wird in den folgenden Verfahren beschrieben.  

 Die allgemeine Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält drei Benachrichtigungsvorlagen: eine für die Benachrichtigung über Genehmigungsanforderungen, eine für die Benachrichtigung über neue Datensätze und eine für die Benachrichtigung über fällige Genehmigungsanforderungen. Die drei vordefinierten Benachrichtigungsvorlagen unterstützen **E-Mail** und **Notizen** als Benachrichtigungsmethode. Informationen zum Anzeigen des Inhalts der drei Benachrichtigungsvorlagen finden Sie im Abschnitt „ Inhalt der Benachrichtigungsvorlagen“ in diesem Thema.

## <a name="to-create-a-new-notification-template"></a>So erstellen Sie eine neue Benachrichtigungsvorlage.  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Benachrichtigungsvorlagen** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **Benachrichtigungsvorlagen** die Aktion **Neu** aus.  
3.  Füllen Sie die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Identifizieren Sie die Benachrichtigungsvorlage.|  
    |**Description**|Beschreiben Sie die Benachrichtigungsvorlage.|  
    |**Benachrichtigungsmethode**|Geben Sie an, ob die Benachrichtigung als E-Mail oder als Hinweis gesendet wird.|  
    |**Typ**|Geben Sie den Geschäftsprozess an, für den die Benachrichtigung verwendet werden soll.<br /><br /> Wählen Sie eine der folgenden Arten aus:<br /><br /> -   **Genehmigung** gibt an, dass die Vorlage verwendet wird, um Benutzer in Genehmigungsworkflows zu benachrichtigen.<br />-   **Neuer Datensatz** gibt an, dass die Vorlage dazu verwendet wird, Genehmiger darüber zu informieren, wenn ein neuer Datensatz, wie eine Debitorenkarte, ihre Genehmigung erfordert.<br />-   **Überfällig** gibt an, dass die Vorlage verwendet wird, um Benutzer über fällige Genehmigungsanforderungen zu benachrichtigen.|  
    |**Standard**|Geben Sie an, ob die Benachrichtigungsvorlage standardmässig verwendet werden soll.|  

## <a name="to-modify-a-notification-template"></a>So ändern Sie eine Benachrichtigungsvorlage  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Benachrichtigungsvorlagen** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **Benachrichtigungsvorlagen** die Benachrichtigungsvorlage aus, die Sie bearbeiten möchten.  
3.  Wählen Sie die Aktion **Vorlageninhalt exportieren** aus.  
4.  Klicken Sie im Fenster **Datei exportieren** auf die Schaltfläche **Speichern**, wählen Sie dann einen Namen für die HTML-Datei aus, und speichern Sie die Datei am gewünschten Speicherort.  
5.  Klicken Sie mit der rechten Maustaste auf die Datei , wählen Sie **Öffnen mit** aus, und wählen Sie die relevante Anwendung aus.  

    > [!NOTE]  
    >  Der Inhalt für Benachrichtigungsvorlagen vom Typ E-Mail ist im HTML-Format. Der Inhalt für Benachrichtigungsvorlagen vom Typ Notiz ist im TXT-Format.  
6.  Bearbeiten Sie den Inhalt der Benachrichtigungsvorlage, indem Sie Parametervariablen hinzufügen, ändern oder entfernen, um den Inhalt nach Wunsch zu gestalten. Speichern Sie die Vorlage dann. Weitere Informationen finden Sie im Abschnitt „Inhalt der Benachrichtigungsvorlagen“.  

    Importieren Sie den geänderten Inhalt zurück in dieselbe oder eine neue Benachrichtigungsvorlage.  
7.  Um die exportierte Benachrichtigungsvorlage zu ändern, wählen Sie im Fenster **Benachrichtigungsvorlagen** die Vorlage aus, die Sie in Schritt 2 angegeben haben.  

    Sie können den geänderten Vorlageninhalt auch in eine neue Benachrichtigungsvorlage importieren, indem Sie das Verfahren „So erstellen Sie eine neue Benachrichtigungsvorlage“ verwenden und dann die neue Benachrichtigungsvorlage auswählen.  
8.  Wählen Sie die Aktion **Vorlageninhalt importieren** aus.  
9. Wenn Sie eine vorhandene Benachrichtigungsvorlage ändern, wählen Sie in der Meldung zum Überschreiben der vorhandenen Vorlage die Schaltfläche **Ja** aus.  
10. Wählen Sie im Fenster **Zu importierende Datei auswählen** die HTML-Datei, die Sie in Schritt 6 geändert haben, und klicken Sie dann auf die Schaltfläche **Öffnen**.  

Die vorhandene oder neue Benachrichtigungsvorlage im Fenster **Benachrichtigungsvorlagen** wurde mit dem geänderten Inhalt aktualisiert.  

### <a name="content-of-the-notification-templates"></a>Inhalt der Benachrichtigungsvorlagen  
Die drei Arten von Benachrichtigungsvorlagen (**Neuer Datensatz**, **Genehmigung** und **Überfällig**) haben unterschiedlichen Inhalt.  

Parameterwerte werden entsprechend dem Typ der Benachrichtigungsvorlage automatisch in Benachrichtigungen eingefügt.  

#### <a name="new-record"></a>Neuer Datensatz  
 ![NAV&#95;notification&#95;template&#95;new&#95;record&#95;type](media/nav_notification_template_new_record.png "NAV_notification_template_new_record")  

#### <a name="approval"></a>Genehmigung  
 ![NAV&#95;notification&#95;template&#95;approval&#95;type](media/nav_notification_template_approval_type.png "NAV_notification_template_approval_type")  

#### <a name="overdue"></a>Überfällig  
 ![NAV&#95;notification&#95;overdue&#95;type](media/nav_notification_overdue_type.png "NAV_notification_overdue_type")  

## <a name="see-also"></a>Siehe auch  
 [Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)   
 [E-Mail einrichten](madeira-how-setup-email.md)   
 [Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)   
 [Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)   
 [Erstellen eines Workflows](across-how-to-create-workflows.md)   
 [Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)   
 [Workflow](across-workflow.md)   

