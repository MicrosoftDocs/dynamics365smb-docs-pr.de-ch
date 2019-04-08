---
title: Info zum Einrichten der Mehrwertsteuer | Microsoft Docs
description: Überprüfen Sie, ob Sie die MwSt für Verkäufe und Einkäufe korrekt berechnen, buchen und melden.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 5f22880f56cd2834c9bd92061f166cd457bc58c1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "819270"
---
# <a name="setting-up-calculations-and-posting-methods-for-value-added-tax"></a>Methoden für die Berechnung und Buchung der Salestax einrichten
Verbraucher und Geschäfte bezahlen Mehrwertsteuer (MwSt), wenn Sie Waren oder Dienstleistungen einkaufen. Der zu bezahlende MwSt-Betrag kann abhängig von verschiedenen Faktoren variieren. In [!INCLUDE[d365fin](includes/d365fin_md.md)], müssen Sie die MwSt einrichten, um die Werte anzugeben, die verwendet werden soll, um die Steuerbeträge auf folgender Grundlage zu berechnen:

* An wen Sie verkaufen  
* Von wem Sie kaufen  
* Was Sie verkaufen  
* Was Sie kaufen  

Sie können die Berechnungen der MwSt manuell einrichten, aber das kann heikel und zeitaufwendig sein. Damit es möglichst einfach ist, stellen wir Ihnen einen Anleitungsfaden **MwSt.-Einrichtung** bereit, der Sie durch die einzelnen Schritte führt. Es wird empfohlen, dass Sie diesen Einrichtungsleitfaden verwenden, um die MwSt einzurichten.

> [!NOTE]  
>   Hinweis: Sie können den Leitfaden nur nutzen, wenn Sie eine "Meine Unternehmen" erstellt haben, und keine Transaktionen gebucht haben, die MWST beinhalten. Sonst wäre es sehr einfach, versehentlich unterschiedliche Mehrwertsteuersätze zu verwenden und mit Mehrwertsteuer verknüpfte Berichte würden ungenau.  

Wenn Sie MwSt-Berechnungen einrichten möchten oder einfach mehr über jeden Schritt erfahren möchten, enthält dieses Thema Beschreibungen jedes Schrittes.

## <a name="to-use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Es wird empfohlen, dass Sie die unterstützte Einrichtung verwenden, um die MwSt einzurichten.
Es wird empfohlen, dass Sie die unterstützte Einrichtung der MwSt verwenden, um die MwSt in [!INCLUDE[d365fin](includes/d365fin_md.md)]einzurichten.

Um die unterstützte Einrichtung zu starten, gehen Sie folgendermassen vor:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Unterstütztes Setup** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie **MwSt Einrichtung** aus.

## <a name="to-set-up-vat-registration-numbers-for-your-country-or-region"></a>MwSt-IdNr. für Ihr Land oder Region einrichten
Um zu helfen sicherzustellen, dass Personal gültige MwSt-IdNr. eingeben, können Sie die MwSt-IdNr für die Länder oder die Bereiche verwenden, in denen Sie Geschäfte tätigen. [!INCLUDE[d365fin](includes/d365fin_md.md)] zeigt eine Fehlermeldung an, wenn jemand einen Fehler macht oder ein Format verwendet, das für das Land bzw. die Region falsch ist.

Um MwSt-Nr. einzurichten, gehen Sie folgendermassen vor:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Länder/Regionen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie das Land bzw. die Region, und wählen die **MwSt Reg. Nr. Formaten** Aktion aus.
3. Im Feld **Formate** definieren Sie das Format, indem Sie einen oder mehrere der folgenden Zeichen eingeben:  

* **#** Erfordert eine einstellige Nummer.  
* **@** Erfordert einen Buchstaben. Die Gross-/Kleinschreibung muss für den Text nicht beachtet werden.  
* **?** Erlaubt jegliches Zeichen.  

    > [!Tip]
    > Sie können andere Zeichen verwenden, sofern sie immer im Land- oder Bereichsformat vorkommen. Wenn Sie beispielsweise eine Periode oder einen Bindestrich zwischen und Nummern einfügen möchten, können Sie ##.####.### oder @@-###-### definieren.  

