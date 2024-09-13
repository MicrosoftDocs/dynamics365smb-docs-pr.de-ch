---
title: Mehrere Umsatzsteuer-Identifikationsnummern
description: Informieren Sie sich über die Funktionsweise mehrerer (alternativer) Umsatzsteuer-Identifikationsnummern.
author: altotovi
ms.topic: conceptual
ms.reviewer: null
ms.search.keywords: 'VAT, multiple, alternative, customer, tax, value-added tax'
ms.search.form: '212, 301,'
ms.date: 08/21/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="multiple-vat-registration-numbers"></a>Mehrere Umsatzsteuer-Identifikationsnummern

Für Unternehmen mit Lagern in mehreren EU-Ländern kann die Verwaltung der Mehrwertsteuer (Mehrwertsteuer) eine Herausforderung darstellen, da für jeden Lagerstandort eine andere Mehrwertsteuernummer erforderlich ist, um den spezifischen Bestimmungen des jeweiligen Landes zu entsprechen. Dieser Artikel informiert über diese Anforderung und erläutert die Funktionsweise mehrerer Umsatzsteuer-Identifikationsnummern. Mit dieser Funktion können Benutzer Steuerregistrierungsnummern für ihre Kunden in verschiedenen Ländern/Regionen einrichten.  

> [!NOTE]
> Die Funktion  *Mehrere Umsatzsteuer-Identifikationsnummern für Kunden*  ist erst ab Business Central 2024 folgen 2 (Version 25) verfügbar.

## <a name="how-to-set-up-the-alternative-vat-registration-numbers"></a>So richten Sie die alternativen Umsatzsteuer-Identifikationsnummern ein

Um alternative Umsatzsteuer-Identifikationsnummern für verschiedene Länder/Regionen einzurichten, führen Sie folgen diese Schritte aus: 

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie  **Alternative Umsatzsteuer-Identifikationsnummer des Kunden** und dann Auswählen das zugehörige verknüpfen ein. 
2. Fügen Sie den Kunden im Feld  **Kundennummer**  und das Land/die Region, das/die sich auf diese Umsatzsteuerregistrierung bezieht, im Feld  **Umsatzsteuer-Länder-/Regionscode hinzu**.  
3. Sie müssen die Umsatzsteuer-Identifikationsnummer im Feld  **Umsatzsteuer-Identifikationsnummer**  eingeben. Sie müssen das Format einhalten, wenn Sie den  **Länder-/Regionscode** verwenden. 
4. Wenn Sie unterschiedliche Mehrwertsteuer- oder allgemeine Buchungsgruppen verwenden möchten, können Sie diese alternativ in den Feldern  **Mehrwertsteuer-Buchungsgruppe**  und  **Allgemeine Geschäftsbuchungsgruppe**  zum Setup hinzufügen. 
5. Schliessen Sie die Seite.   

Um eine alternative Adresse für Ihren Kunden zu erstellen, führen Sie die folgenden Schritte aus:  

1. Öffnen Sie den  **Kunden** Karte für den Kunden, dem Sie eine neue  **Lieferadresse** hinzufügen möchten. 
2. Auswählen **Kunde**, und wählen Sie die Aktion  **Lieferadressen** .   
3. Die Seite  **Liste der Lieferadressen**  wird geöffnet. Wählen Sie  **Neu** aus. 
4. Geben Sie die Informationen zum Lieferziel Ihres Kunden ein.  
5. Wählen Sie den richtigen  **Länder-/Regionscode**.   
6. Wenn Sie unter  **Alternative Kunden-Umsatzsteuerregistrierung** für dieses Land oder diese Region bereits eine neue  **Umsatzsteuer-Identifikationsnummer** konfiguriert haben, geschieht nichts. 
7. Wenn Sie jedoch die  **Umsatzsteuer-Identifikationsnummer** zuvor nicht unter  **Alternative Umsatzsteuer-Identifikationsnummer des Kunden** für dieses Land oder diese Region konfiguriert haben, wird die folgende Benachrichtigung angezeigt:  **Klicken Sie auf „Hinzufügen“, wenn Sie die alternative Umsatzsteuer-Identifikationsnummer für diesen Ländercode des Versandempfängers einfügen möchten.** 
8. Es erscheint eine Benachrichtigung mit der Warnung, dass Sie eine neue Umsatzsteuer-Identifikationsnummer hinzufügen sollten. Wählen Sie hierzu in der Benachrichtigung die Aktion  **Hinzufügen** . Daraufhin wird die Seite  **Alternative Umsatzsteuer-Identifikationsnummer des Kunden**  geöffnet. 
9. Auf dieser Seite wird Ihre  **Kundennummer eingetragen.** Und den  **MwSt.-Länder-/Regionscode**. Sie müssen also nur das Setup hinzufügen, das Sie verwenden möchten. 

## <a name="work-with-the-sales-documents"></a>Arbeiten mit den Verkaufsbelegen

