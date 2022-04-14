---
title: Verkaufspreise und Rabatte für Debitoren einrichten | Microsoft Docs
description: Beschreibt, wie Sie Preis- und Rabattvereinbarungen für Verkaufsbelege definieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 67536b129986343d67c2bc52cc3db8450e177d67
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520167"
---
# <a name="record-special-sales-prices-and-discounts"></a>Spezielle Verkaufspreise und Skonti aufzeichnen
> [!NOTE]
> In Veröffentlichungszyklus 2 von 2020 haben wir optimierte Prozesse zum Einrichten und Verwalten von Preisen und Skonti veröffentlicht. Wenn Sie ein neuer Kunde mit dieser Version sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** in **Funktionsverwaltung** akualisiert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt verschiedene Preisstrategien, wie zum Beispiel:
* Ein-Preis-für-alle-Modelle, bei denen ein Artikel immer zum gleichen Preis verkauft wird.
* Besondere Preisvereinbarungen mit bestimmten Kunden oder Kundengruppen.
* Kampagnen, wenn ein Verkauf die Kriterien für ein Sonderangebot erfüllt. Kriterien können beispielsweise sein, wenn eine Bestellung eine Mindestmenge erfüllt, vor einem bestimmten Datum liegt oder eine bestimmte Art von Artikel enthält.  

Um ein einfaches Preismodell zu verwenden, müssen Sie nur einen Stückpreis angeben, wenn Sie einen Artikel oder eine Ressource einrichten. Dieser Preis wird immer für Verkaufsbelege verwendet. Für fortgeschrittenere Modelle, z. B. wenn Sie Sonderpreise für eine Verkaufskampagne anbieten möchten, können Sie auf der Seite **Verkaufspreise** Kriterien angeben. Sie können Sonderpreise auf der Grundlage einer Kombination der folgenden Informationen anbieten: 

* Debitor
* Artikel
* Einheit
* Mindestmenge
* Daten, die den Zeitraum definieren, für den die Preise gültig sind.