## <a name="to-set-up-vat-business-posting-groups"></a>MWST.-Geschäftsbuchungsgruppen einrichten:
MWST.-Geschäftsbuchungsgruppen sollten die Märkte darstellen, in denen Sie Geschäfte mit Debitoren und Kreditoren tätigen, und definieren, wie die Mehrwertsteuer in jedem Zielmarkt berechnet und gebucht werden. Beispiele von MwSt.-Produktbuchungsgruppen sind **Inland** und **Europäischen Union (EU)**.  

Verwenden Sie aussagekräftige Codes, an die Sie sich leicht erinnern können, z. B. **EU** **Nicht-EU** oder **Inland**. Dieser Code muss eindeutig sein. Sie können beliebig viele Codes einrichten, aber es ist nicht möglich, denselben Code zweimal in einer Tabelle zu verwenden.

Um eine MWST.-Geschäftsbuchungsgruppe einzurichten, gehen Sie folgendermassen vor:

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MwSt Business Buchungsgruppe** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.

Sie richten Vorgabe MWST-Geschäftsbuchungsgruppen ein, indem Sie sie mit den Geschäftsbuchungsgruppen verbinden. [!INCLUDE[d365fin](includes/d365fin_md.md)] fügt automatisch die MwSt Geschäftsbuchungsgruppe hinzu, wenn Sie die Geschäftsbuchungsgruppe einem Debitor, Kreditor oder Sachkonto zuweisen.

## <a name="to-set-up-vat-product-posting-groups"></a>MWST.-Produktbuchungsgruppen einrichten:
Mithilfe der MWST.-Produktbuchungsgruppencodes wird die Berechnung und Buchung der MWST. gemäss der Art des gekauften Artikels oder der Art der verkauften Ressourcen bestimmt.  
Es ist sinnvoll, Codes zu verwenden, an die man sich einfach erinnern kann, und die die Werte, wie **Keine MwSt** oder **Null**, **MwSt** oder **Reduziert** für 10% MwSt beschreiben, und **MwSt 25** oder **Standard** für 25% zu verwenden.

Um eine MWST.-Geschäftsbuchungsgruppe einzurichten, gehen Sie folgendermassen vor:

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MwSt Business Buchungsgruppen** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinieren Sie MWST-Produktbuchungsgruppen in der MWST-Einrichtung
[!INCLUDE[d365fin](includes/d365fin_md.md)] berechnet MwSt.-Beträge in Verkaufs- und Einkaufsberichten basierend auf MwSt.-Buchungsmatrix Einrichtung, die Kombinationen von Mehrwertsteuergeschäfts und -Produktbuchungsgruppen sind. Für jede Kombination können Sie den MWST.-Prozentsatz, die MWST.-Berechnungsart und die Fibupostennummern für die Buchung der MWST. für Verkäufe, Käufe und Erwerbssteuer eingeben. Sie können auch angeben, ob die MWST. neu berechnet wird, wenn Skonto angewandt oder erhalten wird.  

Sie können beliebig viele Codes einrichten. Wenn Sie MwSt.-Buchungsmatrixeinrichtungen mit ähnlichen Attributen in Gruppen zusammenfassen möchten, können Sie für jede Gruppe ein **MwSt.-Kennzeichen** erstellen und das Kennzeichen dann den Gruppenmitgliedern zuweisen.

Um MWST.-Buchungseinrichtungen zu kombinieren, gehen Sie folgendermassen vor:

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MWST Buchungsmatrix Einr.** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-assign-vat-posting-groups-by-default-to-multiple-entities"></a>Weisen Sie mehreren Gruppen MWST-Buchungsgruppen standardmässig zu
Wenn Sie identische MwSt.-Buchungsgruppen für mehrere Einheiten übernehmen möchten, können Sie [!INCLUDE[d365fin](includes/d365fin_md.md)]festlegen, um dies standardmässig durchzuführen. Es gibt mehrere Möglichkeiten, dies zu tun:

* Sie können MWST.-Geschäftsbuchungsgruppen allgemeinen Geschäftsbuchungsgruppen oder Debitoren- oder Kreditorenvorlagen zuweisen.
* Sie können MWST.-Produktbuchungsgruppen allgemeinen Produktbuchungsgruppen zuweisen  

Die MwSt- Geschäfts- oder - Produktbuchungsgruppe wird zugewiesen, wenn Sie eine Geschäfts- oder eine Produktbuchungsgruppe für einen Debitor, einen Kreditor, einen Artikel oder eine Ressource auswählen.

