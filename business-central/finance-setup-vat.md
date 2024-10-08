---
title: MWST einrichten
description: 'Überprüfen Sie, ob Sie die MwSt für Verkäufe und Einkäufe korrekt berechnen, buchen und melden. Es wird empfohlen, dass Sie diesen Einrichtungsleitfaden verwenden, um die MwSt einzurichten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Berechnungen und Buchungsmethoden für Mehrwertsteuer einrichten

Verbraucher und Geschäfte bezahlen Mehrwertsteuer (MwSt), wenn Sie Waren oder Dienstleistungen einkaufen. Der zu bezahlende MwSt-Betrag kann abhängig von verschiedenen Faktoren variieren. In [!INCLUDE[prod_short](includes/prod_short.md)] legen Sie die Sätze fest, die für die Berechnung der Steuerbeträge auf der Grundlage der folgenden Parameter verwendet werden sollen:

* An wen Sie verkaufen  
* Von wem Sie kaufen  
* Was Sie verkaufen  
* Was Sie kaufen  

Sie können die Berechnungen der MwSt manuell einrichten, aber das kann heikel und zeitaufwendig sein. Es kommt leicht vor, dass versehentlich unterschiedliche Mehrwertsteuersätze verwendet werden, wodurch ungenaue Mehrwertsteuer-verknüpfte Berichte entstehen würden. Um die Einrichtung der MWST zu vereinfachen, empfehlen wir Ihnen, die geführte Anleitung **MWST-Einrichtung** im Produkt zu verwenden.

Wenn Sie MwSt-Berechnungen selbst einrichten möchten oder einfach mehr über jeden Schritt erfahren möchten, enthält dieser Artikel Beschreibungen jedes Schrittes.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="set-up-vat-using-the-assisted-setup-guide-recommended"></a>Verwenden der Anleitung zur unterstützten Einrichtung der MWST (empfohlen)

> [!NOTE]
> Sie können die Anleitung **MWST-Einrichtung** nur nutzen, wenn Sie *Mein Unternehmen* erstellt und keine Transaktionen gebucht haben, die MWST beinhalten. Weitere Informationen zu „Mein Unternehmen“ finden Sie unter [Neue Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen](about-new-company.md).

Um die unterstützte Einrichtung zu starten, gehen Sie folgendermassen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"). Symbol. Geben Sie **Unterstützte Einrichtung** ein. 
2. Wählen Sie **MWST einrichten** aus, und führen Sie die Schritte aus.
3. Nachdem Sie die unterstützte Einrichtung abgeschlossen haben, wechseln Sie zur Seite **MWST Buchungsmatrix Einr.** und überprüfen Sie, ob Sie entsprechend den lokalen Anforderungen in Ihrer Version von [!INCLUDE [prod_short](includes/prod_short.md)] weitere Felder ausfüllen müssen. Weitere Informationen unter [Lokale Funktion in Business Central](about-localization.md).  

### <a name="check-the-vat-posting-setup"></a>Überprüfen Sie die Einrichtung der MWST-Buchung

Um Sie beim schnellen Einstieg zu unterstützen, zeigt [!INCLUDE [prod_short](includes/prod_short.md)] Ihnen Benachrichtigungen an, wenn Ihnen Hauptbuchkonten (Fibukonten) in Buchungsgruppen oder Buchungseinstellungen fehlen, wie z. B. die **Einrichtung der MWST-Buchung**-Seite. Sie können diese Art der Benachrichtigung über **Fibukonto ist nicht in der Buchungsgruppe oder Einrichtung vorhanden**-Benachrichtigung in der **Meine Benachrichtigungen**-Seite ein- oder ausschalten. Wählen Sie einfach auf der Seite **Meine Einstellungen** den Link **Ändern, wenn ich Benachrichtigungen erhalte** aus.  

Wenn Sie die Benachrichtigung auswählen, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] automatisch diese Buchungseinstellungen basierend auf den Buchungsgruppen in dem Beleg oder Journal, an dem Sie gerade arbeiten.  

An dieser Stelle können Sie einfach die fehlenden Fibukonten ausfüllen. Aber wenn Sie Ihre Einrichtung später weiter verfeinern, stellen Sie möglicherweise fest, dass Ihre ursprüngliche Einrichtung falsch ist. [!INCLUDE [prod_short](includes/prod_short.md)] ermöglicht Ihnen nicht, eine MWST-Buchungseinrichtung und eine allgemeine Buchungseinrichtung zu löschen, nachdem diese zum Erstellen von Posten verwendet wurden. Um zu verhindern, dass Benutzer versehentlich eine Einrichtung verwenden, die für neue Buchungen nicht mehr relevant ist, können Sie das Feld **Gesperrt** auf der Seite **Buchungsmatrix**.

