---
title: 'Schweizer Finanzbuchhaltungskonten [CH]'
description: In diesem Artikel werden Verbesserungen an den Schweizer Fibukonten und Fibu-Erfassungsjournalen erläutert.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 11500
ms.date: 06/21/2021
ms.author: edupont
---
# Finanzbuchhaltungskonten (Schweiz)
[!INCLUDE[prod_short](../../includes/prod_short.md)] enthält Schweizer Erweiterungen für Fibuposten.

- Verwalten der Fremdwährungssalden eines Bankkontos in der Finanzbuchhaltung  
- Sortieren Sie Finanzbuchhaltungs-Kontonummern auf der Seite **Kontenplan**.  
- Anzeigen einer Vorschau, mit deren Hilfe die Auswirkungen von Finanzbuchhaltungs-Erfassungsjournalbuchungen auf die Salden bestimmter Finanzbuchhaltungskonten vor der eigentlichen Buchung überprüft werden können  

## Finanzbuchhaltungskonten und Finanzbuchhaltungs-Erfassungsjournale  
Unternehmen arbeiten häufig mit unterschiedlichen Bankkonten für Fremdwährungen und verwenden für jedes Bankkonto ein Finanzbuchhaltungskonto. In [!INCLUDE[prod_short](../../includes/prod_short.md)] können Sie Fremdwährungssaldoinformationen und Währungscodes und auf der Seite **Kontenplan** einrichten. Auf diese Weise kann der ursprüngliche Fremdwährungssaldo eines Bankkontos verwaltet werden. Weitere Informationen finden Sie unter [Verständnis des Fibupostens und des COA](../../finance-general-ledger.md).  

Angenommen, ein Unternehmen verfügt über zwei Bankkonten: eines für Landes- bzw. Mandantenwährung (MW) und eines für Euro (EUR). Sie müssen ein Finanzbuchhaltungskonto für jedes Bankkonto erstellen. Für das EUR-Konto definieren Sie den Währungscode **EUR** und buchen Erfassungsjournale in EUR oder MW.  

Wenn sich der Wechselkurs für EUR und MW ändert, können Sie den Landeswährungssaldo für das EUR-Finanzbuchhaltungskonto mit dem Stapelverarbeitungsauftrag "Wechselkurse regulieren" aktualisieren und anpassen. Bei dieser Stapelverarbeitung werden Währungsregulierungsposten in der Finanzbuchhaltung erstellt und gebucht, und der MW-Saldo wird aktualisiert.  

## Datentyp für Finanzbuchhaltungskonten  
Der Datentyp ist in der Fibupostennummer auf Text oder Kontocode festgelegt, um die Sortierungsanforderungen für den standardisierten Kontenplan von kleinen und mittleren Unternehmen (KMU) zu unterstützen. Die Kontonummernliste ist basierend auf dem Datentyp "Text" sortiert. Der KMU-Kontenplan enthält die folgenden Kontonummern:  

- 1176  
- 119.0  
- 1190  

## Anzeigen temporärer Salden in Finanzbuchhaltungs-Erfassungsjournalen  
Bevor Sie ein Finanzbuchhaltungs-Erfassungsjournal buchen, können Sie eine Vorschau anzeigen, die Aufschluss gibt über die Auswirkungen dieser Buchung auf die Salden bestimmter Finanzbuchhaltungskonten. Sie können eine Statistikseite, die die Salden der Konten anzeigt, und die Salden der aktiven Zeilen öffnen, die ungebuchte Werte für das aktuelle Erf.-Journal umfassten. Weitere Informationen finden Sie unter [Anzeigen temporärer Salden in Finanzbuchhaltungs-Erfassungsjournalen](how-to-view-temporary-balances-in-general-ledger-journals.md).  

## Siehe auch

[Anzeigen temporärer Salden in Finanzbuchhaltungs-Erfassungsjournalen](how-to-view-temporary-balances-in-general-ledger-journals.md)  
[Lokale Funktion (Schweiz)](switzerland-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]