## <a name="to-assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>Weisen Sie MWST-Buchungsgruppen einzelnen Konten, Debitoren, Kreditoren, Artikeln und Ressourcen zu
Die folgenden Abschnitten beschreiben, wie die MWST.-Buchungsgruppen einzelnen Einheiten zugewiesen werden.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>So weisen Sie MWST.-Buchungsgruppen einzelnen Fibukonten zu
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.  
2. Öffnet Sie die **Sachkontokarte** für das Konto.  
3. Wählen Sie im Inforegister **Buchen** im Feld **Buchungsart** entweder **Verkauf** oder **Einkauf** aus.  
5. Wählen Sie die MWST.-Buchungsgruppen aus, die Sie für das Verkaufs- bzw. das Wareneingangskonto verwenden möchten.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Um MwSt-Geschäftsbuchungsgruppen Debitoren und Kreditoren zuzuweisen  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") geöffnet wird. Geben Sie **Debitor** oder **Verkäufer** ein und wählen Sie den zugehörigen Link aus.  
2. Auf der Karte **Kunde** oder **Debitor** erweitern Sie das Inforegister **Fakturierung**.  
3. Wählen Sie die MwSt-Geschäftsbuchungsgruppe aus.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Um MwSt-Produktbuchungsgruppen einzelnen Artikeln und Ressourcen zuzuweisen  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") geöffnet wird. Geben Sie **Artikel** oder **Ressource** ein und wählen Sie den zugehörigen Link aus.  
2. Führen Sie einen der folgenden Schritte aus:  

* Auf der Karte **Artikel** erweitern Sie das Inforegister **Preis und Buchung**, und wählen Sie dann **Mehr anzeigen**, um das Feld **MwSt Produktbuchungsgruppe** anzuzeigen.  
* Erweitern Sie auf der Karte **Ressource** das Inforegister **Fakturierung**.  
3. Wählen Sie die MwSt-Produktbuchungsgruppe aus.  

## <a name="setting-up-vat-statement-templates-and-vat-statement-names"></a>Einrichtung von MWST-Abrechnung Vorlagen und - Abrechnung
Steuerbehörden kann Anforderungen für die Buchung der MWST ändern und ändert diese auch. **MWST-Abrechnung Vorlagen** und **MWST-Abrechnung** können dabei behilflich sein, für ausstehende Änderungen das Vorbereiten und einen fliessenden Übergang mit den neuen Anforderungen zu erstellen. Sie können MWST-Abrechnungs-Vorlagen verwenden, um die Felder festzulegen, um in der MWST-Abrechnung zu berücksichtigen, die wiederum die Berechnungen definieren, und Sie können eine neue MWST-Abrechnung Vorlage erstellen, wenn Anforderungen ändern. Beispielsweise kann eine Vorlage die MwSt für dieses Jahre auf dem aktuellen Bedarf berechnen, und eine andere kann MwSt basierend auf Anforderungen für das nächste Jahr berechnen. Vorlagen sind auch eine Art, Aufzeichnungen von MWST-Abrechnungs-Formaten zu behalten, beispielsweise damit Sie prüfen können, wie Sie die MWST in Vorjahren berechnet haben.

## <a name="how-to-define-and-preview-vat-statements"></a>Erstellen von MWST-Abrechnungen definieren und MWST Bericht anzeigen
MWST-Abrechnungen lassen Sie den MWST-Abrechnungsbetrag für eine bestimmte Periode berechnen (zum Beispiel ein Quartal). Nachdem Sie eine MWST-Abrechnung eingeben haben, können Sie diese in der Vorschau anzeigen, um sicherzustellen, dass sie die Anforderungen erfüllt.

