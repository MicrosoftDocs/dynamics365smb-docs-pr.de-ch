---
title: 'Gewusst wie: Importieren von Schweizer Postleitzahlen'
description: Sie können die aktuelle PLZ importieren und damit die Tabelle PLZ aktualisieren. Die PLZ-Datei kann von der Website der Schweizer Post heruntergeladen werden. Nach dem Import der letzten PLZ können PLZ für Debitoren oder Kreditoren definiert werden.
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
ms.openlocfilehash: 11a469d9e7557305cd6c3ed38978a8eab74664da
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301035"
---
# <a name="import-swiss-post-codes"></a>Importieren von Postleitzahlen (Schweiz)
Sie können die aktuelle PLZ importieren und damit die Tabelle **PLZ** aktualisieren. Die PLZ-Datei kann von der Website der [Schweizer Post](https://go.microsoft.com/fwlink/?LinkId=150292) heruntergeladen werden. Nach dem Import der letzten PLZ können PLZ für Debitoren oder Kreditoren definiert werden. Weitere Informationen finden Sie unter [Neue Kreditoren registrieren](../../purchasing-how-register-new-vendors.md).  

## <a name="to-import-post-codes"></a>So importieren Sie PLZ  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Postleitzahlen-Codes** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion**PLZ importieren** aus.  
3.  Geben Sie auf der Seite **Postleitzahlen Import** im Feld **Dateiname** den Namen der PLZ-Datei ein, die Sie in die Tabelle **PLZ** importieren möchten.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

    Die aktuellen PLZ-Informationen werden importiert.  

Nachfolgend wird beschrieben, wie PLZ für Debitoren definiert werden, doch bei der Definition von PLZ für Kreditoren wird die gleiche Gewusst wie verwendet.  

## <a name="to-define-post-codes-for-customers"></a>So definieren Sie PLZ für Debitoren  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Debitoren** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Debitor, für den Sie eine PLZ definieren möchten, und wählen die **Bearbeiten** Aktion aus.  
3.  Wählen Sie auf der Seite **Debitorenkarte** auf dem Inforegister **Allgemein** im Feld **PLZ** die PLZ für die Adresse des Debitors aus.  

    > [!NOTE]  
    >  Bei Auswahl der PLZ werden die Felder **Ort** und **Länder-/Regionscode** automatisch mit den Informationen aus der Tabelle **PLZ** ausgefüllt. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](../../sales-how-register-new-customers.md).  

4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch   
 [Einkaufsbelege und Verkaufsbelege (Schweiz)](swiss-purchase-documents-and-sales-documents.md)   
 [Drucken einer Lagerkommissionierliste von einem Auftrag](how-to-print-an-inventory-picking-list-from-a-sales-order.md)   
 [Registriert einen neuen Kreditor](../../purchasing-how-register-new-vendors.md)  
