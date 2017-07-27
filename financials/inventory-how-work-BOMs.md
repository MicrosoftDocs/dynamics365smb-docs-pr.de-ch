---
title: "Vorgehensweise: Arbeiten mit Stücklisten| Microsoft Docs"
description: "Sie erstellen eine Montagestückliste, um die Komponenten und Ressourcen an, die benötigt werden, um den Artikel zusammenzufügen, den die Montagestückliste darstellt, und die Komponenten eines Montageartikels an."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: de-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-bills-of-material"></a>Vorgehensweise: Arbeiten mit Stücklisten
> [!NOTE]  
>   Die aktuelle Version aus [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält nur den ersten Teil der Montageverwaltungsfunktion. Für den Moment können Sie nur Montagestücklisten erstellen und die zugehörigen übergeordneten Artikel als normale Artikel dann bearbeiten. In einem zukünftigen Update können Sie die tatsächliche Montage von Artikeln von den Komponenten, entweder im Lagermontage- als auch in Auftragsmontageprozessen verwenden und Sie können Komponenten als Kit verkaufen.

Sie verwenden Stücklisten (BOMs), um übergeordnete Artikel zu strukturieren, die Sie als Sets verkaufen, die aus den Komponenten des übergeordneten Artikels bestehen oder für die Sie die Auftragsmontage oder das Lager haben.

In [!INCLUDE[d365fin](includes/d365fin_md.md)], bezeichnet eine Stückliste eine "Montagestückliste". Die Montagestückliste gibt an, welche Komponentenartikel im übergeordneten Artikel enthalten sind. In dieser Dokumentation wird ein übergeordneter Artikel als "ein Montageartikel" bezeichnet.

Montagestücklisten enthalten normalerweise Artikel, können jedoch auch eine oder mehrere Ressourcen enthalten, die die Montageartikel ausführen.

Montagestücklisten können mehrstufig sein, was bedeutet, dass eine Komponente in der Montagestückliste selbst ein Montageartikel sein kann. In diesem Fall lautet das Feld **Montagestückliste** in der Montagestücklistenzeile **Ja**.

Spezielle Anforderungen gelten für Artikel auf Montagestücklisten in Bezug auf die Verfügbarkeit. Weitere Informationen finden Sie im Abschnitt "Verfügbarkeit eines Artikels nach dessen Verwendung in den Montagestücklisten anzeigen [Vorgehensweise: Verschaffen Sie sich eine Übersicht zur Verfügbarkeit](inventory-how-availability-overview.md)".

> [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer Financials Experience](ui-experiences.md).

## <a name="to-create-an-assembly-bom"></a>So erstellen Sie eine Montagestückliste
Um einen übergeordneten Artikel zu definieren, der aus anderen Artikeln und möglicherweise Ressourcen besteht die benötigt werden, um die übergeordnete Baugruppe zusammenzufügen, müssen Sie eine Montagestückliste erstellen.  

Es gibt zwei Schritte zum Erstellen einer Montagestückliste:
- Einrichten einer neuen Artikelkarte
- Gibt die Beschreibung des Montageartikels an.

1. Richten Sie einen neuen Artikel ein. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten neuer Artikel](inventory-how-register-new-items.md).

    Fahren Sie fort, um Komponenten oder Ressourcen in der Montagestückliste einzugeben.  
2. Im Fenster **Artikelkarte** für einen Montageartikel wählen Sie die **Montage** Aktion aus, und wählen Sie die **Montagestückliste** Aktion aus.
3. Füllen Sie im Fenster **Montagestückliste** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Um die Komponenten eines Montageartikels anzuzeigen gemäß der Stücklistenstruktur
Im Fenster **Montagestückliste** können Sie ein separates Fenster öffnen, in dem die Komponenten sowie jegliche Ressourcen angezeigt werden, die gemäß ihrer Stücklistenposition unter den Montageartikel eingerückt werden.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie das Kartenfenster für den Montageartikel. (Das Feld **Montagestückliste** im Fenster **Artikel** enthält **Ja**.)
3. Im Fenster **Artikelkarte** für einen Montageartikel wählen Sie die **Montage** Aktion aus, und wählen Sie die **Montagestückliste** Aktion aus.
4. Wählen Sie im Fenster **Montagestückliste** die Aktion **Stückliste anzeigen** aus.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Montageartikel kaufen, verkaufen oder übertragen
Da die aktuelle Version aus [!INCLUDE[d365fin](includes/d365fin_md.md)] nur die Möglichkeit enthält, Montagestücklisten für Artikel festzulegen und zuzuweisen, können Sie Montageartikel in Belegzeilen  nur als Normalpositionen bearbeiten.

**Vorsicht**: Die Komponenten der Lagermenge werden nicht geändert, wenn Sie das tun.

## <a name="see-also"></a>Siehe auch
[Vorgehensweise: Einen neuen Artikel registrieren](inventory-how-register-new-items.md)  
[Vorgehensweise: Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)     
[Lagerbest](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

