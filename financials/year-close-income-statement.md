---
title: "Schließen Sie Erfolgsrechnungsberichte | Microsoft Docs"
description: "Am Jahresende beispielsweise müssen Sie die Stapelverarbeitung \"Erfolgsrechnungskonten Nullstellung\" laufen lassen, um dies Buchhaltungsperioden zu schließen, aus der sich das Geschäftsjahr zusammensetzt."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6ddd7b504f6faa856e92c336f889ad08db0b3d8b
ms.contentlocale: de-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-close-income-statement-accounts"></a>Vorgehensweise: Schließen Sie Erfolgsrechnungsberichte
Wenn ein Geschäftsjahr vorbei ist, müssen die Perioden, aus denen es besteht, geschlossen werden. Verwenden Sie dazu den Stapelverarbeitungsjob **Jahresabschluss**. Dieser Job überträgt die Ergebnisse des Jahrs auf ein Bilanzkonto und führt die Erfolgsrechnung durch. Hierfür erstellen Sie Zeilen in einem Erf.-Journal, die Sie dann buchen können.

## <a name="to-run-the-close-income-statement-batch-job"></a>Verwenden Sie dazu den Stapelverarbeitungsjob Erfolgsrechnung.
1. Schließen Sie das Geschäftsjahr ab. Das Geschäftsjahr muss geschlossen werden, bevor die Stapelverarbeitung aufgerufen werden kann. Weitere Informationen finden Sie unter [Vorgehensweise: Abschließen von Buchhaltungsperioden](year-close-account-periods.md).
2. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen ")und geben **GuV-Konten-Nullstellung** ein. Wählen Sie dann den zugehörigen Link aus.
3. Wählen Sie die Schaltfläche **OK**, um den Batchauftrag zu starten.

## <a name="about-the-close-income-statement-batch-job"></a>Mehr Informationen zum Stapelverarbeitungsjob Erfolgsrechnung.
Mithilfe dieses Batchauftrags werden alle Fibukonten der Art "Erfolgsrechnung" bearbeitet und Buchungszeilen erzeugt, die eine Nullstellung ihrer Salden bewirken. Anders ausgedrückt, entspricht jeder Posten der Summe aller Fibuposten auf dem Konto im Geschäftsjahr. Diese neuen Posten werden in ein Erfassungsjournal eingefügt, in dem Sie ein Gegenkonto und ein Abschlusskonto GuV in der Bilanz angeben müssen, bevor diese gebucht werden. Wenn Sie das Erfassungsjournal buchen, wird ein Posten auf jedes Erfolgsrechnungskonto gebucht, sodass der Saldo des Kontos Null ist und gleichzeitig das Jahresergebnis in die Bilanz übertragen wird.

Sie müssen das Erfassungsjournal manuell buchen. Durch den Batchauftrag erfolgt keine automatische Buchung der Posten, es sei denn, es wird eine Berichtswährung verwendet. Wenn eine zusätzliche Berichtswährung verwendet wird, bucht die Stapelverarbeitung die Posten direkt in die Fibu.

Das Datum, das von dem Batchauftrag in die Zeilen eingefügt wird, ist stets das Ultimodatum des Geschäftsjahrs. Das Ultimodatum ist ein fiktives Datum zwischen dem letzten Tag des alten und dem ersten Tag des neuen Geschäftsjahres. Der Vorteil des Buchens zu einem Ultimodatum liegt darin, dass die Salden des Geschäftsjahres mit normalen Datumsangaben erhalten bleiben.

Die Stapelverarbeitung **Jahresabschluss** kann mehrmals aufgerufen werden. Sie können im vorigen Geschäftsjahr buchen, selbst wenn die Erfolgskonten-Nullstellung bereits vorgenommen wurde, sofern Sie die Stapelverarbeitung erneut ausführen.

## <a name="see-also"></a>Siehe auch
[Schließen der Bücher](year-close-books.md)  
[Vorgehensweise: Buchen des Jahresabschlusspostens](year-how-post-year-end-close-entry.md)  
[So geht's: Ein neues Geschäftsjahr eröffnen](finance-how-open-new-fiscal-year.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