Um eine MWST-Abrechnung festzulegen, gehen Sie folgendermassen vor:

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MWST-Auszug** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie das Feld **Name**, und wählen Sie dann **Neu** auf der Seite **MWST-Abrechnungsnamen** aus.
3. Füllen Sie die entsprechenden Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!Tip]
> Sie können die Informationen setzen, die in der Abrechnung enthalten sind, je nachdem, was Sie im Feld **Art** auswählen. **Kontosumme** ist hilfreich, wenn Sie die MwSt von einem bestimmten Konto möchten.
**MWST-Summe** ruft die MWST der Konten ab, die zur Auswahl auf **Buchungsart**, **MWST Bus. Buchungsgruppe** und/oder den Feldern **MWST Prod. Buchungsgruppe** zugeordnet werden. **Rubrikensumme** ermöglicht Ihnen die Eingabe von einem schnellen Filterkriterium oder Wert im Feld **Rubrikensumme**. Weitere Informationen finden Sie unter [Suchen, filtern und sortieren von Daten](ui-enter-criteria-filters.md). **Beschreibung** ist oft verwendet, um eine Benachrichtigung der Abrechnung hinzuzufügen. Sie könnten sie beispielsweise als Überschrift verwenden, wenn Sie Zeilenzusammenzählung verwendet haben.

Um eine MWST-Abrechnung anzuzeigen, gehen Sie folgendermassen vor:

1. Wählen Sie **Vorschau** aus.
2. Geben Sie einen Datumsfilter ein, um die Abrechnung auf einen bestimmten Zeitraum zu begrenzen. Weitere Informationen darüber, wie die Seite anpassen, damit der Datumsfilter angezeigt wird, finden Sie unter [Daten suchen, filtern und sortieren](ui-enter-criteria-filters.md).
3. Sie können verschiedene Optionen wählen, um die Art der MWST-Posten zu bestimmten, die in der Abrechnung enthalten sein sollen.
4. Für die Zeilen, für die im Feld **Art** der Eintrag **MWST-Summe** angezeigt wird, kann eine Liste der MWST-Posten angezeigt werden, wenn Sie im Feld **Spaltenbetrag** den Betrag auswählen.   

## <a name="to-set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Einrichten von Klauseln, um die Verwendung von nichtstandardisierten MWST-Sätzen zu erklären
Sie richten eine MWST-Klausel ein, um Informationen über die Art der MWST zu beschreiben, die angewendet wird. Die Informationen werden möglicherweise aufgrund behördlicher Regulierungen verlangt. Nachdem Sie eine MWST.-Klausel festgelegt und sie einer MWST.-Buchungsmatrix zugeordnet haben, wird die MWST.-Klausel in allen gedruckten Verkaufsbelegen, die diese MWST.-Buchungsmatrix Einrichtungsgruppe haben, wie etwa eine Verkaufsrechnung, angezeigt.

Bei Bedarf können Sie auch festlegen, wie Mehrwertsteuerklauseln in andere Sprachen übersetzt werden. Wenn Sie dann für einen Debitor einen Verkaufsbeleg erstellen und ausdrucken, der ein MWST.-Kennzeichen enthält, enthält der gedruckte Beleg die MWST.-Klausel in übersetzter Form. Der Sprachcode, der auf der Debitorenkarte angegeben ist, bestimmt die Sprache.

Sie können eine MWST-Klausel ändern oder löschen, und Ihre Änderungen werden in einem generierten Bericht angezeigt. [!INCLUDE[d365fin](includes/d365fin_md.md)] bewahrt jedoch keinen Verlauf der Änderung auf. In dem Bericht werden die MWST-Klauselbeschreibungen für alle Zeilen im Bericht neben dem MWST-Betrag und MWST-Basisbetrag gedruckt und angezeigt. Wenn eine MWST-Klausel nicht für eine oder mehrere Zeilen des Verkaufsbelegs festgelegt wurde, wird der gesamte Abschnitt weggelassen, wenn der Bericht gedruckt wird.

### <a name="to-set-up-vat-clauses"></a>Einrichten von MWST.-Klauseln
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MWST-Auszug** ein, und wählen dann den zugehörigen Link aus.  
2. Auf der Seite **MwSt.-Klauseln** erstellen Sie eine neue Zeile.  
3. Geben Sie im Feld **Code** eine Kennung für die Klausel ein. Nutzen Sie diesen Code, um die Klausel der MwSt-Buchungsgruppe zuzuweisen.  
4. In dem Feld **Beschreibung** geben Sie den Text ein, der auf Belegen angezeigt wird, die MwSt enthalten können. Geben Sie im Feld **Beschreibung 2**zusätzlichen Text ein, falls erforderlich. Den Text auf neuen Zeilen anzeigen.  
5. Optional: Um die Mehrwertsteuerklausel mit einer MwSt.-Buchung sofort zuzuordnen, wählen Sie **Einrichtung** und dann die Klausel. Wenn Sie warten möchten, können Sie die Klausel später der MWST.-Buchungsseite zuweisen.  
6. Optional: Um zu bestimmen wie die Mehrwertsteuerklausel übersetzt wird, wählen Sie die Aktion **Übersetzungen**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>So weisen Sie eine MWST.-Klausel einer Buchungsgruppe zu
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MWST Buchungsmatrix Einr.** ein, und wählen dann den zugehörigen Link aus.  
2. In der Spalte **MwSt.-Klausel** wählen Sie die Klausel, die für jede MwSt.-Buchungseinrichtung gilt.  

