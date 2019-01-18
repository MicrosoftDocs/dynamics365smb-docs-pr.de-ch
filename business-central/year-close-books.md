---
title: "Überblick über die erforderlichen Aufgaben für das Schliessen der Bücher| Microsoft Docs"
description: "Erhalten von Informationen über das Schliessens der Bücher für ein Geschäftsjahr oder für eine Periode, und was passiert, nachdem Sie das Jahr abgeschlossen haben."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6894fad3654f204d79144946776b36dcb2d43665
ms.contentlocale: de-ch
ms.lasthandoff: 11/26/2018

---
# <a name="closing-the-books"></a>Bucher schliessen
Nachdem sichergestellt wurde, dass sich alle Konten auf dem neuesten Stand befinden und Kosten und Umsatz verteilt wurden, können die Bücher für ein Geschäftsjahr oder für eine Periode abgeschlossen werden.

Ein Jahresabschluss muss nicht zwingend durchgeführt werden, erleichtert Ihnen aber die Arbeit im System, da Sie auf diese Weise die Vorteile der benutzerfreundlichen Filteroptionen nutzen können. Es besteht auch kein Anlass zur Sorge, dass beim Jahresabschluss Details der Transaktionen verloren gehen, da alle Details auch nach Abschluss eines Jahrs beibehalten werden.

## <a name="closing-book-process"></a>Prozess zum Abschliessen der Bücher
Der Prozess für den Abschluss der Bücher umfasst diese Hauptaufgaben:

1. Abschliessen der Buchhaltungsperiode.

    Ein Geschäftsjahr ist definiert als mindestens eine offene Periode entsprechend der Definition auf der Seite **Buchhaltungsperioden**. Üblicherweise umfasst ein Geschäftsjahr 12 Perioden von jeweils einem Monat, das Jahr kann jedoch auch auf andere Weise definiert werden.

    Weitere Informationen finden Sie unter [Abschliessen von Buchhaltungsperioden](year-close-account-periods.md).
2. Erfassen der Vorjahresposten.

    Beim Abschliessen eines Geschäftsjahrs müssen eine Reihe verwaltungsbezogener Transaktionen (wie Artikel mit Vorauszahlung oder abgegrenzte Artikel) eingegeben werden. Diese Transaktionen werden als Regulierungsposten bezeichnet. Für die Buchung dieser Posten gelten keine besonderen Regeln, und auch bei diesen Posten ist das Kontrollkästchen **Nachbuchung** aktiviert, wenn sie für ein Datum gebucht werden, das innerhalb eines abgeschlossenen Geschäftsjahrs liegt. Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Fibuposten gebucht werden.
3. Übertragen der Salden aus der Erfolgsrechnung in die Bilanz.

    Nachdem ein Geschäftsjahr abgeschlossen wurde und alle Nachbuchungen gebucht wurden, müssen die Erfolgsrechnungskonten abgeschlossen werden, und der Nettoertrag des Jahres muss auf ein Konto übertragen werden, das in der Bilanz unter dem Eigenkapital aufgeführt ist. Verwenden Sie zu diesem Zweck die Stapelverarbeitung Erfolgsrechnungskonten Nullstellung. Mithilfe dieser Stapelverarbeitung werden alle Fibukonten vom Typ Erfolgsrechnung verarbeitet und Posten erstellt, mit denen die Salden annulliert werden. Diese Posten werden in ein Erf.-Journal eingefügt, von wo aus sie gebucht werden können. Durch die Stapelverarbeitung erfolgt keine automatische Buchung, es sei denn, es wird eine Berichtswährung verwendet. Bei Verwendung einer Berichtswährung erfolgt eine direkte Buchung in die Fibuposten.

    Weitere Informationen finden Sie unter [Jahresabschluss](year-close-income-statement.md).
4. Buchen des Ultimopostens für den Jahresabschluss sowie Gegenbuchen von Eigenkapitalkontoposten.

    Wenn die Stapelverarbeitung "Erfolgsrechnungsabschluss" generiert wurde, buchen Sie die erstellten Einträge. Wurde in der Stapelverarbeitung kein Erfolgsrechnungs-Abschlusskonto angegeben, geben Sie eine Zeile mit einem Saldoposten ein, durch den der Nettoertrag auf das korrekte Konto (in der Bilanz unter "Eigenkapital") gebucht wird. Anschliessend kann das Erf.-Journal gebucht werden.

    Weitere Informationen finden Sie unter [Buchen von Jahresabschlussposten](year-how-post-year-end-close-entry.md).

## <a name="what-happens-when-you-close"></a>Was erfolgt, wenn Sie abschliessen
Wenn Sie am Ende des Jahres den Jahresabschluss durchführen, werden Ihre Erträge aus den berechneten Erträgen auf das Konto "Gewinnvortragskonto" verschoben. Das Geschäftsjahr wird als "Geschlossen" gekennzeichnet, und alle nachfolgenden Posten für das geschlossene Jahr werden als "Nachbuchungen" gekennzeichnet.

Anschliessend wird ein Ultimoposten generiert, der jedoch nicht automatisch gebucht wird. Sie erhalten die Möglichkeit, die Gegenbuchung der Posten des Eigenkapitalkontos durchzuführen, sodass Sie entscheiden können, wie der Ultimoposten zugeordnet wird. Wenn Ihr Unternehmen über mehrere Geschäftsbereiche verfügt, können Sie vom System einen einzigen Ultimoposten für alle Geschäftsbereiche generieren lassen und dann für das Eigenkapitalkonto jedes Geschäftsbereichs eine Gegenbuchung erstellen.

Sie können Buchungen in einem früheren Geschäftsjahr auch durchführen, nachdem die Erfolgskonten geschlossen wurden, wenn Sie danach die Stapelverarbeitung Erfolgskonten Nullstellung erneut ausführen.

## <a name="see-also"></a>Siehe auch
[Ein neues Geschäftsjahres eröffnen](finance-how-open-new-fiscal-year.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

