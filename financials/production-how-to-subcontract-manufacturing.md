---
title: Produktion untervergeben | Microsoft Docs
description: Nachdem die Bestellung aus dem Fremdarbeitenvorschlag erstellt wurde, kann sie gebucht werden.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2796da1b41569c8c950dc844fc31eaf4f0179efa
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="subcontract-manufacturing"></a>Fertigung durch Fremdarbeitsvertrag
Ausgewählte Arbeitsgänge an Kreditoren weiter zu vergeben, ist in vielen Fertigungsunternehmen üblich. Fremdarbeit kann ein seltener Vorgang oder integraler Bestandteil aller Fertigungsschritte sein.

Es gibt mehrere Werkzeuge für das Verwalten von Fremdarbeit:  

- Arbeitsplatzgruppen mit zugewiesenen Kreditoren: Mit dieser Funktion können Sie eine Arbeitsgruppe einrichten, die einem Kreditor (Subunternehmer) zugewiesen ist. Eine solche Arbeitsplatzgruppe wird als Arbeitsplatzgruppe für Fremdarbeit bezeichnet. Sie können eine Arbeitsplatzgruppe für Fremdarbeit für einen Arbeitsplanvorgang angeben, wodurch Sie die als Fremdarbeit vergebene Aktivität problemlos verarbeiten können. Ausserdem können Sie die Kosten des Vorgangs auf Arbeitsplan- oder Arbeitsplatzebene kennzeichnen.  
- Arbeitsplatzgruppenkosten auf Basis von Einheiten oder Zeit: Über diese Funktion können Sie angeben, ob Kosten, die der Arbeitsplatzgruppe zugewiesen sind, auf einer Fertigungszeit oder einem Pauschalbetrag pro Einheit basieren. Üblicherweise stellen Subunternehmer für ihre Leistungen einen Pauschalbetrag pro Einheit in Rechnung; die Anwendung kann aber mit beiden Optionen (Fertigungszeit und Pauschalbetrag pro Einheit) umgehen.  
- Fremdarbeitenvorschlag: Mit dieser Funktion können Sie nach den Fertigungsaufträgen mit Material suchen, die an einen Subunternehmer gesendet werden können, und können Sie automatisch aus Arbeitsplänen für Fertigungsaufträge Einkaufsbestellungen für Fremdarbeitsvorgänge erstellen. Beim Buchen der jeweiligen Einkaufsbestellung werden dann automatisch Einkaufsbestellungsbeträge für den Fertigungsauftrag gebucht. Ein Fertigungsauftrag muss den Status "Freigegeben" haben, damit aus einem Fremdarbeitenvorschlag auf ihn zugegriffen und er dort verwendet werden kann.  

## <a name="subcontract-work-centers"></a>Arbeitsplatzgruppen für Fremdarbeiten  
Arbeitsplatzgruppen für Fremdarbeiten werden auf gleiche Weise eingerichtet wie normale Arbeitsplatzgruppen, allerdings mit weiteren Informationen. Arbeitsplänen werden sie in gleicher Weise zugewiesen wie andere Arbeitsplatzgruppen.  

### <a name="subcontract-work-center-fields"></a>Felder unter "Arbeitsplatzgruppen für Fremdarbeiten"  
Das Feld **Kreditorennr.** kennzeichnet die Arbeitsplatzgruppe als Arbeitsplatzgruppe für Fremdarbeit. Sie können die Nummer eines Subunternehmers (Fremdarbeiters) eingeben, der die Arbeitsplatzgruppe bereitstellt. Dieses Feld kann zum Verwalten von Arbeitsplatzgruppen verwendet werden, die unternehmensextern sind, in denen aber eine vertragsgebundene Verarbeitung erfolgt.  

Wenn Sie für Fremdarbeiten mit dem Kreditor einen anderen Satz für jeden Prozess vereinbart haben, können Sie das Kontrollkästchen **Spezieller Einstandspreis** aktivieren. Dadurch erhalten Sie die Möglichkeit, für jeden Arbeitsgang einen Betrag einzurichten und somit die Zeit zu sparen, die für die erneute Eingabe der einzelnen Einkaufsbestellungen erforderlich ist. Für die Verarbeitung werden nicht die Kosten in den Kostenfeldern der Arbeitsplatzgruppe, sondern der Einstandspreis im Arbeitsgang verwendet. Durch Aktivieren des Kontrollkästchens **Spezieller Einstandspreis** werden die Einstandspreise für den Kreditor pro Arbeitsplanvorgang berechnet.  

