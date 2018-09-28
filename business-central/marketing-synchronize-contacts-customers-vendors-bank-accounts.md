---
title: Kontakte mit Debitoren, Kreditoren und Bankkonten synchronisieren| Microsoft Docs
description: Sie koppeln synchronisieren Kontaktinformationen der Kontakte, die auch Debitoren, Kreditoren oder Bankkonten sind, so aktualisieren Sie nur Informationen in einem Bereich.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f377236158ae1035fd40dd15342d76822aa91ac8
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten
Wenn einige Ihrer Kontakte auch Debitoren, Kreditoren oder Bankkonten sind, können Sie deren Kontaktinformationen mit dem entsprechenden Debitor, Kreditor oder Bankkonto synchronisieren. Die Synchronisierung macht Informationen, die zwischen Kontakten und Debitoren, Kreditoren oder Bankkonto gleich sind, identisch.  

Bevor Sie Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten synchronisieren, müssen Sie in dem Fenster **Marketing & Vertrieb Einr.** einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten festlegen. Weitere Informationen finden Sie unter [Einrichten von Relationship Management](marketing-setup-marketing.md)

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Unterschiedliche Wege, um Kontakte mit Debitoren, Kreditoren und Bankkonten zu synchronisieren
Sie können Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten synchronisieren, indem Sie eine der folgenden drei Methoden verwenden:

* Verknüpfen Sie Kontakte auf der Kontaktkarte mit bestehenden Debitoren, Kreditoren oder Bankkonten. Weitere Informationen finden Sie unter [Kontakte mit Debitoren, Kreditoren und Bankkonten synchronisieren](marketing-how-link-contact.md).
* Erstellen Sie Debitoren, Kreditoren oder Bankkonten über den Kontakt. Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Erstellen Sie Kontakte aus Debitoren, Kreditoren oder Bankkonten. Weitere Informationen finden Sie unter [Erstellen eines Unternehmenskontakts aus einem Debitor, Kreditor oder Bankkonto](marketing-how-create-contact-companies.md).

## <a name="consequences-of-synchronization"></a>Ergebnisse der Synchronisierung
Wenn der Kontakt mit dem Debitor, Kreditor oder Bankkonto synchronisiert ist:

* Sie müssen die Informationen nur an einer Stelle aktualisieren. Wenn Sie z. B. die Telefonnummer auf des Kontakts ändern, wird die Telefonnummer auf des Debitors-, Kreditors oder Bankkontos automatisch mit der gleichen Änderung aktualisiert.
* Wenn Sie beim Erstellen einer Debitoren-, Kreditoren- oder Bankkontokarte eine Nummernserie für Kontakte angegeben haben, wird automatisch eine Kontaktkarte für den Debitor, den Kreditor bzw. das Bankkonto erstellt.
* Über den Kontakt können Sie Verkaufsofferten und -Aufträge, Einkaufsofferten und –Aufträge erstellen.
* Sie können Ihre Aktivitäten beim Durchführen von Aktionen erfassen lassen, z. B. das Drucken von Aufträgen oder Rahmenbestellungen, Erstellen von Verkaufsserviceaufträgen, Senden von E-Mails usw.
* Wenn Sie einen Kontakt löschen, der mit einem Debitor, Kreditor oder Bankkonto verknüpft ist, wird nur der Kontakt entfernt. Der Debitor, Kreditor oder das Bankkonto bleibt erhalten.
* Wenn Sie einen Debitor, einen Kreditor oder ein Bankkonto löschen, der bzw. das mit einem Kontakt verknüpft ist, bleibt der Kontakt erhalten.

> [!NOTE]  
>   Einige Informationen, wie Fakturierungs- und Buchungsdetails, erscheinen nicht auf der Kontaktkarte. Sie können sie manuell auf der Debitoren-, Kreditoren- und/oder Bankkontenkarte hinzufügen, wenn Sie Kontakte als Debitoren, Kreditoren oder Bankkonten erstellen.

## <a name="see-also"></a>Siehe auch
[Kontakte verwalten](marketing-contacts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

