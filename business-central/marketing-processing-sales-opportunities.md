---
title: Verarbeiten von Verkaufschancen in Verkaufszyklen | Microsoft Docs
description: Sie können Verkaufschancen anzeigen, schliessen oder löschen, und Sie können auch Offertee und Aufträge für Verkaufschancen einrichten und eine Verkaufschance über die einzelnen Phasen des Verkaufsprozesses verschieben.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: c3c86d622ca14d07eb19bb293066b0fbfaf74c42
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243057"
---
# <a name="process-sales-opportunities"></a>Verarbeiten von Verkaufschancen
Nachdem Sie eine Verkaufschance erstellen haben, gibt es einige Funktionen für die Verwaltung der Verkaufschance und deren Abschluss.

## <a name="to-view-opportunities"></a>Anzeigen von Verkaufschancen
Vorhandene Verkaufsverkaufschancen sind auf der Seite **Verkaufschancenliste** verfügbar. Es gibt unterschiedliche Arten, um auf diese Seite für die Verarbeitung von Verkaufschancen zuzugreifen:

| Verkaufschancen anzeigen für | Dann |
| --- | --- |
| Alle Verkäufer und Kontakte |Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkaufschancenliste** ein, und wählen dann den zugehörigen Link aus. |
| Ein bestimmter Verkäufer |Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkäufer** ein, und wählen dann den zugehörigen Link aus. Wählen Sie den Verkäufer, wählen sie die Aktion **Verkaufschancen** und dann die Aktion **Liste**. |
| Ein bestimmter Kontakt |Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontakte** ein, und wählen dann den zugehörigen Link aus. Wählen Sie den Kontakt aus der Liste, und wählen sie die Aktion **Verkaufschancen**. |

Jede dieser Aufgaben öffnet die Seite **Verkaufschancenliste**.

## <a name="to-close-opportunities"></a>Um Verkaufschancen abzuschliessen
Sie können Verkaufschancen abschliessen, wenn die Verhandlungen abgeschlossen sind. Wenn Sie eine Verkaufschance schließen, können Sie angeben, ob sie gewonnen oder verloren wurde und dafür die Gründe festlegen. Um einen Grund anzugeben, müssen Sie Verkaufschancenabschlusscodes einrichten.

1. Auf der Seite **Verkaufschancenliste** wählen Sie die Verkaufschance und die **Abschluss**-Aktion aus. Die Seite **Verkaufschance abschliessen** wird geöffnet.
2. Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **OK** aus.

   Die Felder **Verkaufschancenabschlusscode** und **Abschlussdatum** sind erforderlich und müssen ausgefüllt werden, bevor Sie auf die Schaltfläche **Ok** klicken können.

   Geben Sie im **Verkaufschancenabschlusscode**-Feld einen der vorhandenen Verkaufschancenabschlusscodes aus oder fügen Sie einen neuen Code hinzu. Um einen neuen Code hinzuzufügen, wählen Sie in der Dropdownliste **Aus vollständiger Liste auswählen** aus in wählen Sie dann **Neu**. Füllen Sie in der neuen leeren Zeile die Felder **Code**, **Art** und **Beschreibung** aus, und wählen Sie dann die **OK**-Schaltfläche.

## <a name="to-create-quotes-for-opportunities"></a>Um Angebote für Verkaufschancen zu erstellen
Sie können Verkaufsangebote für Kontakte erstellen, die nicht als Debitoren erfasst werden.

1. Auf der Seite **Verkaufschancenliste** wählen Sie die Verkaufschance und dann die **Verkaufsofferte zuweisen**-Aktion aus. Die Seite **Verkaufsofferte** wird geöffnet.
2. Füllen Sie die entsprechenden Felder aus.

## <a name="to-create-sales-orders-for-opportunities"></a>Verkaufsaufträge für Verkaufschancen erstellen
Sie können Verkaufsaufträge aus Verkaufsofferten erstellen, die Sie für Ihre Verkaufschancen erfasst haben. Bevor Sie Verkaufsaufträge für Ihre Kontakte erstellen können, müssen Sie den Kontakt als Debitor erstellen. Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

