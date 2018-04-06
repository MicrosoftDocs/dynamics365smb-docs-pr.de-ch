---
title: Abschreibungsrsicherung einrichten| Microsoft Docs
description: "Um die Abdeckung der Anlagenversicherung zu verwalten, müssen Sie pro Versicherung einige allgemeine Versicherungsinformationen und eine Versicherungskarte einrichten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fd59a1aea6cb42dbeac7c6978619a5648f877b52
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-insurance"></a>Um Anlagenversicherung einzurichten:
Um die Abdeckung der Anlagenversicherung zu verwalten, müssen Sie pro Versicherung einige allgemeine Versicherungsinformationen und eine Versicherungskarte einrichten.

## <a name="to-set-up-general-insurance-information"></a>So richten Sie allgemeine Versicherungsinformationen ein
Um die Versicherungsfunktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)]  verwenden zu können, müssen Sie einige allgemeine Versicherungsinformationen einrichten.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen ](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Anlagen einrichten** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>So richten Sie Versicherungsarten ein
Sie können die Versicherungspolicen in Kategorien gruppieren, beispielsweise für Diebstahl- und Feuerversicherungen. Die Versicherungsarten werden auf der Versicherungskarte verwendet.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen ](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Anlagen einrichten** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-set-up-insurance-cards"></a>So richten Sie Versicherungskarten ein
Sie können die gesammelten Informationen über die einzelnen Versicherungspolicen auf der Versicherungskarte eingeben.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Versicherung** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **Versicherung** die Aktion **Neu** aus, um eine neue Karte für eine Versicherungspolice zu erstellen.  
3. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-set-up-insurance-journal-templates"></a>So richten Sie Versicherungs Erfassungsjournalvorlagen ein
[!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt automatisch eine Versicherungs-Buch.-Blattvorlage, wenn Sie zum ersten Mal das Fenster **Versicherungs Buch.-Blatt** öffnen; Sie können aber zusätzliche Vorlagen einrichten. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  

1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Versicherungjournal-Vorlage** ein und wählen den zugehörenden Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-set-up-insurance-journal-batches"></a>So richten Sie Versicherungs Erfassungsjournalnamen ein
Sie können zusätzliche Namen in einer Versicherungs Erfassungsjournalvorlage einrichten. Die Werte in dem Erfassungsjournalnamen werden als Vorgabewerte verwendet, wenn die Felder in den Erfassungsjournalzeilen nicht ausgefüllt sind. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  

1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Versicherungjournal-Vorlage** ein und wählen den zugehörenden Link aus.  
2. Wählen Sie eine Vers. Buch.-Blattvorlage und dann die Aktion **Buch.-Blattnamen** aus.
3. Füllen Sie im Fenster **Vers. Buch.-Blattnamen** die notwendigen Felder aus.

> [!NOTE]  
>   Zahlen haben in Erfassungsjournalnamen eine spezielle Funktion. Wenn die Erfassungsjournalvorlage oder der Erfassungsjournalname eine Nummer enthält, wird diese beim Buchen des Erfassungsjournals automatisch um eins hochgezählt. Wenn z. B. HH1 in dem Feld **Name** verwendet wurde, ändert sich der Name auf HH2, nachdem das Erfassungsjournal HH1 gebucht wurde.

## <a name="see-also"></a>Siehe auch
[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Finanzen](finance.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