Nachdem Sie Sonderpreise eingerichtet haben, kann [!INCLUDE[prod_short](includes/prod_short.md)] den besten Preis für Verkaufs- und Einkaufsbelege sowie für Auftrags- und Artikelerfassungszeilen berechnen. Weitere Informationen finden Sie unter [Beste Preisberechnung](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Für Verkaufsrabatte können Sie zwei Arten einrichten:

| Skontoart | Beschreibung |
| --- | --- |
| **Verkaufszeilenskonto** |Ein Betrag, der in Verkaufszeilen eingefügt wird, wenn sie eine bestimmte Kombination aus Kunde, Artikel, Mindestmenge, Mengeneinheit oder Anfangs-/Enddatum enthalten. Dieser Typ gilt auf gleiche Weise für Verkaufsbelege. |
| **RechnungsSkonto** |Ein Skontoprozentsatz, der von der Gesamtsumme des Verkaufsbelegs abgezogen wird, wenn die Summe aller Zeilen des Belegs einen bestimmten Mindestwert übersteigt. |

> [!TIP]  
> Wenn ein Artikel nie mit einem Skonto verkauft werden sollte, lassen Sie die Skontofelder auf der Artikelseite leer und schliessen Sie den Artikel nicht in einer ZeilenSkontoeinrichtung ein.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Um Verkaufspreise für einen Debitor zu erstellen:

Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte „Aktuelle Erfahrung“. 

#### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience/)

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Kunden und klicken dann auf die Aktion **Preise**.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

#### <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience/)  

Standardmässig lautet der Status neuer Preislisten Entwurf. Preislistenentwürfe gehen nicht in die Preiskalkulation ein. Wenn Sie mit dem Hinzufügen von Zeilen fertig sind und die Preise verwenden möchten, können Sie den Status in Aktiv ändern.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Debitor und wählen Sie dann die Aktion **Verkaufspreislisten**. 
3. Wählen Sie **Neu**, um eine neue Verkaufspreisliste zu erstellen.
4. Füllen Sie bei Bedarf die Felder in den Inforegistern **Allgemein** und **Salestax** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Führen Sie einen der folgenden Schritte aus, um Elemente zur Liste hinzuzufügen:
   * Um viele Elemente hinzuzufügen, wählen Sie **Linien vorschlagen**. Geben Sie anschliessend Filterkriterien ein, um die hinzuzufügenden Elementtypen anzugeben. Optional können Sie auch andere Einstellungen für die Artikel eingeben, die für die Preisliste spezifisch sind. Bei Bedarf können Sie diese Einstellungen später ändern.
   * Um Artikel aus einer anderen Preisliste zu kopieren, wählen Sie **Zeilen kopieren** und wählen Sie dann die zu kopierende Preisliste aus.
   * Um Elemente manuell hinzuzufügen, wählen Sie im Raster im Feld **Produkt-Typ** den Produkttyp aus, für den die Preisliste bestimmt ist. Füllen Sie je nach Auswahl die restlichen Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Um die Preisliste zu verwenden, klicken Sie auf das Feld **Status** und wählen Sie **Aktiv**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Verwenden von Verkaufs- und Einkaufspreislisten
> [!NOTE]
> Die Verwendung von Preislisten erfordert, dass Ihr Administrator das Funktionsupdate **Neue Verkaufspreis-Erfahrung** in der **Funktionsverwaltung** aktiviert. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Die meisten der neuen Erfahrungen mit Verkaufspreisen ähneln der aktuellen Erfahrung, es gibt jedoch einige Unterschiede. In den folgenden Abschnitten werden diese Unterschiede erläutert.

Die **Ausgleich mit Typ** und **Ausgleich mit Nummer** In den Feldern können Sie auswählen, für was eine Preisliste gelten soll, z. B. Debitor oder Debitorenpreisgruppe. Mit **Spalten anzeigen für** können Sie Spalten ein- oder ausblenden, die für das Festlegen von Preisen, Rabatten oder Preisen und Rabatten relevant sind.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Konvertieren vorhandener Preise, wenn Sie die Aktualisierung der Preisfunktion aktivieren
Wenn Sie das Funktionsupdate **Neue Verkaufspreis-Erfahrung** auf der Seite **Funktionsverwaltung** aktivieren, wird die Anleitung **Funktionsdatenupdate** geöffnet. Verwenden Sie den Umschalter **Standardpreise verwenden** wie folgt:

* Wenn Sie mit allen Preisen auf einer einzigen Seite arbeiten möchten, aktivieren Sie sie. Bestehende Preise werden in eine Standardpreisliste für jeden der folgenden Belege umgewandelt:

    * Verkauf
    * Einkauf
    * Projektumsätze
    * Projekteinkäufe 

    Sie können alle Preise für diese Regionen auf der Seite **Preise Arbeitsblatt** bearbeiten. Die Standardpreislisten werden auf den Seiten **Einrichtung von Verkäufen und Forderungen**, **Einrichtung von Käufen und Verbindlichkeiten** und **Projekteinrichtung** festgelegt. 

> [!NOTE]
> Wenn Preise nur für Artikel- oder Ressourcenkarten festgelegt sind, werden die Standardpreislisten während der Datenaktualisierung nicht mit diesen Preisen ausgefüllt. Sie können jedoch jede der Standardpreislisten oder die Seite Preisarbeitsblatt öffnen und die Aktion **Zeilen vorschlagen** nutzen, um die auf Artikel- oder Ressourcenkarten festgelegten Preise hinzuzufügen. 

* Um Verkaufspreislisten zu verwenden, deaktivieren Sie sie. Bestehende Preise werden für jede Kombination aus Debitor, Debitorengruppe oder Kampagne sowie Start- und Enddatum und Währung in eine neue Preisliste umgewandelt. Wenn Sie viele Kombinationen haben, haben Sie viele Preislisten.

Wenn Sie die neue Preisgestaltung bereits aktiviert haben, können Sie Standardpreislisten manuell erstellen oder eine vorhandene Preisliste als Standard angeben. Um eine vorhandene Preisliste als Standard festzulegen, aktivieren Sie den Schalter **Aktualisieren von Standardeinstellungen zulassen** auf der Preisliste. Setzen Sie dann auf den Seiten **Einrichtung von Verkäufen und Forderungen**, **Einrichtung von Käufen und Verbindlichkeiten** und **Projekteinrichtung** die Preisliste als standardmässig.

### <a name="editing-active-price-lists"></a>Bearbeiten der aktiven Preislisten
Damit Bearbeiter Preise in aktiven Preislisten für Artikel, Ressourcen, Debitoren, Kreditoren und andere Entitäten, die Preise verwenden, bearbeiten können, aktivieren Sie den Umschalter **Bearbeiten des aktiven Preises zulassen** auf den Seiten **Einrichtung von Verkäufen und Forderungen** und **Einrichtung von Käufen und Verbindlichkeiten**.   

Wenn der Umschalter **Bearbeiten des aktiven Preises zulassen** deaktiviert ist, müssen Sie, um Preise in einer Preisliste zu aktualisieren, den Status der Preisliste in **Entwurf** ändern, Ihre Änderung vornehmen und die Preisliste erneut aktivieren.

Die **Preisübersicht** Seite bietet eine Übersicht über alle Preise in Preislisten. Sie können Filter setzen, um die Preisliste einzugrenzen, die Sie ändern oder ergänzen möchten. Nachdem Sie die Preise geändert haben, verwenden Sie die Aktion **Zeilen überprüfen**, um die Preise mit anderen Preislistenzeilen zu vergleichen. Die Überprüfung von Preisen hilft, Duplikate und Mehrdeutigkeiten bei der Preisberechnung zu vermeiden. 

> [!NOTE]
> Wenn Sie eine Zeile in einer aktiven Preisliste bearbeiten, wird der Status der Zeile auf „Entwurf“ gesetzt, und die Zeile wird bei der Preisberechnung erst berücksichtigt, wenn Sie die Aktion **Zeilen überprüfen** verwenden. Nachdem Sie den Preis überprüft haben, wird der Status der Position Aktiv und in Preisberechnungen berücksichtigt.

Um neue Preise hinzuzufügen, verwenden Sie auf der Seite **Preisübersicht** die Aktion **Neue Zeilen hinzufügen**. Die Seite **Arbeitsblatt Preise** öffnet sich und Sie können Preiszeilen hinzufügen, indem Sie sie entweder anhand von Kriterien vorschlagen, aus anderen Preislisten kopieren oder manuell eingeben. Anschliessend können Sie mit der Aktion **Preisvorschlag übernehmen** die neuen Preise mit anderen Preislisten vergleichen, um Duplikate und Unklarheiten bei der Preisberechnung zu vermeiden.

## <a name="to-copy-sales-prices"></a>Verkaufspreise kopieren
Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte „Aktuelle Erfahrung“.

#### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience/)  

Falls Sie Verkaufspreise kopieren möchten, wie z. B. den Preis eines einzelnen Debitors, um ihn in einer Debitorengruppe zu verwenden, müssen Sie die Stapelverarbeitung **VK-Preis vorschlagen** ausführen. Stapelverarbeitung auf der Seite **VK-Preisarbeitsblatt**.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Verkaufspreisarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den **Vorgeschlagenen Verkaufspreis auf dem Arbeitsblatt.** Aktion  
3. Füllen Sie im Inforegister **Verkaufspreis** die Felder mit der **Verkaufsart** und dem **Verkaufscode** der ursprünglichen Preise aus, die Sie kopieren möchten.  
4. Füllen Sie im oberen Bereich der Anforderungsseite die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.  
5. Wenn Sie mit dem Batchauftrag neue Preise erstellen wollen, wählen Sie in das Feld **Neue Preise generieren**.  
6. Wählen Sie die Schaltfläche **OK**, um die Zeilen auf der Seite **VK-Preisarbeitsblatt** mit den neuen Preisvorschlägen auszufüllen, und geben Sie an, dass diese für die gewählte Verkaufsart gültig sind.  

   > [!NOTE]  
   > Die Stapelverarbeitung erzeugt nur Vorschläge, implementiert die vorgeschlagenen Änderungen aber nicht. Falls Sie die Vorschläge annehmen möchten, d. h. sie auf der Seite **VK-Preise** übernehmen möchten, können Sie die Aktion **Preisvorschlag übernehmen** verwenden, die Sie auf der Seite **VK-Preisarbeitsblatt** finden.

#### <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience/)  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Verkaufspreislisten** ein, und wählen Sie dann den zugehörigen Link. 
2. Wählen Sie die zu kopierende Preisliste aus und wählen Sie dann **Zeilen kopieren**.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Sie können nicht zwei Zeilen mit denselben Einstellungen, aber unterschiedlichen Preisen verwenden. In diesem Fall wird eine Meldung angezeigt, wenn Sie eine Preisliste aktivieren. Sie können den zu verwendenden Preis auswählen, indem Sie die Liste öffnen und den falschen Preis löschen.  
  
---

## <a name="to-bulk-update-item-prices"></a>So aktualisieren Sie Debitorenartikelpreise auf einmal
Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte „Aktuelle Erfahrung“.

#### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience/)

Wenn Sie Artikelpreise, wie alle Lagerzugangs-Artikelpreise durch einen Prozentsatz auf einmal aktualisieren möchten, müssen Sie Verkaufspreisarbeitsblatt mithilfe der folgenden Batchvorgänge ausfüllen:

* **VK-Preis vorschlagen** schlägt Änderungen vor, indem ein Anpassungsfaktor auf vorhandene Verkaufspreise angewendet oder vorhandene Verkaufspreisvereinbarungen auf andere Debitoren, Debitorpreisgruppen oder Verkaufsaktionen kopieren.
* **Artikelpreis auf dem Arbeitsblatt vorschlagen** Schlägt Änderungen vor, indem ein Anpassungsfaktor auf vorhandene Einheitspreise auf Artikelkarten angewendet wird oder indem Preise für neue Kombinationen von Währungen, Masseinheiten usw. vorgeschlagen werden. Die Stückpreise für Artikel werden durch diesen Batch-Job nicht geändert.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Verkaufspreisarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den **Vorgeschlagenen Verkaufspreis auf dem Arbeitsblatt.** Aktion  
3. Geben Sie auf dem Inforegister **Zeilen** im Feld **Artikelnummer** oder **Bestand-Buchungsgruppe** oder andere Felder mit den ursprünglichen Artikelpreisen aus, die Sie aktualisieren möchten ein.  
4. Füllen Sie im oberen Bereich der Anforderungsseite die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.
5. Wenn Sie möchten, dass die Stapelverarbeitung automatisch eingegeben wird, geben Sie Anpassung ein im Feld **Korrekturfaktor**. Beispielsweise geben Sie entsprechend 1.15 unter **Korrekturfaktor** für die Preiserhöhung für den Artikelpreis um 15% ein.  
6. Wenn Sie mit dem Batchauftrag neue Preise erstellen wollen, aktivieren Sie den Schalter **Neue Preise generieren**.  
7. Wählen Sie die Schaltfläche **OK**, um die Zeilen auf der Seite **Verkaufspreisarbeitsblatt** mit den vorgeschlagenen neuen Preisen auszufüllen.
8. Um die Vorschläge umzusetzen, verwenden Sie die Aktion **Preisänderungen implementieren**. Der Batch-Job erstellt Vorschläge, setzt diese jedoch nicht um. 

#### <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience/)

Um die Preise für mehrere Artikel zu aktualisieren, müssen Sie eine neue Preisliste erstellen und dann die Zeilen aus einer vorhandenen Preisliste kopieren. Wenn Sie die Zeilen kopieren, können Sie mithilfe von Filtern angeben, was kopiert werden soll, und Sie können eine Integer oder eine Dezimalzahl im Feld **Anpassungsfaktor** zum Erhöhen oder Verringern der Preise angeben. Die Preisliste muss sich im Status **Entwurf** befinden. Bei Bedarf können Sie dann die alte Preisliste deaktivieren.

> [!NOTE]
> Sie können nicht zwei Zeilen mit denselben Einstellungen, aber unterschiedlichen Preisen verwenden. In diesem Fall wird eine Meldung angezeigt, wenn Sie eine Preisliste aktivieren. Sie können den zu verwendenden Preis auswählen, indem Sie die Liste öffnen und den falschen Preis löschen.  

---

## <a name="best-price-calculation"></a>Beste Preisberechnung
Nachdem Sie Sonderpreise und Zeilenrabatte für Verkäufe und Käufe erfasst haben, sorgt [!INCLUDE[d365fin](includes/d365fin_md.md)] dafür, dass Ihre Gewinne immer optimal sind. Es berechnet den besten Preis für Verkaufs- und Einkaufsbelege sowie für Auftrags- und Artikelerfassungszeilen.

Der beste Preis ist der niedrigste mögliche Preis mit dem höchsten möglichen Zeilenskonto an einem bestimmten Datum. [!INCLUDE[d365fin](includes/d365fin_md.md)] berechnet die besten Preise, wenn Sie den Verkaufspreis und den prozentualen Zeilenrabatt für Artikel auf neuen Beleg und Erfassungsjournalzeilen eingefügt haben.

> [!NOTE]  
> Nachfolgend wird erläutert, wie die besten Preise für Verkäufe berechnet werden. Die Berechnung ist die gleiche wie für Einkäufe.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] prüft die Kombination aus Rechnungsempfänger und Artikel und wählt den entsprechenden Preis/Skonto unter Verwendung der folgenden Kriterien:

    - Hat dieser Debitor eine spezielle Vereinbarung für Preise oder Zeilenskonto oder gehört der Debitor zu einer Gruppe, die solche Vereinbarungen hat?
    - Ist der Artikel oder die Artikelskontogruppe in der Zeile in einer dieser Vereinbarungen enthalten?
    - Liegt das Auftragsdatum (oder das Buchungsdatum für die Rechnung und Gutschrift) innerhalb des Start- und Enddatums der Preis-/Zeilenskonto-Vereinbarung?
    - Wurde ein Einheitencode angegeben? Falls dies der Fall ist, prüft [!INCLUDE[d365fin](includes/d365fin_md.md)] Preise/Skonti mit dem gleichen Einheitencode und die Preise und Skonti, bei denen kein Einheitencode angegeben wurde.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] prüft, ob Preis-/Rabattvereinbarungen für Informationen auf der Beleg- oder Journalzeile gelten. Anschliessend fügt es den anwendbaren Einheitspreis und den Zeilenrabattprozentsatz unter Verwendung der folgenden Kriterien ein:

    - Gibt es eine Mindestanzahl in der Preis-/Skontovereinbarung, die erfüllt ist?
    - Gibt es eine Währungsanforderung in der Preis-/Skontovereinbarung, die erfüllt ist? In diesem Fall werden der niedrigste Preis und der höchste Zeilenskonto für diese Währung eingefügt, selbst wenn lokale Währung einen besseren Preis liefern würde. Falls es für den angegebenen Währungscode keine Preis-/Zeilenrabatte gibt, verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)] den niedrigsten Preis und den höchsten Zeilenrabatt in Ihrer lokalen Währung.