Wenn Sie für Fremdarbeiten einen einzelnen Satz pro Kreditor vereinbart haben, belassen Sie das Feld **Spezieller Einstandspreis** deaktiviert. Die Einstandspreise werden eingerichtet, indem die Felder **EK-Preis**, **Kosten %** und **Gemeinkostensatz** ausgefüllt werden.  

### <a name="routings-that-use-subcontract-work-centers"></a>Arbeitspläne, in denen Arbeitsplatzgruppen für Fremdarbeit verwendet werden  
Arbeitsplatzgruppen für Fremdarbeit können für Arbeitsgänge in Arbeitsplänen in gleicher Weise verwendet werden wie normale Arbeitsplatzgruppen.  

Sie können einen Arbeitsplan erstellen, für den eine externe Arbeitsplatzgruppe als standardmässiger Fertigungsschritt verwendet wird. Alternativ können Sie den Arbeitsplan für einen bestimmten Fertigungsauftrag so ändern, dass er einen externen Arbeitsgang enthält. Dies kann in einer Notsituation, z. B. wenn ein Server nicht ordnungsgemäss funktioniert, oder in einer Zeitspanne mit höherem Bedarf erforderlich sein, in der Arbeiten, die in der Regel innerbetrieblich ausgeführt werden, an einen Subunternehmer vergeben werden müssen.  

Weitere Informationen finden Sie unter [Arbeitspläne erstellen](production-how-to-create-routings.md).  

## <a name="subcontracting-worksheet"></a>Fremdarbeitenvorschlag  
Sobald Sie den  Fremdarbeitenvorschlag berechnet haben, wird der entsprechende Beleg (in diesem Fall eine Einkaufsbestellung) erstellt.  

# <a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a>Fremdarbeitenvorschläge berechnen und Fremdarbeitsbestellung erstellen
Die Fenster **Fremdarbeitenvorschlag** funktioniert wie die  **Planungsvorschlag**indem es den erforderlichen Vorrat berechnet, in diesem Fall Bestellungen, die Sie im Vorschlag überprüfen und dann mit der Funktion **Ereignismeldung durchführen** erstellen.  

> [!NOTE]  
>  Ein Fertigungsauftrag muss den Status **Freigegeben** haben, damit aus einem Fremdarbeitenvorschlag auf ihn zugegriffen und er dort verwendet werden kann.  

### <a name="to-calculate-the-subcontracting-worksheet"></a>Fremdarbeitenvorschlag berechnen  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Arbeitsblatt Fremdarbeit** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Damit der Vorschlag berechnet wird, klicken Sie auf  Aktionen **Fremdarbeit berechnen**.  
3.  Definieren Sie im Fenster **Fremdarbeit berechnen** den Filter für an Subunternehmer vergebene Arbeitsgänge oder die Arbeitsplatzgruppen, in der sie ausgeführt werden, um nur die relevanten Fertigungsaufträge zu berechnen.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

    Sehen Sie sich die Zeilen im **Fremdarbeitenvorschlag** an. Die Informationen in diesem Vorschlag stammen aus dem Fertigungsauftrag und den FA-Arbeitsgängen und werden in die Einkaufsbestellung übernommen, wenn dieser Beleg erstellt wird. Wie bei den anderen Vorschlägen auch können Sie eine Zeile aus dem Vorschlag löschen, ohne dass sich dies auf die ursprünglichen Informationen auswirkt. Die Informationen werden wieder angezeigt, wenn Sie die Funktion **Fremdarbeit berechnen** das nächste Mal ausführen.  

### <a name="to-create-the-subcontract-purchase-order"></a>Einkaufsbestellung für Fremdarbeit generieren  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Arbeitsblatt Fremdarbeit** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Vorgang** die Option **Ereignismeldung durchführen** aus.  
3.  Wählen Sie das Feld **Bestellungen/Aufträge drucken**, um die Einkaufsbestellung zu drucken, wenn diese erstellt wird.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

