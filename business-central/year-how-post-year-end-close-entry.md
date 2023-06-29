---
title: So buchen Sie den Jahresabschlussposten
description: 'Beschreibt, wie Sie das Erf.-Journal öffnen, dass Sie in der Stapelverarbeitung "Jahresabschluss" definiert haben und dann den Jahresabschlusseintrag überprüfen und buchen.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: 100
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="posting-the-year-end-closing-entry"></a><a name="posting-the-year-end-closing-entry"></a>Buchen der Jahresendabschlussbuchung

Nachdem Sie die Stapelverarbeitung **GuV-Konten Nullstellung** ausgeführt haben, um den bzw. die Ultimoposten für den Jahresabschluss zu generieren, müssen Sie das in der Stapelverarbeitung angegebene Buchungsblatt öffnen und die Posten überprüfen und buchen.  

> [!TIP]
> Abhängig von den Arbeitsprozessen Ihres Unternehmens können Sie wählen, ob Abrechnungsperioden und Geschäftsjahre in [!INCLUDE [prod_short](includes/prod_short.md)] geschlossen werden sollen oder nicht. Das folgende Verfahren setzt voraus, dass Sie das Geschäftsjahr mit der Option *Buchhaltungsperioden* abgeschlossen haben, einen Jahresabschlusseintrag mit dem Batch-Job **Gewinn- und Verlustrechnung schliessen** generiert haben und nun bereit sind, den Abschlusseintrag zum Jahresende zusammen mit den Gegenbuchungen des Eigenkapitalkontos zu buchen. Ihre Organisation kann sich dafür entscheiden, anders zu arbeiten, z. B. den Abschluss zum Jahresende als Teil des Abschlusses des Geschäftsjahres zu veröffentlichen.

## <a name="to-post-the-year-end-closing-entry"></a><a name="to-post-the-year-end-closing-entry"></a>So buchen Sie den Jahresabschlussposten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Fibu Erf.-Journal** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Fibu Erf.-Journal** im Feld **Erf.-Journalname** das Erf.-Journal mit den Abschlussposten aus.
3. Überprüfen Sie die Posten.
4. Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Erfassungsjournal zu buchen.

> [!NOTE]  
> Wenn ein Fehler erkannt wird, wird eine Fehlermeldung angezeigt. Wurde die Buchung ordnungsgemäss durchgeführt, werden die gebuchten Posten aus dem Erfassungsjournal entfernt. Nachdem die Buchung abgeschlossen ist, wird ein Posten auf jedes Erfolgsrechnungskonto gebucht, sodass der Saldo des Kontos Null ist und das Jahresergebnis in die Bilanz übertragen wird.

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Schliessen von Buchhaltungsperioden](year-close-account-periods.md)  
[Schliessen der Bücher](year-close-books.md)  
[GuV-Konten Nullstellung](year-close-income-statement.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