Sie können eine neue  [Verkaufsrechnung](sales-how-invoice-sales.md) oder einen neuen  [Verkaufsauftrag](sales-how-sell-products.md) in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen. Wenn Sie eine Lieferadresse verwenden müssen, die von der Adresse des Kunden abweicht und in einem anderen Land liegt, folgen Sie die Schritte:  

### <a name="alternate-shipping-address"></a>Alternative Lieferadresse

1. Erweitern Sie die Registerkarte  **Versand und Rechnungsstellung** .   
2. Wählen Sie im Feld „Lieferadresse“ die Option  **Alternative Lieferadresse** . 
3. Die Seite  **Liste der Lieferadressen**  mit verfügbaren alternativen Adressen wird angezeigt. 
4. Wählen Sie eine der Adressen mit unterschiedlichem  **Länder-/Regionscode**. 
5. Die Dialogseite  **Alternative Kunden-Umsatzsteuer-Registrierung bestätigen**  wird mit einer Liste der Felder angezeigt, die Sie aufgrund der Einrichtungsänderung für die  **Alternative Kunden-Umsatzsteuer-Registrierung**  geändert haben. 
6. Auswählen **OK** zur Bestätigung.   

> [!NOTE]
> Wenn Sie eine solche Auswahl nicht mehr bestätigen möchten, können Sie das Feld  **Nicht mehr anzeigen**  mit Auswählen markieren. In Zukunft werden Ihnen diese Art von Benachrichtigungen über Änderungen nicht mehr angezeigt. Wenn Sie sie jedoch erneut aktivieren möchten, können Sie dies tun, indem Sie das Feld  **Alternative Mehrwertsteuerregistrierung bestätigen**  unter  **Mehrwertsteuer-Setup** aktivieren.  
   
7. Nach der Bestätigung werden die Werte mit den Werten aus der Einrichtung der  **Alternativen Kunden-Umsatzsteuer-Registrierung**  überschrieben. Sie können alle mit der Mehrwertsteuer in Zusammenhang stehenden Felder unter der Registerkarte  **Rechnungsdetails**  überprüfen.  
8. Buchen Sie den Beleg.  

### <a name="custom-address"></a>Benutzerdefinierte Adresse

Falls Sie die Lieferadresse nicht konfiguriert haben, aber dennoch eine andere Adresse für den Versand verwenden möchten, können Sie diese Option nutzen.  

1. Erweitern Sie die Registerkarte  **Versand und Rechnungsstellung** .   
2. Wählen Sie im Feld „Lieferempfänger“ die Option  **Benutzerdefinierte Adresse** .  
3. Ändern Sie das Land im Feld  **Land/Region** .  
4. Sobald Sie den Länder-/Regionscode so geändert haben, dass er mit dem  **Länder-/Regionscode für die Umsatzsteuer**  der  **alternativen Umsatzsteuerregistrierung des Kunden** übereinstimmt, wird die Dialogseite  **Alternative Umsatzsteuerregistrierung des Kunden bestätigen**  mit einer Liste der geänderten Felder angezeigt. 
5. [!INCLUDE[prod_short](includes/prod_short.md)] ändert außerdem alle mit der Mehrwertsteuer in Zusammenhang stehenden Felder unter der Registerkarte  **Rechnungsdetails** .  

### <a name="work-with-no-shipment"></a>Arbeiten ohne Sendung

Wenn im Rahmen des Prozesses kein Versand erfolgt, können Sie dennoch von der Einrichtung der  **Alternativen Kunden-Mehrwertsteuerregistrierung**  profitieren.

Sie finden den  **Länder-/Regionscode für die Mehrwertsteuer**  im Verkaufsauftrag oder in der Rechnung unter der Registerkarte  **Rechnungsdetails**  und können dort den Wert angeben, der mit der Einrichtung der  **Alternativen Mehrwertsteuerregistrierung des Kunden**  übereinstimmt. Und Sie sollten dieselbe Bestätigungsdialogseite wie oben sehen. 

In diesem Fall können Sie eine Verkaufsrechnung mit der richtigen  **Umsatzsteuer-Identifikationsnummer**  für Ihren Kunden buchen, auch wenn Sie mit diesem Dokument keine Artikel versenden. 

### <a name="work-with-the-sales-credit-memo"></a>Arbeiten mit der Verkaufsgutschrift

Wenn Sie die Rechnung mit einer  **Lieferadresse** oder einem  **MwSt.-Länder-/Regionscode**  buchen, der andere Buchungsdaten aufweist, übernimmt die korrigierende  **Verkaufsgutschrift** die Werte aus der  **gebuchten Verkaufsrechnung** Kopfzeile, während diese Werte aus der  **alternativen Umsatzsteuerregistrierung des Kunden** stammen. Es sind also keine weiteren Aktionen erforderlich. 

## <a name="see-also"></a>Siehe auch

[Überblick zur Umsatzsteuerverwaltung](finance-manage-vat.md)    
[Mehrwertsteuer einrichten](finance-setup-vat.md)    
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)    
[Melden Sie die Mehrwertsteuer an eine Steuerbehörde](finance-how-report-vat.md)    
[Lokale Funktion in Business Central](about-localization.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
