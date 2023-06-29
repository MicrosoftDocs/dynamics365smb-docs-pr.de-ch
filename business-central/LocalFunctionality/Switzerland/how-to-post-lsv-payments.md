---
title: Buchen von LSV+-Zahlungen
description: Zahlungen können nach Empfang einer LSV+ (Lastschrift Verfahren)-Zahlungsanzeige von der Bank gebucht werden.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '3010830, 3010831, 3010832,3010834, 3010835'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="post-lsv-payments"></a><a name="post-lsv-payments"></a>Buchen von LSV+-Zahlungen
Zahlungen können nach Empfang einer LSV+ (Lastschrift Verfahren)-Zahlungsanzeige von der Bank gebucht werden.  

## <a name="to-post-lsv-payments"></a><a name="to-post-lsv-payments"></a>So buchen Sie LSV+-Zahlungen

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Tell Me-Funktion") Geben Sie im **Zahlungseingangsprotokolle** ein, und wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie das entsprechende Journal aus und wählen Sie dass **Journal bearbeiten** aus.  

    > [!NOTE]  
    >  Sie können den Erf.-Journalnamen für LSV auswählen, wo das betreffende Gegenkonto definiert ist. Es kann jeweils nur eine LSV-Journalzeile in ein Zahlungseingangs Erf.-Journal importiert werden. Weitere Informationen finden Sie unter Zahlungseingangs Erf.-Journal (Seite).  

3.  Wählen Sie die Aktion **von LSV-Erf.-Journal abrufen** aus.  
4.  Wählen Sie auf der Seite **LSV-Journal Liste** die LSV-Journalzeile aus, die Sie in das Zahlungseingangs Erf.-Journal importieren möchten.  

    > [!NOTE]  
    >  Es können nur Erf.-Journalzeilen importiert werden, in denen das Feld **LSV-Status** auf **Datei erstellt** festgelegt ist.  

5.  Wählen Sie die Schaltfläche **OK** aus.  

    Die LSV-Journalzeile wird in das Zahlungseingangs Erf.-Journal importiert. Der Wert im Feld **LSV-Status** auf der Seite **LSV-Journal Liste** ändert sich von **Datei erstellt** in **Beendet**.  

    Sie können die importierten Zahlungen überprüfen und sie mit der Bankzahlungsanzeige auf der Seite **Zahlungseingangs Erf.-Journal** vergleichen. Sie können auch die Zahlungszeilen löschen, die von der Bank nicht verarbeitet werden konnten und für die Sie sich manuell mit dem Debitor in Verbindung setzen müssen.  

6.  Wählen Sie die Aktion **Buchen** aus.  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch
 [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md)   
 [Verarbeiten eines LSV-Einzugs](how-to-process-an-lsv-collection.md)   
 [Abschliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md)   
 [Exportieren von Zahlungen mit LSV](how-to-export-payments-using-lsv.md) 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
