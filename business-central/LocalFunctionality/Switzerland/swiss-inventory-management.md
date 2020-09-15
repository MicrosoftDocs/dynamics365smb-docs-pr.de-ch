---
title: Lagerverwaltung (Schweiz)
description: Schweizer Erweiterungen enthalten spezielle Lagerverwaltungsfunktionen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 31aead817f0bfc034744f4932b9b16b88066ac13
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778166"
---
# <a name="swiss-inventory-management"></a>Lagerverwaltung (Schweiz)
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] enthält Schweizer Erweiterungen für Lagerverwaltung. Dies beinhaltet Folgendes:  

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