Wenn keine Spezialpreise für die Artikel in der Zeile gefunden werden, werden entweder letzte Einkaufspreis oder der VK-Preis von der Artikelkarte oder der Lagerhaltungsdatenkarte verwendet.

## <a name="sales-invoice-discounts-and-service-charges"></a>Verkaufsrechnungsskonti und Zuschläge
Wenn Sie Rechnungsskonti verwenden, bestimmt der Gesamtbetrag des Rechnungsbetrages die Höhe des Skontos, der gewährt wird. Auf der Seite **Debitorenrechnungsrabatte** können Sie einen Zuschlag für Rechnungen über einem bestimmten Betrag einrichten.  

Bevor Sie Rechnungsrabatte mit Verkäufen verwenden können, müssen Sie einige Informationen in der Anwendung definieren. Sie müssen Folgendes entscheiden:  

- Welchen Debitoren diese Art von Rabatt gewährt wird?  
- Welche Rabattprozentsätze Sie verwenden möchten?  

Wenn Sie Rechnungsskonti automatisch berechnen möchten, aktivieren Sie auf der Seite **Debitoren & Verkauf Einr.** den Umschalter für **Rechnungsskonto berechnen**.  

Für jeden Debitor können Sie festlegen, ob Sie Rechnungsrabatte gewähren, wenn eine Rechnung bestimmte Kriterien erfüllt. Zum Beispiel, wenn der Rechnungsbetrag gross genug ist. Rechnungsrabatte können in Landeswährung für inländische Debitoren oder in Fremdwährung für ausländische Debitoren gewährt werden.  