### <a name="to-specify-translations-for-vat-clauses"></a>Um Beschreibungen für Mehrwertsteuerklauseln festzulegen
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MWST-Auszug** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Übersetzung** aus.  
3. Im **Sprachcode** Feld wählen Sie die Sprache aus, in die Sie übersetzen.  
4. Geben Sie in den Feldern **Beschreibung**und **Beschreibung 2**den Text ein, der eine Übersetzung der Beschreibungen ist. Dieser Text wird in den übersetzten MWST.-Berichten angezeigt.  

## <a name="to-create-a-vat-posting-setup-to-handle-import-vat"></a>Erstellen Sie eine MWST-Buchungsmatrix, um Einfuhrumsatzsteuer zu verarbeiten
Die Einfuhrumsatzsteuerfunktion wird verwendet, wenn Sie einen Beleg buchen müssen, dessen gesamter Betrag als MWST. zu betrachten ist. Sie sehen dies, wenn Sie eine MWST-Rechnung für importierte Waren von der Steuerbehörde erhalten.  

Gehen Sie folgendermassen vor, um Codes für die Einfuhrsteuerfelder festzulegen:  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MwSt Business Buchungsgruppen** ein, und wählen dann den zugehörigen Link aus.  
2. Auf der Seite MWST Produktbuchungsgruppe richten Sie eine neue MWST.-Produktbuchungsgruppen für Einfuhrsteuer ein.  
3. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MWST Buchungsmatrix Einr.** ein, und wählen dann den zugehörigen Link aus.  
4. Auf der Seite MWST Buchungseinrichtung erstellen Sie eine neue Zeile oder nutzen einen bestehende MWST-Buchungsgruppe in Kombination mit der neuen MWST.-Produktbuchungsgruppe für die Einfuhrsteuer.  
5. Wählen Sie im Feld **MwSt.-Berechnungsart** **Volle MwSt.** aus.  
6. Geben Sie im Feld **Vorsteuerkonto** das Sachkonto an, auf das Sie Einfuhrumsatzsteuer buchen wollen. Alle anderen Konten sind optional.  

## <a name="to-verify-vat-registration-numbers"></a>MwSt-IdNr. prüfen
Es ist wichtig, dass die MWST Nummern, die Sie für Debitoren, Kreditoren und Kontakte haben, gültig sind. Beispielsweise ändern Mandanten ihren Steuerschuldstatus, und in einigen Ländern verlangen die Steuerbehörde möglicherweise Berichte, wie der EU-Verkaufslistes-Bericht, der die MwsT-IdNr., aufführt, die Sie verwenden, wenn Sie Geschäftsbeziehungen unterhalten.

Die Europäische Berechnung stellt den MwSt Nummern-Überprüfungsdienst auf der Website bereit, der öffentlich und frei ist. [!INCLUDE[d365fin](includes/d365fin_md.md)] kann Ihnen diesen Schritt ersparen und Sie können den VIES-Dienst nutzen, um MwSt. Nummern für Debitoren, Kreditoren und Kontakte direkt vom Debitor, Kreditor und den Kontaktkarten zu prüfen und nachzuverfolgen. Der Service in [!INCLUDE[d365fin](includes/d365fin_md.md)] wird **EU MwSt Reg.Nr. Validierungsservice** genannt. Er ist auf der Seite **Dienstverbindungen** verfügbar, und Sie können ihn sofort nutzen. Der Service ist frei und die Anmeldung ist nicht erforderlich.

> [!Note]
> Um den MwSt Reg. Nr. Überprüfungs-Dienst zu aktivieren, müssen Sie Administratorrechte haben.