## <a name="set-up-a-default-vat-date-for-documents-and-journals"></a>Richten Sie ein Standard-MWST-Datum für Belege und Journale ein

Umsatzsteuermeldung in [!INCLUDE [prod_short](includes/prod_short.md)] basiert auf dem **MWST-Datum**, um MWST-Einträge in MWST-Berichte in eine MWST-Periode aufzunehmen. Das MWST-Datum kann für alle Belege und Journale geändert werden, aber Sie müssen einen Standardwert für das MWST-Datum angeben.

> [!NOTE]
> Nach dem Buchen des Belegs oder Journals erscheint das **MWST-Datum** unter **MWST-Einträge** und **Fibukonteneinträge** sowie auf dem gebuchten Beleg, falls vorhanden.

Gehen Sie folgendermassen vor, um einen Standardwert für ein MWST-Datum einzurichten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Fibuposten Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Inforegister **Allgemein** im **Standard-MWST-Datum** entweder **Buchungsdatum** oder **Belegdatum**.
3. Die Seite schliessen.  

> [!NOTE]
> Standardmässig ist das **Standard-MWST-Datum** das **Buchungsdatum**.

### <a name="enable-or-disable-the-vat-date-feature"></a>Das Feature „MWST-Datum“ aktivieren oder deaktivieren

Manche Länder/Regionen verlangen, dass Unternehmen ein bestimmtes MWST-Datum verwenden, andere Länder/Regionen jedoch nicht. In einigen Ländern/Regionen müssen Unternehmen in bestimmten Situationen das MWST-Datum ändern, nachdem sie die Belege gebucht haben, in anderen Ländern/Regionen ist eine Änderung des MWST-Datums jedoch nicht zulässig. Um unterschiedliche Kontexte zu berücksichtigen, können Sie wählen, ob und in welchem Umfang Sie diese Funktionalität nutzen möchten.

Führen Sie die folgenden Schritte aus, um die Höhe der Verwendung von MWST-Daten einzurichten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Fibuposten Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie auf dem Inforegister **Allgemein** im Feld **Verwendung des MWST-Datums** den Grad an, zu dem Sie das Feature für das MWST-Datum verwenden möchten. Sie haben eine der folgenden Optionen auswählen:

   | Art | Beschreibung |
   |--------------------|-----------------------------------------|
   | **Die Funktion MWST-Datum vollumfänglich verwenden** | Alles rund um das **MWST-Datum** funktioniert standardmässig und Sie haben die grösstmögliche **MWST-Datum**-Funktionalität. Sie können das Datum einrichten, es in Belegen ändern, darauf basierende Berichte erstellen und das Datum nach der Buchung ändern, solange der Zeitraum nicht geschlossen oder durch zulässige Daten für die Buchung geschützt ist. |
   | **Verwenden ohne Änderungen zuzulassen** | Alles rund um das **MWST-Datum** funktioniert standardmässig mit einer Ausnahme. Sie können das **MWST-Datum** in **MWST-Posten**. |
   | **Die Funktion MWST-Datum nicht verwenden** | [!INCLUDE [prod_short](includes/prod_short.md)] blendet die Felder **MWST-Datum** aus und macht sie für Belege, Erfassungsjournale und Posten nicht verfügbar. Das **Standard-MWST-Datum** wird als **Buchungsdatum** konfiguriert. |

3. Schliessen Sie die Seite.

> [!IMPORTANT]
> Auch wenn Sie die Option **Die Funktion MWST-Datum nicht verwenden** wählen, nutzt [!INCLUDE [prod_short](includes/prod_short.md)]**MWST-Datum** im Hintergrund. Weil das **Standard-MWST-Datum** als **Buchungsdatum** konfiguriert ist und Sie es in diesem Fall nicht ändern können, ist die Erfahrung dieselbe wie ohne diese Funktion. Die **MWST-Datum**-Felder werden von allen Seiten entfernt, aber dieses Feld ist weiterhin in Tabellen vorhanden und Berichte funktionieren basierend darauf.

### <a name="limiting-periods-for-posting-and-changing-the-vat-date"></a>Zeiträume für die Buchung und Änderung des MWST-Datums einschränken

Sie können verhindern, dass Personen MWST-Posten in bestimmten Datumsbereichen buchen oder ändern. Sie legen die Einschränkung mithilfe von zwei Einstellungen fest:

* Basierend auf dem geschlossenen **MWST-Rückgabezeitraum**
* Basierend auf den Feldern **Buchungen zulassen ab** und **Buchungen zulassen bis**.

