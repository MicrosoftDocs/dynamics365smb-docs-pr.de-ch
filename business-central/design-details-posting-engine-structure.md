---
title: Design Details - Buchungsmodulstruktur | Microsoft Docs
description: Buchungsschnittstelle und verschiedene andere Funktionen in Codeunit 12 verwenden Buchungsmodulfunktionen, um Fibuposten und MWST.-Posten-Datensätze vorzubereiten und einzufügen. Das Buchungsmodul ist auch für Sachpostenjournalerstellung zuständig.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b4bc639675591bb91ad2fa4e56f4e3ed88fed975
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303090"
---
# <a name="design-details-posting-engine-structure"></a>Designdetails: Buchungs-Modul-Struktur
Buchungsschnittstelle und verschiedene andere Funktionen in Codeunit 12 verwenden Buchungsmodulfunktionen, um Fibuposten und MWST.-Posten-Datensätze vorzubereiten und einzufügen. Das Buchungsmodul ist auch für Sachpostenjournalerstellung zuständig.  
  
 Die Funktionalität in der folgenden Tabelle stellen ein Standardframework für das Entwerfen von Buchungsverfahren (wie Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry und Reverse) und exklusivem Zugriff auf Tabelle 17, Fibuposten bereit.  
  
|Routine|Description|  
|-------------|---------------------------------------|  
|StartPosting|Initialisiert Buchungspuffer TempGLEntryBuf, sperrt Fibuposten- und MWST.-Posten-Tabellen und initialisiert Buchhaltungsperiode, Fibupostenjournal und Wechselkurs. Sollte nur einmal aufgerufen werden, dann ist NextEntryNo 0.|  
|ContinuePosting|Prüft und bucht nicht vereinnahmte MWST. für vorheriges Transaktioninkrement NextTransactionNo und bereitet das Buchen der nächsten Zeile vor.|  
|FinishPosting|Vervollständigt die Buchung durch das Einfügen von Fibuposten vom temporären Puffer in Datenbanktabelle. Immer zusammen mit StartPosting verwendet. Prüft auf Inkonsistenzen.|  
|InitGLEntry|Wird verwendet, um die neuen Fibuposten für Gen initialisieren. Buch.-Blattzeile. Gibt GLEntry als Parameter zurück.|  
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