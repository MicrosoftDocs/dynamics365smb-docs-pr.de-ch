---
title: Artikel-Arten verstehen| Microsoft Docs
description: Sie können die Lagerbewertung eines Artikels anpassen, indem Sie die FIFO. oder " Standard "oder Durchschnittskostenmethode anwenden, z. B. wenn Artikelkosten für Gründe, die keine Transaktionen betreffen, ändern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b08d5a227f2133989948634f32d88aa614941a0f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780099"
---
# <a name="about-item-types"></a>Info zu Elementtypen
Im Feld **Art** auf der Seite **Artikelkarte** können Sie auswählen, welche Artikel in Ihrer Unternehmung verwendet werden und deshalb im System verwaltet werden. Drei Optionen sind verfügbar:

|Option|Typischer Zweck|
|------|-----------|
|Lagerbestand|Eine physikalische Einheit, wie z. B. Rennrad für volle Geschäftsunterstützung.|
|Nicht-Lager|Eine physikalische Einheit, wie ein Bolzen, für begrenzte Geschäftsunterstützung beispielsweise da der Artikel nur intern verwendet wird und Basis Einstandspreis hat.|
|Dienst|Eine Arbeitszeiteinheit, wie eine Beratungsstunde, für begrenzte Geschäftsunterstützung.|

Der **Lagerbestand** umfasst das vollständige Tracking der Lagermenge und des Wertes. Daher werden alle Artikeltransaktionstypen unterstützt, und Artikel der Art Lager können mit allen Artikelbehandlungsfunktionen verwendet werden.

Die Arten **Service** und **Nicht-Lager** umfassen kein Tracking von Lagermengen und Werten. Daher werden nur die ausgewählten Geschäftsarten und Funktionen unterstützt.

Die drei Elementtypen unterstützen die folgenden Funktionen entsprechend.

|Artikelart|Verkauf|Einkauf|Job-Verbrauch|Serviceverbrauch|Verbrauch für Montage|Produktions-Verbrauch|Montageausstoss|Fertig produzierte Artikel (Istmeldungen)|Lagerortumlagerung|Physische Zählung|Lagerbestandsneubewertung|Lagerkosten|Artikeltracking|Reservierung|Lagerhaus|Planung|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lagerbestand|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Nicht-Lager|Ja|Ja|Ja|Ja|Ja|Ja|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nein|Nein|Nein|Nein|
|Dienst|Ja|Ja|Ja|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|

## <a name="costing-methods-for-types-of-items"></a>Kalkulationsmethoden für Artikeltypen
Wenn Sie Lagerbuchungen vornehmen, werden die Mengen- und Wertänderungen des Lagerbestands in den Lagerposten bzw. Wertposten erfasst. 

Für Lagerartikel werden die Kosten im Feld **Einstandsbetrag (tatsächl.)** auf der Seite **Werteinträge** erfasst und bei der Abstimmung mit Fibuposten werden die Kosten im Feld **Gebuchte Lagerregulierung** angezeigt. Weitere Informationen finden Sie unter [Designdetails: Lagerkosten](design-details-inventory-costing.md).

Für Nicht-Bestands- und Serviceartikel werden die Kosten im Feld **Einst.-Betr. (lagerwertunabh.)** auf der Seite **Werteinträge** erfasst. Für Nicht-Bestands- und Serviceartikel werden die Kosten in den Verkaufs-, Montage- und Produktionsbelegen und Erfassungsjournalen angegeben. Die Standardkosten können im Feld **Einstandspreis** auf den Seiten **Artikelkarte** und **Lagerhaltungsdaten** angegeben werden. Die Kosten für diese Arten von Artikeln werden nicht mit Fibuposten abgeglichen. 

## <a name="catalog-and-service-items"></a>Katalog- und Serviceartikel
Sie können Ihren Debitoren bestimmte Artikel als Dienstleistung anbieten, die Sie nicht im Lager verwalten möchten, bis Sie den Verkauf sie starten. Katalogelemente sollen nicht mit regulären Artikel der Art Nicht-Lager verwechselt werden. Weitere Informationen finden Sie unter [Arbeiten mit Katalogelementen](inventory-how-work-nonstock-items.md).

Die Artikel der Debitoren, die Sie im Service, wie z.B Drucker anbieten, werden Serviceartikel genannt. Serviceartikel haben nichts mit regulärem oder Katalogelementen zu tun. Aber Dienstkomponenten können normale Artikel sein. Weitere Informationen finden Sie unter [Serviceartikelkomponenten und Serviceartikel einrichten](service-how-setup-service-items.md).

## <a name="see-also"></a>Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Bestand einrichten](inventory-setup-inventory.md)  
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
