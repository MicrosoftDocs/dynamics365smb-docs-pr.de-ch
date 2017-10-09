---
title: "Mehrere Verträge | Microsoft Docs"
description: "Abhängig von den Servicelevelvereinbarungen mit dem Kunden, kann es sein, dass Sie einen Serviceartikel in mehr als einem Servicevertrag berücksichtigen müssen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c4abfbcb3bc182fa14c44c427bc41ebd9d67f6cf
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="multiple-contracts"></a>Mehrere Verträge
Abhängig von den Servicelevelvereinbarungen mit dem Kunden, kann es sein, dass Sie einen Serviceartikel in mehr als einem Servicevertrag berücksichtigen müssen.  
  
Wenn Sie einen Serviceartikel in mehreren Serviceverträgen berücksichtigen, können Sie folgendermassen vorgehen:  
  
* Verschiedene Verträge für denselben Serviceartikel ausstellen.  
* Separaten Service für Teile leisten.  
* Berücksichtigen, dass verschiedene Teile des Serviceartikels, wie z. B. mechanische Komponenten und Software, unterschiedliche Qualifikationen für die Serviceerbringung benötigen.  
* Verschiedene Reaktionszeiten und Serviceintervalle für verschiedene Teile des Serviceartikels vereinbaren.  
* Verschiedene Serviceleistungen berücksichtigen, die an einem Serviceartikel ausgeführt werden müssen, wenn dieser verschiedene Arten von Serviceleistungen in verschiedenen Zeitintervallen benötigt.  
* Einer Serviceartikelzeile eine geeignete Vertragsnummer zuordnen, wenn Sie einen Servicevertrag erstellen.  
* Relevante Finanzdaten zu Serviceartikeln und Servicelevelvereinbarungen verwalten.  
  
Die folgenden Beispiele zeigen den Verwendungszweck der Funktionalität "Mehrere Verträge".  
  
## <a name="creating-multiple-contracts-per-service-item"></a>Erstellen von mehreren Verträgen pro Serviceartikel  
Sie können manuell einen Servicevertrag oder eine Servicevertragsofferte für Serviceartikel erstellen, die bereits in ungekündigten Verträgen mit demselben Kunden enthalten sind. Wenden Sie dazu die Standardvorgehensweise zur Erstellung eines Servicevertrags oder einer Servicevertragsofferte an. Weitere Informationen finden Sie unter [Vorgehensweise: Arbeiten mit Serviceverträgen und Servicevertragsofferten](service-how-to-create-service-contracts-and-service-contract-quotes.md).  
  
Wenn Sie einen Serviceartikel einer Vertragszeile hinzufügen, der bereits in einem anderen Servicevertrag oder einem anderen Servicevertragsangebot enthalten ist, erscheint eine Warnung, dass der Serviceartikel bereits zu einem oder mehreren Serviceverträgen oder Vertragsangeboten gehört. Wenn Sie diese Warnung bestätigen, werden alle entsprechenden Serviceartikeldaten in eine neue Servicevertragszeile kopiert.  
  
## <a name="copying-documents"></a>Belege kopieren  
Sie können einen Servicevertrag oder eine Vertragsofferte für einen Serviceartikel automatisch erstellen, der bereits in einem anderen Servicevertrag oder einer Vertragsofferte enthalten ist, indem Sie die Funktion **Beleg kopieren** verwenden.  
  
## <a name="creating-service-orders-for-multiple-contracts"></a>Erstellen von Serviceaufträgen für mehrere Verträge  
Sie können manuell einen Serviceauftrag für einen Serviceartikel, der in mehreren aktiven Verträgen hinterlegt ist, erstellen. Ein Servicevertrag ist aktiv, wenn er unterzeichnet und nicht abgelaufen ist.  
  
## <a name="see-also"></a>Siehe auch  
[Erfüllen von Serviceverträgen](service-fulfill-service-contracts.md)  
[Vorgehensweise: Erstellen von Serviceaufträgen](service-how-to-create-service-orders.md)  

