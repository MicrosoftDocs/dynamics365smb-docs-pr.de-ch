---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 70d4e0ac0729f8d259f87c65915dfafd8749abbd
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435186"
---
Nachdem Sie Lieferbenachrichtigungen erstellt haben, müssen Sie sie registrieren und ausdrucken, sodass Sie Mahnungen an Kreditoren verschicken können. Vor der Registrierung der Lieferanmahnungen können Sie einen Testbericht drucken.  

Beim Registrieren der Lieferantenbenachrichtigungen erzeugt die Anwendung Lieferantenbenachrichtigungsposten. Sie können die generierten Posten auf der Seite **Lieferanmahnungsposten** ansehen.  

## <a name="to-issue-delivery-reminders"></a>So registrieren Sie Lieferbenachrichtigungen  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../../media/ui-search/search_small.png "Tell me-Funktion") Geben Sie **Lieferanmahnung** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie auf der Seite **Lieferanmahnung** die Lieferanmahnung, die Sie registrieren möchten, und wählen Sie dann die Aktion **Bearbeiten**.  
3. Wählen Sie die Aktion **Ausgeben** aus.  
4. Füllen Sie auf der Seite **Lieferanmahnung registrieren** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**D&rucken**|Wählen Sie diese Option aus, um die Lieferbenachrichtigungen zu drucken, wenn sie registriert werden.|  
    |**Buchungsdatum ersetzen**|Wählen Sie diese Option aus, um das vorhandene Buchungsdatum für die Lieferbenachrichtigungen zu ersetzen.|  
    |**Buchungsdatum**|Das Buchungsdatum für die Lieferbenachrichtigung.<br /><br /> Dieses Buchungsdatum wird für alle Lieferbenachrichtigungen verwendet, wenn Sie das Kontrollkästchen **Buchungsdatum ersetzen** aktiviert haben. Wenn das Kontrollkästchen **Buchungsdatum ersetzen** deaktiviert ist, wird dieses Datum nur für diejenigen Lieferbenachrichtigungen verwendet, für die kein Buchungsdatum verfügbar ist.|  

5. Optional wählen Sie im Inforegister **Lieferbenachrichtigungen Kopfzeile** die entsprechenden Filter aus.  

    > [!NOTE]  
    >  Sie können Filter entfernen und allen Lieferbenachrichtigungen gleichzeitig registrieren.  

6. Wählen Sie die Schaltfläche **OK** aus.  

Sie können die registrierten Lieferanmahnungen auf der Seite **Reg. Lieferanmahnung** betrachten. Optional können Sie jetzt eine Lieferbenachrichtigung drucken.  

## <a name="to-view-delivery-reminder-ledger-entries"></a>Um sich detaillierte Lieferbenachrichtigungen anzeigen zu lassen  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../../media/ui-search/search_small.png "Tell me-Funktion") Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Bestellung, für die Sie den Mahnungsstatus anzeigen möchten, und wählen die Aktion **Bearbeiten**.  
3. Wählen Sie die Aktion **Lieferbenachrichtigungs-Einträge** aus.  

Auf der Seite **Lieferanmahnungsposten** können Sie die Lieferanmahnungsposten für die ausgewählte Bestellung betrachten.  
