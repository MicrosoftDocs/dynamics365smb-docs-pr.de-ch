---
title: Nicht abziehbare MWST einrichten
description: 'In diesem Artikel wird erläutert, wie Sie die nicht abziehbare MWST in Microsoft Dynamics 365 Business Central konfigurieren.'
author: altotovi
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
ms.reviewer: bholtorf
---

# Nicht abziehbare MWST einrichten

Bei der nicht abziehbaren Mehrwertsteuer (MWST) handelt es sich um die Mehrwertsteuer, die von einem Kaufenden zu zahlen ist, aber nicht von seiner eigenen Mehrwertsteuerschuld des Kaufenden abgezogen werden kann. Unternehmen können in der Regel die MWST beim Kauf von Waren und Dienstleistungen im Zusammenhang mit ihrer Geschäftstätigkeit zurückfordern. In manchen Situationen fällt einem Unternehmen jedoch MWST an, die nicht abzugsfähig ist. Diese Situationen hängen typischerweise mit den örtlichen Vorschriften zusammen und können sich von Land zu Land sowie Region zu Region unterscheiden. Das Modell der Verwendung der nicht abziehbaren oder teilweise abziehbaren MWST ist jedoch ähnlich. Sie können die anteilige MWST verwenden, um die MWST zu berechnen, wenn es abziehbare und nicht abziehbare MWST gibt.

Im Allgemeinen kann die MWST für einige Käufe aufgrund der folgenden Faktoren nicht abgezogen werden:

- **Die Art der gekauften Waren oder Dienstleistungen**: Die MWST ist aufgrund einer gesetzlichen Bestimmung über Waren wie Autos, Mobiltelefone und Lebensmittel, die in Restaurants gekauft werden, ganz oder teilweise nicht abziehbar.
- **Teilweise abziehbare anteilige MWST**: Die MWST wird entsprechend dem Verhältnis zwischen den Verkaufsvorgängen, für die die MWST geschuldet wird, und allen durchgeführten Vorgängen anteilig berechnet. MWST, die dieses Verhältnis übersteigt, kann nicht abgezogen werden.

Da es schwierig sein kann, zu wissen, wo und wie ein Artikel verwendet wird, wenden Sie sich an die örtlichen Salestaxbehörden in Ihrem Land/Ihrer Region. Sie können anhand historischer Daten ermitteln, ob Sie einen bestimmten Prozentsatz der MWST abziehen können.

> [!IMPORTANT]
> Dieses globale Feature ist **ausser in Belgien, Italien und Norwegen** in allen Ländern mit aktivierter MWST verfügbar. Diese Lokalisierungen verfügen bereits über lokale Features und werden in Zukunft aktualisiert. Führen Sie dieses Feature in diesen Ländern nicht aus, da es kein Upgrade-Verfahren gibt.

## Nicht abziehbare MWST verwenden

1. Wählen Sie die ![Glühbirne, welche die 3. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **MWST-Einrichtung** ein und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie das Kontrollkästchen **Nicht abzugsfähige MWST zulassen**.

    > [!IMPORTANT]
    > Nachdem Sie die nicht abzugsfähige MWST aktiviert haben, können Sie sie nicht deaktivieren, da das Feature möglicherweise Änderungen an Daten beinhaltet und möglicherweise ein Upgrade einiger Datenbanktabellen einleitet. Microsoft empfiehlt dringend, dass Sie dieses Feature zuerst in der Sandkastenumgebung aktivieren und testen, bevor Sie es in der Produktionsumgebung aktivieren.

3. Konfigurieren Sie, wie [!INCLUDE [prod_short](includes/prod_short.md)] mit nicht abziehbaren MWST-Werten umgeht.

    1. Geben Sie im Feld **Für Artikelkosten verwenden** an, ob die nicht abziehbare MWST beim Kauf von Artikeln zu den Artikelkosten hinzugerechnet werden muss. Andernfalls hat die nicht abziehbare MWST keinen Einfluss auf die Artikelkosten, und der volle Betrag wird nur auf Fibukontoebene erfasst.
    2. Wählen Sie das Kontrollkästchen **Für Anlagenkosten verwenden**, um die nicht abziehbare MWST zu den Anlagenkosten hinzuzufügen, wenn Sie neue Anlagen kaufen. Andernfalls hat die nicht abziehbare MWST keinen Einfluss auf die Anlagenkosten, und der volle Betrag wird nur auf Fibukontoebene erfasst.
    3. Wählen Sie das Kontrollkästchen **Für Projektkosten verwenden**, um anzugeben, dass die nicht abziehbare MWST zu den Projektkosten hinzugefügt werden muss, wenn Sie Artikel für das Projekt kaufen. Andernfalls hat die nicht abziehbare MWST keinen Einfluss auf die Projektkosten, und der volle Betrag wird nur auf Fibukontoebene erfasst.
    4. Wählen Sie das Kontrollkästchen **Nicht abziehbare MWST in Zeilen anzeigen**, um anzugeben, dass die nicht abziehbare MWST auf Belegzeilenseiten angezeigt werden muss, um die MWST-Beträge einfacher bearbeiten zu können.

## Den nicht abziehbaren MWST-Prozentsatz verwenden

1. Wählen Sie die ![Glühbirne, welche die 3. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MWST-Buchungseinrichtung** ein und wählen Sie dann den entsprechenden Link aus.
2. Füllen Sie auf der Seite **MWST-Buchungsmatrix** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.

    | Feld | Description |
    |-------|-------------|
    | Nicht abzugsfähige MWST zulassen | Geben Sie an, ob der Betrag für die nicht abziehbare MWST für die aktuelle Kombination einer MWST-Geschäftsbuchungsgruppe und einer MWST-Produktbuchungsgruppe berücksichtigt wird. |
    | Nicht abzugsfähige MWST % | Geben Sie den Prozentsatz des Betrages der Transaktion an, auf den die MWST nicht angewandt wird. |
    | Nicht abzugsfähige MWST Konto Einkauf | Geben Sie das Konto an, das mit dem MWST-Betrag verknüpft ist, der aufgrund der Art der gekauften Waren oder Dienstleistungen nicht abgezogen wird. |

    > [!NOTE]
    > Um Fibukontoeinträge zu haben, die das dedizierte Konto anstelle des Verkaufs-/Einkaufskontos verwenden, können Sie entweder das Feld **Konto für nicht abzugsfähige Vorsteuer** leer lassen oder das Feld **Fibukonto** festlegen.

3. Wählen Sie **OK** aus.

> [!NOTE]
> Sie können die nicht realisierte MWST nicht zusammen mit der nicht abzugsfähigen MWST verwenden.
>
> Verwenden Sie nicht dasselbe **MWST ID** für beide normale MWST, wo das Feld **Nicht abzugsfähige MWST %** auf **0** (Null) eingestellt ist, und die normale MWST, wenn das Feld **Nicht abzugsfähige MWST %** auf einen anderen Wert als Null eingestellt ist. Andernfalls wird der gesamte nicht abzugsfähige MWST-Betrag falsch berechnet.

## Siehe auch 

[Finanzmanagement](finance.md)  
[Designdetails: Nicht abziehbare MWST](design-details-nondeductible-vat.md)  
[Nicht abziehbare MWST verwenden](finance-how-use-non-deductible-vat.md)  
[Berechnungen und Buchungsmethoden für die Mehrwertsteuer festlegen](finance-setup-vat.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
