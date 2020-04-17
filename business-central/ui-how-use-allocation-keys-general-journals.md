---
title: Verwenden von Umlageschlüsseln in Fibu Erf.-Journals | Microsoft Docs
description: Erfahren Sie, wie Sie Verteilungsschlüssel in Buch.-Blättern verwenden können.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 408dfeaeb56f271a2b9b3d5cf515e41abeaf78e8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195569"
---
# <a name="use-allocation-keys-in-general-journals"></a>Verwenden von Umlageschlüsseln in Fibu Erf.-Journals
Die Posten einer Fibu Erf.-Journalzeile lassen sich beim Buchen des Erf.-Journals auf verschiedene Konten verteilen. Die Verteilung kann nach Anzahl, Prozent oder Betrag vorgenommen werden.

## <a name="to-set-up-allocation-keys"></a>Einrichten von Verteilungsschlüsseln
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Wiederk. Fibu Erf.-Journal** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Fibu Erf.-Journalnamen** den **Erf.-Journalnamen**.
3. Sie können entweder Zuordnungen in einer vorhandene Charge in der Liste ändern oder eine neue Charge mit Zuordnungen erstellen.
   * Um eine neue Chargennummer zu erstellen, wählen Sie die Aktion **Neu** und gehen Sie zum nächsten Schritt.
   * Um die Zuordnungen eines vorhandenen Erfassungsjournals zu ändern, wählen Sie das Erfassungsjournal und gehen Sie zum Schritt 7.    
4. Geben Sie im Feld **Name** einen Namen für das Buch.-Blatt ein, wie beispielsweise REINIGUNG. Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie z. B. Reinigungsausgaben Erfassungsjournal.
5. Wenn Sie fertig sind, schliessen Sie die Seite. Ein neues, leeres wiederkehrendes Erfassungsjournal wird geöffnet.
6. Füllen Sie die Felder in der Zeile aus.
7. Wählen Sie die Aktion **Verteilung** aus.
8. Erstellen Sie für jede Verteilung eine Zeile. Sie müssen entweder das Feld **Verteilung %**, **Anzahl Verteilungen** oder **Betrag** ausfüllen. Sie müssen ebenfalls das Feld **Kontonr.** ausfüllen und, wenn Sie auf globale Dimensionen verteilen, auch die Felder "globale Dimensionen".
9. Wenn Sie in der Zeile einen Prozentsatz eingeben, wird der Betrag im Feld **Betrag** automatisch berechnet. Diese Beträge haben das gegenteilige Vorzeichen von dem Gesamtbetrag im Feld **Betrag** des wiederkehrenden Erfassungsjournals.
10. Nachdem Sie die Zuteilungszeilen eingegeben haben, wählen Sie **OK** aus, um zur Seite **Wiederk. Fibu Erf.-Journal** zurückzukehren. Das Feld **Zugewiesener Betrag (USD)** ist ausgefüllt und entspricht dem Feld **Betrag**.
11. Buchen Sie die Erf.-Journalzeile.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Ändern eines bereits eingerichteten Umlageschlüssels
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Wiederk. Fibu Erf.-Journal** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Wiederk. Fibu Erf.-Journal** das Erf.-Journal mit der Verteilung aus.
3. Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **Zuweisungen** aus.
4. Ändern Sie die relevanten Felder und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Journale und Belege buchen](ui-post-documents-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
