---
title: Designdetails - Artikeltracking-Buchungsstruktur | Microsoft Docs
description: "Erfahren Sie, wie der Lagerposten als primäre Transportmitteln von Artikeltrackingnummern verwendet wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item tracking, posting, inventory
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bde0b129455dbdd7cbc91bd50b6d993abf727100
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-item-tracking-posting-structure"></a>Designdetails: Artikeltracking-Buchungsstruktur
Um der Bestandskalkulationsfunktionen zu entsprechen und eine einfachere und robustere Lösung zu erhalten, werden Lagerposten als der primäre Träger von Artikeltrackingnummern verwendet.  
  
Artikeltrackingnummern auf Auftragsnetzwerkeinheiten und nicht auftragsbezogenen Netzwerkeinheiten werden in der Tabelle **Reservierungsposten** (T337) angegeben. Artikeltrackingnummern, die mit den historischen Informationen verknüpft sind, werden direkt aus den Lagerposten abgerufen, die mit der jeweiligen Transaktion verknüpft werden. Das bedeutet, dass Lagerposten die Artikeltrackingspezifikationen der gebuchten Auftragszeile widerspiegeln.  
  
Das Fenster **Artikeltrackingzeilen** ruft die Informationen aus T337 und den Lagerposten ab und zeigt sie in der temporären Tabelle, **Trackingspezifikation** (T336) an. T336 enthält auch die temporären Dateien im **Fenster Artikeltrackingzeilen** für Artikeltrackingmengen, die noch fakturiert werden müssen.  
  
## <a name="one-to-many-relation"></a>1:n-Beziehung  
Die Tabelle **Lagerpostenverbindung**, die verwendet wird, um eine gebuchte Belegzeile mit den entsprechenden Lagerposten zu verknüpfen, besteht aus zwei Hauptteilen:  
  
* Ein Verweis zu der gebuchten Belegzeile, das Feld **Auftragszeilennr.**. Feld  
* Eine Postennummer, die auf einem Lagerposten verweist, das Feld **Lagerposten Lfd. Nr.**.  
  
Die Funktionen des vorhandenen **Lfd. Nr.**- Feldes, das einen Lagerposten mit einer gebuchten Belegzeile verknüpft, bearbeitet die typische Eins-zu-eins-Verknüpfung, wenn keine Artikeltrackingnummern auf der gebuchten Belegzeile vorhanden sind. Wenn Artikeltrackingnummern vorhanden sind, bleibt das Feld **Lfd. Nr.** leer, und die Eins-zu-viele-Relation wird durch die Tabelle **Lagerpostenverbindung** verarbeitet. Wenn die gebuchte Belegzeile Artikeltrackingnummern enthält, sich jedoch nur auf einem einzelnen Lagerposten bezieht, verarbeitet das Feld **Lfd. Nr.** die Verknüpfung, und es wird kein Datensatz in der Tabelle **Lagerpostenverbindung** erstellt.  
  
## <a name="codeunits-80-and-90"></a>Codeunit 80 und 90  
Um die Lagerposten für die Buchung zu teilen, ist der Code in Codeunit 80 und in Codeunit 90 durch Schleifen eingekreist, die durch globale temporäre Datensatzvariablen laufen. Dieser Code ruft Codeeinnheit 22 mit einer Artikel Erf.-Journalzeile auf. Diese Variablen werden initialisiert, wenn Artikeltrackingnummern für die Belegzeile vorhanden sind. Um den Code einfach zu halten, wird diese Schleifenstruktur immer verwendet. Wenn keine Artikeltrackingnummern für die Belegzeile vorhanden, wird ein einzelner Datensatz eingefügt, und die Schleife wird einmal ausgeführt.  
  
## <a name="posting-the-item-journal"></a>Buchen des Artikel Erf.-Journals.  
Artikeltrackingnummern werden über die Reservierungsposten übertragen, die mit dem Lagerposten verknüpft sind, und der Kreis durch die Artikeltrackingnummern erfolgt in Codeunit 22. Das Konzept arbeitet gleich wie wenn eine Artikel-Erf.-Journalzeile indirekt verwendet wird, um einen Einkauf oder eine Einkaufsbestellung beispielsweise zu buchen, wenn die Artikel-Erf.-Journalzeile direkt verwendet wird. Wenn das Artikel Erf.-Journal direkt verwendet wird, auf das Feld **Quellzeile ID** der Artikel Erf.-Journalzeile selbst.  
  
## <a name="code-unit-22"></a>Code Unit 22  
Codeunit 80 und 90 durchlaufen den Aufruf von Codeunit 22 während der Rechnungsbuchung von Artikeltrackingnummern und während der Fakturierung der vorhandenen Lieferungen oder Wareneingänge.  
  
Während der Mengenbuchung von Artikeltrackingnummern ruft Codeunit 22 Artikeltrackingnummern aus den Posten in T337 ab, die sich auf die Buchung beziehen. Diese Posten werden direkt in die Artikel Erf.-Journalzeile gesetzt.  
  
Codeunit 22 durchläuft die Artikeltrackingnummern und teilt die Posten in die entsprechenden Lagerposten ein, die die Artikeltrackingnummern enthalten. Informationen darüber, welche Lagerposten erstellt werden, werden auf T337 zurückgegeben, indem ein temporärer Datensatz T336 verwendet wird, der durch ein Verfahren in Codeunit 22 aufgerufen wird. Dieses Verfahren wird gestartet, wenn Codeunit 22 seine Ausführung beendet, da für diesen Artikel, das Objekt der Codeunit 22 die Informationen enthält. Wenn der temporäre Datensatz T336 abgerufen wird, erstellen Codeunit 80 und 90 Datensätze in der Tabelle **Lagerpostenverbindung**, um die erstellten Lagerposten mit der erstellten Lieferung oder der Lieferzeile zu verknüpfen. Codeunit 80 oder Codeunit 90 konvertiert dann die temporären T336-Datensätze zu realen T336-Datensätzen, die zu der jeweiligen Zeile gehören. Jedoch tritt diese Konvertierung nur auf, wenn die gebuchte Belegzeile nicht gelöscht wird, da sie nur teilweise gebucht wird.  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Artikeltracking](design-details-item-tracking.md)   
[Designdetails: Artikeltrackingdesign](design-details-item-tracking-design.md)