#### <a name="to-limit-posting-based-on-vat-return-period"></a>Um die Buchung basierend auf dem MWST-Rückgabezeitraum zu begrenzen

1. Wählen Sie die ![Glühbirne, die da „Wie möchten Sie weiter verfahren“-Feature 1.](media/ui-search/search_small.png "Tell Me-Funktion") öffnet. Symbol. Geben Sie **Finanzbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie auf dem Inforegister **Allgemein** im Feld **MWST-Zeitraum kontrollieren** den Grad ein, bis zu dem der MWST-Rückgabezeitraum kontrolliert werden kann. Die Optionen werden in der folgenden Tabelle beschrieben.

| Art | Beschreibung |
|--------------------|-----------------------------------------|
| **Buchung innerhalb geschlossenen Zeitraums sperren und für freigegebenen Zeitraum warnen** | Verhindern Sie, dass Belege oder Journale gebucht oder MWST-Posten geändert werden, die ein MWST-Datum innerhalb eines geschlossenen **MWST-Rückgabezeitraums** haben. [!INCLUDE [prod_short](includes/prod_short.md)] zeigt auch eine Warnung an, wenn Ihr **MWST-Rückgabezeitraum** geöffnet ist, aber der Status der **MWST-Rückgabe** auf **Freigegeben** oder **Eingereicht** steht. |
| **Buchung innerhalb geschlossenen Zeitraums sperren** | Verhindern Sie, dass Belege oder Journale gebucht oder MWST-Posten geändert werden, die ein MWST-Datum innerhalb des geschlossenen **MWST-Rückgabezeitraums** haben. |
| **Bei Buchung in geschlossenem Zeitraum warnen** | Zeigen Sie eine Warnung an, aber blockieren Sie die Buchung nicht, wenn Sie einen Beleg oder ein Journal buchen möchten, dessen MWST-Datum in einem geschlossenen **MWST-Rückgabezeitraum** liegt. |
| **Deaktiviert** | Ergreifen Sie keine Massnahmen basierend auf einem geschlossenen **MWST-Rückgabezeitraum**. |

#### <a name="limit-posting-based-on-allow-fromto-period"></a>Buchen basierend auf dem „Erlauben ab/bis“-Zeitraum einschränken

> [!NOTE]
> Ab Business Central Version 23.1 wird dieses Steuerelement geändert. In früheren Versionen gab es auf der Seite **Finanzbuchhaltung Einrichtung** nur ein Steuerelement sowohl für das Buchungsdatum als auch für das MWST-Datum. Jetzt sind diese Steuerelemente aufgeteilt, sodass das Steuerelement auf der Seite **Finanzbuchhaltung Einrichtung** nur für das **Buchungsdatum** gilt und das Steuerelement auf der Seite **MWST-Einrichtung** gilt nur für das **MWST-Datum**. Es gibt auch neue Datumssteuerelemente auf der Seite **Benutzereinstellungen**.  

##### <a name="version-231-or-newer"></a>Version 23.1 oder neuer

> [!IMPORTANT]
> Beachten Sie beim Upgrade auf eine neue Version, dass die Werte im neuen **MWST-Datum zulassen von** auf der Seite **MWST-Einrichtung** basierend auf den Werten von **Buchungen zulassen ab/bis** unter **Finanzbuchhaltung Einrichtung** aktualisiert werden. Wenn Sie andere Datumssteuerelemente verwenden möchten, öffnen Sie die Seite **MWST-Einrichtung** und nehmen Sie Änderungen vor.  

Sie können Einschränkungen für das Unternehmen oder bestimmte Benutzerebenen einrichten.

So beschränken Sie alle Buchungen für das gesamte Unternehmen:

1. Wählen Sie die ![Glühbirne, welche die 1. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Geben Sie **MWST-Einrichtung** ein und wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie auf dem Inforegister **MWST-Datum** im Feld **MWST-Datum zulassen von** das MWST-Datum an, ab dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MWST-Datum vor diesem Datum ist nicht zulässig.  
3. Geben Sie auf dem Inforegister **MWST-Datum** im Feld **MWST-Datum zulassen bis** das MWST-Datum an, bis zu dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MWST-Datum nach diesem Datum ist nicht zulässig. 

So begrenzen Sie Buchungen für einen bestimmten Benutzenden:  

1. Wählen Sie die ![Glühbirne, welche die 1. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Benutzereinrichtung** ein und wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie unter **Benutzer-ID** den Benutzenden an, der in einem bestimmten Zeitraum buchen darf.  
3. Geben Sie im Feld **MWST-Datum zulassen von** das MWST-Datum an, ab dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MWST-Datum vor diesem Datum ist nicht zulässig. 
4. Geben Sie im Feld **MWST-Datum zulassen bis** das MWST-Datum an, bis zu dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MWST-Datum nach diesem Datum ist nicht zulässig.  

##### <a name="versions-before-231"></a>Versionen vor 23.1

Sie können eine Einschränkung für das Unternehmen oder bestimmte Benutzerebenen einrichten.

So beschränken Sie alle Buchungen für das gesamte Unternehmen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Finanzbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie auf dem Inforegister **Allgemein** im Feld **Buchungen zulassen ab** das MWST-Datum an, ab dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MWST-Datum vor diesem Datum ist nicht zulässig.  
3. Geben Sie auf dem Inforegister **Allgemein** im Feld **Buchungen zulassen bis** das MWST-Datum an, bis zu dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MWST-Datum nach diesem Datum ist nicht zulässig.

So begrenzen Sie Buchungen für einen bestimmten Benutzenden:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Benutzereinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie unter **Benutzer-ID** den Benutzenden an, der in einem bestimmten Zeitraum buchen darf.  
3. Geben Sie im Feld **Buchungen zulassen ab** das MWST-Datum an, ab dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MWST-Datum vor diesem Datum ist nicht zulässig.
4. Geben Sie im Feld **Buchungen zulassen bis** das MWST-Datum an, bis zu dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MWST-Datum nach diesem Datum ist nicht zulässig.

## <a name="set-up-vat-registration-numbers-for-your-countryregion"></a>MWST-Nummern für Ihr Land/Ihre Region festlegen

Um zu helfen sicherzustellen, dass Personal gültige MwSt-IdNr. eingeben, können Sie die MwSt-IdNr für die Länder/Regionen verwenden, in denen Sie Geschäfte tätigen. [!INCLUDE[prod_short](includes/prod_short.md)] zeigt eine Fehlermeldung an, wenn jemand einen Fehler macht oder ein Format verwendet, das für das Land/die Region falsch ist.

Um MwSt-Nr. einzurichten, gehen Sie folgendermassen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 2.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Länder/Regionen** ein.
2. Wählen Sie das Land bzw. die Region, und wählen die **MwSt Reg. Nr. Formaten** Aktion aus.
3. Im Feld **Formate** definieren Sie das Format, indem Sie einen oder mehrere der folgenden Zeichen eingeben:  

* **#** Erfordert eine einstellige Nummer.  
* **@** Erfordert einen Buchstaben. Bei diesem Format wird nicht zwischen Gross- und Kleinschreibung unterschieden.  
* **?** Erlaubt jegliches Zeichen.  

    > [!TIP]
    > Sie können andere Zeichen verwenden, sofern sie immer im Land- oder Bereichsformat vorkommen. Wenn Sie also eine Periode oder einen Bindestrich zwischen und Nummern einfügen möchten, können Sie ##.####.### oder @@-###-### definieren.  

## <a name="set-up-vat-business-posting-groups"></a>MWST-Geschäftsbuchungsgruppen festlegen

MWST.-Geschäftsbuchungsgruppen sollten die Märkte darstellen, in denen Sie Geschäfte mit Debitoren und Kreditoren tätigen, und definieren, wie die Mehrwertsteuer in jedem Zielmarkt berechnet und gebucht werden. Beispiele von MwSt.-Produktbuchungsgruppen sind **Inland** und **Europäischen Union (EU)**.  

Verwenden Sie aussagekräftige Codes, an die Sie sich leicht erinnern können, z. B. **EU** **Nicht-EU** oder **Inland**. Jeder Code muss eindeutig sein. Sie können beliebig viele Codes einrichten, aber es ist nicht möglich, denselben Code zweimal in einer Tabelle zu verwenden.

Um eine MWST.-Geschäftsbuchungsgruppe einzurichten, gehen Sie folgendermassen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **MWST-Geschäftsbuchungsgrp. ein** und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus.

Sie richten Vorgabe MWST-Geschäftsbuchungsgruppen ein, indem Sie sie mit den Geschäftsbuchungsgruppen verbinden. [!INCLUDE[prod_short](includes/prod_short.md)] fügt automatisch die MwSt Geschäftsbuchungsgruppe hinzu, wenn Sie die Geschäftsbuchungsgruppe einem Debitor, Kreditor oder Sachkonto zuweisen.

## <a name="set-up-vat-product-posting-groups"></a>Richten Sie MWST.-Produktbuchungsgruppen ein.

Mithilfe der MWST-Produktbuchungsgruppencodes wird die Berechnung und Buchung der MWST gemäss der Art des gekauften Artikels oder der Art der Ressourcen bestimmt.

Es ist sinnvoll, Codes zu verwenden, an die man sich einfach erinnern kann und die die Werte beschreiben, wie etwa **Keine MWST** oder **Null**, **MWST** oder **Reduziert** für 10 % MWST und **MWST 25** oder **Standard** für 25 %.

Um eine MWST.-Geschäftsbuchungsgruppe einzurichten, gehen Sie folgendermassen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **MWST-Produktbuchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinieren Sie MWST.-Produktbuchungsgruppen in der MWST.-Einrichtung

[!INCLUDE[prod_short](includes/prod_short.md)] berechnet MwSt.-Beträge in Verkaufs- und Einkaufsberichten basierend auf MwSt.-Buchungsmatrix Einrichtung, die Kombinationen von Mehrwertsteuergeschäfts und -Produktbuchungsgruppen sind. Für jede Kombination können Sie den MWST.-Prozentsatz, die MWST.-Berechnungsart und die Fibupostennummern für die Buchung der MWST. für Verkäufe, Käufe und Erwerbssteuer eingeben. Sie können auch angeben, ob die MWST. neu berechnet wird, wenn Skonto angewandt oder erhalten wird.  

Sie können beliebig viele Codes einrichten. Um MWST-Buchungsmatrixeinrichtungen mit ähnlichen Attributen in Gruppen zusammenzufassen, definieren Sie für jede Gruppe eine **MWST ID** und weisen Sie das Kennzeichen dann den Gruppenmitgliedern zu.  

> [!NOTE]
> Eine **MWST ID** ist ein Code, den Sie zum Gruppieren ähnlicher Attribute verwenden können. Wir empfehlen Ihnen, unterschiedliche MWST-Kennzeichen für unterschiedliche MWST-Prozentsätze zu verwenden.  

Um MWST.-Buchungseinrichtungen zu kombinieren, gehen Sie folgendermassen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 5.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **MWST-Buchungseinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Weisen Sie mehreren Gruppen MWST.-Buchungsgruppen standardmässig zu

Wenn Sie identische MwSt.-Buchungsgruppen für mehrere Einheiten übernehmen möchten, können Sie [!INCLUDE[prod_short](includes/prod_short.md)]festlegen, um dies standardmässig durchzuführen.

* Sie können MWST-Geschäftsbuchungsgruppen allgemeinen Geschäftsbuchungsgruppen oder Debitoren- oder Kreditorenvorlagen zuweisen.
* Sie können MWST-Produktbuchungsgruppen allgemeinen Produktbuchungsgruppen zuweisen.  

Die MwSt- Geschäfts- oder - Produktbuchungsgruppe wird zugewiesen, wenn Sie eine Geschäfts- oder eine Produktbuchungsgruppe für einen Debitor, einen Kreditor, einen Artikel oder eine Ressource auswählen.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Weisen Sie einzelnen Konten, Debitoren, Kreditoren, Artikeln und Ressourcen MWST-Buchungsgruppen zu.

Die folgenden Abschnitten beschreiben, wie die MWST.-Buchungsgruppen einzelnen Einheiten zugewiesen werden.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>So weisen Sie MWST-Buchungsgruppen einzelnen Fibukonten zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 6.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnet Sie die **Sachkontokarte** für das Konto.  
3. Wählen Sie im Inforegister **Buchen** im Feld **Buchungsart** entweder **Verkauf** oder **Einkauf** aus.  
4. Wählen Sie die MWST.-Buchungsgruppen aus, die Sie für das Verkaufs- bzw. das Wareneingangskonto verwenden möchten.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Um MwSt-Geschäftsbuchungsgruppen Debitoren und Kreditoren zuzuweisen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 7.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Kunde** oder **Kreditor** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Karte **Kunde** oder **Debitor** erweitern Sie das Inforegister **Fakturierung**.  
3. Wählen Sie die MwSt-Geschäftsbuchungsgruppe aus.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Um MwSt-Produktbuchungsgruppen einzelnen Artikeln und Ressourcen zuzuweisen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 8.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Element** oder **Ressource** ein und wählen Sie dann den zugehörigen Link.  
2. Führen Sie einen der folgenden Schritte aus:  

    * Auf der Karte **Artikel** erweitern Sie das Inforegister **Preis und Buchung**, und wählen Sie dann **Mehr anzeigen**, um das Feld **MwSt Produktbuchungsgruppe** anzuzeigen.  
    * Erweitern Sie auf der Karte **Ressource** das Inforegister **Fakturierung**.  
3. Wählen Sie die MwSt-Produktbuchungsgruppe aus.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-nonstandard-vat-rates"></a>Klauseln zur Erklärung der MWST-Befreiung oder von nicht standardmässigen MWST-Sätzen einrichten

Sie richten eine MWST-Klausel ein, um Informationen über die Art der MWST zu beschreiben, die angewendet wird. Diese Informationen werden möglicherweise aufgrund behördlicher Regulierungen verlangt. Nachdem Sie eine MWST-Klausel festgelegt und einer MWST-Buchungsmatrix zugeordnet haben, wird die MWST-Klausel auf allen gedruckten Verkaufsbelegen angezeigt, die diese MWST-Buchungsgruppeneinrichtung verwenden.

Bei Bedarf können Sie auch festlegen, wie Mehrwertsteuerklauseln in andere Sprachen übersetzt werden. Wenn Sie für einen Debitor einen Verkaufsbeleg erstellen und drucken, der eine MWST ID enthält, enthält der gedruckte Beleg die MWST-Klausel in übersetzter Form. Der auf der Kundenkarte angegebene Sprachcode bestimmt die Sprache.

Wenn Sie in verschiedenen Belegtypen, wie Rechnungen oder Gutschriften, nicht standardisierte MWST-Sätze verwenden, müssen Sie möglicherweise Text für die Mehrwertsteuerbefreiung (MWST-Klausel) einfügen. Aus dem Befreiungstext geht hervor, warum ein ermässigter MWST-Satz oder ein Nullsteuersatz berechnet wurde. Auf der Seite **MWST-Klauseln nach Belegtyp** können Sie für jeden Belegtyp unterschiedliche MWST-Klauseln definieren, die in Geschäftsbelege aufgenommen werden sollen.

Sie können eine MWST-Klausel ändern oder löschen, und Ihre Änderungen werden in einem generierten Bericht angezeigt. [!INCLUDE[prod_short](includes/prod_short.md)] bewahrt jedoch keinen Verlauf der Änderung auf. In dem Bericht werden die MWST-Klauselbeschreibungen für alle Zeilen im Bericht neben dem MWST-Betrag und MWST-Basisbetrag gedruckt und angezeigt. Wenn eine MWST-Klausel nicht für eine oder mehrere Zeilen des Verkaufsbelegs festgelegt wurde, wird der gesamte Abschnitt weggelassen, wenn der Bericht gedruckt wird.

### <a name="to-set-up-vat-clauses"></a>Einrichten von MWST.-Klauseln

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 9.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **MWST-Klauseln** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **MwSt.-Klauseln** erstellen Sie eine neue Zeile.  
3. Geben Sie im Feld **Code** eine Kennung für die Klausel ein. Nutzen Sie diesen Code, um die Klausel der MwSt-Buchungsgruppe zuzuweisen.  
4. Geben Sie im Feld **Beschreibung** den Text für die Mehrwertsteuerbefreiung ein, den Sie für Belege, die Mehrwertsteuer enthalten können, anzeigen möchten. Geben Sie im Feld **Beschreibung 2** bei Bedarf weiteren Text ein. Der Text wird auf neuen Belegzeilen angezeigt.
5. Wählen Sie die Aktion **Beschreibung nach Dokumenttyp**.
6. Über die Seite **MWST-Klausel von Belegtyp** füllen Sie die Felder aus, um festzulegen, welcher MWST-Befreiungstext für welche Dokumentart angezeigt werden soll.  
7. Optional: Um die MWST-Klausel sofort einem Setup für die Mehrwertsteuerbuchung zuzuordnen, wählen Sie **Einrichtung**, und wählen Sie dann die Klausel. Wenn Sie warten möchten, können Sie die Klausel später auf der Seite **MWST Buchungsmatrix Einr.** zuordnen.  
8. Optional: Um zu bestimmen wie die Mehrwertsteuerklausel übersetzt wird, wählen Sie die Aktion **Übersetzungen**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>So weisen Sie eine MWST.-Klausel einer Buchungsgruppe zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 10.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **MWST-Buchungseinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. In der Spalte **MwSt.-Klausel** wählen Sie die Klausel, die für jede MwSt.-Buchungseinrichtung gilt.  

### <a name="to-specify-translations-for-vat-clauses"></a>Um Beschreibungen für Mehrwertsteuerklauseln festzulegen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 11.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **MWST-Klauseln** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Übersetzung** aus.  
3. Wählen Sie im Feld **Sprachcode** Sie die Sprache aus, in die Sie übersetzen.  
4. Geben Sie in den Feldern **Beschreibung**und **Beschreibung 2**den Text ein, der eine Übersetzung der Beschreibungen ist. Dieser Text wird in den übersetzten MWST.-Berichten angezeigt.  

### <a name="to-specify-extended-text-for-vat-clauses"></a>So legen Sie Zusatztexte für Mehrwertsteuerklauseln fest

> [!NOTE]  
> Wenn Ihr Land oder Ihre Region einen längeren Text für die MWST-Klauseln erfordert, als die Standardversion unterstützt, können Sie den längeren Text für die MWST-Klauseln als *Zusatztext* angeben, damit dieser in den Verkaufs- und Einkaufsberichten gedruckt wird.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 11.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **MWST-Klauseln** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Zusatztexte** aus.  
3. Wählen Sie die Aktion **Neu** aus.  
4. Füllen Sie die Felder **Sprachencode** und **Beschreibung** aus.  
5. Wählen Sie optional das Feld **Alle Sprachcodes** aus, oder geben Sie die entsprechende Sprache im Feld **Sprachcode** an, wenn Sie Sprachcodes verwenden.  
6. Füllen Sie die Felder **Startdatum** und/oder **Enddatum** aus, wenn Sie die Verwendung des Zusatztexts zeitlich einschränken möchten.  
7. Geben Sie den Zusatztext für Ihre MWST-Klauseln in den Zeilen für **Text** ein.  
8. Wählen Sie die entsprechenden Felder für die Belegtypen aus, deren Zusatztexte gedruckt werden sollen.  
9. Schliessen Sie die Seite.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Erstellen Sie eine MWST.-Buchungsmatrix, um Einfuhrumsatzsteuer zu verarbeiten

Verwenden Sie die Funktion *Import-MWST*, wenn Sie einen Beleg buchen müssen, bei dem der gesamte Betrag aus MWST besteht. Sie verwenden diese Funktion, wenn Sie eine MWST-Rechnung für importierte Waren von der Salestaxbehörde erhalten.  

Gehen Sie folgendermassen vor, um Codes für die Einfuhrsteuerfelder festzulegen:  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 12.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **MWST-Produktbuchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite MWST Produktbuchungsgruppe richten Sie eine neue MWST.-Produktbuchungsgruppen für Einfuhrsteuer ein.  
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 13.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **MWST-Buchungseinrichtung** ein und wählen Sie dann den zugehörigen Link.  
4. Auf der Seite MWST Buchungseinrichtung erstellen Sie eine neue Zeile oder nutzen einen bestehende MWST-Buchungsgruppe in Kombination mit der neuen MWST.-Produktbuchungsgruppe für die Einfuhrsteuer.  
5. Wählen Sie im Feld **MwSt.-Berechnungsart** **Volle MwSt.** aus.  
6. Geben Sie im Feld **Vorsteuerkonto** das Fibukonto an, auf das Sie Einfuhrumsatzsteuer buchen wollen. Alle anderen Konten sind optional.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countriesregions"></a>Benutzen Sie die Erwerbssteuer für den Handel zwischen EU-Ländern/-Regionen

Gewisse Unternehmen müssen Erwerbssteuer abführen, wenn Sie Handel mit anderen Ländern innerhalb der EU betreiben. Die Regel gilt beispielsweise für Einkäufe aus EU-Ländern/-Regionen und Verkäufe an EU-Länder/-Regionen.  

> [!NOTE]  
> Diese Regel gilt für den Handel mit Unternehmen, die in einem anderen EU-Land/in einer anderen EU-Region als umsatzsteuerpflichtig registriert sind. Wenn Sie direkt mit Verbrauchern in anderen EU-Ländern/-Regionen Geschäfte tätigen, sollten Sie sich bei den Salestaxbehörden über die geltenden Regeln für die MWST. informieren.  

> [!TIP]  
> Sie können überprüfen, ob ein Unternehmen in einem anderen EU-Land bzw. einer anderen EU-Region als umsatzsteuerpflichtig registriert ist, wenn Sie den EU-MWST Nummer-Überprüfungsdienst verwenden. Der Service ist in [!INCLUDE[prod_short](includes/prod_short.md)] kostenlos verfügbar. Weitere Informationen finden Sie unter [Überprüfen von MWST-Registrierungsnummern](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countriesregions"></a>Verkäufe in EU-Ländern/-Regionen

Auf Verkäufe an umsatzsteuerpflichtige Unternehmen in anderen EU-Ländern/-Regionen wird keine MWST berechnet. Der Wert derartiger Verkäufe an EU-Länder/-Regionen muss separat auf der MWST.-Abrechnung ausgewiesen werden.  

Um MWST. bei Verkäufen in EU-Länder/-Regionen korrekt zu berechnen, gehen Sie folgendermassen vor:  

* Richten Sie eine Zeile für Verkäufe mit den gleichen Informationen ein, wie zuvor für Einkäufe beschrieben. Wenn Sie im Fenster **MWST Buchungsmatrix Einr.** Zeilen für Einkäufe aus EU-Ländern/-Regionen einrichten, können Sie diese Zeilen auch für Verkäufe verwenden.  
* Weisen Sie die MWST.-Geschäftsbuchungsgruppen im Feld **MWST.-Geschäftsbuchungsgruppe** auf dem Inforegister **Fakturierung** der Debitorenkarte jedes EU-Debitors zu. Sie sollten auch die USt-IdNr. des Debitors im Feld **USt-IdNr.** im Inforegister **Aussenhandel** eingeben.  

Wenn Sie einen Verkauf an einen Debitor in einem anderen EU-Land/einer anderen EU-Region buchen, berechnet [!INCLUDE [prod_short](includes/prod_short.md)] den MWST-Betrag und erstellt einen MWST-Posten basierend auf Informationen zur Erwerbssteuer und zur MWST Basis. Dieser Betrag wird zur Berechnung des MWST-Betrags verwendet. Auf die MWST-Konten in der Finanzbuchhaltung werden keine Posten gebucht.

Wenn Sie die Kombination aus MWST-Geschäftsbuchungsgruppe und MWST-Produktbuchungsgruppe in den regelmässigen MWST-Erklärungen als Dienstleistung aufführen möchten, markieren Sie das Feld **EU-Service**.

> [!NOTE]  
> Das Feld **EU-Service** gilt nur für MWST-Berichte. Das Feld steht in keinem Zusammenhang mit den Funktionen **Service-Deklaration** oder **Intrastat für Dienstleistungen** .

## <a name="vat-rounding-for-documents"></a>MWST-Rundung für Belege

Beträge in Belegen, die nicht gebucht sind, werden gerundet und auf eine Weise angezeigt, die der endgültigen Rundung gebuchter Beträge entspricht. [!INCLUDE [prod_short](includes/prod_short.md)] berechnet die MWST für einen vollständigen Beleg. Die MWST-Berechnung basiert auf der Summe aller Zeilen mit derselben MWST ID im Beleg.  

## <a name="set-up-vat-reporting"></a>MWST-Berichterstellung einrichten

Sie müssen Informationen dazu festlegen, wie die Steuerbehörden in Ihrem Land oder in Ihrer Region von Ihnen verlangen, MWST-Berichte einzureichen. Die folgenden Schritte veranschaulichen die am häufigsten verwendeten Informationen. Für Ihr Land oder Ihre Region sind jedoch möglicherweise zusätzliche Schritte erforderlich. Weitere Informationen finden Sie in dem entsprechenden Artikel im Abschnitt *Lokale Funktionen* in der Leiste auf der linken Seite.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Siehe auch

[Vorlagen für Umsatzsteuerabrechnungen und Namen von Umsatzsteuerabrechnungen einrichten](finance-how-setup-vat-statement.md)  
[Nicht realisierte Mehrwertsteuer einrichten](finance-setup-unrealized-vat.md)  
[MWST an die Steuerbehörde melden](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Arbeiten mit dem Tool zur Änderung des MWST-Satzes](finance-how-use-vat-rate-change-tool.md)  
[Umsatzsteuer-Identifikationsnummern überprüfen](finance-how-validate-vat-registration-number.md)  
[Lokale Funktion in Business Central](about-localization.md)  
[MWST-Berichterstattung in der deutschen Version](LocalFunctionality/Germany/vat-reporting.md)  
[Belgische MwSt](LocalFunctionality/Belgium/belgian-vat.md)  
[Italienische MwSt](LocalFunctionality/Italy/italian-vat.md)  
[Elektronische Mehrwertsteuer- und ICP-Erklärungen in der niederländischen Version einrichten](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[MWST-Bericht in der spanischen Version](LocalFunctionality/Spain/vat-reports.md)  
[Waren- und Dienstleistungssteuer-Buchung in der australischen Version einrichten](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[MWST in der tschechischen Version](LocalFunctionality/Czech/finance-vat.md)  
[MWST-Abrechnung in der norwegischen Version](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Steuern auf Waren und Dienstleistungen und Harmonized Sales Tax in Kanada melden](LocalFunctionality/Canada/sales-tax-goods-services.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
