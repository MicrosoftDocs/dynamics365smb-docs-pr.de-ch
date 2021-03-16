---
title: Exportieren von Zahlungen mit LSV
description: Nachdem der LSV-Einzug abgeschlossen wurde, können Sie LSV+-Dateien (Lastschriftverfahren) mit Zahlungsinformationen exportieren oder erstellen. Sie können die generierten Dateien auf einem Datenträger an die Bank senden oder eine elektronische Methode der Dateiübertragung wie die Onlinebankingsoftware oder ein Internetportal verwenden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f17eedb34a61dbfbc279e442fc87d5e1cb516f0f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383993"
---
# <a name="export-payments-using-lsv"></a>Exportieren von Zahlungen mit LSV
Nachdem der LSV-Einzug abgeschlossen wurde, können Sie LSV+-Dateien (Lastschriftverfahren) mit Zahlungsinformationen exportieren oder erstellen. Sie können die generierten Dateien auf einem Datenträger an die Bank senden oder eine elektronische Methode der Dateiübertragung wie die Onlinebankingsoftware oder ein Internetportal verwenden.  

## <a name="to-export-payments-using-lsv"></a>So exportieren Sie Zahlungen mit LSV  

1.  Wählen Sie das Symbol ![Glühbirne , das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell me-Funktion") aus, geben Sie **LSV-Erfassungsjournalliste** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie auf der Seite **LSV-Journal Liste** das gewünschte LSV-Journal aus.  
3.  Wählen Sie die Aktion **LSV-Datei schreiben** aus.  
4.  Füllen Sie auf der Seite **LSV Datei schreiben** die Felder auf dem Inforegister **Optionen** wie in der folgenden Tabelle beschrieben aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nr.**|Geben Sie die Nummer des LSV-Journalsummer an, das Sie exportieren möchten.|  
    |**Prüfen**|Geben Sie an, ob Sie Testlieferungen an Ihre Bank senden. Testdateien werden nicht von der Bank verarbeitet.|  

5.  Alle zugehörigen Zeilen werden in das LSV-Journal übertragen. Die LSV-Datei wird im angegebenen Ordner erstellt.  

## <a name="see-also"></a>Siehe auch  
 [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md)   
 [Verarbeiten eines LSV-Einzugs](how-to-process-an-lsv-collection.md)   
 [Abschliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md)   
 [Buchen von LSV+-Zahlungen](how-to-post-lsv-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]