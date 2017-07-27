---
title: "Überblick der Aufgaben zum Verwalten von Einkauf | Microsoft Docs"
description: "Zeigt die Aufgaben zum Verwalten der Einkaufs- oder Beschaffungsvorgänge, einschließlich das Vorgehen bei Einkaufsrechnungen und Bestellungen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 653cd9b5e9651f2039ab18f3e7a26b299238d817
ms.contentlocale: de-ch
ms.lasthandoff: 07/07/2017


---
# <a name="purchasing"></a>Einkauf
Sie erstellen eine Einkaufsrechnung oder Einkaufsbestellung, um die Kosten der Einkäufe zu erfassen und Kreditoren zu verfolgen. Wenn Sie einen Bestand steuern müssen, werden Einkaufsrechnungen auch verwendet, um Lagerbestände dynamisch zu aktualisieren, sodass Sie Ihre Lagerbestandskosten minimieren und besseren Kundenservice bereitstellen können. Die Einkaufskosten, einschließlich Servicekosten und Bestandswerte, die aus der Buchung von Einkaufsrechnungen resultieren, tragen zu den Gewinnzahlen und anderen finanziellen Kennziffern auf Ihrer Startseite bei.

Sie müssen Einkaufsbestellungen verwenden, wenn es für den Einkaufsprozess erforderlich ist, Teillieferungen einer Bestellmenge zu erfassen, weil beispielsweise die vollständige Menge beim Kreditor nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Einkaufsbestellungen verwenden. Weitere Informationen finden Sie unter [So geht's: Direktlieferungen erstellen](sales-how-drop-shipment.md) In allen anderen Aspekten ist das Vorgehen bei Einkaufsbestellungen genau wie bei Einkaufsrechnungen.

Sie können Verkaufsrechnungen automatisch erstellen lassen, indem Sie den OCR-Dienst (optische Zeichenerkennung) verwenden, um PDF-Rechnungen Ihrer Kreditoren zu elektronischen Belegen umwandeln, die dann zu Einkaufsrechnungen durch einen Workflow umgewandelt werden. Um diese Funktionalität nutzen zu können, müssen Sie den OCR-Service zuerst anmelden und dann verschiedene Einrichtungen ausführen. Weitere Informationen finden Sie unter [So gehts: Eingehende Belege verarbeiten](across-process-income-documents.md).      

Produkte können Lagerartikel und Dienstleistungen sein. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten neuer Artikel](inventory-how-register-new-items.md).

Für alle Einkaufsprozesse können Sie einen Genehmigungsworkflows einfügen, beispielsweise um große Einkäufe an bestimmten Kreditoren vom Buchhaltungs-Manager zu genehmigen. Weitere Informationen erhalten Sie unter [Genehmigungsworkflow verwenden](across-how-use-approval-workflows.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert. Diese Aufgaben sind in der Reihenfolge aufgeführt, in der sie normalerweise ausgeführt werden.

| Aktion | Informationen |
| --- | --- |
| Erstellen Sie eine Einkaufsrechnung, um Ihre Vereinbarung mit dem Kreditor zu erfassen, bestimmte Produkte unter speziellen Lieferungs- und Zahlungsbedingungen zu kaufen. |[Vorgehensweise: Erfassen eines Einkaufs](purchasing-how-record-purchases.md) |
| Erstellen Sie eine Einkaufsrechnung für alle oder die ausgewählten Zeilen auf einer Verkaufsrechnung. |[Vorgehensweise: Einkauf von Produkten für einen Verkauf](purchasing-how-purchase-products-sale.md) |
| Aktionen ausführen in einer unbezahlten gebuchten Einkaufsrechnung, um einen Gutschriftsprozess automatisch zu erstellen, und entweder die Einkaufsrechnung zu stornieren oder neu zu erstellen um Korrekturen vorzunehmen. |[Vorgehensweise: Ändern oder Löschen einer unbezahlten Verkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Erstellen Sie eine Einkaufsgutschrift, um eine bestimmte gebuchte Einkaufsrechnung wiederherzustellen, um anzugeben, welche Produkte Sie an den Kreditor zurückliefern und welchen Zahlungsbetrag Sie eintreiben. |[Vorgehensweise: Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen](purchasing-how-register-new-vendors.md)V |
| Erstellen Sie eine Kreditorenkarte für jeden Kreditor, von dem Sie einkaufen. |[Vorgehensweise: Einen neuen Kreditor registrieren](purchasing-how-register-new-vendors.md) |

## <a name="see-also"></a>Siehe auch
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Projekte verwalten](projects-manage-projects.md)    
[Lieferkette](madeira-supply-chain.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
