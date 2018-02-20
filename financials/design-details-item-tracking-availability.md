---
title: "Designdetails: Artikeltracking und Verfügbarkeit | Microsoft Docs"
description: "Die **Artikeltrackingzeilen** und **Artikeltracking-Zusammenfassung** Fenster stellen dynamische Verfügbarkeitsinformationen für Serien- oder Chargennummern bereit. Der Zweck besteht darin, die Transparenz für Benutzer bei ausgehenden Belegen, wie etwa Verkaufsaufträgen, zu erhöhen, indem ihnen gezeigt wird, welche Seriennummern oder wie viele Einheiten einer Charge derzeit auf anderen offenen Belegen zugewiesen sind. Dadurch wird die Ungewissheit reduziert, die durch doppelte Zuteilung entsteht und den Auftragsbearbeiter wird das Vertrauen vermittelt, dass die Artikeltrackingnummern und die Daten, die sie in nicht gebuchten Verkaufsaufträgen versprechen, erfüllt werden können."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bd69a3da7a0a5e766a232e8999056ac60109e7b1
ms.openlocfilehash: cdfb96475c46d56f32e5f0133efc7852a10ae446
ms.contentlocale: de-ch
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-item-tracking-availability"></a>Designdetails: Artikeltrackingverfügbarkeit
Die **Artikeltrackingzeilen** und **Artikeltracking-Zusammenfassung** Fenster stellen dynamische Verfügbarkeitsinformationen für Serien- oder Chargennummern bereit. Der Zweck besteht darin, die Transparenz für Benutzer bei ausgehenden Belegen, wie etwa Verkaufsaufträgen, zu erhöhen, indem ihnen gezeigt wird, welche Seriennummern oder wie viele Einheiten einer Charge derzeit auf anderen offenen Belegen zugewiesen sind. Dadurch wird die Ungewissheit reduziert, die durch doppelte Zuteilung entsteht und den Auftragsbearbeiter wird das Vertrauen vermittelt, dass die Artikeltrackingnummern und die Daten, die sie in nicht gebuchten Verkaufsaufträgen versprechen, erfüllt werden können. Weitere Informationen finden Sie unter [Designdetails: Artikeltrackingzeilenfenster.](design-details-item-tracking-lines-window.md)  

 Bei Öffnen des Fensters **Artikeltrackingzeilen** werden Daten aus den Tabellen **Lagerposten** und **Reservierungsposten** abgerufen, jedoch ohne Datumsfilter. Wenn Sie das Feld **Seriennr.** oder das Feld **Chargennr.** auswählen, wird das Fenster geöffnet und eine Zusammenfassung der **Artikeltrackinginformationen** in der Tabelle **Reservierungsposten** angezeigt. Die Zusammenfassung enthält die folgenden Informationen über jede Serien- oder Chargennummer auf der Artikeltrackingzeile:  

|Feld|Description|  
|---------------------------------|---------------------------------------|  
|**Gesamtmenge**|Die Gesamtmenge der aktuell im Lager vorhandenen Chargen- oder Seriennummern.|  
|**Total angeforderte Menge**|Enthält die Gesamtmenge der aktuell angeforderten Chargen- oder Seriennummer in allen Belegen.|  
|**Aktuell ausstehende Menge**|Die Menge, die in der aktuellen Instanz des Fensters **Artikelnachverfolgungszeilen** eingegeben ist, jedoch noch nicht in der Datenbank aufgezeichnet wurde.|  
|**Total verfügbare Menge**|Die Menge der Serien- oder Chargennummer, die für Nachfragen durch den Benutzer verfügbar ist.<br /><br /> Diese Menge wird aus anderen Feldern im Fenster berechnet, wie folgt:<br /><br /> Gesamtmenge (erforderliche Gesamtmenge - Aktuell ausstehende Menge).|  

> [!NOTE]  
>  Sie können die Informationen in der vorangehenden Tabelle anzeigen, indem Sie die Funktion **Einträge auswählen** im Fenster **Artikeltrackingzeile** verwenden.  

 Um die Datenbankleistung beizubehalten, werden Verfügbarkeitsdaten nur einmal aus der Datenbank abgerufen, wenn Sie das **Artikeltrackingzeilen**-Fenster öffnen und die **Verfügbarkeit aktualisieren**-Funktion im Fenster verwenden.  

## <a name="calculation-formula"></a>Formel  
 Wie in der vorangehenden Tabelle beschrieben, wird die Verfügbarkeit einer bestimmten Serien- oder Chargennummer wie folgt berechnet.  

 gesamte verfügbare Menge = Menge im Lagerbestand - (alle Bedarfsposten + Menge noch nicht in die Datenbank übernommen)  

> [!IMPORTANT]  
>  Diese Formel impliziert dass die Serien- oder Chargennummerenverfügbarkeitsberechnung nur den Lagerbestand berücksichtigt und voraussichtliche Wareneingänge ignoriert. Entsprechend beeinflussen Vorräte, die noch nicht gebucht sind, nicht die Artikeltrackingverfügbarkeit, im Gegensatz zur regulären Artikelverfügbarkeit, in der voraussichtliche Wareneingänge enthalten sind.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Artikeltracking](design-details-item-tracking.md)