Wenn alle als Fremdarbeit zu vergebende Arbeitsgänge an denselben Kreditor gesendet werden müssen, dann wird nur eine Einkaufsbestellung erstellt.  

Die Vorschlagszeile, die in eine Einkaufsbestellung umgewandelt wurde, wird aus dem Vorschlag gelöscht. Sobald eine Einkaufsbestellung erstellt wurde, erscheint sie nicht mehr im Vorschlag.  

## <a name="posting-subcontract-purchase-orders"></a>Einkaufsbestellungen für Fremdarbeiten buchen  
Sobald die Einkaufsbestellungen für Subunternehmer erstellt wurden, können sie gebucht werden. Nach Empfang der Bestellung wird ein Kapazitätsposten im Fertigungsauftrag gebucht, und bei der Fakturierung der Bestellung wird der EK-Preis der Einkaufsbestellung im Fertigungsauftrag gebucht.  

Wenn der Einkauf als eingegangen gebucht wird, wird automatisch ein Istmeldungs-Erfassungsjournalzeilenposten für den Produktionsauftrag gebucht. Dieses wird nur angewendet, wenn der Nebenvertragsarbeitsgang der letzte Arbeitsgang im FA-Arbeitsplan ist.  

> [!CAUTION]  
>  Automatisches Buchen von Ausgaben für einen aktuellen Fertigungsauftrag, wenn Fremdartikel eingehen, wird nicht erforderlich sein. Gründe für dieses könnten sein, dass die voraussichtlich fertig gestellte Menge, die gebucht wurde, sich von der tatsächlichen Menge unterscheidet und dass das Buchungsdatum der automatischen Istmeldung möglicherweise irreführend ist.  
>   
>  Damit nicht die erwartete Menge eines Fertigungsauftrags gebucht wird, wenn Fremdarbeitsbestellungen eingehen, vergewissern Sie sich, dass der vergebene Arbeitsgang nicht der letzte Arbeitsgang ist. Alternativ können Sie einen neuen letzten Arbeitsgang für die endgültig fertig gestellte Menge eingeben.

## <a name="to-post-a-subcontract-purchase-order"></a>So buchen Sie eine Fremdarbeitsbestellung  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Aufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Öffnen Sie eine Einkaufsbestellung, die über den Fremdarbeitenvorschlag erstellt wurde.  

    In den Einkaufsbestellungszeilen werden dieselben Informationen angezeigt, die im Arbeitsblatt enthalten waren. Die **Fertigungsauftrag Auftragsnr.**, **Fertigungsauftrag Auftragszeilennr.**, **Arbeitsgangnr.** und **Arbeitsplatzgruppennr.** Felder werden mit den Informationen aus dem ursprünglichen Fertigungsauftrag ausgefüllt.  

3.  Wählen Sie die Aktion **Buchen** aus.  

Wenn der Einkauf als eingegangen gebucht wird, wird automatisch ein Istmeldungs-Erfassungsjournalzeilenposten für den Produktionsauftrag gebucht. Dieses wird nur angewendet, wenn der Nebenvertragsarbeitsgang der letzte Arbeitsgang im FA-Arbeitsplan ist.  

> [!CAUTION]  
>  Automatisches Buchen von Ausgaben für einen aktuellen Fertigungsauftrag, wenn Fremdartikel eingehen, wird nicht erforderlich sein. Gründe für dieses könnten sein, dass die voraussichtlich fertig gestellte Menge, die gebucht wurde, sich von der tatsächlichen Menge unterscheidet und dass das Buchungsdatum der automatischen Istmeldung möglicherweise irreführend ist.  
>   
>  Damit nicht die erwartete Menge eines Fertigungsauftrags gebucht wird, wenn Fremdarbeitsbestellungen eingehen, vergewissern Sie sich, dass der vergebene Arbeitsgang nicht der letzte Arbeitsgang ist. Alternativ können Sie einen neuen letzten Arbeitsgang für die endgültig fertig gestellte Menge eingeben.  

Wenn die Einkaufsbestellung als fakturiert gebucht wird, wird der EK-Preis der Einkaufsbestellung auf die Produktion gebucht.  

## <a name="see-also"></a>Siehe auch  
[Bearbeitungen](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbesttand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