Sie verknüpfen Rabattprozentsätze mit bestimmten Rechnungsbeträgen auf den Seiten **Debitorenrechnungsrabatte** für jeden Debitor. Sie können eine beliebige Anzahl von Prozentsätzen auf jeder Seite eingeben. Jeder Debitor kann eine eigene Seite haben, oder Sie können verschiedene Debitoren mit der gleichen Seite verknüpfen.  

Zusätzlich (oder anstatt) eines Skontoprozentsatzes können Sie einen Zuschlag mit einem bestimmten Rechnungsbetrag verknüpfen.  

> [!TIP]  
> Bevor Sie diese Informationen eingeben, ist es sinnvoll, eine Skizze der Skontostruktur vorzubereiten, die Sie verwenden möchten. Dadurch wird es Ihnen erleichtert, zu erkennen, welche Debitoren mit derselben Rechnungsskontoseite verknüpft werden können. Wenn Sie weniger Seiten einrichten müssen, können Sie die Basisinformationen schneller eingeben.

Weitere Informationen zur Schulung für Skonti bei Verkäufen finden Sie unter [Einrichten von Skonti für Ihre Kunden](/learn/modules/customer-discounts-dynamics-365-business-central/index) unter Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Rechnungsskonti bei Verkäufen berechnen

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>So erstellen Sie Verkaufszeilenskonti für einen Debitor:
Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte „Aktuelle Erfahrung“.

#### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience/)  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Zeilenskonti**.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

> [!Note]
> Wenn Sie die Seiten **Verkaufspreise** und **Verkaufszeilenskonti** von einem bestimmten Debitoren öffnen, werden die Felder **Verkaufsartfilter** und **Verkaufscodefilter** für den Debitor festgelegt und können nicht geändert oder entfernt werden.
>
> Um Preise oder Zeilenskonti für alle Debitoren, eine Debitorenpreisgruppe oder Kampagne einzurichten, müssen Sie die Seiten von einer Artikelkarte aus öffnen. Verwenden Sie alternativ für Verkaufspreise die Seite **Verkaufspreis-Arbeitsblatt**. Weitere Informationen finden Sie unter [So führen Sie eine Sammelaktualisierung von Artikelpreisen durch](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience/)  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Debitor und wählen Sie dann die Aktion **Verkaufspreislisten**.
3. Öffnen Sie die Preisliste, für die der Zeilenskonto angegeben werden soll.
4. Erstellen Sie eine neue Zeile oder wählen Sie eine vorhandene Zeile aus und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Wählen Sie im Feld **Definiert** entweder **Preis und Skonto** oder einfach **Skonto**. 
6. Legen Sie im Feld **Zeilenskonto %** den Skontoprozentsatz fest.

    > [!TIP]
    > Wenn Sie eine vorhandene Zeile bearbeiten, können Sie die Zeilen filtern, indem Sie die entsprechende Option im Feld **Spalten anzeigen für** auswählen.

    > [!NOTE]  
    > Rechnungsskontocodes werden durch Bestandskundenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsskontobedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt. Um kundenspezifische Rechnungsskontobedingungen einzurichten, setzen Sie das Feld **Rechnungs-Skonto-Code** auf den Kundencode des Kunden und fahren Sie dann mit dem nächsten Schritt fort.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Um RechnungsSkontokonditionen für Einkäufe einzurichten:
