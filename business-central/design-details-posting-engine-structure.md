---
title: Designdetails – Struktur der Buchungsmaschine
description: 'Die Buchungsschnittstelle verwendet die Funktionen der Buchungsmaschine, um Datensätze für das Hauptbuch und die MWST-Posten vorzubereiten und einzufügen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Designdetails: Buchungs-Modul-Struktur
Buchungsschnittstelle und verschiedene andere Funktionen in Codeunit 12 verwenden Buchungsmodulfunktionen, um Fibuposten und MWST.-Posten-Datensätze vorzubereiten und einzufügen. Das Buchungsmodul ist auch für Fibupostenjournalerstellung zuständig.  
  
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
  
## Siehe auch  
 [Designdetails: Buchungs-Schnittstellenstruktur](design-details-posting-interface-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]