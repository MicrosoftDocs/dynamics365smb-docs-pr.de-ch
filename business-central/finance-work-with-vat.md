---
title: So arbeiten Sie mit MWST im Verkauf und Einkauf
description: 'Dieser Artikel beschreibt die verschiedenen Möglichkeiten, mit der MWST sowohl manuell als auch mit automatischer Einrichtung zu arbeiten, damit Sie die länder-/regionsspezifischen Vorschriften einhalten können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 05/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Mit MWST im Verkauf und Einkauf arbeiten

Wenn Ihr Land oder Ihre Region verlangt, dass Sie die MWST auf Verkaufs- und Einkaufstransaktionen berechnen und melden, können Sie in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, dass MWST berechnet wird. Weitere Informationen finden Sie [Einrichten der Berechnungs- und Buchungsmethoden für Salestax](finance-setup-vat.md).

Es gibt jedoch Mehrwertsteuer-verknüpfte Aufgaben, die Sie manuell tun können. Beispielsweise müssen Sie möglicherweise einen gebuchten Betrag korrigieren, wenn Sie feststellen, dass ein Kreditor eine andere Rundungsmethode verwendet.  

> [!TIP]
> Sie können [!INCLUDE[prod_short](includes/prod_short.md)] die MWST Nummern und andere Unternehmensinformationen beim Erstellen oder Aktualisieren von Belegen überprüfen lassen. Weitere Informationen finden Sie unter [MWST Nummern validieren](finance-how-validate-vat-registration-number.md).

## Berechnen und Anzeigen von MWST-Beträgen in Verkaufs- und Einkaufsbelegen  

Wenn Sie eine  Artikelnummer im **Nr.** Feld auf einem Verkaufs- oder Einkaufsbeleg, [!INCLUDE[prod_short](includes/prod_short.md)] füllt die Felder **Einzelpreis** und **Zeilenbetrag**. Der Verkaufspreis wird von der **Artikel**karte übernommen oder anhand der Artikelpreise berechnet, die für den Artikel und den Debitor zulässig sind. [!INCLUDE[prod_short](includes/prod_short.md)] berechnet den Zeilenbetrag nur dann, wenn Sie eine Menge für die Zeile eingeben.  

