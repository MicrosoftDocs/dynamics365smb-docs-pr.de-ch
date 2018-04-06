---
title: Buchen von LSV+-Zahlungen
description: "Zahlungen können nach Empfang einer LSV+ (Lastschrift Verfahren)-Zahlungsanzeige von der Bank gebucht werden."
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
ms.openlocfilehash: 26fa934e00b380b7416417f2a1d37e7bde4a5098
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="post-lsv-payments"></a>Buchen von LSV+-Zahlungen
Zahlungen können nach Empfang einer LSV+ (Lastschrift Verfahren)-Zahlungsanzeige von der Bank gebucht werden.  

## <a name="to-post-lsv-payments"></a>So buchen Sie LSV+-Zahlungen  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Barbeleg-Buchblatt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie das entsprechende Journal aus und wählen Sie dass **Journal bearbeiten** aus.  

    > [!NOTE]  
    >  Sie können den Erf.-Journalnamen für LSV auswählen, wo das betreffende Gegenkonto definiert ist. Es kann jeweils nur eine LSV-Journalzeile in ein Zahlungseingangs Erf.-Journal importiert werden. Weitere Informationen finden Sie im Fenster "Zahlungseingangs Erf.-Journal".  

3.  Wählen Sie die Aktion **von LSV-Erf.-Journal abrufen** aus.  
4.  Wählen Sie im Fenster **LSV-Journal Liste** die LSV-Journalzeile aus, die Sie in das Zahlungseingangs Erf.-Journal importieren möchten.  

    > [!NOTE]  
    >  Es können nur Erf.-Journalzeilen importiert werden, in denen das Feld **LSV-Status** auf **Datei erstellt** festgelegt ist.  

5.  Wählen Sie die Schaltfläche **OK** aus.  

    Die LSV-Journalzeile wird in das Zahlungseingangs Erf.-Journal importiert. Der Wert im Feld **LSV-Status** im Fenster **LSV-Journal Liste** ändert sich von **Datei erstellt** in **Beendet**.  

    Sie können die importierten Zahlungen überprüfen und sie mit der Bankzahlungsanzeige im Fenster **Zahlungseingangs Erf.-Journal** vergleichen. Sie können auch die Zahlungszeilen löschen, die von der Bank nicht verarbeitet werden konnten und für die Sie sich manuell mit dem Debitor in Verbindung setzen müssen.  

6.  Wählen Sie die Aktion **Buchen** aus.  

## <a name="see-also"></a>Siehe auch  
 [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md)   
 [Verarbeiten eines LSV-Einzugs](how-to-process-an-lsv-collection.md)   
 [Schliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md)   
 [Exportieren von Zahlungen mit LSV](how-to-export-payments-using-lsv.md) 

