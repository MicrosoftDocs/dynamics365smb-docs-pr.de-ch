---
title: Design Details - Buchungsmodulstruktur | Microsoft Docs
description: "Buchungsschnittstelle und verschiedene andere Funktionen in Codeunit 12 verwenden Buchungsmodulfunktionen, um Fibuposten und MWST.-Posten-Datensätze vorzubereiten und einzufügen. Das Buchungsmodul ist auch für Sachpostenjournalerstellung zuständig."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e37bd2be3d0a30c3274e27d7ccbce7a3e14c30b1
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-posting-engine-structure"></a>Designdetails: Buchungs-Modul-Struktur
Buchungsschnittstelle und verschiedene andere Funktionen in Codeunit 12 verwenden Buchungsmodulfunktionen, um Fibuposten und MWST.-Posten-Datensätze vorzubereiten und einzufügen. Das Buchungsmodul ist auch für Sachpostenjournalerstellung zuständig.  
  
 Die Funktionalität in der folgenden Tabelle stellen ein Standardframework für das Entwerfen von Buchungsverfahren (wie Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry und Reverse) und exklusivem Zugriff auf Tabelle 17, Fibuposten bereit.  
  
|Routine|Description|  
|-------------|---------------------------------------|  
|StartPosting|Initialisiert Buchungspuffer TempGLEntryBuf, sperrt Fibuposten- und MWST.-Posten-Tabellen und initialisiert Buchhaltungsperiode, Fibupostenjournal und Wechselkurs. Sollte nur einmal aufgerufen werden, dann ist NextEntryNo 0.|  
|ContinuePosting|Prüft und bucht nicht vereinnahmte MWST. für vorheriges Transaktioninkrement NextTransactionNo und bereitet das Buchen der nächsten Zeile vor.|  
|FinishPosting|Vervollständigt die Buchung durch das Einfügen von Fibuposten vom temporären Puffer in Datenbanktabelle. Immer zusammen mit StartPosting verwendet. Prüft auf Inkonsistenzen.|  
|InitGLEntry|Wird verwendet, um die neuen Fibuposten für Fibu Erf.-Journalzeile zu initialisieren. Gibt GLEntry als Parameter zurück.|  
|InitGLEntryVAT|Dasselbe wie InitGLEntry, weist jedoch auch Gegenkontonr. und SummarizeVAT zu.|  
|InitGLEntryVATCopy|Entsprechend InitGLEntryVAT, aber kopiert auch Buchungsgruppendaten aus dem MWST.-Posten vor SummarizeVAT.|  
|InsertGLEntry|Die einzige Funktion, die Fibuposten in globale TempGLEntryBuf-Tabelle eingefügt. Verwenden Sie immer diese Funktion für Einfügung.|  
|CreateGLEntry|Führt ein InitGLEntry aus, weist zusätzlichen Währungs-Betrag zu und führt dann InsertGLEntry aus. Ersetzt mehrere Codezeilen mit einem einzigen Funktionsaufruf.|  
|CreateGLEntryBalAcc|Dasselbe wie CreateGLEntry, weist jedoch auch Gegenkontoart und Gegenkontonr. zu.|  
|CreateGLEntryVAT|Das gleiche wie CreateGLEntry, aber mit zusätzlicher Verarbeitung für Buchungsgruppen und Speicherung im temporären MWST.-Puffer:<br /><br /> `GLEntry.CopyPostingGroupsFromDtldCVBuf(DtldCVLedgEntryBuf,GenJnlLine."Gen. Posting Type");`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryVATCollectAdj|Das gleiche wie CreateGLEntry, aber mit zusätzlicher Sammlung von Anpassungen und Speicherung im temporären MWST.-Puffer:<br /><br /> `CollectAdjustment(AdjAmount,GLEntry.Amount,GLEntry."Additional-Currency Amount",OriginalDateSet);`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryFromVATEntry|Dasselbe wie CreateGLEntry, kopiert jedoch auch Buchungsgruppen von MWST.-Posten.|  
  
## <a name="see-also"></a>Siehe auch  
 [Designdetails: Buchungs-Schnittstellenstruktur](design-details-posting-interface-structure.md)
