---
title: Finanzbuchhaltungskonten (Schweiz)
description: Schweizer Erweiterungen enthalten spezielle Fibupostenfunktionen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 54e1a1c67847704e4ae211249404517cbf40760a
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="swiss-general-ledger-accounts"></a>Finanzbuchhaltungskonten (Schweiz)
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] enthält Schweizer Erweiterungen für Fibuposten.

- Verwalten der Fremdwährungssalden eines Bankkontos in der Finanzbuchhaltung  
- Sortieren von Finanzbuchhaltungs-Kontonummern im Fenster **Kontenplan**  
- Anzeigen einer Vorschau, mit deren Hilfe die Auswirkungen von Finanzbuchhaltungs-Erfassungsjournalbuchungen auf die Salden bestimmter Finanzbuchhaltungskonten vor der eigentlichen Buchung überprüft werden können  

## <a name="general-ledger-accounts-and-general-journals"></a>Finanzbuchhaltungskonten und Finanzbuchhaltungs-Erfassungsjournale  
Unternehmen arbeiten häufig mit unterschiedlichen Bankkonten für Fremdwährungen und verwenden für jedes Bankkonto ein Finanzbuchhaltungskonto. In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], können Sie Fremdwährungssaldoinformationen und Währungscodes und im Fenster **Kontenplan** einrichten. Auf diese Weise kann der ursprüngliche Fremdwährungssaldo eines Bankkontos verwaltet werden. Weitere Informationen finden Sie unter [Kontenplan (Fenster)](assetId:///fa407624-b670-44b6-8397-91aa606e4c39) und [Fibukonto (Tabelle)](assetId:///a65c2b09-9bb2-43db-8c53-c047bfc49777).  

Angenommen, ein Unternehmen verfügt über zwei Bankkonten: eines für Landes- bzw. Mandantenwährung (MW) und eines für Euro (EUR). Sie müssen ein Finanzbuchhaltungskonto für jedes Bankkonto erstellen. Für das EUR-Konto definieren Sie den Währungscode **EUR** und buchen Erfassungsjournale in EUR oder MW.  

Wenn sich der Wechselkurs für EUR und MW ändert, können Sie den Landeswährungssaldo für das EUR-Finanzbuchhaltungskonto mit dem Stapelverarbeitungsauftrag "Wechselkurse regulieren" aktualisieren und anpassen. Bei dieser Stapelverarbeitung werden Währungsregulierungsposten in der Finanzbuchhaltung erstellt und gebucht, und der MW-Saldo wird aktualisiert.  

## <a name="data-type-for-general-ledger-accounts"></a>Datentyp für Finanzbuchhaltungskonten  
Der Datentyp ist in der Fibupostennummer auf Text oder Kontocode festgelegt, um die Sortierungsanforderungen für den standardisierten Kontenplan von kleinen und mittleren Unternehmen (KMU) zu unterstützen. Weitere Informationen finden Sie unter [Kontenplan (Fenster)](assetId:///fa407624-b670-44b6-8397-91aa606e4c39). Die Kontonummernliste ist basierend auf dem Datentyp "Text" sortiert. Der KMU-Kontenplan enthält die folgenden Kontonummern:  

- 1176  
- 119.0  
- 1190  

## <a name="viewing-temporary-balances-in-general-journals"></a>Anzeigen temporärer Salden in Finanzbuchhaltungs-Erfassungsjournalen  
Bevor Sie ein Finanzbuchhaltungs-Erfassungsjournal buchen, können Sie eine Vorschau anzeigen, die Aufschluss gibt über die Auswirkungen dieser Buchung auf die Salden bestimmter Finanzbuchhaltungskonten. Sie können ein Statistikfenster, das die Salden der Konten anzeigt und die Salden der aktiven Zeilen öffnen, die ungebuchte Werte für das aktuelle Erf.-Journal umfassten. Weitere Informationen finden Sie unter [Anzeigen temporärer Salden in Finanzbuchhaltungs-Erfassungsjournalen](how-to-view-temporary-balances-in-general-ledger-journals.md).  

## <a name="see-also"></a>Siehe auch  
 [Anzeigen temporärer Salden in Finanzbuchhaltungs-Erfassungsjournalen](how-to-view-temporary-balances-in-general-ledger-journals.md)   
 [Lokale Funktion (Schweiz)](switzerland-local-functionality.md)

