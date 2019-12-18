---
title: 'Designdetails: Artikeltracking und Verfügbarkeit | Microsoft Docs'
description: Die Artikeltrackingzeilen und Artikeltracking-Zusammenfassungsseiten stellen dynamische Verfügbarkeitsinformationen für Serien- oder Chargennummern bereit. Der Zweck besteht darin, die Transparenz für Benutzer bei ausgehenden Belegen, wie etwa Verkaufsaufträgen, zu erhöhen, indem ihnen gezeigt wird, welche Seriennummern oder wie viele Einheiten einer Charge derzeit auf anderen offenen Belegen zugewiesen sind.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8e44eb5c81babccd88443b50a209cfec891e8cc7
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880222"
---
# <a name="design-details-item-tracking-availability"></a>Designdetails: Artikeltrackingverfügbarkeit
Die Seiten **Artikeltrackingzeilen** und **Artikeltracking-Zusammenfassung** stellen dynamische Verfügbarkeitsinformationen für Serien- oder Chargennummern bereit. Der Zweck besteht darin, die Transparenz für Benutzer bei ausgehenden Belegen, wie etwa Verkaufsaufträgen, zu erhöhen, indem ihnen gezeigt wird, welche Seriennummern oder wie viele Einheiten einer Charge derzeit auf anderen offenen Belegen zugewiesen sind. Dadurch wird die Ungewissheit reduziert, die durch doppelte Zuteilung entsteht und den Auftragsbearbeiter wird das Vertrauen vermittelt, dass die Artikeltrackingnummern und die Daten, die sie in nicht gebuchten Verkaufsaufträgen versprechen, erfüllt werden können. Weitere Informationen finden Sie unter [Designdetails: Artikeltrackingzeilenseite](design-details-item-tracking-lines-window.md).  

 Bei Öffnen der Seite **Artikeltrackingzeilen** werden Daten aus den Tabellen **Lagerposten** und **Reservierungsposten** abgerufen, jedoch ohne Datumsfilter. Wenn Sie das Feld **Seriennr**. oder das Feld **Chargennr**. auswählen, wird die Seite geöffnet und eine Zusammenfassung der **Artikeltrackinginformationen** in der Tabelle **Reservierungsposten** angezeigt. Die Zusammenfassung enthält die folgenden Informationen über jede Serien- oder Chargennummer auf der Artikeltrackingzeile:  

|Feld|Description|  
|---------------------------------|---------------------------------------|  
|**Gesamtmenge**|Die Gesamtmenge der aktuell im Lager vorhandenen Chargen- oder Seriennummern.|  
|**Total angeforderte Menge**|Enthält die Gesamtmenge der aktuell angeforderten Chargen- oder Seriennummer in allen Belegen.|  
|**Aktuell ausstehende Menge**|Die Menge, die in der aktuellen Instanz der Seite **Artikeltrackingzeilen** eingegeben ist, jedoch noch nicht in der Datenbank aufgezeichnet wurde.|  
|**Total verfügbare Menge**|Die Menge der Serien- oder Chargennummer, die für Nachfragen durch den Benutzer verfügbar ist.<br /><br /> Diese Menge wird aus anderen Feldern der Seite berechnet, wie folgt:<br /><br /> Gesamtmenge (erforderliche Gesamtmenge - Aktuell ausstehende Menge).|  

> [!NOTE]  
>  Sie können die Informationen in der vorangehenden Tabelle anzeigen, indem Sie die Funktion **Einträge auswählen** auf der Seite **Artikeltrackingzeile** verwenden.  

 Um die Datenbankleistung beizubehalten, werden Verfügbarkeitsdaten nur einmal aus der Datenbank abgerufen, wenn Sie die Seite **Artikeltrackingzeilen** öffnen und die **Verfügbarkeit aktualisieren**-Funktion im Fenster verwenden.  

## <a name="calculation-formula"></a>Formel  
 Wie in der vorangehenden Tabelle beschrieben, wird die Verfügbarkeit einer bestimmten Serien- oder Chargennummer wie folgt berechnet.  

 gesamte verfügbare Menge = Menge im Lagerbestand - (alle Bedarfsposten + Menge noch nicht in die Datenbank übernommen)  

> [!IMPORTANT]  
>  Diese Formel impliziert dass die Serien- oder Chargennummerenverfügbarkeitsberechnung nur den Lagerbestand berücksichtigt und voraussichtliche Wareneingänge ignoriert. Entsprechend beeinflussen Vorräte, die noch nicht gebucht sind, nicht die Artikeltrackingverfügbarkeit, im Gegensatz zur regulären Artikelverfügbarkeit, in der voraussichtliche Wareneingänge enthalten sind.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Artikeltracking](design-details-item-tracking.md)
