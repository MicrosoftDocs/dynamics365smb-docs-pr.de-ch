---
title: Verstehen des Hauptbuchs und des COA
description: Beschreibt das Hauptbuch, den Kontenplan und die Kontenkategorien. Verwenden Sie die Seite Finanzbuchhaltung Einrichtung, um die Handhabung der Buchhaltung in Ihrer Firma festzulegen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 8590571283ae810d442d514e6968c1feb9865cd8
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 06/30/2021
ms.locfileid: "6321128"
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

### <a name="example"></a>Beispiel

Zum Beispiel hat der Standard-Bilanzauszug eine Unterkategorie für *Kasse* unter *Anlagevermögen*. Sie möchten, dass der Kontoauszug Portokasse und Scheck berücksichtigt, also gehen Sie wie folgt vor:  

1. Fügen Sie zwei neue Unterkategorien hinzu:

    * Eine für die Portokasse  
    * Eine für Ihr Girokonto  
2. Geben Sie die zusätzlichen Berichtsdefinition **Bargeldkonten** für diese Unterkategorien an.  
3. Fassen Sie diese in der Unterkategorie **Bar** zusammen.  

Wenn Sie das nächste Mal Kontenschema erstellen, zeigt Ihr Kontoauszug einen Gesamtsaldo für Bargeld und zwei Zeilen mit Salden für die Portokasse und das Girokonto.  

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Zugriff auf das Erstellen und Bearbeiten von Konten und Kontokategorien

In einer kleinen Organisation, wie der CRONUS-Demo-Firma, können die meisten Benutzer den Kontenplan bearbeiten, mit Ausnahme von Benutzern mit einer TEAM MEMBER-Lizenz. In grösseren Organisationen ist der Zugriff auf die Bearbeitung des Kontenplans jedoch durch Rollen und Berechtigungen eingeschränkt. Wenn Sie ein Administrator sind oder die Rolle *Geschäftsführer* oder *Buchhalter* haben, können Sie die Berechtigungen für alle Benutzer überprüfen, um sicherzustellen, dass die richtigen Personen Zugriff auf die relevanten Tabellen haben. Weitere Informationen finden Sie unter [So erhalten Sie eine Übersicht der Benutzerberechtigungen](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Einrichten oder Ändern des Kontenplans](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  
[Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]