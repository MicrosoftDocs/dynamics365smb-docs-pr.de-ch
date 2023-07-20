---
title: "Designdetails\_– nicht abzugsfähige MWST"
description: 'Dieser Artikel enthält Informationen zur nicht abzugsfähigen Mehrwertsteuer (MWST), die von einem Käufer zu zahlen ist, aber nicht von der eigenen Steuerschuld des Käufers abgezogen werden kann.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
---

# <a name="design-details-non-deductible-vat"></a>Designdetails: Nicht abzugsfähige MWST

Bei der nicht abzugsfähigen Salestax handelt es sich um die Mehrwertsteuer, die von einem Käufer zu zahlen ist, aber nicht von seiner eigenen Steuerschuld des Käufers abgezogen werden kann. Da es schwierig sein kann, zu wissen, wo und wie ein Artikel verwendet wird, müssen Sie sich an die örtlichen Steuerbehörden in Ihrem Land oder Ihrer Region wenden, um herauszufinden, ob ein bestimmter Prozentsatz der MWST abzugsfähig ist. Auch wenn Sie wissen, dass ein bestimmter Prozentsatz der MWST nicht abzugsfähig ist, gibt es unterschiedliche Modelle für den Umgang mit nicht abzugsfähigen Beträgen im Zusammenhang mit **Artikeln** und **Anlagen**.

## <a name="prerequisites-for-using-non-deductible-vat"></a>Voraussetzungen für die Nutzung der nicht abzugsfähigen MWST

Gehen Sie wie folgt vor, um die nicht abzugsfähige MWST zu verwenden und zu buchen.

1. Wählen Sie auf der Seite **MWST-Einrichtung** **Nicht abzugsfähige MWST aktivieren** aus, um das Feature zu aktivieren.
2. Wählen Sie auf der Seite **MWST-Buchungseinrichtung** aus, welche MWST-Buchungsgruppen die nicht abzugsfähige MWST verwenden können.

## <a name="examples"></a>Beispiele

Für die folgenden Beispiele ist die nicht abzugsfähige MWST aktiviert und die folgende Einrichtung ist abgeschlossen:

- Das Feld **MWST-Produktbuchungsgruppe** ist auf **NDVAT** eingestellt.
- Gehen Sie auf der Seite **MWST-Buchungseinrichtung** wie folgt vor:

    - **NDVAT** wird als MWST-Produktbuchungsgruppe und **INLAND** als MWST-Geschäftsbuchungsgruppe festgelegt.
    - Der Wert **MWST ID** muss eindeutig sein.
    - Das Feld **MWST %** ist auf **25** eingestellt.
    - Das Feld **Nicht abzugsfähige MWST zulassen** ist auf **Zulassen** eingestellt.
    - Das Feld **Nicht abzugsfähige MWST %** ist auf **100** eingestellt.
    - Das Feld **MWST-Berechnungsart** ist auf **Normale MWST** eingestellt.
    - Es sind nur das MWST-Konto und das Vorsteuerkonto konfiguriert.

In allen Beispielen werden Artikel und Anlagen verwendet, bei denen die MWST-Produktbuchungsgruppe **NDVAT** lautet.

### <a name="items"></a>Arti&kel

Für einen neuen Artikel ist **NDVAT** als MWST-Produktbuchungsgruppe festgelegt. Im Einkaufsbeleg sind **Menge** = **1** und **EK-Preis ohne MWST** = **1.000,00**.

Unabhängig von der verwendeten Option sind die Ergebnisse bei MWST-Posten dieselben.

| Belegtyp | Typ | Grundplatte | Betrag | Nicht abzugsfähige MWST Basis | Nicht abzugsfähiger MWST Betrag |
|---|---|---|---|---|---|
| Fakturierung | Einkauf | 0.00 | 0.00 | 1,000.00 | 250.00 |

Die Details werden in den Werteinträgen angezeigt.

> [!NOTE]
> Sie können das Feld **Für Artikelkosten verwenden** auf der Seite **MWST-Einrichtung** aktivieren.

#### <a name="use-for-item-cost-isnt-enabled"></a>Die Verwendung für Artikelkosten ist nicht aktiviert

| Lagerpostenart | Postenart  | Einstandsbetrag (tatsächl.) | Lagerpostenmenge |
|---|---|---|---|
| Einkauf | Direkte Kosten | 1,000.00 | 0 |

#### <a name="use-for-item-cost-is-enabled"></a>Die Verwendung für Artikelkosten ist aktiviert

| Lagerpostenart | Postenart  | Einstandsbetrag (tatsächl.) | Lagerpostenmenge |
|---|---|---|---|
| Einkauf | Direkte Kosten | 1,250.00 | 0 |

### <a name="fixed-assets"></a>Anlagen

Für eine neue Anlage ist das Anschaffungskostenkonto so eingestellt, dass **NDVAT** als MWST-Produktbuchungsgruppe verwendet wird. Im Einkaufsbeleg sind **Menge** = **1** und **EK-Preis ohne MWST** = **1.000,00**.

Unabhängig von der verwendeten Option sind die Ergebnisse bei MWST-Posten dieselben.

| Belegtyp | Typ | Grundplatte | Betrag | Nicht abzugsfähige MWST Basis | Nicht abzugsfähiger MWST Betrag |
|---|---|---|---|---|---|
| Fakturierung | Einkauf | 0.00 | 0.00 | 1,000.00 | 250.00 |

Die Details werden in den Anlagenposten angezeigt.

> [!NOTE]
> Sie können das Feld **Für Anlagenkosten verwenden** auf der Seite **MWST-Einrichtung** aktivieren.

#### <a name="use-for-fixed-asset-cost-isnt-enabled"></a>Die Verwendung für Anlagenkosten ist nicht aktiviert

| Belegtyp | Anlagenbuchungsart | Betrag | MWST-Betrag |
|---|---|---|---|
| Fakturierung | Anschaffungskosten | 1,000.00 | 250.00 |

#### <a name="use-for-fixed-asset-cost-is-enabled"></a>Die Verwendung für Anlagenkosten ist aktiviert

| Belegtyp | Anlagenbuchungsart | Betrag | MWST-Betrag |
|---|---|---|---|
| Fakturierung | Anschaffungskosten | 1,000.00 | 250.00 |
| Fakturierung | Anschaffungskosten | 250.00 | 0.00 |

## <a name="see-also"></a>Siehe auch

[Nicht abzugsfähige MWST einrichten](finance-setup-nondeductible-vat.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