Wenn Sie unseren Service verwenden, erfassen wir eine Historie der MwSt.-Nummern und Überprüfungen für jeden Debitor, Kreditor oder Kontakt im **MwSt-Registrierungsprotokoll**, damit Sie diese einfacher verfolgen können. Das Protokoll ist auf jeden Debitor zugeschnitten. Beispielsweise ist das Protokoll für die Prüfung hilfreich, dass Sie geprüft haben, dass die aktuelle Mehrwertsteuernummer korrekt ist. Wenn Sie eine Mehrwertsteuernummer überprüfen, spiegelt der **Anforderungs-Bezeichner** im Protokoll, dass Sie Aktionen ausgeführt haben.

Sie finden das MWST-Registrierungsprotokoll auf den Karten Kunde, Kreditor oder Kontakt, auf dem Inforegister **Rechnungsstellung**, indem Sie im Feld **MWST-Nr.** die Suchschaltfläche wählen.  

Mit dem Service sparen Sie auch Zeit, wenn Sie einen Kreditor oder Debitor erstellen. Wenn Sie die MWST-Nummer des Kunden kennen, können Sie sie in das Feld **MWST-Nr.** auf den Karten Kunde oder Kreditor eintragen. Wir tragen den Kundennamen für Sie ein. Einige Länder liefern auch Mandantenadressen in einem strukturierten Format. In jenen Ländern ergänzen wir auch die Adresse.  

Es gibt mehrere Dinge zu beachten bezüglich dem VIES MwSt Überprüfungsservice:

* Dieser Webdienst verwendet das HTTP-Protokoll, d. h., dass die Daten, die durch den Service übertragen werden, nicht verschlüsselt werden.  
* Sie erfahren möglicherweise Ausfallzeiten für den Service, für die Microsoft nicht verantwortlich ist. Der Service ist Teil eines EU-Netzwerks eines nationalen MwST-Registers.

## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Verwenden Sie Erwerbsbesteuerung für den Handel zwischen EU-Ländern/-Regionen
Gewisse Unternehmen müssen Erwerbssteuer abführen, wenn Sie Handel mit anderen Ländern innerhalb der EU betreiben. Die Regel gilt beispielsweise für Einkäufe aus EU-Ländern/-Regionen und Verkäufe an EU-Länder/-Regionen.  

> [!NOTE]  
> Diese Regel gilt für den Handel mit Unternehmen, die in einem anderen EU-Land/in einer anderen EU-Region als umsatzsteuerpflichtig registriert sind. Wenn Sie direkt mit Verbrauchern in anderen EU-Ländern/-Regionen Geschäfte tätigen, sollten Sie sich bei den Salestaxbehörden über die geltenden Regeln für die MWST. informieren.  

> [!TIP]  
> Sie können überprüfen, ob ein Unternehmen als umsatzsteuerpflichtig registriert ist, wenn Sie den EU-MWST-Nummer-Überprüfungsdienst verwenden. Der Service ist in [!INCLUDE[d365fin](includes/d365fin_md.md)] kostenlos verfügbar. Weitere Informationen finden Sie im Abschnitt _MwSt-Registrierungsnummern in diesem Thema_.

### <a name="sales-to-eu-countries-or-regions"></a>Verkäufe in EU-Länder oder Regionen
Auf Verkäufe an umsatzsteuerpflichtige Unternehmen in anderen EU-Ländern/-Regionen wird keine MWST berechnet. Der Wert derartiger Verkäufe an EU-Länder/-Regionen muss separat auf der MWST.-Abrechnung ausgewiesen werden.  

Um MWST. bei Verkäufen in EU-Länder/-Regionen korrekt zu berechnen, gehen Sie folgendermassen vor:  

* Richten Sie eine Zeile für Verkäufe mit den gleichen Informationen ein, wie zuvor für Einkäufe beschrieben. Wenn im Fenster MWST Buchungsmatrix Einr. bereits Zeilen für Einkäufe aus EU-Ländern/-Regionen eingerichtet wurden, können Sie diese Zeilen auch für Verkäufe verwenden.  
* Weisen Sie die MWST.-Geschäftsbuchungsgruppen im Feld **MWST.-Geschäftsbuchungsgruppe** auf dem Inforegister **Fakturierung** der Debitorenkarte jedes EU-Debitors zu. Sie sollten auch die USt-IdNr. des Debitors im Feld **USt-IdNr.** im Inforegister **Aussenhandel** eingeben.  

