---
title: Erhalten von Informationen zu Fibuposten und COA| Microsoft Docs
description: Beschreibt den Fibuposten, den Kontenplan und die Kontokategorien.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dbeb9f9cbe0eff61b28dc4d371a1f8d9031ea1b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747055"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a>Verständnis des Fibupostens und des COA

Die Fibuposten speichern Ihre Finanzdaten, und der Kontenplan zeigt die Konten, auf die alle Fibuposten gebucht werden, an. [!INCLUDE[prod_short](includes/prod_short.md)]umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finanzbuchhaltung Einrichtung und Buchungsmatrix Einrichtung

Die Einrichtung der Fibuposten ist das Kernstück der Finanzvorgängen, da sie definieren, wie Sie Daten buchen.  

Auf der Seite **Fibuposten einrichten** geben Sie an, wie bestimmte finanzbuchhalterische Sachverhalte in Ihrem Unternehmen gehandhabt werden sollen, wie beispielsweise:  

* Rechnungsrundungskontodetails  
* Adressformate  
* Finanzberichterstellung  

Ebenso geben Sie auf der Seite **Buchungsmatrix Einrichtung** an, wie Sie Kombinationen aus Geschäftsbuchungsgruppen und Produktbuchungsgruppen einrichten wollen. Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Fibukonten. Für jede Kombination aus Geschäftsbuchungsgruppe und Produktbuchungsgruppe geben Sie eine Zeile ein. Weitere Informationen finden Sie unter [Gruppenbuchungen einrichten](finance-posting-groups.md).  

> [!TIP]
> Die Seite **Fibuposten Einrichtung** enthält allgemeine Felder sowie Felder, die für Ihr Land oder Ihre Region spezifisch sind. Wenn Sie nicht sicher sind, welche Bedeutung ein Feld hat, empfehlen wir Ihnen, mit Ihrem Buchhalter zusammenzuarbeiten, um zu ermitteln, ob es für Ihre Organisation relevant ist.  

## <a name="the-chart-of-accounts"></a>Kontenplan

Der Kontenschema zeigt alle Fibukonten an. Vom Kontenplan aus können Sie Dinge tun wie:  

* Berichte ansehen, die die Fibuposten und -Salden zeigen.  
* Erfolgsrechnung-Kontennullstellung.  
* Öffnen der Fibukontokarte, um Einstellungen hinzuzufügen oder zu ändern.  
* Sie können ausserdem eine Liste von Buchungsgruppen anzeigen, die auf dieses Konto buchen.
* Ansicht der Soll- und Habensalden von einzelnen Sachkonten  

Sie können Fibukonten hinzufügen, ändern oder löschen. Um jedoch Differenzen zu verhindern, können Sie ein Fibuposten nicht löschen, wenn Daten im Kontenschema verwendet werden.  

## <a name="account-categories"></a>Kontokategorien

Sie können die Struktur der Finanzberichte personalisieren, indem Sie Fibukonten den Kontenkategorien hinzufügen.  

Die Seite **Fibukontokategorien** zeigt Ihre vorhandenen Haupt- und Unterkategorien und die Fibukonten an, die Sie jeder Kategorie zugeordnet haben. Sie können neue Unterkategorien erstellen und diese bestehenden Konten zuweisen.  

Sie erstellen eine Kategoriengruppe, indem Sie weitere Unterkategorien unter einer Zeile auf der Seite **Fibukontokategorien** einrücken. Dieses erleichtert Ihnen den Überblick, da jede Gruppierung einen Gesamtsaldo anzeigt. Beispielsweise können Sie Unterkategorien für unterschiedliche Arten von Anlagen erstellen und dann Kategoriengruppen für Anlagen gegenüber Umlaufvermögen erstellen.  

Für jede Unterkategorie können Sie festlegen, ob Konten dieser Kategorie in bestimmte Arten von Finanzberichten enthalten sein müssen. Die Kontengruppen helfen Ihnen dabei, das Layout Ihrer Finanzberichte zu definieren.  

Beispielsweise gibt es in der Standardsaldoabrechnung eine einzige Unterkategorie für Zahlungen unter Anlagen. Wenn Sie möchten, dass die Saldoabrechnung Handgeld und Giro berücksichtigt, können Sie:  

1. Zwei neue Unterkategorien hinzufügen. Eine für Handgeld und eine für Ihr Girokonto.  
2. Geben Sie die zusätzlichen Berichtsdefinition **Bargeldkonten** für diese Unterkategorien an.  
3. Fassen Sie diese in der Unterkategorie **Bar** zusammen.  

Wenn Sie das nächste Mal ein Kontenschema auf Grundlage Ihre Änderungen erstellt haben, wird die nächste Saldoabrechnung ein Gesamtsaldo für Zahlungen und zwei Zeilen mit Salden für Handgeld und das Girokonto anzeigen.  

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Einrichten oder Ändern des Kontenplans](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]