---
title: 'Gewusst wie: Importieren von Schweizer Postleitzahlen [CH]'
description: 'Sie können die aktuelle Schweizer PLZ importieren und damit die Tabelle PLZ aktualisieren, um PLZ für Debitoren oder Kreditoren zu definieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 11/14/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="import-swiss-post-codes-in-the-swiss-version"></a>Schweizer PLZ importieren in der Schweizer Version
Sie können die aktuelle PLZ importieren und damit die Tabelle **PLZ** aktualisieren. Die PLZ-Datei kann von der Website der [Schweizer Post](https://go.microsoft.com/fwlink/?LinkId=150292) heruntergeladen werden. Nach dem Import der letzten PLZ können PLZ für Debitoren oder Kreditoren definiert werden. Weitere Informationen finden Sie unter [Neue Kreditoren registrieren](../../purchasing-how-register-new-vendors.md).  

## <a name="to-import-post-codes"></a>So importieren Sie PLZ

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Tell me-Funktion") Geben Sie **PLZ** ein, und wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion**PLZ importieren** aus.  
3.  Geben Sie auf der Seite **Postleitzahlen Import** im Feld **Dateiname** den Namen der PLZ-Datei ein, die Sie in die Tabelle **PLZ** importieren möchten.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

    Die aktuellen PLZ-Informationen werden importiert.  

Nachfolgend wird beschrieben, wie PLZ für Debitoren definiert werden, doch bei der Definition von PLZ für Kreditoren wird die gleiche Gewusst wie verwendet.  

## <a name="to-define-post-codes-for-customers"></a>So definieren Sie PLZ für Debitoren

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Tell me-Funktion") Geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Debitor, für den Sie eine PLZ definieren möchten, und wählen die **Bearbeiten** Aktion aus.  
3.  Wählen Sie auf der Seite **Debitorenkarte** auf dem Inforegister **Allgemein** im Feld **PLZ** die PLZ für die Adresse des Debitors aus.  

    > [!NOTE]  
    >  Bei Auswahl der PLZ werden die Felder **Ort** und **Länder-/Regionscode** automatisch mit den Informationen aus der Tabelle **PLZ** ausgefüllt. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](../../sales-how-register-new-customers.md).  

4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch
 [Einkaufsbelege und Verkaufsbelege (Schweiz)](swiss-purchase-documents-and-sales-documents.md)   
 [Drucken einer Lagerkommissionierliste von einem Auftrag](how-to-print-an-inventory-picking-list-from-a-sales-order.md)   
 [Registriert einen neuen Kreditor](../../purchasing-how-register-new-vendors.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