Wenn Sie einen Verkauf an einen Debitor in einem anderen EU-Land/einer anderen EU-Region buchen, wird der MWST.-Betrag berechnet und ein MWST.-Posten mit Informationen zur Erwerbssteuer und zur MWST.-Bemessungsgrundlage (der zur Berechnung der MWST. verwendete Betrag) erstellt. Auf die MWST-Konten in der Finanzbuchhaltung werden keine Posten gebucht.

## <a name="understanding-vat-rounding-for-documents"></a>Machen Sie sich mit der MWST.-Rundung für Belege vertraut.
Beträge in Belegen, die noch nicht gebucht sind, werden gerundet und auf eine Weise angezeigt, die der endgültigen Rundung bereits gebuchter Beträge entspricht. Die MWST wird für einen vollständigen Beleg berechnet, d.h., dass MWST, die in dem Beleg berechnet wird, auf der Summe aller Zeilen mit derselben MWST-ID im Beleg basiert.

## <a name="understanding-the-vat-rate-conversion-process"></a>Verstehen des Prozesses der Umrechnung für die MWST.-Satzänderung  
Die das MWST-Änderungstool führt MWST-Konvertierungen für Masterdaten, Erfassungsjournale und Aufträge auf verschiedene Arten aus. Die ausgewählten Masterdaten und die Erfassungsjournale werden von der neuen Produktbuchungsgruppe oder der MWST.-Produktbuchungsgruppe aktualisiert. Wenn eine Bestellung vollständig oder teilweise geliefert wurde, behalten die gelieferten Artikel die aktuelle Produktbuchungsgruppe oder MWST.-Produktbuchungsgruppe. Eine neue Auftragszeile wird für die nicht gelieferten Artikel erstellt und aktualisiert, um aktuelle und neue Produktbuchungsgruppen oder MWST.-Produktbuchungsgruppen aufeinander auszurichten. Darüber hinaus werden Artikelzu-/-abschlagszuweisungen, Reservierungen und Artikeltrackinginformationen entsprechend aktualisiert.  

Es gibt jedoch mehrere Elemente, die das Werkzeug nicht konvertiert:

* Verkaufs- oder Einkaufsbestellungen und -rechnungen, in denen Lieferungen gebucht wurden. Diese Belege werden unter Verwendung des aktuellen Mehrwertsteuersatzes gebucht.  
* Belege mit gebuchten Vorauszahlungsrechnungen. Beispielsweise haben Sie Vorauszahlungen auf Rechnungen geleistet oder erhalten, die nicht vollständig erledigt sind, bevor Sie das Mehrwertsteuersatz-Änderungstool verwenden. In diesem Fall gibt es eine Differenz zwischen der MWST., die fällig ist, und der MWST., die in den Vorauszahlungen bezahlt wurde, wenn die Rechnung abgeschlossen wird. Das Mehrwertsteuersatz-Änderungstool überspringt diese Belege, und Sie müssen sie manuell aktualisieren.  
* Direktlieferungen oder Spezialaufträge.  
* Verkaufs- oder Einkaufsbestellungen mit Lagerintegration, wenn sie teilweise geliefert oder erhalten werden.  
* Serviceverträge.  

### <a name="to-prepare-vat-rate-change-conversions"></a>So bereiten Sie Mehrwertsteuersatzänderungen vor  
Bevor Sie das Mehrwertsteuersatz-Änderungstool einrichten, müssen Sie die folgenden Vorbereitungen durchführen.

* Wenn Sie Transaktionen haben, die verschiedene Sätze verwenden, müssen sie in verschiedene Gruppen aufgeteilt werden, entweder durch Erstellen neuer Sachkonten für die einzelnen Sätze oder mithilfe von Datenfiltern, um Transaktionen entsprechend dem Satz zu gruppieren.  
* Wenn Sie neue Sachkonten erstellen, müssen Sie auch neue allgemeine Buchungsgruppen erstellen.  
* Um die Anzahl der Belege zu verringern, die konvertiert werden, buchen Sie möglichst viele Belege, und reduzieren Sie nicht gebuchte Belege auf ein Minimum.  
* Sichern von Daten.

