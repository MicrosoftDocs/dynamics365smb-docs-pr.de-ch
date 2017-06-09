---
title: Relationship Management einrichten | Microsoft Docs
description: Beschreibt die Einrichtung der Marketing- und Kontaktverwaltung in Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ba5ed3df4ddbf39863509528a667848015312ab0
ms.contentlocale: de-ch
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-relationship-management"></a>Marketing & Vertrieb einrichten
Bevor mit Ihren Kontakten und Marketinginteressen arbeiten, gibt es einige Entscheidungen und Schritte, die Sie zur Einrichtung der Verwaltung bestimmter Aspekte Ihrer Kontakte durch den Marketingbereich durchführen sollen. Beispielsweise können Sie entscheiden, ob die Kontaktkarte mit der Debitorenkarte, der Kreditorenkarte und der Bankkontokarte synchronisiert wir, wie Nummernkreise definieren werden oder welche Anrede im Schriftverkehr mit Ihren Kontakten verwendet wird.

Die Verwaltung von Kontakten und die Verfolgung einer Strategie zum Identifizieren, Gewinnen und Binden von Debitoren tragen zu einer Optimierung des Unternehmens sowie zu einer Steigerung der Kundenzufriedenheit bei. Ein gutes Kontaktverwaltungssystem ermöglicht zudem das Knüpfen und Pflegen von Kundenbeziehungen. Die Kommunikation ist bei einer solchen Beziehung besonders wichtig. So ist denn auch die Möglichkeit, die Kommunikation exakt auf die jeweiligen Anforderungen von Interessenten, bestehenden Debitoren, Kreditoren und Geschäftspartnern zuschneiden zu können, für den Erfolg eines Unternehmens unverzichtbar. Einer der ersten Schritte besteht darin, eine Strategie auszuarbeiten und zu definieren, wie Kontaktinformationen im Unternehmen verwendet werden sollen. Da diese Informationen innerhalb des Unternehmens einer Vielzahl von Gruppen zur Verfügung stehen, empfiehlt sich die Verwendung eines durchdachten Systems, um eine höhere Produktivität der einzelnen Beteiligten zu erzielen.

Sie richten die Marketing- und Kontaktverwaltung über das Fenster **Marketingeinrichtung** ein. Um das Fenster **Marketing einrichten** zu öffnen wählen Sie in der oberen rechter Ecke das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Marketing einrichten** ein und wählen den entsprechenden Link aus.

## <a name="automatically-copy-specific-information-from-the-contact-companies-to-the-contact-persons"></a>Automatisches Kopieren bestimmter Informationen aus den Kontaktunternehmen in die Kontaktpersonen
Einige Informationen über die Kontaktunternehmen stimmen mit denen über die Kontaktpersonen bei diesen Unternehmen überein, wie z. B. die Adresse. Im **Übernahme**-Abschnitt des Fensters **Marketingeinrichtung** können Sie die Anwendung so einrichten, das bestimmte Felder automatisch von der Kontaktunternehmenskarte in die Kontaktpersonenkarte kopieren werden, wenn Sie eine Kontaktperson für ein Kontaktunternehmen erstellen. Beispielsweise können Sie auswählen, dass Verkäufercode, Adressendaten (Adresse, Adresse 2, Ort, PLZ und Kanton), Kommunikationsdetails (Faxnummer, Telex und Telefonnummer) kopiert werden.

Wenn Sie eines dieser Felder auf der Kontaktunternehmenskarte ändern, wird das Feld auf der Kontaktpersonenkarte automatisch entsprechend geändert (es sei denn, Sie haben das Feld auf der Kontaktpersonenkarte manuell geändert).

Weitere Informationen finden Sie unter [Gewusst wie: Anlegen neuer Kontaktpersonen](marketing-how-create-contact-persons.md).

