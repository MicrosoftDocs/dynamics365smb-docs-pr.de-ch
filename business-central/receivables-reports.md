---
title: Debitoren Berichte und Analysen
description: Sehen Sie, welche Berichte und Analysen in der Standardversion von Business Central verfügbar sind, damit Sie Ihre Debitoren im Blick behalten können.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: 76de1625ee71b666b01d6b2fef1efe5605d9a418
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543415"
---
# <a name="accounts-receivable-reports-and-analytics-in-business-central"></a>Debitoren-Berichte und -Analysen in Business Central

Um Sie bei der Verwaltung Ihrer Debitoren in [!INCLUDE [prod_short](includes/prod_short.md)] zu unterstützen, sind Standardberichte und Analysen integriert. Es geht über die herkömmlichen Berichtsbeschränkungen hinaus und hilft Ihnen, verschiedene Arten von Berichten effizient zu gestalten.  

## <a name="reports"></a>Berichte

Die folgende Tabelle beschreibt einige der wichtigsten Berichte im Debitoren-Reporting.

| Bericht | Objekt-ID | Beschreibung |
|--|--|--|
| **Ausstehende Debitoren** | 120 | Zeigt den ausstehenden Betrag bei Debitoren aufgeschlüsselt nach Zeitintervallen für die überfällige Zeit. Der Bericht zeigt auch den Teil des Saldos der Debitoren an, der nicht fällig ist und kann mit oder ohne Belegdetails für jeden Kunden angezeigt werden. Dieser Bericht ist der Hauptbericht zum Abstimmen des Debitoren-Sachkontos mit der Hauptbuchhaltung. Angenommen, Sie haben die direkte Buchung auf die Konten, die im Forderungskonto der Debitorenbuchungsgruppen verwendet werden, nicht zugelassen, dann ist dieser Bericht eine Spezifikation der Beträge, die Sie in der Hauptbuchhaltung finden. |
| **Debitoren-Auszug** | 1316 | Erzeugt einen Kontoauszug für ein bestimmtes Zeitintervall. Er wird normalerweise an die Debitoren geschickt, um ihnen einen Überblick über die ausstehenden Beträge zu geben und auch als Mahnung, um überfällige Beträge zu bezahlen. Sie können wählen, ob die überfälligen Beträge in einem separaten Abschnitt angezeigt werden sollen. Sie können ein Alterungsband einfügen, ähnlich dem, das im Bericht **Fällige Debitoren** verwendet wird. Für das Alterungsband legen Sie typischerweise *30D* fest, d.h. 30-Tage-Intervalle wie 30, 60, 90 und 90+ Tage überfällig, ausgehend vom Enddatum, oder *1M+CM*, d.h. den aktuellen Monat in einem separaten Intervall und dann monatliche Intervalle für die Vormonate. **Anmerkung**: In der Kundenliste hat dieser Bericht auch eine eigene Aktion, **Geplante Debitoren**. Diese Option filtert nicht auf den von Ihnen gewählten Debitor. Es ist derselbe Bericht, wird aber verwendet, wenn Sie einen Kontoauszug an alle/mehrere Kunden senden wollen. |
| **Kunde – Saldo bis Datum** | 121 | Zeigt die offenen Debitoren-Sachkonto-Buchungen bis zum Enddatum an. Dieser Bericht zeigt einen ähnlichen Inhalt wie der Kontoauszug für Debitoren, aber ohne die Angabe, ob die Buchung überfällig ist. **Hinweis**: Der Datumsfilter wird auf die detaillierten Debitoren-Sachkonto-Einträge angewendet. Das bedeutet, dass, wenn Sie Zahlungen nach dem Enddatum haben, die auf Rechnungen innerhalb des Datumsbereichs angewendet wurden, die Rechnungen im Bericht erscheinen, da sie nicht zum Enddatum abgeschlossen wurden. |
| **Debitor – Bilanz** | 129 | Zeigt die Netto-Änderungen für Debitoren für den im Datumsfilter angegebenen Zeitraum sowie die Netto-Änderung seit Jahresbeginn für das Geschäftsjahr, das dem gewählten Zeitraum entspricht. Der Bericht ist nach Debitorenbuchungsgruppen gruppiert und bietet eine andere Sicht auf das Sachkonto als der Bericht **Gealterte Debitoren**. **Hinweis**: Wenn Sie keine Buchhaltungsperiode festgelegt haben, weiss das System nicht, welches Geschäftsjahr zu verwenden ist und zeigt entweder Jahr-zu-Jahr ab dem zuletzt definierten Geschäftsjahr an oder wählt einfach die Periode aus, die vom Anfang eines Jahres sein kann oder auch nicht.|
| **Kunde – Detail Test Bilanz** | 104 | Zeigt alle Debitoren-Sachkonto-Einträge innerhalb des angegebenen Datumsfilters. Dieser Bericht wird im Allgemeinen verwendet, um zu prüfen, ob alle Buchungen für einen bestimmten Kunden verbucht sind, oder für andere interne Prüfungen der Debitorenbücher. |
| **Kunde – Zahlungseingang** | 211 | Erzeugt einen Zahlungseingang für jeden Debitoren-Sachkonto-Eintrag vom Typ **Zahlung**. Wenn die Zahlung auf Rechnungen angewandt wurde, werden die Rechnungen angegeben; andernfalls wird nur der Zahlungsbetrag als nicht angewandt angegeben. Dieser Bericht wird verwendet, um an Debitoren zu senden, die einen Beleg für den Zahlungseingang wünschen.|
| **Kunden- und Kreditorenkonten abstimmen** | 33 |Zeigt die Sachkonteneinträge, die sich aus den Buchungen von Debitoren und Kreditoren ergeben, aufgeteilt nach Fibukonto und Buchungsgruppen. Dieser Bericht dient zum Abstimmen der Salden der Debitoren- und Kreditoren-Sachkonten mit den Salden des Hauptbuchs. |
| **Debitor – Zusammenfassung Alterung Simp.**| 109 |Dies ist eine veraltete Version eines Fälligkeitsberichts für Debitoren. Wir empfehlen Ihnen, stattdessen den Bericht **Alter Debitoren** zu verwenden. |
| **Verkaufsstatistik** |112  |[!INCLUDE [reports-sales-statistics](includes/reports-sales-statistics.md)]<br>Dieser Bericht kann auch in der Debitorenbuchhaltung verwendet werden, da es einfacher ist, einen schnellen Überblick über gebuchte Zahlungen, Rabatte und Verkäufe für einen bestimmten Debitor zu erhalten.|
|**Kundenliste**|101| Zeigt verschiedene Arten von Basisinformationen für Debitoren an, wie z.B. die Buchungsgruppe des Kunden, die Skontogruppe, Informationen zu Finance-Gebühren und Zahlungen, den Verkäufer, die Standardwährung des Kunden und das Kreditlimit in Ihrer lokalen Währung (LCY) sowie den aktuellen Saldo des Kunden (in LCY). Der Bericht kann z.B. für die Pflege der Informationen in der Tabelle Debitoren verwendet werden.|

## <a name="see-also"></a>Siehe auch

[Finanzauswertungen analysieren in Microsoft Excel](finance-analyze-excel.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Verwaltung von Anlagen](fa-manage.md)  
[Lokale Funktionen – Übersicht](about-localization.md)  
[Buchhalter-Erfahrung in [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]