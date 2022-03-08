---
title: Gebuchte Einkaufs- und Verkaufsbelege bearbeiten | Microsoft Docs
description: Erfahren Sie mehr über die verschiedenen Buchungsfunktionen zum Buchen von Einkaufsbelegen und wie Sie gebuchte Belege aktualisieren können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6fbb4e458b0e4f9068b234748a3921dbca6b3222
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300607"
---
# <a name="edit-posted-documents"></a>Gebuchte Belege bearbeiten
Manchmal müssen Sie einen gebuchten Beleg aktualisieren, da sich die für den Beleg relevanten Informationen geändert haben. Bei einem gebuchten Verkaufsbeleg kann dies beispielsweise die Paketverfolgungsnummer des Spediteurs sein. Bei einem gebuchten Einkaufsbeleg kann es sich um einen Zahlungsreferenztext handeln.

Sie führen die Änderung an einer bearbeitbaren Version des Originalbelegs durch, was durch „**- Update**“ im Seitentitel angegeben wird. Die Seite enthält eine Teilmenge der Felder im Originalbeleg, von denen einige nicht bearbeitbare Felder sind, die nur zu Informationszwecken angezeigt werden.

Die Funktionalität ist für folgende Belege in allen Länderversionen verfügbar:
- Geb. Verkaufslieferung
- Geb. Einkaufsrechnung
- Gebuchte Rücklieferung
- Gebuchte Rücksendung

Die folgenden zusätzlichen Belege können in ausgewählten Länderversionen bearbeitet werden:
- ES: Gebuchte Verkaufsrechnung, Geb. Verkaufsgutschrift, Gebuchte Einkaufsgutschrift
- APAC: Geb. Verkaufsgutschrift, Gebuchte Einkaufsgutschrift
- RU: Geb. Verkaufsgutschrift
- IT: Geb. Umlag.-Ausgang, Gebuchte Servicelieferung

## <a name="to-edit-a-posted-sales-shipment"></a>So bearbeiten Sie eine gebuchte Verkaufslieferung
Im Folgenden wird erläutert, wie Sie eine gebuchte Verkaufslieferung bearbeiten. Die Schritte sind für die anderen unterstützten Belege ähnlich.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Gebuchte Warenversände** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie den zu bearbeitenden Beleg aus, und wählen Sie anschliessend die Aktion **Beleg aktualisieren** aus. Alternativ können Sie den Beleg öffnen und dann die Aktion auswählen.
3. Auf der Seite **Gebuchte Verkaufslieferungen - Update** bearbeiten Sie das Feld **Pakettrackingnr.** zum Beispiel.
4. Wählen Sie die Schaltfläche **OK** aus.

Die gebuchte Verkaufslieferung wird aktualisiert.

## <a name="see-also"></a>Siehe auch
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Journale und Belege buchen](ui-post-documents-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
