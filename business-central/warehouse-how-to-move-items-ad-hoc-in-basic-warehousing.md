---
title: 'Vorgehensweise: Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen | Microsoft Docs'
description: "Möglicherweise müssen Sie gelegentlich Artikel zwischen internen Lagerplätzen umlagern, ohne Eingangs- oder Versandlagerort und ohne einen speziellen Bedarf aus einem Herkunftsbeleg. Sie können diese Ad-hoc-Lagerplatzumlagerungen zum Beispiel durchführen, um das Lager neu zu organisieren, Artikel in einen Inspektionsbereich zu bringen oder zusätzliche Artikel an einen bzw. aus einem Fertigungsbereich zu bewegen, ohne dass ein Systembezug zum Herkunftsbeleg des Fertigungsauftrags besteht."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ac7b80c3ada7a5dd27fc74d3d8be5e38f1552725
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen
Möglicherweise müssen Sie gelegentlich Artikel zwischen internen Lagerplätzen umlagern, ohne Eingangs- oder Versandlagerort und ohne einen speziellen Bedarf aus einem Herkunftsbeleg. Sie können diese Ad-hoc-Lagerplatzumlagerungen zum Beispiel durchführen, um das Lager neu zu organisieren, Artikel in einen Inspektionsbereich zu bringen oder zusätzliche Artikel an einen bzw. aus einem Fertigungsbereich zu bewegen, ohne dass ein Systembezug zum Herkunftsbeleg des Fertigungsauftrags besteht.  

In den Basislagerkonfigurationen können für Lagerplätze, die das Einrichtungsfeld **Lagerplatz notwendig** und möglicherweise die Einrichtungsfelder **Kommissionierung erforderlich** und **Einlagerung erforderlich** verwenden, Ad-hoc-Lagerplatzumlagerungen ohne Herkunftsbelege auf die folgenden Arten registriert werden:  

- Im Fenster **Interne Umlagerung**.  
- Mit dem Fenster **Umlagerungs Erfassungsjournal**.  

> [!NOTE]  
>  In erweiterten Lagerkonfigurationen sind dies Lagerplätze, die das Einrichtungsfeld **Gesteuerte Einlag. u. Kommiss.** verwenden. Um die Artikel ad hoc zwischen Lagerplätzen zu verschieben, verwenden Sie die Fenster **Lagerplatzumlagerungsvorschlag** oder **Interne Kommissionierung** oder **Interne Einlagerung**.  

## <a name="to-move-items-as-an-internal-movement"></a>Um Artikel als interne Umlagerung zu verschieben  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **interne Umlagerung** ein, und wählen dann den zugehörigen Link aus.  
2.  Füllen Sie auf dem Inforegister **Allgemein** das Feld **Nr.** aus. Feld, das Sie entweder leer lassen oder indem Sie die Schaltfläche **AssistEdit** klicken, um in der Nummernserie eine Auswahl zu treffen.  
3.  Geben Sie im Feld **Lagerortcode** den Lagerort ein, an dem die Bewegung stattfindet.  

    Wenn der Lagerort bereits als Ihr Standardlagerort als Lagermitarbeiter eingerichtet ist, wird der Lagerortcode automatisch eingefügt.  
