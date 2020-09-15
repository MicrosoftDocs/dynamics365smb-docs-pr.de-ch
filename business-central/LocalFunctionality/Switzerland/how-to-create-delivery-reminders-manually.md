---
title: Manuelles Erstellen von Lieferbenachrichtigungen
description: In Business Central können Sie Lieferbenachrichtigungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde. Sie können eine einzelne Lieferbenachrichtigung manuell erstellen oder Sie können Lieferbenachrichtigungen für alle überfälligen Lieferungen erstellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: af5cb6be90b5819ee61537713257153e112ff859
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779851"
---
# <a name="create-delivery-reminders-manually"></a>So erstellen Sie Lieferanmahnungen manuell
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], können Sie Lieferbenachrichtigungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde. Sie können eine einzelne Lieferbenachrichtigung manuell erstellen oder Sie können Lieferbenachrichtigungen für alle überfälligen Lieferungen erstellen. Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-generate-delivery-reminders.md).

> [!NOTE]
> Um Lieferbenachrichtigungen zu erstellen, müssen Sie Eigenschaften für Lieferbenachrichtigungen einrichten. Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-set-up-delivery-reminders.md).

## <a name="to-create-a-delivery-reminder-manually"></a>So erstellen Sie eine Lieferbenachrichtigung manuell  

1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](../../media/ui-search/search_small.png "Tell me-Funktion") Symbol öffnet, geben Sie **Lieferanmahnung** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Füllen Sie auf der Seite **Lieferbenachrichtigung** im Inforegister **Allgemein** die erforderlichen Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nr.**|Die eindeutige Kennnummer für die Lieferbenachrichtigung.|  
    |**Kreditorennr**|Die Nummer des Kreditors, für den Sie die Lieferbenachrichtigung buchen möchten.<br /><br /> Wenn Sie die Kreditorennummer auswählen, werden die Felder **Name**, **Adresse**, **PLZ-Code/Ort** und **Kontakt** automatisch ausgefüllt.|  
    |**Buchungsdatum**|Das Buchungsdatum für die Lieferbenachrichtigung. Dieses Datum wird in alle Lieferbenachrichtigungsposten kopiert.|  
    |**Belegdatum**|Das Belegdatum für die Lieferbenachrichtigung. Dieses Datum wird auch verwendet, um das Fälligkeitsdatum der Lieferbenachrichtigung zu berechnen. Sie können das Buchungsdatum bei Bedarf ändern.|  
    |**Mahnstufe**|Die Lieferbenachrichtigungsstufe. Dieser Wert basiert auf der Anzahl der Lieferbenachrichtigungen, die bereits gesendet wurden. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminder-terms-levels-and-text.md).|  
    |**Mahnmethodencode**|Geben Sie den Lieferbenachrichtigungsmethodencode an, der für den Kreditor eingerichtet ist.|  
    |**Fälligkeitsdatum**|Das Fälligkeitsdatum für die Lieferbenachrichtigung.|  

4.  Wählen Sie die Aktion **Mahnungszeile vorschlagen**  

    Bei überfälligen Lieferungen vom angegebenen Kreditor werden diese der Lieferbenachrichtigung hinzugefügt.  

5.  Wählen Sie die Schaltfläche **OK** aus.  

    Die Lieferbenachrichtigung wird erstellt. Jetzt können Sie die Lieferbenachrichtigungen ausstellen und drucken.  

## <a name="see-also"></a>Siehe auch  
 [Lieferanmahnungen](delivery-reminders.md)   
 [So erstellen Sie Lieferanmahnungen](how-to-generate-delivery-reminders.md)   
 [Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md)   
 [Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md)   
 [So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [Lieferbenachrichtigung registrieren](how-to-issue-delivery-reminders.md)   
 [So drucken Sie Testberichte vor dem Registrieren von Lieferanmahnungen](how-to-print-test-reports-for-delivery-reminders.md)
