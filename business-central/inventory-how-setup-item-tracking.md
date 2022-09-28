---
title: Artikeltracking mit Serien-, Chargen- und Paketnummern einrichten
description: Artikeltracking mit Seriennummern, Chargennummern und Paketnummern einrichten
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/31/2021
ms.author: edupont
ms.openlocfilehash: c298903d62da4cfd346a46ff1978ab91644fb13f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533282"
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers"></a>Artikeltracking mit Serien-, Chargen- und Paketnummern einrichten

Behalten Sie den Überblick über Lagerartikel auch in komplexen Lagerkonfigurationen mit Nummern, die für jeden Artikel spezifisch sind, entweder als einzelnes Objekt, als Charge oder als Paket. Mit dem Artikeltracking können Sie Artikel über interne Lagerbewegungen sowie ausgehende und eingehende Belege verfolgen.

Gibt gebuchte Serien- und Chargennummern an, die in einer Lieferkette vorwärts oder rückwärts verfolgt werden können. Dies ist für allgemeine Massnahmen für die Qualitätssicherung und für Rückrufe eines fehlerhaften Produktes nützlich. Weitere Informationen finden Sie unter [Nachverfolgte Artikel reservieren](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> Schalten Sie im 1. Veröffentlichungszyklus 2021 und später die Funktionsaktualisierung *Verwenden Sie das Tracking nach Paketnummer im Reservierungs‑ und Trackingsystem* ein, wenn Sie mit Paketnummern sowie Serien‑ und Chargennummern arbeiten möchten. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](admin-feature-management.md). Sobald die Funktion aktiviert ist, können Sie ausgehenden und eingehenden Belegen Paketnummern zuweisen, ähnlich wie Sie mit Chargennummern arbeiten können.  

## <a name="numbers-and-item-tracking"></a>Zahlen‑ und Artikeltracking

Im Rahmen Ihrer Lagerprozesse können Sie Ihren Lagerbestand in Paketen, Kartons, Containern usw. bündeln. Um den Überblick über die Artikel zu behalten, weisen Sie eindeutige Nummern als Identifikation zu. Sie stellen beispielsweise einen Stuhl mit der Artikelnummer *1900-S* her und verkaufen ihn. Jeder einzelne Stuhl hat eine Seriennummer, *1001*, aber Sie bündeln auch vier Stühle zu einer Charge, *LOT0001*, und Sie versenden die Stühle in einem Container mit der Paketnummer *CONTAINER010*. Das schliesst auch andere Elemente ein, wie z. B. *LOT0100* mit Beistelltischen und *LOT200* mit Lampen.  

Abhängig von Ihrer Konfiguration verwenden Sie diese unterschiedlichen Nummern, um den Lagerbestand in [!INCLUDE [prod_short](includes/prod_short.md)] in den verschiedenen Phasen des Einkaufs, Verkaufs, Lagerbetriebs usw. zu verfolgen.

## <a name="to-set-up-item-tracking-codes"></a>Um Artikelverfolgungscodes einzurichten

Ein Artikeltrackingcode spiegelt die unterschiedlichen Betrachtungen wider, die ein Unternehmen bezüglich der Verwendung von Serien- und Chargennummern von Artikeln anstellt, die sich durch das Lager bewegen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Artikeltrackingen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. In den Inforegistern **Seriennr.**, **Chargennr.**, und der **Paketnr.** Definieren Sie die Vorgehensweisen zum Artikeltracking nach Serien-, Chargen‑ und Paketnummern.  

> [!NOTE]  
> Wenn Sie bestimmte Artikel oder bestimmte Chargen während der Lebensdauer verfolgen möchten, müssen Sie die Felder **Seriennr.-spezifische Verf.** und **Chargennr.-spezifische Verf.** auswählen. Wenn Sie eine ausgehende Einheit eines Artikels mit dem Artikeltrackingcode verarbeiten, müssen Sie immer angeben, welche vorhandene Seriennummer oder welche vorhandene Chargennummer betroffen sein soll. Das bedeutet, dass der Artikel, von dem eine gewissen Menge verkauft wird, aus einem bestimmten Bereich von Seriennummern im Lagerbestand entnommen werden muss. Mit anderen Worten: die Seriennummer, die einem Artikel beim Wareneingang zugewiesen wurde, muss genau derjenigen beim Warenausgang entsprechen.

