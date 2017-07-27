---
title: Verkaufssteuer sowie Steuergruppen in den USA und in Kanada einrichten| Microsoft Docs
description: "Mehr erfahren über das Einrichten der Salestax sowie von Steuergruppen, Steuergebieten (Staat, Kantone, Städte und Standorte), Steuerzuständigkeiten und Steuereinzelheiten."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 763bb1b954b30734b0f81f121a6534c83442321a
ms.contentlocale: de-ch
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-sales-tax-in-the-us-and-canada"></a>Salestax in den USA und in Kanada melden
Wenn Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] zum ersten Mal starten, können Sie eine unterstützte Einrichtung in Anspruch nehmen, um Verkaufssteuersteuerinformationen für Ihre Firma, Debitoren und Kreditoren schnell und einfach zu einrichten. In Minutenschnelle sind Sie bereit, Verkaufsbelege und Einkaufsbelege mit der Salestax zu erstellen, die richtig berechnet werden kann. Dies wird erklärt [in unserem Blogeintrag](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Wenn Sie auf das leere "Mein Unternehmen" umlagern, empfiehlt es sich, dass Sie beginnen, jedes einzelne der unterstützen Setuphandbücher zu verwenden, einschließlich demjenigen für die Salestax. Wenn Sie es vorziehen, die Salestax selber einzurichten, beschreibt dieser Artikel, was Sie berücksichtigen müssen.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Steuergruppen, Steuergebiete und Steuerzuständigkeiten
In [!INCLUDE[d365fin](includes/d365fin_md.md)] besteht eine Steuergruppe aus einer Gruppe von Artikeln oder Ressourcen, die den gleichen Steuersätzen unterliegen. Beispielsweise können Sie eine Salestaxgruppe für steuerpflichtige Artikel und eine weitere für nicht zu versteuernde Artikel einrichten. Sie müssen Salestaxgruppencodes den Lagerartikeln und den Fibukonten zuweisen. Ebenso müssen Sie Salestaxgebietscodes, Lagerorte und Ihren eigenen Mandanteneinstellungen den Debitoren zuweisen. Das unterstützende Setuphandbuch hilft Ihnen dabei.  

Jedes Salestaxgebiet ist ein Gruppierung von Salestaxzuständigkeitsbereichen auf Basis einer bestimmten geografischen Lage. Beispielsweise hat das Salestaxgebiet in Miami, Florida, drei Salestaxzuständigkeitsbereiche: Stadt (Miami), Gemeinde (Dade) und Staat (Florida). [!INCLUDE[d365fin](includes/d365fin_md.md)] schließt eine begrenzte Zahl von Steuergebieten mit einer Standardkonfiguration ein, Sie können sie aber ändern und neue Steuergebiete hinzufügen.  

Wenn Sie neue Steuergebiete und Steuerzuständigkeiten einrichten, müssen Sie sicherstellen, dass Sie die richtig Felder ausfüllen. In den Vereinigten Staaten von Amerika können Staaten, Gemeinden, Orte und Lokale Salestax belasten. In Kanada verlangen die Bundesregierung und die Provinzen Salestax. Unternehmen erheben und leisten Salestax an diese Regierungsbehörden für die Produkte, die an Endbenutzer verkauft werden. Salestax kann auch zur vorhandenen Salestax berechnet werden. Beispielsweise kann Steuer auf einem Verkaufsrechnungsbetrag berechnet werden, der bereits die Steuerbeträge von anderen Zuständigkeitsbereichen umfasst.  

In Kanada müssen Steuerbeträge für jede Salestaxzuständigkeit detailliert dokumentiert sein. Bis zu vier Zuständigkeiten können in einem Beleg angezeigt werden und die Zuständigkeiten, die die gleiche Druckreihenfolge haben, werden zusammengefasst, wenn diese gedruckt werden.  

## <a name="tax-details"></a>Salestaxdetails
Das Fenster **Steuerdetails** zeigt verschiedene Kombinationen von Salestaxzuständigkeitsbereichen und Mehrwertsteuergruppen an, um Salestaxsätze einzurichten. Für jede Salestaxzuständigkeit empfiehlt es sich, dass Sie eine Salestaxgruppe für normale Salestax, eine andere Salestaxgruppe für Artikel oder Services, die nicht besteuert werden, und eine zusätzliche Salestaxgruppe für jede Art Artikel oder Service einrichten, die mit einem anderen Salestaxsteuersatz in diesem Salestaxzuständigkeitsbereich vorhanden ist.  

Wenn Sie in den USA einem Debitor an einem Lagerort verkaufen, in dem Sie keinen *Status* oder gültigen Lagerort haben, erheben Sie keine Salestax. Bei Lagerorten, in denen Sie keinen Status haben, ist sichergestellt, dass sowohl die Felder **Salestax unter Steuergrenze** und die **Salestax über Steuergrenze** 0.00 aufweisen.  

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Verkaufssteuer sowie Steuern auf Waren und Dienstleistungen in Kanada](ca-finance-tax.md)  
[Einfaches Einrichten der Verkaufssteuer](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

