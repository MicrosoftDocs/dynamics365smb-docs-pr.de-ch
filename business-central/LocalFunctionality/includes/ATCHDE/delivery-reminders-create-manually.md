---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: df06e45136e3ab948fb6ca090c84d10609b76f45
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747544"
---
In [!INCLUDE[prod_short](../../../includes/prod_short.md)] können Sie Lieferanmahnungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde. Sie können eine einzelne Lieferanmahnung manuell erstellen oder Sie können Lieferanmahnungen für alle überfälligen Lieferungen erstellen.  

> [!NOTE]
> Um Lieferanmahnungen zu erstellen, müssen Sie die Lieferanmahnungsbestimmungen, -stufen und -texte eingerichtet haben.

## <a name="to-create-a-delivery-reminder-manually"></a>So erstellen Sie eine Lieferbenachrichtigung manuell  

1. Wählen Sie das Symbol ![Glühbirne, das die Tell me Funktion](../../../media/ui-search/search_small.png "Tell me-Funktion") öffnet, geben Sie **Lieferanmahnung** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie auf der Seite **Lieferanmahnung** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nr.**|Die eindeutige Kennnummer für die Lieferbenachrichtigung.|  
    |**Kreditorennr**|Die Nummer des Kreditors, für den Sie die Lieferbenachrichtigung buchen möchten.<br /><br /> Wenn Sie die Kreditorennummer auswählen, werden die Felder **Name**, **Adresse**, **PLZ-Code/Ort** und **Kontakt** automatisch ausgefüllt.|  
    |**Buchungsdatum**|Das Buchungsdatum für die Lieferbenachrichtigung. Dieses Datum wird in alle Lieferbenachrichtigungsposten kopiert.|  
    |**Belegdatum**|Das Belegdatum für die Lieferbenachrichtigung. Dieses Datum wird auch verwendet, um das Fälligkeitsdatum der Lieferbenachrichtigung zu berechnen. Sie können das Buchungsdatum bei Bedarf ändern.|  
    |**Mahnstufe**|Die Lieferbenachrichtigungsstufe. Dieser Wert basiert auf der Anzahl der Lieferbenachrichtigungen, die bereits gesendet wurden.|  
    |**Mahnmethodencode**|Geben Sie den Lieferbenachrichtigungsmethodencode an, der für den Kreditor eingerichtet ist.|  
    |**Fälligkeitsdatum**|Das Fälligkeitsdatum für die Lieferbenachrichtigung.|  

4. Wählen Sie die Aktion **Mahnungszeile vorschlagen**.  

    Wenn es überfällige Lieferungen vom angegebenen Kreditor gibt, werden diese der Lieferanmahnung hinzugefügt.  

5. Wählen Sie die Schaltfläche **OK** aus.  

    Die Lieferbenachrichtigung wird erstellt. Jetzt können Sie die Lieferbenachrichtigungen ausstellen und drucken.  
