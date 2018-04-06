---
title: 'Gewusst wie: Importieren von Schweizer Postleitzahlen'
description: "Sie können die aktuelle PLZ importieren und damit die Tabelle **PLZ** aktualisieren. Die PLZ-Datei kann von der Website der Schweizer Post heruntergeladen werden. Nach dem Import der letzten PLZ können PLZ für Debitoren oder Kreditoren definiert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e053a7a32e091b34fbc0e2f06cea9ce4c79f19d4
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="import-swiss-post-codes"></a>Importieren von Postleitzahlen (Schweiz)
Sie können die aktuelle PLZ importieren und damit die Tabelle **PLZ** aktualisieren. Die PLZ-Datei kann von der Website der [Schweizer Post](http://go.microsoft.com/fwlink/?LinkId=150292) heruntergeladen werden. Nach dem Import der letzten PLZ können PLZ für Debitoren oder Kreditoren definiert werden. Weitere Informationen finden Sie unter [Neue Kunden registrieren](../../purchasing-how-register-new-vendors.md).  

## <a name="to-import-post-codes"></a>So importieren Sie PLZ  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Postleitzahlen-Codes** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion**PLZ importieren** aus.  
3.  Geben Sie im Fenster **Postleitzahlen Import** im Feld **Dateiname** den Namen der PLZ-Datei ein, die Sie in die Tabelle **PLZ** importieren möchten.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

    Die aktuellen PLZ-Informationen werden importiert.  

Nachfolgend wird beschrieben, wie PLZ für Debitoren definiert werden, doch bei der Definition von PLZ für Kreditoren wird die gleiche Gewusst wie verwendet.  

## <a name="to-define-post-codes-for-customers"></a>So definieren Sie PLZ für Debitoren  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kunden** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Debitor, für den Sie eine PLZ definieren möchten, und wählen die **Bearbeiten** Aktion aus.  
3.  Im Fenster **Debitorenkarte** im Inforegister **Allgemein**, im Feld **PLZ**, wählen Sie die PLZ für die Adresse des Debitors aus.  

    > [!NOTE]  
    >  Bei Auswahl der PLZ werden die Felder **Ort** und **Länder-/Regionscode** automatisch mit den Informationen aus der Tabelle **PLZ** ausgefüllt. Weitere Informationen finden Sie unter [Neue Kunden registrieren](../../sales-how-register-new-customers.md).  

4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch   
 [Einkaufsbelege und Verkaufsbelege (Schweiz)](swiss-purchase-documents-and-sales-documents.md)   
 [Drucken einer Lagerkommissionierliste von einem Auftrag](how-to-print-an-inventory-picking-list-from-a-sales-order.md)   
 [So drucken Sie im Verlauf von Stapelbuchungen Verkaufsaufträge und Bestellungen](how-to-print-sales-and-purchase-orders-during-batch-posting.md)   
 [Registriert einen neuen Kreditor](../../purchasing-how-register-new-vendors.md)  

