---
title: Kategorisieren Sie Artikel| Microsoft Docs
description: "Um Artikel zu finden, können Sie Artikelattribute zuweisen und Artikel nach den definierten Kategorien organisieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c62d26dc9dc444359c0d8b5a9354b29132857de1
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="categorize-items"></a>Artikel kategorisieren
Um eine Übersicht über Ihre Artikel zu verwalten und das Sortieren und Finden von Artikeln zu erleichtern, ist es nützlich, Ihre Artikel in Artikelkategorien zu organisieren.

Um Artikel nach Eigenschaften zu finden, können Sie Artikelattribute Artikeln und auch Artikelkategorien zuordnen. Weitere Informationen finden Sie unter [Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>So erstellen Sie eine Artikelkategorie
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Logistik Artikelkategorien** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Artikelkategorie** die Aktion **Neu** aus.
3. Füllen Sie im Fenster **Artikelkategorienkarte** im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Geben Sie im Inforegister **Attribute** alle Artikelattribute für die Artikelkategorie an. Weitere Informationen finden Sie im Abschnitt "So weisen Sie Artikelattribute Artikelkategorien zu" in [Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md).

> [!NOTE]  
>   Hinweis: Wenn die Artikelkategorie eine übergeordnete Artikelkategorie besitzt, wie durch das Feld **Übergeordnete Kategorie** angegeben, werden alle Artikelattribute, die dieser übergeordneten Artikelkategorie zugewiesen sind, im Inforegister **Attribute** bereits eingetragen.

> [!NOTE]  
>   Artikelattribute, die Sie einer Artikelkategorie zuordnen, werden automatisch auf den Artikel angewendet, der der Artikelkategorie zugeordnet ist.

## <a name="to-assign-an-item-category-to-an-item"></a>So ordnen Sie eine Artikelkategorie einem Artikel zu
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die Karte des Artikels, den Sie einer Artikelkategorie zuordnen möchten.
3. Klicken Sie im Feld **Artikelkategoriencode** auf die Schaltfläche suchen und wählen Sie eine bereits vorhandene Artikelkategorie aus. Alternativ wählen Sie die Aktion **Neu**, um zuerst eine neue Artikelkategorie so zu erstellen, wie es im Abschnitt "So erstellen Sie eine Artikelkategorie" erklärt wird.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md)  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

