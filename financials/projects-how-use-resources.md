---
title: "Vorgehensweise: Ressourcen nutzen für Projekte  | Microsoft Docs"
description: Beschreibt, wie Arbeitszeittabellen verwendet werden, um Projekte zu verwalten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34d8b133a11324e1821780e3988158bb0989349b
ms.contentlocale: de-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-resources-for-jobs"></a>Gewusst wie: Verwenden von Ressourcen für Projekte
Wenn Sie den Verbrauch von Ressourcen im Projekt Erf.-Journal buchen, können Sie die Einstands- und Verkaufspreise, die Arbeitstypen und die damit verknüpften Projekte verfolgen. Weitere Informationen finden Sie unter [So gehts: Nutzung von Projekten](projects-how-record-job-usage.md).

Sie können auch den Verbrauch einer Ressource in einem Ressourcen Erf.-Journal buchen. Posten, die in einem Ressourcen Erf.-Journal gebucht werden, haben keinen Einfluss auf die Fibu.

**Hinweis: ** Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter] [Benutzeroberfläche [!INCLUDE[d365fin](includes/d365fin_md.md)] (ui-experiences.md) anpassen.

## <a name="to-assign-resources-to-jobs"></a>So weisen Sie Projekten Ressourcen zu
Sie weisen Projekten Ressourcen zu, indem Sie Projektplanungszeilen für das Projekt erstellen. Weitere Informationen finden Sie unter [Gewusst wie: Projekte erstellen](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Um Ressourcenverbrauch für ein Projekt buchen
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus **![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Job Journalkonto** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie das relevante Projekt-Erf.-Journal und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

## <a name="to-adjust-resource-prices"></a>Um Ressourcenpreise zu justieren:
Wenn Sie die Einstands- und Verkaufspreise für eine große Anzahl von Ressourcen ändern möchten, können Sie den Batchauftrag verwenden.  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen eingeben"). Geben Sie **Kosten/Preise anpassen ein** und wählen Sie dann den entsprechenden Link aus.
2. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.

**Hinweis**: Diese Stapelverarbeitung erzeugt oder aktualisiert keine alternativen Einkaufs- oder Verkaufspreise für Ressourcen. Sie ändert lediglich den Inhalt des Feldes auf der Ressourcenkarte für das Feld **Feld korrigieren**, das Sie in der Stapelverarbeitung ausgewählt haben. Die Änderung tritt für die Ressourcen sofort in Kraft, überprüfen Sie daher Ihre Korrekturfaktoren, bevor Sie die Stapelverarbeitung ausführen.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Um Ressourcen-Preisänderungsvorschläge auf Basis bestehender alternativer Preise zu erstellen:
Wenn Sie bereits alternative Ressourcenpreise für mehrere Ressourcen eingerichtet haben, können Sie den Batchauftrag verwenden, um alternative Ressourcenpreise einzurichten.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen eingeben"). Geben Sie **Ressourcen Preisänderungen ein** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Res. Preisänderung (Preis) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie das Fenster **Ressourcen-Preisänderungen**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>So erstellen Sie Ressourcenpreisvorschläge auf Basis bestehender Standard-VK-Preise
Wenn Sie einen oder mehrere alternative Ressourcenpreise basierend auf den Standardpreisen auf den Ressourcenkarten festlegen möchten, dann können Sie den Batchauftrag verwenden.  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen eingeben"). Geben Sie **Ressourcen Preisänderungen ein** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Res. Preisänderung (Res) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.  
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie das Fenster **Ressourcen-Preisänderungen**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Um Ressourcenpreisvorschläge auf Basis alternierender Preise zu erhalten
Wenn Sie bereits alternative Ressourcenpreise für mehrere Ressourcen eingerichtet haben, können Sie den Batchauftrag verwenden, um alternative Ressourcenpreise einzurichten.

1. Geben Sie im Feld **Suchen** **Servicepreiskorrekturgruppen (Preis)** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie das Fenster **Ressourcen-Preisänderungen**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="see-also"></a>Siehe auch
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)     
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]  

