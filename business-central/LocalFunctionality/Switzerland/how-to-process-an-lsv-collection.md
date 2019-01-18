---
title: 'Gewusst wie: Verarbeiten eines LSV-Einzugs'
description: "Mithilfe von **LSV-Journalen** können Zahlungen von LSV+-Debitoren (Lastschriftverfahren) erstellt und verarbeitet werden. Sie können diese Zahlungen im Zahlungseingangs-Erfassungsjournal erfassen, eine LSV-Datei erstellen und dann den Einzugsauftrag drucken."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: f447e0c20081cf64709e14cbe524d80fd8075b1c
ms.contentlocale: de-ch
ms.lasthandoff: 11/26/2018

---
# <a name="process-an-lsv-collection"></a>Verarbeiten eines LSV-Einzugs
Mithilfe von **LSV-Journalen** können Zahlungen von LSV+-Debitoren (Lastschriftverfahren) erstellt und verarbeitet werden. Sie können diese Zahlungen im Zahlungseingangs-Erfassungsjournal erfassen, eine LSV-Datei erstellen und dann den Einzugsauftrag drucken. Weitere Informationen finden Sie unter Zahlungseingangs Erf.-Journal (Seite) und [Exportieren von Zahlungen mit LSV](how-to-export-payments-using-lsv.md).  

Wenn Sie den Stapelverarbeitungsauftrag **LSV Einzugsvorschlag** ausführen, wird jeder vorgeschlagene Einzug in einer LSV-Journalzeile erfasst, und die offenen Rechnungen werden in die LSV-Journale übertragen. Weitere Informationen finden Sie unter LSV-Erf.-Journal – Tabelle.  

Sie können die vorgeschlagenen Zahlungszeilen anzeigen, bearbeiten oder löschen. Falls Sie den vorgeschlagenen Betrag korrigieren, wird die Differenz als Rabatt markiert. Der Stapelverarbeitungsauftrag kann mehrmals für unterschiedliche Debitorengruppen ausgeführt werden. Die Vorschlagszeilen können in dasselbe Erfassungsjournal eingefügt werden.  

## <a name="to-create-an-lsv-collection"></a>So erstellen Sie einen LSV-Einzug  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite ober Bericht suchen") und geben **LSV Erf.-Journal Liste** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Füllen Sie auf der Seite **LSV-Journal Liste** die erforderlichen Felder wie in der folgenden Tabelle beschrieben aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**LSV Bankcode**|Wählen Sie den LSV Bankcode für die Bank, die die Konsolidierung durchführt.|  
    |**LSV Journalbeschreibung**|Geben Sie eine Beschreibung für den Eintrag ein.|

4.  Wählen Sie den erforderlichen LSV-Journaleintrag, und wählen die Aktion **LSV Sammlung vorschlagen** aus, um die Zahlungen automatisch von LSV zu erfassen.  
5.  Füllen Sie auf der Seite **LSV Einzugsvorschlag** die Felder auf dem Inforegister **Optionen** wie in der folgenden Tabelle beschrieben aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nr.**|Geben Sie die LSV Erf.-Journalzeilen ein.|  
    |**Von Fälligkeitsdatum**|Geben Sie das Start- Fälligkeitsdatum von offenen Posten an, die für die Sammlung vorgeschlagen werden sollen.|  
    |**Bis Fälligkeitsdatum**|Geben Sie das End- Fälligkeitsdatum von offenen Posten an, die für die Sammlung vorgeschlagen werden sollen.|  
    |**Einzugsdatum**|Geben Sie das Datum an, an dem die Sammlung schliesst. Der LSV+-Einzugsauftrag muss mindestens drei Banktage vor dem Einzugsdatum gesendet werden.|  

6.  Wählen Sie die Schaltfläche **OK** aus.  

Alle zugehörigen Zeilen werden in das LSV-Journal übertragen. Nach der Verarbeitung des LSV-Einzugs können Sie die vorgeschlagenen Zahlungen auf der Seite **LSV Journal** anzeigen, überprüfen oder bearbeiten. Weitere Informationen finden Sie unter LSV-Erf.-Journal-Zeilen – Tabelle.  

## <a name="to-manage-suggested-payments"></a>So verwalten Sie vorgeschlagene Zahlungen  

1.  Auf der Seite **LSV-Erf.-Journal-Liste** wählen Sie den erforderlichen Journaleintrag, und wählen die **LSV-Erf.-Journalzeile** Aktion aus.  

    Sie können die vorgeschlagenen Zahlungen auf dieser Seite anzeigen und ändern. Dieser Wert kann bei Bedarf manuell eingegeben oder geändert werden. Für neue Erfassungsjournalzeilen wird das Feld **LSV-Status** auf **Öffnen** festgelegt, um anzugeben, dass die Rechnung unbezahlt ist.  

3.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
 [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md)   
 [Schliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md)   
 [Buchen von LSV+ Zahlungen](how-to-post-lsv-payments.md)   
 [Exportieren von Zahlungen mit LSV](how-to-export-payments-using-lsv.md)

