---
title: Lagerverwaltung [CH]
description: In diesem Artikel werden die Schweizer Erweiterungen der speziellen Lagerverwaltungsfunktionen in Business Central beschrieben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/21/2021
ms.author: edupont
ms.openlocfilehash: 8986455ccbab0adc26a17605fdb7f4889732d950
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 06/30/2021
ms.locfileid: "6319302"
---
# <a name="swiss-inventory-management"></a>Lagerverwaltung (Schweiz)
[!INCLUDE[prod_short](../../includes/prod_short.md)] enthält Schweizer Erweiterungen für Lagerverwaltung. Dies beinhaltet Folgendes:  

- Detaillierte Berichte.  Weitere Informationen finden Sie unter Verkaufstatistikbericht und Lagerlistenbericht.  
- Die Fähigkeit, eine Rechnung mit mehreren Lieferungen nachzuverfolgen.  
- Einschliessen eines Artikelkarten-Lagerortcodes als Standardlagerortcode für Verkaufszeilen und Artikelerfassungsjournale. Weitere Informationen finden Sie unter [Einrichten von Lagerorten](../../inventory-how-setup-locations.md).

## <a name="managing-item-details"></a>Verwalten von Artikeldetails  
Unternehmen haben u. U. verschiedene Lager für verschiedene Produktkategorien. In diesem Fall muss der von der Artikelkarte abgerufene Standardlagerortcode verwendet werden. Wenn Sie einen Lagerortcode für einen Artikel definieren, wird dieser auf die Verkaufszeilen und Artikelerfassungsjournale als Standardlagerortcode übertragen. Weitere Informationen finden Sie unter Verkaufszeile und Artikel Erf.-Journalzeile.  

Zusätzliche Informationen, wie Debitorennummer, Lieferadresscode und Debitorenvertriebsmitarbeitercode wird in Lagerposten gespeichert. Diese Informationen sollen dabei helfen, benutzerdefinierte Berichterstellungskriterien wie Einnahmen pro Debitor zu erstellen und Artikel oder Debitoren für Verkäufer bereitzustellen. Weitere Informationen erhalten Sie in der Tabelle "Lagerposten".  

## <a name="invoices-with-multiple-shipments"></a>Rechnungen mit mehreren Lieferungen  
Sind mehrere Lieferungen für einen Debitoren gebucht worden, können Sie Sammelrechnungen mit der Funktion **Lieferzeilen abrufen** erstellen. Weitere Informationen finden Sie auf der Seite „Versandzeilen abrufen“. Wenn Sie diese Funktion verwenden, enthält der Text, der in den Rechnungszeilen erstellt wird, die Informationen über die Nummer der Auslieferung und das Lieferdatum. Beispielsweise kann der Text als Lieferungsnummer erscheinen. 102040 von 25.01.01. Auf diese Weise können Sie Rechnungen mit mehreren Lieferungen verfolgen.  

## <a name="see-also"></a>Siehe auch  
 [Lokale Funktion (Schweiz)](switzerland-local-functionality.md)   
 [Einrichten von Lagerorten](../../inventory-how-setup-locations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]