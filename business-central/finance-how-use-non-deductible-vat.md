---
title: Nicht abzugsfähige MWST verwenden
description: 'In diesem Artikel wird erläutert, wie Sie die nicht abzugsfähige MWST verwenden und Bericht darüber erstatten.'
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, return, settlement'
ms.search.form: '50, 51, 52, 161, 187, 317, 403, 6640, 9401'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="use-non-deductible-vat"></a>Nicht abzugsfähige MWST verwenden

In diesem Artikel wird erläutert, wie Sie die nicht abzugsfähige MWST verwenden und Bericht darüber erstatten.

## <a name="create-a-purchase-invoice-with-non-deductible-vat"></a>Erstellen Sie eine Einkaufsrechnung mit nicht abzugsfähiger MWST

1. Wählen Sie die ![Glühbirne, welche die 3. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu**, um eine Einkaufsrechnung zu erstellen, und geben Sie die entsprechenden Informationen im Rechnungskopf ein.
3. Erstellen Sie im Abschnitt **Positionen** basierend auf der MWST-Geschäftsbuchungsgruppe und der MWST-Produktbuchungsgruppe eine neue Position beliebigen Typs, in der Sie die nicht abzugsfähige MWST konfigurieren.
4. Geben Sie in den Feldern **Menge** und **EK-Preis** die entsprechenden Werte ein.

    Wenn Sie das Kontrollkästchen **Nicht abziehbare MWST in Positionen anzeigen** auf der Seite **MWST Einrichtung** auswählen, werden die Beträge in den Feldern **Nicht abziehbare MWST-Basis** und **Nicht abziehbare MWST-Betrag** basierend auf dem Feld **Nicht abzugsfähige MWST %** auf der Seite **MWST Buchungsmatrix Einr.** berechnet.

5. Buchen Sie die Rechnung.

## <a name="create-a-purchase-order-with-non-deductible-vat"></a>Erstellen Sie eine Einkaufsbestellung mit nicht abzugsfähiger MWST

1. Wählen Sie die ![Glühbirne, welche die 3. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu**, um eine Einkaufsbestellung zu erstellen, und geben Sie die entsprechenden Informationen im Belegkopf ein.
3. Erstellen Sie im Abschnitt **Positionen** basierend auf der MWST-Geschäftsbuchungsgruppe und der MWST-Produktbuchungsgruppe eine neue Position beliebigen Typs, in der Sie die nicht abzugsfähige MWST konfigurieren.
4. Geben Sie in den Feldern **Menge** und **EK-Preis** die entsprechenden Werte ein.

    Wenn Sie das Kontrollkästchen **Nicht abziehbare MWST in Positionen anzeigen** auf der Seite **MWST Einrichtung** auswählen, werden die Beträge in den Feldern **Nicht abziehbare MWST-Basis** und **Nicht abziehbare MWST-Betrag** basierend auf dem Feld **Nicht abzugsfähige MWST %** auf der Seite **MWST Buchungsmatrix Einr.** berechnet.

5. Buchen Sie die Einkaufsbestellung.

## <a name="adjust-rounded-vat-amounts-before-document-posting"></a>Gerundete MWST-Beträge vor Belegbuchung anpassen

Wenn MWST-Beträge in Ihrer Umgebung und im externen Buchhaltungssystem (dem ursprünglichen Rechnungsbeleg) nicht auf die gleiche Weise gerundet werden, können Sie den MWST-Betrag vor dem Buchen des Belegs anpassen. Gehen Sie folgendermassen vor, um diese Anpassung vorzunehmen, bevor Sie den Beleg buchen.

1. Wählen Sie im Aktionsbereich **Statistisch** aus.
2. Wenn Sie mit einer Einkaufsrechnung arbeiten, gehen Sie folgendermassen vor:

    1. Wählen Sie auf dem Inforegister **Positionen** den MWST-Betrag oder den nicht abzugsfähigen MWST-Betrag aus.
    2. Legen Sie die erforderlichen Werte aus dem Originalbeleg fest und schliessen Sie dann die Seite **Einkaufsrechnungsstatistik**.

3.  Wenn Sie mit der Einkaufsbestellung arbeiten, gehen Sie folgendermassen vor:

    1. Wählen Sie auf dem Inforegister **Fakturierung** **Anzahl der Steuerpositionen** aus, um die Seite **MWST-Betragspositionen** zu öffnen.
    2. Wählen Sie den MWST-Betrag oder den nicht abzugsfähigen MWST-Betrag aus, den Sie korrigieren möchten.
    3. Geben Sie die erforderlichen Werte aus dem Originalbeleg ein, schliessen Sie die Seite **MWST-Betragspositionen** und schliessen Sie dann die Seite **Einkaufsbestellungsstatistik**.

Um Anpassungen von MWST-Betrag zu verwenden, müssen Sie die Anpassungen aktivieren. Geben Sie auf der Seite **Finanzbuchhaltung Einrichtung** im Feld **Max. MWST-Differenz zulässig** den maximal zulässigen MWST-Betrag zur Korrektur ein. Wählen Sie dann auf der Seite **Kreditoren & Einkauf Einr.** **MWST-Differenz zulassen** aus.

Sie können die Werte der Felder **MWST-Betrag** und **Nicht abzugsfähiger MWST-Betrag** anpassen. Der Wert des Felds **Abzugsfähiger MWST-Betrag** ergibt sich aus diesen beiden Werten. Der Betrag, den Sie in das Feld **Nicht abzugsfähiger MWST-Betrag** eingeben, darf nicht höher sein als der Betrag, den Sie im Feld **MWST-Betrag** eingeben. Das Feld **Max. MWST-Differenz zulässig** auf der Seite **Finanzbuchhaltung Einrichtung** funktioniert für abzugsfähige und nicht abzugsfähige MWST-Beträge auf Statistikseiten unabhängig, wenn Sie MWST-Beträge anpassen möchten.

> [!IMPORTANT]
> Sie können auf Vorauszahlungsrechnungen keine nicht abzugsfähige MWST verwenden.

## <a name="see-also"></a>Siehe auch

[Finanzmanagement](finance.md)

[Berechnungen und Buchungsmethoden für die Mehrwertsteuer festlegen](finance-setup-vat.md)  

[Nicht absetzbare MWST einrichten](finance-setup-nondeductible-vat.md)

[Designdetails über nicht abzugsfähige MWST](design-details-nondeductible-vat.md)

[MWST an die Steuerbehörden melden](finance-how-report-vat.md)

[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
