---
title: "Ergebnisse der Übertragung | Microsoft Docs"
description: "Dieses Thema beschreibt, welche passiert, nachdem Sie Fibuposten in Kostenposten übertragen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bc693bf3f3339b54a5d8d8847beb06c3fc018a0f
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Kriterien für die Übertragung von Fibuposten in Kostenposten
Während der Übertragung der Fibuposten zu den Kostenposten erstellt [!INCLUDE[d365fin](includes/d365fin_md.md)] Verknüpfungen in den Posten in der Tabelle **Fibuposten**, der Tabelle **Kostenposten** und der Tabelle **Kostenjournal**, damit es möglich ist, Verbindungen zwischen Kostenposten und Fibuposten zu verfolgen.  

## <a name="general-ledger-entries"></a>Sachposten  
Für jeden Fibuposten, der zur Kostenrechnung übertragen wird, füllt [!INCLUDE[d365fin](includes/d365fin_md.md)] das Kostenfeld **Laufnr.** aus.  

## <a name="cost-entries"></a>Kostenposten  
Für jeden Kostenposten speichert [!INCLUDE[d365fin](includes/d365fin_md.md)] die Laufnummer des entsprechenden Fibupostens im Feld **Fibuposten Laufnr.** in der Tabelle **Kostenposten**.  

Für kombinierte Kostenposten speichert [!INCLUDE[d365fin](includes/d365fin_md.md)] die laufende Nummer des letzten Fibupostens, der dem Posten mit der höchsten laufenden Nummer entspricht.  

Das Feld **Fibukonto** in der Tabelle **Kostenposten** enthält die Nummer des Fibukontos, von dem der Kostenposten stammt.  

Für einzelne Kostenposten überträgt [!INCLUDE[d365fin](includes/d365fin_md.md)] den Buchungstext aus dem Fibuposten in das Textfeld **Beschreibung**. Für kombinierte Posten zeigt das Textfeld, dass diese Posten als kombinierte Posten übertragen werden. Zum Beispiel kann für einen kombinierten Posten für den Monat Oktober 2013 der Text lauten: **Kombinierte Posten, Oktober 2013**.  

## <a name="cost-register"></a>Kostenjournal  
In der Tabelle **Kostenregister** erstellt [!INCLUDE[d365fin](includes/d365fin_md.md)] einen Posten mit der Quellenübertragung aus dem Fibukonto. Der Posten erfasst die erste und letzte Postennummer der übertragenen Sachposten sowie die erste und letzte Nummer der erstellten Kostenposten.  

## <a name="see-also"></a>Siehe auch  
[So übertragen Sie Fibuposten in Kostenposten](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
[Kriterien für die Übertragung von Sachposten in Kostenposten](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
[Automatische Übertragung und kombinierte Posten](finance-automatic-transfer-combined-entries.md)   
[Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md)  

