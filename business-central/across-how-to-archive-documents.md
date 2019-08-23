---
title: Einkaufs- und Verkaufsbelege archivieren | Microsoft Docs
description: Sie können auch Aufträge oder Bestellungen, Offerten, Reklamationen und Rahmenaufträge archivieren, und Sie können den archivierten Beleg verwenden, um den Beleg neu zu erstellen, dass er aus archiviert wurde.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2019
ms.author: sgroespe
ms.openlocfilehash: 4d7d9ad0e9c84d5c767095b7b7e786be932625e7
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796702"
---
# <a name="archive-documents"></a>Beleg archivieren
Sie können Verkaufs- und Einkaufsaufträge, Offerten und Rücklieferungen sowie Rahmenaufträge archivieren, beispielsweise weil Sie eine Kopie eines Belegs zur späteren Wiederverwendung speichern möchten. Sie können ein Verkaufs- oder Einkaufsbeleg mehrmals archivieren, wobei Sie jedes Mal eine andere archivierte Version speichern.

Für archivierte Belege, bei denen das Original immer noch vorhanden und nicht gebucht ist, können Sie die Funktion **Wiederherstellen** verwenden, um das Original mit der archivierten Version des Belegs zu überschreiben. Dies ist nützlich, wenn Sie die Inhalte eines Belegs auf einen früheren Zustand wiederherstellen müssen.

Für archivierte Belege, bei denen das Original gelöscht ist, können Sie den Inhalt nur erneut verwenden, indem Sie die Daten beispielsweise mit der Funktion **Beleg kopieren** kopieren.   

## <a name="to-set-up-automatic-document-archiving"></a>So richten Sie die automatische Archivierung von Belegen ein  
Sie können die automatische Archivierung von Verkaufs- und Einkaufsbelegen einrichten – beispielsweise Offerten, Rahmenbestellungen und Aufträge – bevor Sie Belege löschen.

Nachfolgend wird beschrieben, wie die automatische Archivierung von Verkaufsbelegen eingerichtet wird. Die Schritte sind für Einkaufsbelege ähnlich.
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitoren & Verkauf einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie auf der Seite **Debitoren und Verkauf Einr.** die folgenden Felder aus:

|Feld|Description|
|-----|-----------|
|**Verkaufsofferten archivieren**|**Nie**, wenn Verkaufsbelege beim Löschen nie archiviert werden sollen. **Frage**, wenn der Benutzer angeben soll, ob er Verkaufsbelege beim Löschen archivieren möchte. **Immer**, wenn Verkaufsofferten automatisch beim Löschen archiviert werden sollen.|
|**Rahmenaufträge archivieren**|Wählen Sie diese Option aus, um Rahmenaufträge bei jedem Löschen automatisch zu archivieren.|
|**Aufträge und Reklamationen archivieren**|Wählen Sie diese Option aus, um Verkaufsaufträge bei jedem Löschen automatisch zu archivieren.|

## <a name="to-archive-a-sales-order"></a>Verkaufsauftrag archivieren
Nachfolgend wird beschrieben, wie Sie einen Auftrag archivieren Die Schritte für alle Aufträge, Rahmenaufträge, Reklamationen und Offerten sind ähnlich.

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.  
2.  Öffnen Sie einen Verkaufsauftrag für Artikel, die Sie archivierne möchten.  
3.  Wählen Sie die **Beleg archivieren**-Aktion aus.

Der Auftrag ist archiviert. Sie können sie auf der Seite **Archivierte Verkaufsaufträge** anzeigen.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>So stellen Sie einen nicht gebuchten Verkaufsauftrag aus dem Archiv wieder her
Die folgende Vorgehensweise beschreibt, wie Sie den Inhalt eines archivierten Verkaufsauftrags zum ursprünglichen Verkaufsauftrag zurück bereitstellen. Dies ist nur möglich, wenn der Originalbeleg nicht gebucht wurde. Die Schritte für alle Aufträge, Rahmenaufträge, Reklamationen und Offerten sind ähnlich.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Archivierte Verkaufsaufträge** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie den archivierten Verkaufsauftrag oder eine Version davon aus, die Sie wiederherstellen möchten, und wählen Sie dann die Aktion **Wiederherstellen** aus.  

Die Inhalte des ursprünglichen Auftrags werden durch die der ausgewählten archivierten Version ersetzt.

## <a name="to-delete-archived-sales-orders"></a>Archivierte Auftragsversionen löschen
Nachfolgend wird beschrieben, wie Sie einen archivierten Auftrag löschen. Die Schritte sind für alle anderen archivierten Einkaufs- und Verkaufsbelege ähnlich.

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Archivierte Verkaufsauftragsversionen löschen** ein, und wählen dann den zugehörigen Link aus.  
2.  Auf der Seite **Archivierte Auftragsversionen löschen** wählen Sie den entsprechenden Filter aus.  
3.  Wählen Sie die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch
[Nachverfolgen von Belegzeilen](across-how-to-track-document-lines.md)  
[Verkauf](sales-manage-sales.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
