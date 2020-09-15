---
title: So erstellen Sie Lieferanmahnungen in der Schweizer Version aus
description: Nachdem Sie Lieferbenachrichtigungen erstellt haben, müssen Sie sie registrieren und ausdrucken, sodass Sie Mahnungen an Kreditoren verschicken können. Vor dem Ausstellen von Lieferbenachrichtigungen können Sie einen Testbericht drucken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2020
ms.author: edupont
ms.openlocfilehash: f71107b8b7ca5b259baf17276ab66b0583521a19
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778230"
---
# <a name="issue-delivery-reminders-in-the-swiss-version"></a>Lieferanmahnungen in der Schweizer Version ausstellen

Nachdem Sie Lieferbenachrichtigungen erstellt haben, müssen Sie sie registrieren und ausdrucken, sodass Sie Mahnungen an Kreditoren verschicken können. Vor dem Ausstellen von Lieferbenachrichtigungen können Sie einen Testbericht drucken. Weitere Informationen finden Sie unter [Vorgehensweise: Drucken von Testberichten für  Lieferbenachrichtigungen](how-to-print-test-reports-for-delivery-reminders.md).  

Beim Registrieren der Lieferantenbenachrichtigungen erzeugt die Anwendung Lieferantenbenachrichtigungsposten. Sie können die generierten Posten auf der Seite **Lieferanmahnungsposten** ansehen.  

## <a name="to-issue-delivery-reminders"></a>So registrieren Sie Lieferbenachrichtigungen  

1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](../../media/ui-search/search_small.png "Tell me-Funktion") Symbol öffnet, geben Sie **Lieferanmahnung** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie auf der Seite **Lieferanmahnung** die Lieferanmahnung, die Sie registrieren möchten, und wählen Sie dann die Aktion **Bearbeiten**.  
3.  Wählen Sie die Aktion **Ausgeben** aus.  
4.  Füllen Sie auf der Seite **Lieferanmahnung registrieren** auf dem Inforegister **Optionen** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**D&rucken**|Wählen Sie diese Option aus, um die Lieferbenachrichtigungen zu drucken, wenn sie registriert werden.|  
    |**Buchungsdatum ersetzen**|Wählen Sie diese Option aus, um das vorhandene Buchungsdatum für die Lieferbenachrichtigungen zu ersetzen.|  
    |**Buchungsdatum**|Das Buchungsdatum für die Lieferbenachrichtigung.<br /><br /> Dieses Buchungsdatum wird für alle Lieferbenachrichtigungen verwendet, wenn Sie das Kontrollkästchen **Buchungsdatum ersetzen** aktiviert haben. Wenn das Kontrollkästchen **Buchungsdatum ersetzen** deaktiviert ist, wird dieses Datum nur für diejenigen Lieferbenachrichtigungen verwendet, für die kein Buchungsdatum verfügbar ist.|  

5.  Optional wählen Sie im Inforegister **Lieferbenachrichtigungen Kopfzeile** die entsprechenden Filter aus.  

    > [!NOTE]  
    >  Sie können Filter entfernen und allen Lieferbenachrichtigungen gleichzeitig registrieren.  

6.  Wählen Sie die Schaltfläche **OK** aus.  

Sie können die registrierten Lieferanmahnungen auf der Seite **Reg. Lieferanmahnung** betrachten. Optional können Sie jetzt eine Lieferbenachrichtigung drucken.  

## <a name="to-view-delivery-reminder-ledger-entries"></a>Um sich detaillierte Lieferbenachrichtigungen anzeigen zu lassen  

1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature öffnet](../../media/ui-search/search_small.png "Tell me-Funktion") Symbol, geben Sie **Bestellungen** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Bestellung, für die Sie den Mahnungsstatus anzeigen möchten, und wählen die Aktion **Bearbeiten**.  
3.  Wählen Sie die Aktion **Lieferbenachrichtigungs-Einträge** aus.  

Auf der Seite „Lieferanmahnungsposten” können Sie die Lieferanmahnungsposten für die ausgewählte Bestellung betrachten.  

## <a name="see-also"></a>Siehe auch  
 [Lieferanmahnungen](delivery-reminders.md)   
 [So erstellen Sie Lieferanmahnungen](how-to-generate-delivery-reminders.md)   
 [So erstellen Sie Lieferanmahnungen manuell](how-to-create-delivery-reminders-manually.md)