Da dieses Einrichtungsfeld alle möglichen Transaktionen für den Artikel abdeckt, werden die einzelnen Felder für Eingang und Ausgang ebenfalls mit Häkchen versehen. Die einzelnen Eingangs- und Ausgangsfelder haben aber nichts mit dem Ausgleich innerhalb des Lagers zu tun – sondern sie haben lediglich die Aufgabe, den Arbeitsablauf eines Unternehmens bezüglich der Zuweisung von Artikeltrackingnummern abzubilden.  

> [!NOTE]  
>  Um Artikeltrackingnummern bei Lageraktivitäten zuzuordnen, müssen die Felder **Seriennr.-Verf. Lager** und **Chargennr.-Verf. Lager** auf der Karte des Artikels ausgewählt werden.  

## <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Regeln für den Ablauf von Serien- oder Chargennummern einrichten:

Für einige Artikel möchten Sie möglicherweise spezielle Ablaufdaten und Regeln in dem Artikeltrackingcode festlegen. Diese Funktionalität ermöglicht Ihnen nachzuvollziehen, wann bestimmte Serien- und Chargennummern ablaufen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Artikeltrackingen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie einen bestehenden Artikeltrackingcode aus bestehenden Artikelkarten aus, und wählen Sie die Aktion **Bearbeiten**.  
3. Aktivieren Sie im Inforegister **Sonst.** die folgenden Felder:  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Fixes Ablaufdatum**|Gibt an, dass ein Ablaufdatum, das der Artikeltrackingsnummer beim Wareneingang zugewiesen wurde, beim Warenausgang berücksichtigt werden muss.|  
    |**Ablaufdatumseintrag anfordern**|Gibt an, dass Sie in der Artikeltrackingzeile ein Ablaufdatum eingeben müssen.|  
    |**Ablaufdatumsangaben verwenden**|Gibt an, dass Sie keine Ablaufdatumsangaben berechnen möchten. |  

## <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Garantien für Serien- oder Chargennummern einrichten:

Für einige Artikel möchten Sie möglicherweise spezielle Garantievereinbarungen in dem Artikeltrackingcode festlegen. Diese Funktionalität ermöglicht Ihnen nachzuvollziehen, wann die Garantien auf spezielle Serien- oder Chargennummern in Ihrem Lager auslaufen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Artikeltrackingen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie einen bestehenden Artikeltrackingcode aus bestehenden Artikelkarten aus, und wählen Sie die Aktion **Bearbeiten**.  
3. Füllen Sie im Inforegister **Sonstiges** das Feld **Garantiedatumsformel** aus, und markieren Sie die Felder wie folgt:  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Garantiedatumsformel**|Gibt das letzte Garantiedatum für den Artikel an.|  
    |**Garantiedatumseintrag anfordern**|Zeigt an, dass Sie in der Artikeltrackingzeile manuell ein Garantiedatum eingeben müssen.|  


## <a name="to-set-up-items-for-tracking-with-the-correct-item-tracking-codes"></a>So richten Sie Artikel für die Tracking mit den richtigen Artikeltrackingcodes ein

Um das Artikeltracking zu aktivieren, müssen Sie einem Artikel zunächst die Artikeltrackingcodes zuweisen. Es gibt zwei Möglichkeiten, Artikeltrackingcodes hinzuzufügen, indem Sie den Code aus einer vordefinierten Liste auswählen oder einen neuen eindeutigen Code zuweisen. Zeigen Sie mit der Maus auf die Felder, um eine Kurzbeschreibung zu lesen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Element** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie einen vorhandenen Artikel aus der Liste aus, und öffnen Sie die Seite **Artikelkarte**.  
3. Weisen Sie im Inforegister **Artikeltracking** die entsprechenden Artikeltrackingcodes zu, und wählen Sie den **Artikeltrackingcode**, die **Seriennummern** und die **Chargennummern** aus.
    1. Alternativ können Sie auch einen neuen Artikeltrackingcode erstellen, indem Sie die Aktion **Neu** auswählen.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/prepare-item-tracking/)

## <a name="see-also"></a>Siehe auch 

[Arbeiten mit Chargennummern und Seriennummern](inventory-how-work-item-tracking.md)  
[Verfolgen von Artikeln mit Artikelverfolgung](inventory-how-to-trace-item-tracked-items.md)  
[Bestand](inventory-manage-inventory.md)  
[Designdetails: Artikeltracking](design-details-item-tracking.md)  
[Designdetails: Artikeltracking und Reservierungen](design-details-item-tracking-and-reservations.md)  
[Artikel reservieren](inventory-how-to-reserve-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