1. Suchen Sie auf der Seite **Verkaufschancenliste** die Verkaufschance, für die Sie eine Verkaufsofferte erstellt haben.
2. Wählen Sie die Aktion **Verkaufsangebot zuweisen** aus. Die Seite **Verkaufsofferte** wird geöffnet. Es enthält die Verkaufsofferte, die der Verkaufschance zugewiesen wurde.
3. Füllen Sie die weiteren Felder aus, und wählen Sie dann die Aktion **Auftrag erstellen** aus.

Bei der Bearbeitung von Verkaufschancen können Sie eine Offerte für den Kontakt erstellen, mit dem die Verkaufschance verknüpft ist.

## <a name="to-delete-opportunities"></a>Um Verkaufchancen zu löschen
Sie können Verkaufschancen z. B. löschen, wenn Sie ein Geschäft abgeschlossen haben. Es können jedoch nur abgeschlossene Verkaufschancen gelöscht werden. Es gibt zwei Möglichkeiten, um abgeschlossene Verkaufschancen zu löschen. Sie können einzelnen abgeschlossene Verkaufschancen über die Seite **Verkaufschancenliste** löschen, oder Sie können die Stapelverarbeitung **Geschlossene Verkaufschancen löschen...** ausführen, um mehrere Verkaufschancen auf Grundlage von Kriterien zu löschen.

Um abgeschlossene Verkaufschancen aus der Seite **Verkaufschancenliste** zu löschen, wählen Sie die Verkaufschance, und wählen Sie dann die Aktion **Löschen** aus.

Um abgeschlossene Verkaufschancen über die Stapelverarbeitung **Geschlossene Verkaufschancen löschen...** zu löschen verwenden, gehen Sie folgendermassen vor:

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Chancen löschen** ein, und wählen dann den zugehörigen Link aus.
2. Im **Verkaufschance**-Abschnitt richten Sie die Filter ein, die die zu löschenden abgeschlossenen Verkaufschancen definieren.
3. Wählen Sie die Schaltfläche **OK** aus.

Nachdem Sie eine Verkaufschance gelöscht haben, wird sie aus der Seite **Verkaufschancenliste** entfernt.

## <a name="to-move-an-opportunity-through-sales-cycle-stages"></a>Verschieben einer Verkaufschance über Verkaufsprozessstufen
Wenn eine Verkaufschance einem Verkaufsprozess folgt, können Sie sie vorwärts oder rückwärts durch die verschiedenen Stufen verschieben oder eine Stufe überspringen.

1. Wählen Sie auf der Seite **Verkaufschancenliste** die Aktion **Aktualisieren**. Der Assistent **Verkaufschance aktualisieren** wird geöffnet.
2. Verwenden Sie das **Aktionsart**-Feld, um die Verkaufschance durch die Verkaufsprozessstufen zu verschieben:
   * **Nächste** verschiebt die Verkaufschance eine Stufe weiter.
   * **Überspringen** verschiebt die Verkaufschance eine oder mehrere Stufen im Verkaufsprozess weiter, die Sie im Feld **Präsentation** angeben. Sie können nur Stufen überspringen, die eingerichtet wurden, um das Überspringen zu ermöglichen.
   * **Vorherige** verschiebt die Verkaufschance eine Stufe zurück.
   * **Überspringen** verschiebt die Verkaufschance eine oder mehrere Stufen im Verkaufsprozess zurück, die Sie im Feld **Präsentation** angeben.
   * **Aktualisieren** ermöglicht das Ändern von Informationen (z. B. Ihre Einschätzung zu den Erfolgschancen und den erwarteten Zahlen), ohne die Verkaufschance auf eine andere anderen Stufe zu verschieben.
3. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Erstellen und Verwalten von Kontakten](marketing-contacts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