Wenn Sie möchten, dass die Einzelpreise und Zeilenbeträge Mehrwertsteuer enthalten, wenn Sie beispielsweise an Endverbraucher verkaufen, wählen Sie das **Preise inkl. MwSt**-Kontrollkästchen auf dem Dokument aus. Weitere Informationen finden Sie unter [Einschliesslich oder ohne Mehrwertsteuer in Preisen und Zeilenbeträgen](#including-or-excluding-vat-in-prices-and-line-amounts). 

Sie können MWST-Beträge in Verkaufs- und Einkaufsbelegen unterschiedlich berechnen und anzeigen. Der Unterschied hängt von der Art des jeweiligen Debitors oder Kreditors ab. Sie können den berechneten MWST-Betrag auch manuell ändern, z. B. um ihn an den von Ihrem Lieferanten für eine bestimmte Transaktion berechneten MWST-Betrag anzupassen.

### Einschliesslich oder ohne Mehrwertsteuer in Preisen und Zeilenbeträgen

Wenn Sie das Kontrollkästchen **Preise inkl. MWST** aktivieren, werden die Felder **VK-Preis** und **Zeilenbetrag** mit der MWST berechnet. Die Werte in diesen Feldern enthalten standardmässig keine MWST. Die Namen der Felder geben an, ob die Preise Mehrwertsteuer enthalten.  

Sie können die Standardeinstellung der **Preise inkl. MwSt.** für alle Verkaufsbelege eines Debitors im Feld **Preise inkl. MwSt.** auf der **Debitor**-Karte einrichten. Darüber hinaus können Sie auch Artikelpreise inklusive oder exklusive MWST einrichten. In der Regel enthalten die Preise auf der Artikelkarte keine MWST.

Die folgende Tabelle bietet einen Überblick darüber, wie in der Anwendung Verkaufspreise für einen Verkaufsbeleg berechnet werden, wenn auf der Seite **VK-Preise** keine Preise eingerichtet wurden:  

|**Feld "VK-Preis inkl. MWST" auf Artikelkarte**|**Feld „Preise inkl. MWST“**|**Durchgeführte Aktion**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Nicht aktiviert|Nicht aktiviert|Der **VK-Preis** auf der Artikelkarte wird in das Feld **VK-Preis ohne MWST** in den Verkaufszeilen kopiert.|  
|Nicht aktiviert|Aktiviert|Die Anwendung berechnet den MWST-Betrag pro Einheit und fügt ihn dem **VK-Preis** auf der Artikelkarte hinzugefügt. Dieser Gesamtverkaufspreis wird dann in das Feld **VK-Preis inkl. MWST** in den Verkaufszeilen eingegeben.|  
|Aktiviert|Nicht aktiviert|Die Anwendung berechnet den MWST-Betrag, der im **VK-Preis** auf der **Artikelkarte** unter Verwendung des MWST-Prozentsatzes enthalten ist, der mit der Kombination aus MWST-Geschäftsbuchungsgruppe (Preis) und MWST-Produktbuchungsgruppe verknüpft ist. Der **VK-Preis** auf der Artikelkarte minus MWST-Betrag wird anschliessend im Feld **VK-Preis ohne MWST** in den Verkaufszeilen eingegeben. Weitere Informationen finden Sie unter [Verwenden von MWST-Geschäftsbuchungsgruppen und Kundenpreisgruppen](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups).|  
|Aktiviert|Aktiviert|Der **VK-Preis** auf der Artikelkarte wird in das Feld **VK-Preis inkl. MWST** in den Verkaufszeilen kopiert.|

#### Verwenden von MWST-Geschäftsbuchungsgruppen und Kundenpreisgruppen 

Wenn Sie möchten, dass die Preise Mehrwertsteuer enthalten, können Sie Mehrwertsteuer-Geschäftsbuchungsgruppen verwenden, um den Betrag basierend auf der Mehrwertsteuerbuchungseinrichtung für die Gruppe zu berechnen. Weitere Informationen finden Sie unter [MWST-Geschäftsbuchungsgruppen festlegen](finance-setup-vat.md#set-up-vat-business-posting-groups).

Je nachdem, was Sie tun möchten, können Sie Debitoren oder Verkaufsbelegen eine MWST-Geschäftsbuchungsgruppe auf folgende Weise zuweisen:

* Um für alle Kunden denselben Mehrwertsteuersatz zu verwenden, können Sie eine Gruppe im **MWST-Geschäftsbuchungsgruppe (Preis)**-Feld auf der **Einrichtung von Verkäufen und Forderungen**-Seite auswählen.
* Um einen Mehrwertsteuersatz für einen bestimmten Kunden zu verwenden, können Sie auf der Seite **Debitorenkarte** im Feld **MWST-Geschäftsbuchungsgruppe (Preis)** eine Gruppe auswählen. 
* Um einen MWST-Satz für bestimmte Debitoren zu verwenden, können Sie auf der Seite **Debitorenpreisgruppe** im Feld **MWST-Geschäftsbuchungsgruppe (Preis)** eine Gruppe auswählen. Diese Einstellung ist beispielsweise hilfreich, wenn Sie möchten, dass ein Preis für alle Debitoren in einer bestimmten geografischen Region oder einer bestimmten Branche gilt.
* Auf allen Verkaufsbelegen im Feld **MWST-Geschäftsbuchungsgrp.**. Der für die Gruppe angegebene Mehrwertsteuerbetrag wird nur für den Beleg verwendet, an dem Sie gerade arbeiten.

> [!NOTE]
> Wenn Sie keine Gruppe im **MWST-Geschäftsbuchungsgruppe (Preis)** angeben, wird Mehrwertsteuer nicht in den Preisen enthalten sein.

#### Beispiele

Faktoren wie das Land oder die Region, in dem bzw. der Sie verkaufen, oder die Art der Branchen, in die Sie verkaufen, können sich auf die Höhe der MWST auswirken, die Sie abführen müssen. Beispielsweise kann ein Restaurant 6 % Mehrwertsteuer für Mahlzeiten berechnen, die im Haus eingenommen werden, und 17 % für Speisen zum Mitnehmen. Um dies zu erreichen, erstellen Sie eine Umsatzsteuer-Geschäftsbuchungsgruppe (Preis) für „Inhouse“ und eine für „Mitnahme“.

## Arbeiten mit MWST-Datum

### Umsatzsteuerdatum in Belegen

Wenn Sie neue Verkaufs- oder Einkaufsbelege erstellen, basiert das **MWST-Datum** auf der Einstellung im Feld **Standard-MWST-Datum** auf der Seite **Fibu Einrichtung**. Dieser Standardwert kann derselbe sein wie **Buchungsdatum** oder **Belegdatum**. Wenn Sie ein anderes MWST-Datum benötigen, können Sie den Wert im Feld **MWST-Datum** manuell ändern. Wenn Sie den Beleg buchen, wird das **MWST-Datum** auf dem Buchungsbeleg und in den MWST- und Fibuposten ausgewiesen.

> [!NOTE]
> Wenn das Feld **MWST-Datum** in Ihren Belegen oder Erfassungsjournalen nicht verfügbar ist, bedeutet dies, dass **Die Funktion „MWST-Datum“ nicht verwenden** im Feld **„MWST-Datum“-Nutzung** auf der Seite **Hauptbuchhaltungs-Einrichtung** nicht ausgewählt.  

> [!IMPORTANT]
> Wenn Sie **MWST-Zeitraum kontrollieren** in der **Hauptbuchhaltungs-Einrichtung** als **Buchung innerhalb geschlossenen Zeitraums sperren** oder **Buchung innerhalb geschlossenen Zeitraums sperren und für freigegebenen Zeitraum warnen** konfigurieren, können Sie Belege oder Erfassungsjournals nur buchen, wenn sich das Datum im **MWST-Datum**-Feld nicht in einem geschlossenen Zeitraum in **Mehrwertsteuer-Rückgabeperioden** befindet. Auch wenn der Zeitraum im Feld **Mehrwertsteuer-Rückgabeperioden** offen ist, erhalten Sie möglicherweise eine Warnung basierend auf dem **MWST-Rückgabestatus** und der Konfiguration unter **MWST-Zeitraum kontrollieren**.

> [!IMPORTANT]
> Ab Version 23.1 können Sie das Buchen des **MWST-Datums** für bestimmte Datumsbereiche verhindern oder zulassen, indem Sie die Felder **MWST-Datum zulassen von** und **MWST-Datum zulassen bis** in der **MWST-Einrichtung** und der **Benutzereinrichtung** verwenden. Wenn Sie ältere Versionen verwenden, können Sie das Buchen des **MWST-Datums** für bestimmte Datumsbereiche verhindern oder zulassen, indem Sie die Felder **Buchungen zugel. ab** und **Buchungen zugel. bis:** in der **Hauptbuchhaltungs-Einrichtung** und der **Benutzereinrichtung** verwenden.  

> [!NOTE]
> Wenn Sie **MWST-Datum** leer lassen, verwendet [!INCLUDE [prod_short](includes/prod_short.md)] die Standardeinrichtung aus **Standard-MWST-Datum** in der **Hauptbuchhaltungs-Einrichtung** als ein **MWST-Datum** in der gebuchten Transaktion.  

### Ändern des MWST-Datums in gebuchten Einträgen

Bei Bedarf können Sie die gebuchten Belege zum MWST-Datum ändern. Zum Ändern des Datums im Feld **MWST-Datum** für gebuchte Belege müssen Sie die folgenden Schritte ausführen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **MWST-Posten** ein und wählen Sie dann den entsprechenden Link. 
2. Finden Sie den Eintrag mit falschem MWST-Datum.  
3. Wählen Sie die Aktion **Liste bearbeiten** und geben Sie dann das richtige Datum in das Feld **MWST-Datum** ein.  
4. Wenn Sie die Seite schliessen, wird das MWST-Datum in entsprechenden **Fibuposten** und im gebuchten Beleg geändert.  

> [!NOTE]
> Sie können das Feld **MWST-Datum** in **MWST-Einträge** nur ändern, wenn Ihr aktuelles Datum nicht in einem abgeschlossenen MWST-Rückgabezeitraum enthalten ist. Auch wenn der Zeitraum im Feld **Mehrwertsteuer-Rückgabeperioden** offen ist, erhalten Sie möglicherweise eine Warnung basierend auf dem **MWST-Rückgabestatus**.  

> [!NOTE]
> Wenn Ihr Beleg mehr als einen **MWST-Eintrag** enthält, müssen Sie nur den Wert im Feld **MWST-Datum** in einem Eintrag ändern, der sich auf den Beleg bezieht. Um die Einträge konsistent zu halten, ändert [!INCLUDE[prod_short](includes/prod_short.md)] das MWST-Datum in MWST-Einträgen, die sich auf diese Transaktion beziehen, automatisch. [!INCLUDE [prod_short](includes/prod_short.md)] aktualisiert das **MWST-Datum** in anderen Tabellen (FIBU-Einträge und Belege), jedoch nur in Bezug auf diese Transaktion.  

## MWST-Beträgen in Verkaufs- und Einkaufsbelegen manuell korrigieren  

Sie können Korrekturen an gebuchten MWST-Posten vornehmen und die Umsatzsteuer- und Vorsteuerbeträge verändern, ohne die MWST Basis zu verändern. Zum Beispiel, wenn Sie eine Rechnung von einem Lieferanten mit einem falschen Mehrwertsteuerbetrag erhalten.  

Auch wenn Sie möglicherweise bereits eine oder mehrere Kombinationen für die Verarbeitung der Einfuhr-MWST eingerichtet haben, müssen Sie mindestens eine MWST-Produktbuchungsgruppe einrichten. Beispielsweise können Sie den Namen **RICHTIG** für Korrekturen angeben, es sei denn, Sie können dasselbe Fibukonto im Feld **Vorsteuerkonto** in der MWST-Buchungsmatrixzeile verwenden. Weitere Informationen finden Sie [Einrichten der Berechnungs- und Buchungsmethoden für Salestax](finance-setup-vat.md).

Wenn Skonto auf der Basis einer Rechnung inklusive MWST berechnet wurde, haben Sie die Möglichkeit, den Skontoanteil des MWST-Betrages zu berichtigen, wenn Skonto gewährt wird. Sie müssen das Feld **Skonto berichtigen** sowohl in der Finanzbuchhaltungseinrichtung im Allgemeinen als auch in der MWST-Buchungseinrichtung für bestimmte Kombinationen von MWST-Geschäftsbuchungsgruppen und MWST-Produktbuchungsgruppen aktivieren.  

### Einrichtung des Systems für die manuelle MWST-Posten in Verkaufsbelegen

Führen Sie die folgenden Schritte aus, um manuelle MWST-Änderungen auf Verkaufsbelegen zu aktivieren. Die Schritte sind auf der Seite **Einrichten von Einkäufen und Verbindlichkeiten** gleich.

1. Geben Sie im Fenster **Finanzbuchhaltungs-Einrichtung:** eine **maximal zulässige MWST-Differenz** zwischen dem von der Anwendung berechneten Betrag und dem manuell eingegebenen Betrag an.  
2. Aktivieren Sie im Fenster **Debitoren & Verkauf Einr.** die Option **MWST-Differenz zulassen**.  

### Die MWST. für einen Verkaufsbeleg anpassen:

1. Öffnen Sie den entsprechenden Verkaufsauftrag.  
2. Wählen Sie die Aktion **Statistik** aus.  
3. Auf dem Inforegister **Fakturierung** wählen Sie im Feld den Wert **Anzahl der Steuerpositionen** aus.
4. Füllen Sie das Feld **MWST-Betrag** aus.   

> [!NOTE]  
> Der gesamte MWST-Betrag für die Rechnung wird gruppiert nach MWST ID in den Zeilen angezeigt. Sie können den Betrag manuell im Feld **MWST-Betrag** in den Zeilen für jede MWST ID anpassen. Wenn Sie das Feld **MWST-Betrag** ändern, prüft die Anwendung, ob die Mehrwertsteuer um einen höheren Betrag als die maximal zulässige Differenz geändert worden ist. Liegt der Betrag ausserhalb des unter **Max. MWST-Differenz zulässig** angegebenen Bereichs, werden Sie in einer Warnmeldung über die maximal zulässige Differenz informiert. Sie können erst dann fortfahren, wenn der Betrag an die zulässigen Parameter angeglichen wurde. Klicken Sie auf **OK** , und geben Sie einen anderen **MWST-Betrag** ein, der innerhalb des zulässigen Bereichs liegt. Wenn die MWST-Differenz der zulässigen Abweichung entspricht oder höher ist, wird die MWST proportional auf die Belegzeilen mit derselben MWST ID aufgeteilt.  

## Manuelle MWST-Berechnung mithilfe von Erfassungsjournalen  

Sie können MWST-Beträge auch in den Erfassungsjournalen Allgemein, Verkauf und Einkauf anpassen. Sie müssen unter Umständen eine Anpassung vornehmen, wenn Sie eine Kreditorenrechnung in das Erfassungsjournal eingeben und zwischen der von der [!INCLUDE[prod_short](includes/prod_short.md)] berechneten MWST und dem MWST-Betrag auf der erhaltenen Kreditorenrechnung eine Differenz besteht.  

### So richten Sie das System für manuelle MWST-Posten in Fibu-Erfassungsjournalen ein

Sie müssen die folgenden Schritte ausführen, bevor Sie die Mehrwertsteuer manuell in ein Fibu Erf.-Journal eingeben.  

1. Geben Sie im Fenster **Finanzbuchhaltungs-Einrichtung:** eine **maximal zulässige MWST-Differenz** zwischen dem von der Anwendung berechneten Betrag und dem manuell eingegebenen Betrag an.  
2. Wählen Sie auf der Seite **Allgemeine Erf.-Journal Vorlage** das Kontrollkästchen **MWST-Differenz zulassen** mit einem Häkchen.  

### Einrichtung des Systems für die manuellen MWST-Posten in einem Verkaufs- und Einkaufs-Erf.-Journal

Sie müssen die folgenden Schritte ausführen, bevor Sie die Mehrwertsteuer manuell in ein Verkaufs- oder Einkaufs-Fibu Erf.-Journal eingeben.

1. Auf der Seite **Kreditoren & Einkauf Einr.** wählen Sie das Kontrollkästchen **MWST-Differenz zulassen**.  
2. Wiederholen Sie Schritt 1 für die Seite**Einkäufe und Verkäufe einrichten**.
3. Nachdem Sie die oben beschriebene Einrichtung abgeschlossen haben, können Sie den Betrag im Feld **MWST-Betrag** in der Fibu-Erfassungsjournal-Zeile oder das Feld **Gegenkonto MWST-Betrag** in der Verkaufs- oder Einkaufserfassungsjournal-Zeile an den MWST-Betrag der Rechnung anpassen. [!INCLUDE[prod_short](includes/prod_short.md)] überprüft, ob die Differenz die festgelegte maximale Differenz übersteigt.  

> [!NOTE]  
> Wenn die Differenz grösser ist, wird in einer Warnmeldung über die maximal zulässige Differenz informiert. Um fortfahren, müssen Sie den Betrag korrigieren. Klicken Sie auf **OK** , und geben Sie einen anderen MwSt.-Betrag ein, der innerhalb des zulässigen Bereichs liegt. Wenn die MWST-Differenz der maximal zulässigen Differenz entspricht oder höher ist, wird [!INCLUDE[prod_short](includes/prod_short.md)] die Abweichung im Feld **MWST-Differenz** angezeigt.  

## Einfuhrsteuer mit Einkaufsrechnungen buchen
Für die Buchung einer Rechnung mit Einfuhrumsatzsteuer kann anstelle eines Fibu-Erf.-Journals auch eine Einkaufsrechnung verwendet werden.  

### Einkauf für die Buchung von Rechnungen mit Einfuhrumsatzsteuer einrichten

1. Richten Sie eine Kreditorenkarte für die Einfuhrbehörde ein, die Ihnen die Einfuhrumsatzsteuerrechnung sendet. Die **Geschäftsbuchungsgruppe** und **MWST-Geschäftsbuchungsgruppe** werden genauso eingerichtet, wie das Fibukonto für die Einfuhrumsatzsteuer.  
2. Erstellen Sie eine **Produktbuchungsgruppe** für die Einfuhrumsatzsteuer, und richten Sie eine **Vorg.-MWST.-Produktbuchungsgruppe** für die Einfuhrumsatzsteuer für die zugehörige **Produktbuchungsgruppe** ein.  
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
4. Markieren Sie das Fibukonto Einfuhrumsatzsteuer und wählen Sie dann die Aktion **Bearbeiten**.  
5. Wählen Sie auf dem Inforegister **Buchung** im Feld **Produktbuchungsgruppe** die Option MWST aus. [!INCLUDE[prod_short](includes/prod_short.md)] wird automatisch das Feld **MWST Prod. Buchungsgruppe** ausfüllen.  
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Allgemeine Buchungsmatrixeinrichtung** ein, und wählen Sie dann den zugehörigen Link.  
7. Im Fenster erstellen Sie eine Kombination **Gen. Bus. Buchungsgruppe** für die MWST-Behörde und der **Gen. Prod. Buchungsgruppe** für die Einfuhrumsatzsteuer. Für diese Kombination im Feld **Einkaufskonto** wählen Sie das Fibukonto für die Einfuhr-MWST aus.  

### So erstellen Sie eine neue Rechnung für die als Kreditor fungierende Einfuhrbehörde, nachdem Sie die Einrichtung abgeschlossen haben  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Einkaufsrechnung.  
3. Wählen Sie im Feld **Kreditorennr.** die als Kreditor fungierende Einfuhrbehörde, und klicken Sie danach auf **OK**.  
4. Klicken Sie in der ersten Einkaufszeile im Feld **Art**und wählen Sie **Fibukonto** und dann das **Nr.** Feld, wählen das Fibukonto Einfuhr-MWST aus.  
5. Geben Sie im Feld **Menge** den Wert **1** ein.  
6. Geben Sie im Feld **EK-Preis ohne MWST** den MWST-Betrag an.  
7. Buchen Sie die Rechnung.  

## Versorgungszertifikate verarbeiten

Wenn Sie Waren an einen Debitor in einem anderen EU-Land/einer anderen EU-Region verkaufen, müssen Sie dem Debitoren eine Gelangensbestätigung zusenden, die dieser unterschreiben und an Sie zurücksenden muss. Die folgenden Verfahren sind für die Bearbeitung von Zertifikaten von Vorrat für Verkaufslieferungen gedacht, dieselben Schritte gelten jedoch auch für Servicelieferungen von Artikeln und Rücklieferungen an Kreditoren.  

### So zeigen Sie die Details der Gelangensbestätigung an  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Gebuchte Verkaufslieferungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die relevante Verkaufslieferung an einen Debitor in einem anderen EU-Land/einer anderen EU-Region aus.  
3. Wählen Sie **Details der Gelangensbestätigung**.  
4. Standardmässig ist bei der Einrichtung des MWST-Buchungsgruppen-Setup für den Debitor das Kontrollkästchen **Gelangensbestätigung erforderlich** ausgewählt, dann ist das Feld **Status** standardmässig auf **Erforderlich** festgelegt. Sie können das Feld automatisch aktualisieren, um anzugeben, dass Sie das Zertifikat von dem Debitor erhalten haben.  

> [!Note]  
>  Wenn bei der MWST.-Buchungsgruppen-Einrichtung nicht das Kontrollkästchen **Gelangensbestätigung erforderlich** ausgewählt ist, wird ein Datensatz erstellt und das Feld **Status** auf **Nicht anwendbar** festgelegt. Sie können das Feld automatisch aktualisieren, um die richtigen Statusinformationen widerzuspiegeln. Sie können den Status bei Bedarf manuell von **Nicht anwendbar** in **Erforderlich** und von **Erforderlich** in **Nicht anwendbar** ändern.  

   Wenn Sie das Feld **Status** von **Erforderlich** in **Empfangen** oder in **Nicht erhalten** aktualisieren, wird ein Zertifikat erstellt.  

> [!TIP]  
>  Sie können auf der Seite **Gelangensbestätigung** verwenden, um eine Ansicht des Status aller gebuchten Lieferungen zu erhalten, für die eine Gelangensbestätigung erstellt wurde.  

5. Wählen Sie **Gelangensbestätigung drucken**.  

> [!Note]  
> Sie können den Beleg in der Vorschau anzeigen oder drucken. Wenn Sie **Gelangensbestätigung drucken** auswählen und den Beleg drucken, wird das Kontrollkästchen **Gedruckt** automatisch ausgewählt. Darüber hinaus wird der Status des Zertifikats, wenn dies nicht bereits angegeben ist, zu **Erforderlich** aktualisiert. Sofern erorderlich, legen Sie das gedruckte Zertifikat der Lieferung bei.  

### So drucken Sie eine Gelangensbestätigung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Gebuchte Verkaufslieferungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die relevante Verkaufslieferung an einen Debitor in einem anderen EU-Land/einer anderen EU-Region aus.  
3. Wählen Sie **Gelangensbestätigung drucken**.  

> [!NOTE]  
> Alternativ können Sie ein Zertifikats im Fenster **Gelangensbestätigung** drucken.  

4. Setzen Sie den Umschaltstatus auf **Positionsdetails drucken**, um Informationen aus den Zeilen im Warenausgangsbeleg auf der Gelangensbestätigung zu berücksichtigen.  
5. Damit [!INCLUDE[prod_short](includes/prod_short.md)] Zertifikate für gebuchte Lieferungen erstellt, für die noch keine vorliegen, aktivieren Sie die Option **Gelangensbestätigungen erstellen, falls nicht bereits erstellt**. Wenn Sie die Option aktivieren, werden neue Zertifikate für alle gebuchten Lieferungen erstellt, die über keine Zertifikate innerhalb des ausgewählten Bereichs verfügen.  
6. Standardmässig betreffen die Filtereinstellungen den Warenausgangsbeleg, den Sie ausgewählt haben. Füllen Sie die Filterinformationen aus, um eine spezifische Gelangensbestätigung auszuwählen, die Sie drucken möchten.  
7. Wählen Sie im Fenster **Gelangenbestätigung** die Schaltfläche **Drucken** aus, um den Bericht zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.  

   > [!Note]  
   > Das **Gelangenbestätigung**-Feld und das Feld **Gedruckt**werden für die Lieferung auf der Seite **Gelangensbestätigungen** aktualisiert.  

8. Sie müssen die gedruckte Gelangensbestätigung zur Unterschrift an den Debitor senden.  

### Um den Status einer Gelangensbestätigung für eine Lieferung zu aktualisieren  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Gebuchte Verkaufslieferungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die relevante Verkaufslieferung an einen Debitor in einem anderen EU-Land/einer anderen EU-Region aus.  
3. Wählen Sie im Feld **Status** die entsprechende Option aus.  

   Wenn der Debitor eine Gelangensbestätigung zurücksendet, wählen Sie **Erhalten** aus. Das Feld **Eingangsdatum** wird aktualisiert. Standardmässig ist das Wareneingangsdatum auf das aktuelle Arbeitsdatum festgelegt.  

   Sie können das Datum ändern, sodass das Datum angezeigt wird, an dem Sie die unterschriebene Gelangensbestätigung des Debitors erhalten haben. Sie können mit der Standard-[!INCLUDE[prod_short](includes/prod_short.md)]-Verknüpfung einen Link zu dem unterschriebenen Zertifikat hinzufügen.  

   Wenn der Debitor keine Gelangensbestätigung zurücksendet, wählen Sie **Nicht erhalten** aus. Sie müssen dem Debitor dann eine neue Rechnung mit MWST senden, da das Finanzamt die ursprüngliche Rechnung nicht akzeptiert.  

Um eine Gruppe von Zertifikaten anzuzeigen, beginnen Sie auf der Seite **Gelangensbestätigungen** und aktualisieren dann die Informationen über den Status der ausstehenden Zertifikate nach und nach, wenn Sie sie von den Debitoren erhalten. Die aktualisierten Informationen können hilfreich sein, wenn Sie für alle Zertifikate suchen möchten, die einen bestimmten Status haben, beispielsweise **Erforderlich**, um deren Status auf **Nicht erhalten** zu aktualisieren.  

### Um den Status einer Gelangensbestätigungsgruppe zu aktualisieren  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Gelangensbestätigungen** ein, und wählen Sie den entsprechenden Link.  
2. Dient zum Filtern des Feldes **Status** über den gewünschten Wert, um die Liste der Zertifikate zu erstellen, die Sie verwalten möchten.  
3. Um die Statusinformationen zu aktualisieren, aktivieren Sie **Liste bearbeiten**.  
4. Wählen Sie im Feld **Status** die entsprechende Option aus.  

   Wenn der Debitor eine Gelangensbestätigung zurücksendet, wählen Sie **Erhalten** aus. Das Feld **Eingangsdatum** wird aktualisiert. Standardmässig ist das Wareneingangsdatum auf das aktuelle Arbeitsdatum festgelegt.  

   Sie können das Datum ändern, sodass das Datum angezeigt wird, an dem Sie die unterschriebene Gelangensbestätigung erhalten haben. Sie können mit der Standard-[!INCLUDE[prod_short](includes/prod_short.md)]-Verknüpfung einen Link zu dem unterschriebenen Zertifikat hinzufügen.  

> [!NOTE]
> Sie können keine neue Gelangensbestätigung auf der Seite **Gelangensbestätigung** erstellen, indem Sie sie mithilfe dieses Verfahrens öffnen. Um ein Zertifikat für eine Lieferung zu erstellen, die nicht so eingerichtet wurde, dass eines erforderlich ist, öffnen Sie die gebuchte Verkaufslieferung und eine der beiden zuvor beschriebenen Verfahren:  
>
> * So erstellen Sie eine Gelangensbestätigung manuell  
> * So drucken Sie eine Gelangensbestätigung.

## Siehe auch 

[Methoden für die Berechnung und Buchung der Salestax einrichten](finance-setup-vat.md)  
[MWST an die Steuerbehörde melden](finance-how-report-vat.md)  
[Eine Umsatzsteuer-Identifikationsnummer überprüfen](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
