---
title: "Vorgehensweise: Arbeiten mit  Zuständigkeitseinheiten | Microsoft Docs"
description: "Zuständigkeitseinheiten ermöglichen die Verwaltung von Verwaltungscentern. Eine Zuständigkeitseinheit kann ein Cost Center, ein Profit Center, ein Investment Center oder ein anderes unternehmensdefiniertes Verwaltungscenter sein."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 643d0b7be64addf3604283dbed58d59a54df2032
ms.contentlocale: de-ch
ms.lasthandoff: 11/26/2018

---
# <a name="work-with-responsibility-centers"></a>Arbeiten mit Zuständigkeitseinheiten
Zuständigkeitseinheiten ermöglichen die Verwaltung von Verwaltungscentern. Eine Zuständigkeitseinheit kann ein Cost Center, ein Profit Center, ein Investment Center oder ein anderes unternehmensdefiniertes Verwaltungscenter sein. Beispiele von Zuständigkeitseinheiten können ein Verkaufsbüro, eine Einkaufsabteilung für mehrere Lagerorte und ein Fabrikplanungsbüro sein. Mithilfe dieser Funktionalität können Unternehmen beispielsweise benutzerspezifische Ansichten von Verkaufs- und Einkaufsdokumenten einrichten, die ausschliesslich mit einem bestimmten Verwaltungscenter zusammenhängen.  

Die Verwendung mehrerer Lagerorte und Zuständigkeitseinheiten bietet Unternehmen mit mehreren Lagerorten die Möglichkeit, ihre Unternehmensabläufe äusserst flexibel und zugleich so optimal wie möglich zu verwalten.

Die Funktionalität "Mehrere Lagerorte" ermöglicht Unternehmen die Verwaltung ihres Lagers an mehreren Lagerorten mithilfe einer Datenbank. Zwei Konzepte, Lagerorte und Lagerhaltungsdaten, bilden die Eckpfeiler dieses Elements. Ein Lagerort ist definiert als ein Ort, der die physische Platzierung von Artikeln sowie Artikelmengen verwaltet. Das begriffliche Konzept erstreckt sich auch auf Anlagen oder Produktionsstätten sowie Vertriebsstellen, Lager, Verkaufsräume und Dienstfahrzeuge. Lagerhaltungsdaten sind definiert als ein Artikel an einem bestimmten Lagerort und/oder als Variante. Mithilfe von Lagerhaltungsdaten sind Unternehmen mit mehreren Standorten in der Lage, Beschaffungsdaten, Adressen sowie einige Finanzbuchungsdaten auf Standortebene hinzuzufügen. Dadurch sind sie in der Lage, Varianten desselben Artikels für einen einzelnen Lagerort zu beschaffen und Artikel für die einzelnen Standorte auf der Grundlage standortspezifischer Beschaffungsdaten zu bestellen.  

Zuständigkeitseinheiten erweitern die Funktionalität "Mehrere Lagerorte"; Benutzer erhalten hier die Möglichkeit des Umgangs mit Verwaltungscentern. Eine Zuständigkeitseinheit kann ein Cost Center, ein Profit Center, ein Investment Center oder ein anderes unternehmensdefiniertes Verwaltungscenter sein. Beispiele von Zuständigkeitseinheiten können ein Verkaufsbüro, eine Einkaufsabteilung für mehrere Lagerorte und ein Fabrikplanungsbüro sein. Mithilfe dieser Funktionalität können Unternehmen beispielsweise benutzerspezifische Ansichten von Verkaufs- und Einkaufsdokumenten einrichten, die ausschliesslich mit einem bestimmten Verwaltungscenter zusammenhängen.

## <a name="to-set-up-a-responsibility-center"></a>Zuständigkeitseinheiten einrichten  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verantwortlichkeits-Centers** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Wenn Sie den Mandanten mithilfe von Zuständigkeitseinheiten verwalten, empfiehlt es sich möglicherweise, eine standardmässige Zuständigkeitseinheit für den Mandanten einzurichten.
4. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Unternehmungsinformation** ein, und wählen dann den zugehörigen Link aus.
5. In dem Feld **Zuständigkeitseinheiten** können Sie einen Zuständigkeitseinheitencode eingeben.

Dieser Code wird auf Einkaufs- und Verkaufsbelegen oder Servicedokumenten verwendet werden, wenn der Anwender, Debitor oder Kreditor keine Vorgabe Zuständigkeitseinheit hat. Auf allen möglichen Verkaufs- oder Einkaufs-Servicebelegen können Sie eine andere als der Vorgabe Zuständigkeitseinheit eingeben.

> [!NOTE]  
>  Wenn Sie einen Zuständigkeitseinheitencode in einem Beleg angeben, beeinflusst er die Adresse, Dimensionen und Preise im Beleg.  

## <a name="to-assign-responsibility-centers-to-users"></a>Zuständigkeitseinheiten für Benutzer zuweisen:  
Sie können Benutzer so einrichten, dass in ihrer täglichen Routine die Anwendung nur die entsprechenden Belege für ihre speziellen Arbeitsbereiche anzeigt. Benutzer werden normalerweise mit einer Zuständigkeitseinheit verknüpft und arbeiten nur mit Belegen, die mit speziellen Anwendungsbereichen in dieser Zuständigkeitseinheit verbunden sind.  

Um dies einzurichten, weisen Sie Benutzern Zuständigkeitseinheiten in drei Basisfunktionsbereichen zu: Kreditoren, Einkauf und Servicemanagement.  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer einrichten** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **Benutzer einrichten** den Benutzer, dem Sie eine Zuständigkeitseinheit zuweisen wollen. Wenn sich der Benutzer nicht in der Liste befindet, müssen Sie eine Benutzer-ID im Feld **Benutzer-ID** eingeben.  
3.  Im Feld **Verk.-Zuständigk.-Einh. Filter** geben Sie die Zuständigkeitseinheit ein, in der der Benutzer Aufgaben haben wird, die mit "Debitoren & Verkauf" verbunden sind.  
4.  Im Feld  **Eink.-Zuständigk.-Einh. Filter** geben Sie die Zuständigkeitseinheit ein, in der der Benutzer Aufgaben haben wird, die mit "Kreditoren &amp; Einkauf" verknüpft sind.  
5.  Im Feld **Serv.-Zuständigk.-Einh. Filter** geben Sie die Zuständigkeitseinheit ein, in der der Benutzer Aufgaben haben wird, die mit Serviceverwaltung verknüpft sind.  

> [!NOTE]  
>  Benutzer werden weiterhin in der Lage sein, alle gebuchten Belege und Posten einzusehen, nicht nur diejenigen, die mit ihrer eigenen Zuständigkeitseinheit verbunden sind.

## <a name="see-also"></a>Siehe auch  
[Bestand einrichten](inventory-setup-inventory.md)  
Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)
[Bestand](inventory-manage-inventory.md)[Lagerortverwaltung](warehouse-manage-warehouse.md).  
[Logistik](warehouse-manage-warehouse.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