## <a name="use-predefined-defaults-on-new-contacts"></a>Vordefinierte Standards für neue Kontakte nutzen
Sie können festlegen, dass jedem neuen Kontakt bei seiner Erstellung automatisch ein bestimmter Sprachcode, Gebietscode, Verkäufercode und Länder-/Regionscode als Vorgabe zugeordnet wird. Ausserdem können Sie einen Vorgabewert für einen Verkaufsprozesscode eingeben, der jeder neuen Verkaufschance bei ihrer Erstellung zugeordnet wird.

Durch die Übernahme von Feldern werden die Vorgabewerte überschrieben, die Sie eingerichtet haben. Wenn Sie z. B. Englisch als Vorgabesprache eingerichtet haben, die Sprache des Kontaktunternehmens jedoch Deutsch ist, wird den Kontaktpersonen dieses Unternehmens automatisch die Sprache Deutsch zugewiesen.

<!--You can also setup a default salutation that the program automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, the program will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-record-interactions"></a>Automatisch aufgezeichnete Aktivitäten
[!INCLUDE[d365fin](includes/d365fin_md.md)]Die Anwendung kann Verkaufs- und Einkaufsbelege (z. B. Aufträge, Rechnungen, Lieferungen usw.) sowie E-Mails, Telefonanrufe und Deckblätter automatisch speichern.

Weitere Informationen finden Sie unter [Aktivitäten mit Kontakten automatisch aufzeichnen](marketing-auto-record-interactions.md).

## <a name="synchronize-contacts-with-customers-and-more"></a>Synchronisieren von Kontakten mit Debitoren und anderen
Um die Kontaktkarte mit der Debitoren-, der Kreditoren- und der Bankkontenkarte zu synchronisieren, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten auswählen. Sie können z. B. einen Kontakt nur mit einem bestehenden Debitor verknüpfen, wenn Sie in dem Fenster **Marketingeinrichtung** einen Geschäftsbeziehungscode für Debitoren ausgewählt haben.

Weitere Informationen finden Sie unter [Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten](marketing-synchronize-contacts-customers-vendors-bank-accounts.md).

## <a name="assign-a-number-series-to-contacts-and-opportunities"></a>Zuweisen von Nummernserien zu Kontakten und Verkaufschancen
Sie können Nummernserien für Kontakte und Verkaufschancen einrichten. Wenn Sie eine Nummernserie für Kontakte eingerichtet haben, drücken Sie beim Erstellen eines Kontakts im Feld Nummer der Kontaktkarte EINGABE und die Anwendung fügt die nächste verfügbare Kontaktnummern ein.

Weitere Informationen über Nummernserien finden Sie unter [Erstellen von Nummernserien](ui-create-number-series.md)

## <a name="search-for-duplicate-contacts-when-contacts-are-created"></a>Suche nach Kontaktdubletten, wenn Kontakte erstellt werden
Sie können einrichten, dass jedes Mal, wenn Sie ein Kontaktunternehmen erstellen, nach Dubletten gesucht wird oder Sie können dies manuell vornehmen, nachdem Sie Kontakte erstellt haben. Sie können auch einstellen, dass bei jeder Veränderung der Informationen über den Kontakt oder bei seiner Erstellung automatisch die Suchtexte aktualisiert werden. Sie können den Prozentsatz der Übereinstimmung festlegen, d. h., den Prozentsatz der Suchtexte, der zwischen den beiden Kontakten identisch sein muss, damit sie von der Anwendung als Dubletten erkannt werden.

## <a name="set-up-email-logging"></a>Einrichten der E-Mail-Protokollierung
Sie können mit Ihren Kontakten, Debitoren, Kreditoren usw. E-Mails austauschen. Sie können E-Mails in der Anwendung oder in Outlook versenden und erhalten. Bevor Sie auf diese Weise E-Mails austauschen können und sie im System speichern und in die Warteschlangeeinreihen können, müssen Sie einige Parameter einstellen, wie beispielsweise das Zeitintervall, in dem Anwendung prüft, ob E-Mails zur Verarbeitung anstehen, E-Mail-Protokollierungs-Profilname usw.

## <a name="see-also"></a>Siehe auch
[Kontakte verwalten](marketing-contacts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]  

