---
title: Anlagen verwalten| Microsoft Docs
description: Erhalten Sie Informationen zu den Funktionen von Anlagen und eine Übersicht , wie mit Anlagen gearbeitet wird.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fabff17b66dd3d5a8c57537df34bddedba0d7248
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243862"
---
# <a name="fixed-assets"></a>Anlagevermögen
Die Anlagenfunktion in [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt Ihnen einen Überblick über Ihre Anlagen und stellt die korrekten periodischen Abschreibungen sicher. Ausserdem erhalten Sie dort einen Überblick über die Wartungskosten, können die Versicherungen verwalten, Anlagentransaktionen buchen und verschiedene Berichte und Statistiken generieren.

Sie müssen für jede Anlage eine Karte mit den entsprechenden Informationen über die Anlage einrichten. Sie können Gebäude oder Produktionseinrichtungen als Hauptanlage mit einer Komponentenliste einrichten und sie unterschiedlich gruppieren, z. B. nach Klasse, Abteilung oder Standort. Dann können Sie beginnen, die Anlagen zu erwerben, zu verwalten und zu verkaufen. Sie können auch Plananlagen einrichten. Dadurch haben Sie die Möglichkeit, geplante Anschaffungen und Verkäufe in Berichten zu berücksichtigen.

Um Anlagenabscheibungen sowie andere finanzielle Transaktionen, die sich auf die Anlagen beziehen, nachzuverfolgen, richten Sie mindestens ein Abschreibungsbuch für jede Anlage in Ihrem Unternehmen ein. Die Abschreibung wird getätigt, indem ein Bericht ausgeführt wird, der die periodische Abschreibung berechnet und ein Erf.-Journal mit den daraus resultierenden Posten ausfüllt, die dann gebucht werden. [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt verschiedene AfA-Methoden. Weitere Informationen finden Sie unter [AfA-Methoden](fa-depreciation-methods.md). Sie können mehrere AfA-Bücher pro Anlage für unterschiedliche Zwecke einrichten, beispielsweise eins für eine Steuerberichterstellung und ein weiteres zur internen Berichterstellung.

Für jede Anlage können Sie die Wartungskosten und das nächste Servicedatum erfassen. Durch die Überwachung der Wartungskosten wird die Budgetierung und die Entscheidung über den Verkauf einer Anlage erleichtert.

Jede Anlage kann mit einer oder mehreren Versicherungspolicen verknüpft werden. Daher haben Sie die Möglichkeit zu überprüfen, ob die Deckungsbeiträge in den Versicherungspolicen mit dem Wert der Anlagen übereinstimmen. Damit ist auch die Möglichkeit gegeben, die jährlichen Versicherungsprämien zu prüfen.

> [!NOTE]  
>   Hinweis: Sie können Anlagentransaktionen auf der Seite **Anlagen Fibu Erf.-Journal** oder auf der Seite **Anlagen Erf.-Journal** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind. Die Hilfe zu den Anlagen beschreibt lediglich, wie das Fenster **Anlagen Fibu Erf.-Journal** verwendet wird. Weitere Informationen finden Sie unter [Anlagen-Abschreibungsbücher automatisch einrichten](fa-how-setup-depreciation.md).

Bevor Sie mit dem Verwalten von Anlagen beginnen können, müssen Sie Standardwerte, Anlagenbuchungen,  Buchungsgruppen, Verteilungsschlüsseln, Buch.-Blätter und Buchungsarten einrichten. Weitere Informationen finden Sie unter [Einrichten von Anlagen](fa-setup.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

| An | Informationen |
| --- | --- |
| Erstellen von Anlagen, Zuordnen von Abschreibungsmethoden, Buchen von Anschaffungen und Restwerten sowie Drucken von Anlagenlisten |[Erworbene Anlagen](fa-how-acquire.md) |
| Erfassen von Servicebesuchen, Buchen und Überwachen von Wartungskosten. |[Anlagen verwalten](fa-how-maintain.md) |
| Aktualisieren von Versicherungsinformationen, Buchen von Anschaffungskosten auf Versicherungspolicen, Anpassen der Versicherungsdeckung, Anzeigen der Versicherungsstatistik und Auflisten von Versicherungspolicen |[Versichern von Anlagen](fa-how-insure.md) |
| Umbuchen von Anlagen, Transferieren von Anlagen an verschiedene Standorte sowie Aufteilen oder Zusammenfassen von Anlagen |[Übertragen, Teilen oder Kombinieren von Anlagen.](fa-how-trans-split-combine.md) |
| Anpassen der Werte von Anlagen, Buchen von Zuschreibungen und Buchen von erhöhten Abschreibungstransationen |[Anlagen neu bewerten](fa-how-revalue.md) |
| Berechnen und Buchen der Abschreibung und Analysieren der Abschreibung in Anlagenberichten. |[Anlagen abschreiben oder amortisieren](fa-how-depreciate-amortize.md) |
| Buchen von Verkaufstransaktionen, Anzeigen von Verkaufsposten und Buchen von Teilverkäufen |[Anlagen entsorgen oder ausser Dienst stellen](fa-how-dispose-retire.md) |
| Verwalten von Anlagenbudgets, Budgetieren von Anschaffungskosten, Budgetieren von Anlagenverkäufen und Budgetieren der Abschreibung. |[Budgets für Anlagen verwalten.](fa-how-manage-budgets.md) |

## <a name="see-also"></a>Siehe auch
[Anlagen einrichten](fa-setup.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  
[Finanzen](finance.md)  
[Erste Schritte](product-get-started.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