Nachdem Sie entschieden haben, welche Kunden für Rechnungsrabatte in Frage kommen, geben Sie den Rechnungsrabattcode auf den Debitorenkartenseiten ein. Legen Sie dann die Bedingungen für jeden Code fest.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Debitorenseite für einen Debitor, der für Rechnungsskonti in Frage kommt.
3. Geben Sie im Feld **Rechnungsskontocode** einen Code für das jeweilige Rechnungsskontofenster ein, das die Anwendung verwenden soll, um Rechnungsskonti für den Debitor zu berechnen. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Rechnungsskontocodes werden durch Bestandskundenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsskontobedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt.

Fahren Sie fort, um neue Verkaufsrechnungsskonto-Bedingungen einzurichten.

1. Auf der Seite **Debitoren** wählen Sie die Aktion **Rechnungsskonto** aus. Die Seite **Debitorenrechnungsskonti** wird geöffnet.
2. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die RechnungsSkontokonditionen gelten sollen. Wenn Sie RechnungsSkontobedingungen in EUR einrichten möchten, dann lassen Sie das Feld leer.
3. Geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Skonto in Frage zu kommen.
4. Geben Sie im Feld **Skonto** den Rechnungsskonto als Prozentsatz des Rechnungsbetrages ein.
5. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Debitor einen Rechnungsskonto erhält.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Weitere Informationen

[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]