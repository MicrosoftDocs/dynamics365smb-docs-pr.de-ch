---
title: "Einrichten von Serviceverträgen | Microsoft Docs"
description: "Vorgehensweise: Einrichten von Serviceverträgen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 954438a19ed4b7aadc707cbb5e646f1752aa37a0
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-service-contracts"></a>Serviceverträge einrichten
Um mit Verträgen arbeiten zu können, müssen Sie Folgendes einrichten: 

* Die Tabelle **Servicevertragsgruppe** enthält eine Gruppe von Serviceverträgen, die miteinander in Verbindung stehen.
* Sie können **Servicevertragskontengruppen** verwenden, um Serviceverträge zu gruppieren. Diese Gruppen können dann für die Servicerechnungen von Serviceverträgen verwendet werden. Sie können diese Gruppen anschliessend Ihren Serviceverträgen zuordnen.  
* Sie können **Vertragsvorlagen** als eine vordefinierte Grundlage für Serviceverträge verwenden, die die gängigsten Servicevertragsdetails enthält. Wenn Sie Servicevertragsofferten erstellen, können Sie diese unter Verwendung dieser Vorlagen erstellen. Wenn Sie eine neue Vertragsofferte erstellen, enthalten die Felder automatisch den Inhalt der Vorlagenfelder.
* **Debitorenvorlagen**, mit denen Sie Offerten für Kontakte oder potenzielle Kunden erstellen können, die nicht als Debitoren in [!INCLUDE[d365fin](includes/d365fin_md.md)] registriert sind.  

## <a name="to-set-up-a-service-contract-group"></a>So richten Sie Servicevertragsgruppen ein  
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Servicevertragsgruppe** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Aktivieren Sie das Feld **Rabatt nur auf Vertr.-Aufträge**, wenn Vertrags- oder Servicerabatte nur für Vertragsaufträge, wie z. B. Wartung, gültig sein sollen.  

## <a name="to-set-up-a-service-contract-account-group"></a>So richten Sie eine Servicevertragskontengruppe ein  
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Servicevertragsgruppe** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Erstellen Sie eine neue Servicevertragskontengruppe.   
3. Füllen Sie die Felder **Code** und **Beschreibung** aus. Diese Felder beschreiben die Servicekontengruppe.  
4. Füllen Sie das Feld **Nicht vorausbez. Vertragskonto** aus. Dieses Feld enthält die Fibukontennummer des Kontos, auf das nicht vorausbezahlte Beträge gebucht werden.  
5. Füllen Sie das Feld **Vorausbez. Vertragskonto** aus. Dieses Feld enthält die Fibukontennummer des Kontos, auf das nicht vorausbezahlte Beträge gebucht werden.  

## <a name="to-set-up-a-contract-template"></a>So richten Sie Vertragsvorlagen ein  
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Servicevertragsgruppe** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Erstellen Sie eine neue Servicevertragsvorlage.  
3. Geben Sie im Feld **Nr.** eine Nummer für die Vertagsvorlage ein.  
  
     Wenn Sie Nummernserien für Vertragsvorlagen im Fenster **Service Einrichtung** definiert haben, drücken Sie die EINGABETASTE, damit die nächste verfügbare Vertragsvorlagennummer eingefügt wird. Füllen Sie die anderen Felder aus, falls diese benötigt werden.  
  
4. Füllen Sie im Inforegister **Rechnung** das Feld **Servicevertragskonto-Gruppencode** aus und geben Sie das **Fakturierungsintervall** usw. an. Füllen Sie die anderen Felder aus, falls diese benötigt werden.  
5. Wählen Sie die **Servicerabatte** Aktion aus, um Vertragsrabatte hinzuzufügen.  

## <a name="to-set-up-a-customer-template"></a>So richten Sie Debitorenvorlagen ein  
1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Kundenvorlage** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Erstellen Sie eine neue Debitorenvorlagenkarte.  
3. Geben Sie auf dem Inforegister **Allgemein** der Debitorenvorlagenkarte im Feld **Code** einen Code und im Feld **Beschreibung** eine Beschreibung für die Debitorenvorlage ein. 
4. Die anderen Felder, z. B. **Länder-/Regionscode**, **Gebietscode** und **Sprachcode**, werden als Suchkriterien verwendet und können ausgefüllt werden.  
5. Die Felder  **Geschäftsbuchungsgruppe** und  **Debitorenbuchungsgruppe** müssen ausgefüllt werden.  

## <a name="see-also"></a>Siehe auch
[Einrichten der Serviceverwaltung](service-setup-service.md)