4.  Geben Sie im Feld **Nach Lagerplatzcode** einen Code für den Lagerort ein, an den Sie den Artikel umlagern möchten. Für die Produktion könnte dies z. B. der Fert.-Bereitst.-Lagerplatzcode oder der Off. Fert.-Ber.-Lagerplatz.-Code sein, wie auf der Lagerortkarte oder in der Arbeitsplatzgruppe definiert.  
5.  Geben Sie im Feld **Fälligkeitsdatum** das Datum ein, an dem die Umlagerung abgeschlossen sein muss.  
6.  Wählen Sie im Inforegister **Zeilen** das Feld **Artikelnr.**, um das Fenster **Lagerplatzinhaltsliste** zu öffnen, und wählen Sie den Artikel aus, der basierend auf seiner Verfügbarkeit an Lagerorten umgelagert werden soll. Alternativ aktivieren Sie die Aktion **Lagerplatzinhalt holen**, um die Zeilen für die interne Umlagerung basierend auf Ihrem Filter auszufüllen. Weitere Informationen finden Sie unter der QuickInfo für die **Lagerplatzinhalt abrufen** Aktion.   

    Wenn Sie den Artikel ausgewählt haben, wird das Feld **Von Lagerplatzcode** automatisch entsprechend dem ausgewählten Lagerplatzinhalt ausgefüllt, Sie können es aber in jeden beliebigen anderen Lagerort ändern, an dem der Artikel verfügbar ist.  

    > [!NOTE]  
    >  Da das Feld **Artikelnr.** und das Feld **Von Lagerplatzcode** verbunden sind, ändern sich deren voneinander abhängige Werte, wenn eines der Felder bearbeitet wird.  

    Das Feld **Nach Lagerplatzcode** wird mit dem Wert ausgefüllt, den Sie im Kopf eingegeben haben. Sie können es aber in der Zeile in jeden beliebigen anderen Lagerplatzcode ändern, der nicht gesperrt oder für spezielle Zwecke dediziert ist. Weitere Informationen zum Erstellen von den dedizierten Lagerplätzen finden Sie unter .  
7.  Wenn Sie die Lagerplätze festgelegt haben, von denen und an die Sie den Artikel verschieben möchten, geben Sie im Feld **Menge** die umzulagernde Menge ein.  

    > [!NOTE]  
    >  Die Menge muss im Feld "Von Lagerplatzcode" verfügbar sein.  

8.  Wenn Sie bereit sind, die interne Umlagerung zu verarbeiten, wählen Sie die Aktion **Lagerbestandsumlagerung erstellen** aus.  

    > [!NOTE]  
    >  Wenn Sie die Lagerbestandsumlagerung erstellt haben, werden die Zeilen für die interne Umlagerung gelöscht.  

    Die restliche Ad-hoc-Umlagerung führen Sie im Fenster **Lagerbestandsumlagerung** auf dieselbe Weise aus, wie Sie eine Lagerplatzumlagerung basierend auf Herkunftsbelegen ausführen würden. Weitere Informationen finden Sie unter [Umlagern von Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Um Artikel mit dem Artikel-Umlagerungs-Erfassungsjournal umzulagern
Anstelle der Verwendung von Lagerplatzumlagerungsbelegen können Sie die Umlagerung von Artikeln erfassen, indem Sie deren Lagerplatzcodes neu klassifizieren. Weitere Informationen finden Sie unter [Erfassen, Regulieren und Umbuchen von Lagerbestand](inventory-how-count-adjust-reclassify.md).   
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Artikel Anlagen Umbuch. Erf.-Journal** ein, und wählen dann den zugehörigen Link aus.  
2.  Legen Sie in jeder Erfassungsjournalzeile die Lagerplätze fest, von denen und auf die Sie Artikel umlagern möchten, indem Sie die Felder **Lagerplatzcode** und **Neuer Lagerplatzcode** ausfüllen.  

    1.  Um den gesamten Inhalt eines Lagerplatzes in einen anderen Lagerplatz umzulagern, wählen Sie die Aktion **Lagerplatzinhalt holen** aus.  
    2.  Geben Sie die Filter ein, um den Lagerplatz zu suchen, dessen Inhalt Sie umlagern möchten, und bestätigen Sie mit **OK**. Die Erfassungsjournalzeilen werden mit dem Inhalt des Lagerplatzes ausgefüllt.  
3.  Füllen Sie die übrigen Felder jeder Erf.-Journalzeile aus.   
4.  Buchen Sie das UmErfassungsjournal.  

    > [!NOTE]  
    >  Anders als bei Lagerplatzumlagerungsbelegen erstellt eine Lagerplatzumlagerung, die mit dem Umlagerungs Erfassungsjournal gebucht wird, keine Logistikanforderung, die physische Aufgabe auszuführen.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