### <a name="to-set-up-the-vat-rate-change-tool"></a>So richten Sie das Mehrwertsteuersatz-Änderungstool ein  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MWST-Satzänderung einrichten** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie auf den Inforegistern **Masterdaten**, **Buch.-Erfassungsjournale** und **Belege** einen Buchungsgruppenwert aus der Liste der Optionen für erforderliche Felder aus.  

### <a name="to-set-up-product-posting-group-conversion"></a>So richten Sie die Produktbuchungsgruppenkonvertierung ein  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MWST-Satzänderung einrichten** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **MWST-Satzänderung einrichten** auf der Registerkarte **Start** in der Gruppe **Prozess** entweder **Umrech. für MWST-Produktbuchungsgruppe** oder **Umrech. für Produktbuchungsgruppe** aus.  
3. Geben Sie im Feld **Code ab** die aktuelle Buchungsgruppe ein.  
4. Geben Sie den neuen Standort in dem Feld **Cod zu** ein.  

### <a name="to-perform-vat-rate-change-conversion"></a>So führen Sie eine Umrechnung für die MWST.-Satzänderung aus  
Sie verwenden das MwSt.-Satz-Änderungstool, um Änderungen im Standard-MwSt.-Satz zu verwalten. Sie führen MwSt.- und Buchungsgruppenkonvertierungen durch, um Mehrwertsteuersätze zu ändern und für präzise MwSt.-Berichte zu sorgen. Abhängig von Ihrem Setup werden folgende Änderungen vorgenommen:  

* MWST.-Buchungsgruppen und Buchungsgruppen werden konvertiert.  
* Änderungen werden in den Fibuposten, den Debitoren, den Kreditoren, den offenen Belegen, den Erfassungsjournalzeilen usw. implementiert.  

> [!IMPORTANT]  
>  Bevor Sie die Umrechnung für MWST-Satzänderungen ausführen, können Sie die Konvertierung testen. Um dies zu tun, führen Sie die Schritte unten aus, stellen Sie aber sicher, dass Sie die Kontrollkästchen **Konvertierung durchführen** und **Tool zum Ändern des MWST-Satzes abgeschlossen** deaktivieren. Während der Testkonvertierung wird das Feld **Konvertiert** in der Tabelle **Protokollposten für MWST-Satzänderung** gelöscht und das Feld **Konvertierungsdatum** in der Tabelle **Protokollposten für MWST-Satzänderung** ist leer. Nach der Umrechnung wählen Sie auf der Registerkarte Start, in der Gruppe Prozess die Option **Änderungsprotokollposten für MWST-Satz** aus, um die Ergebnisse der Umrechnung anzuzeigen. Prüfen Sie jeden Posten, bevor Sie die Umrechnung ausführen. Insbesondere überprüfen Sie Transaktionen, die einen alten MWST-Satz verwenden.     

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") geöffnet wird. geben Sie **MwSt** ein, und wählen dann **MwSt Satzänderung einrichten**den zugehörigen Link aus.  
2. Vergewissern Sie sich, dass Sie bereits die MWST.-Produktbuchungsgruppen-Umrechnung oder die Produktbuchungsgruppen-Umrechnung eingerichtet haben.  
3. Wählen Sie das Kontrollkästchen **Konvertierung durchführen**.  

    > [!IMPORTANT]  
    >  Deaktivieren Sie das Kontrollkästchen **Tool zum Ändern des MWST-Satzes abgeschlossen**. Das Kontrollkästchen wird automatisch aktiviert, wenn die Umrechnung für die MWST.-Satzänderung abgeschlossen ist.  

4. Wählen Sie die Aktion **Konvertieren** aus.  
5. Nachdem der Umrechnung wählen Sie auf der Registerkarte **Start**, in der Gruppe **Prozess** die Option **Änderungsprotokollposten für MWST.-Satz** aus, um die Ergebnisse der Umrechnung anzuzeigen.  

> [!IMPORTANT]  
>  Nachdem die Umrechnung abgeschlossen ist, wird das Feld **Konvertiert** in der Tabelle **Protokollposten für MWST-Satzänderung** ausgewählt und das Feld **Konvertierungsdatum** in der Tabelle **Protokollposten für MWST-Satzänderung** wird mit dem Umrechnungsdatum ausgefüllt.  

## <a name="see-also"></a>Siehe auch  
[Einrichten von unrealisierter Mehrwertsteuer](finance-setup-unrealized-vat.md)  
[So gehts: Melden von MWST an eine Steuerbehörde](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
