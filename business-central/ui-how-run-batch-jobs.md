---
title: "Erstellen und führen Sie eine Stapelverarbeitung | Microsoft Docs"
description: "Sie führen Stapelverarbeitungen durch , um Daten zu verarbeiten und Informationen zu aktualisieren, um periodische Buchhaltungsaktivitäten oder Berechnungen durchzuführen."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ac50d0ca59ece5365c000a9bfca06a0c18654512
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="run-batch-jobs"></a>Ausführen von Stapelverarbeitungen
Bei einer Stapelverarbeitung handelt es sich um einen Vorgang, bei dem Daten stapelweise verarbeitet werden, beispielsweise bei der Stapelverarbeitung **Wechselkurs regulieren**. Es stehen Stapelverarbeitungen für periodische Buchhaltungsaktivitäten zur Verfügung, beispielsweise zum Abschliessen der Erfolgsrechnung am Ende eines Geschäftsjahrs. Viele Stapelverarbeitungen dienen zum Ausführen von Berechnungsaufgaben – beispielsweise zum Berechnen von Zuschlägen, Wechselkursregulierungen oder VK-Preisen.

Eine Stapelverarbeitung gleicht einem Bericht, die Ergebnisse der Stapelverarbeitung werden jedoch zur direkten Aktualisierung der Informationen verwendet, anstatt diese lediglich auszugeben.

## <a name="to-run-a-batch-job"></a>So führen Sie eine Stapelverarbeitung aus:
1. Um das Anforderungsfenster für die gewünschte Stapelverarbeitung zu öffnen, wählen Sie das Symbol ![Suche für Seite oder Bericht](media/ui-search/search_small.png "Nach Seite oder Bericht suchen ")und geben den Namen der Stapelverarbeitung ein und wählen dann den zugehörigen Link aus.
2. Ist für die Stapelverarbeitung ein Inforegister vom Typ **Optionen** verfügbar, füllen Sie die Felder aus, um die Stapelverarbeitung zu konfigurieren.
3. Das Fenster kann mehrere Inforegister mit Filtern enthalten, mit denen sich die in die Stapelverarbeitung einzubeziehenden Daten einschränken lassen. Sie können Kriterien in die vorgeschlagenen Filter eingeben oder weitere Filter hinzufügen.
4. Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.

## <a name="see-also"></a>Siehe auch
[Eingeben von Kriterien in Filtern](ui-enter-criteria-filters.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

