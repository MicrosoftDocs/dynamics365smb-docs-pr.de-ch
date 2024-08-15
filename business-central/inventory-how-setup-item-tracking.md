---
title: 'Artikeltracking mit Serien-, Chargen- und Paketnummern einrichten'
description: 'Artikeltracking mit Seriennummern, Chargennummern und Paketnummern einrichten'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# Artikeltracking mit Serien-, Chargen- und Paketnummern einrichten

Behalten Sie den Überblick über Lagerartikel auch in komplexen Lagerkonfigurationen mit Nummern, die für jeden Artikel spezifisch sind, entweder als einzelnes Objekt, als Charge oder als Paket. Mit dem Artikeltracking können Sie Artikel über interne Lagerbewegungen sowie ausgehende und eingehende Belege verfolgen.

Gibt gebuchte Serien- und Chargennummern an, die in einer Lieferkette vorwärts oder rückwärts verfolgt werden können. Dies ist für allgemeine Massnahmen für die Qualitätssicherung und für Rückrufe eines fehlerhaften Produktes nützlich. Weitere Informationen finden Sie unter [Nachverfolgte Artikel reservieren](inventory-how-to-trace-item-tracked-items.md).  

## Zahlen‑ und Artikeltracking

Im Rahmen Ihrer Lagerprozesse können Sie Ihren Lagerbestand in Paketen, Kartons, Containern usw. bündeln. Um den Überblick über die Artikel zu behalten, weisen Sie eindeutige Nummern als Identifikation zu. Sie stellen beispielsweise einen Stuhl mit der Artikelnummer *1900-S* her und verkaufen ihn. Jeder einzelne Stuhl hat eine Seriennummer, *1001*, aber Sie bündeln auch vier Stühle zu einer Charge, *LOT0001*, und Sie versenden die Stühle in einem Container mit der Paketnummer *CONTAINER010*. Das schliesst auch andere Elemente ein, wie z. B. *LOT0100* mit Beistelltischen und *LOT200* mit Lampen.  

Abhängig von Ihrer Konfiguration verwenden Sie diese unterschiedlichen Nummern, um den Lagerbestand in [!INCLUDE [prod_short](includes/prod_short.md)] in den verschiedenen Phasen des Einkaufs, Verkaufs, Lagerbetriebs usw. zu verfolgen.

## Um Artikelverfolgungscodes einzurichten

Ein Artikeltrackingcode spiegelt die unterschiedlichen Betrachtungen wider, die ein Unternehmen bezüglich der Verwendung von Serien- und Chargennummern von Artikeln anstellt, die sich durch das Lager bewegen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Artikeltrackingen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Definieren Sie auf den Inforegistern  **Seriennr.**,  **Chargennr.** und  **Paketverfolgung**  Richtlinien für die Artikelverfolgung nach Serien-, Chargen- und Paketnummern.  

> [!NOTE]  
> Wenn Sie bestimmte Artikel oder Chargen während der Lebensdauer verfolgen möchten, müssen Sie die Felder **Seriennr. Tracking**, **Chargennr. Tracking** bzw. **Paketspezifisches Tracking** auswählen. Wenn Sie eine ausgehende Einheit eines Artikels mit dem Artikeltrackingcode verarbeiten, müssen Sie immer angeben, welche vorhandene Seriennummer oder welche vorhandene Chargennummer betroffen sein soll. Das bedeutet, dass der Artikel, von dem eine gewissen Menge verkauft wird, aus einem bestimmten Bereich von Seriennummern im Lagerbestand entnommen werden muss. Mit anderen Worten, die Serien-, Chargen oder Paketnummer, die einem Artikel beim Wareneingang zugewiesen wurde, muss genau derjenigen beim Warenausgang entsprechen.

Da diese Einrichtungsfelder alle möglichen Transaktionen für den Artikel abdecken, werden die einzelnen Felder für Eingang und Ausgang ebenfalls mit Häkchen versehen. Die einzelnen Ein-/Ausgangsfelder haben jedoch nichts mit der bestandsübergreifenden Anwendung zu tun. Sie definieren lediglich den Workflow Ihres Unternehmens bezüglich der Zuweisung von Artikeltrackingnummern.  

> [!NOTE]  
> Um Artikeltrackingnummern bei Lageraktivitäten zuzuordnen, müssen die Felder **Seriennr.-Verf. Lager** und **Chargennr.-Verf. Lager** auf der Karte des Artikels ausgewählt werden.  

## Regeln für den Ablauf von Serien- oder Chargennummern einrichten:

Für einige Artikel möchten Sie möglicherweise spezielle Ablaufdaten und Regeln in dem Artikeltrackingcode festlegen. Diese Funktionalität ermöglicht Ihnen nachzuvollziehen, wann bestimmte Serien- und Chargennummern ablaufen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Artikeltrackingen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie einen bestehenden Artikeltrackingcode aus bestehenden Artikelkarten aus, und wählen Sie die Aktion **Bearbeiten**.  
3. Aktivieren Sie im Inforegister **Sonst.** die folgenden Felder:  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Fixes Ablaufdatum**|Gibt an, dass ein Ablaufdatum, das der Artikeltrackingsnummer beim Wareneingang zugewiesen wurde, beim Warenausgang berücksichtigt werden muss.|  
    |**Ablaufdateneintrag anfordern**|Gibt an, dass Sie in der Artikeltrackingzeile ein Ablaufdatum eingeben müssen.|  
    |**Ablaufdatumsangaben verwenden**|Gibt an, dass Sie keine Ablaufdatumsangaben berechnen möchten. |  

## Garantien für Serien- oder Chargennummern einrichten:

Für einige Artikel möchten Sie möglicherweise spezielle Garantievereinbarungen in dem Artikeltrackingcode festlegen. Diese Funktionalität ermöglicht Ihnen nachzuvollziehen, wann die Garantien auf spezielle Serien- oder Chargennummern in Ihrem Lager auslaufen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Artikeltrackingen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie einen bestehenden Artikeltrackingcode aus bestehenden Artikelkarten aus, und wählen Sie die Aktion **Bearbeiten**.  
3. Füllen Sie im Inforegister **Sonstiges** das Feld **Garantiedatumsformel** aus, und markieren Sie die Felder wie folgt:  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Garantiedatumsformel**|Gibt das letzte Garantiedatum für den Artikel an.|  
    |**Garantiedatumseintrag anfordern**|Zeigt an, dass Sie in der Artikeltrackingzeile manuell ein Garantiedatum eingeben müssen.|  

## So richten Sie Artikel für die Tracking mit den richtigen Artikeltrackingcodes ein

Um die Artikelverfolgung zu aktivieren, müssen Sie zunächst einem Artikel die Artikelverfolgungscodes zuweisen. Es gibt zwei Möglichkeiten, Artikeltrackingcodes hinzuzufügen, indem Sie den Code aus einer vordefinierten Liste auswählen oder einen neuen eindeutigen Code zuweisen. Zeigen Sie mit der Maus auf die Felder, um eine Kurzbeschreibung zu lesen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Element** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie einen vorhandenen Artikel aus der Liste aus, und öffnen Sie die Seite **Artikelkarte**.  
3. Weisen Sie im Inforegister **Artikeltracking** die entsprechenden Artikeltrackingcodes zu, und wählen Sie den **Artikeltrackingcode**, die **Seriennummern** und die **Chargennummern** aus.
    1. Alternativ können Sie auch einen neuen Artikeltrackingcode erstellen, indem Sie die Aktion **Neu** auswählen.

## Um Eröffnungssalden für die Artikel anzugeben, verfolgen Sie

Sie können Anfangssalden für die von Ihnen verfolgten Artikel erstellen. Da Sie verschiedene Lagerkonfigurationen wählen können, gibt es zwei Möglichkeiten:

* Aktivieren Sie bestimmte Stapel auf der Seite **Artikel Erf.-Journal**, auf der Serien-, Chargen- und Verpackungsdaten direkt in Erfassungsjournalzeilen eingeben können.
* Für Standorte, an denen der Umschalter **Gezieltes Einlagern und Kommissionieren** eingeschaltet ist, verwenden Sie die Seite **Logistik Inventur Erf.-Journal** , um alle Artikeltrackingfelder verfügbar zu machen. Zu den verfügbaren Feldern gehören die Felder **Garantiedatum** und **Ablaufdatum**.

### Artikel-Erfassungsjournale

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Element Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Feld **Name** aus, um eine Liste der Artikel Erf.-Journalnamen zu öffnen.
3. Wählen Sie **Neu**, um einen neuen Stapel zu erstellen, und schalten Sie dann den Umschalter **Artikeltracking auf Positionen** ein.
4. Wählen Sie **OK**, um den von Ihnen erstellten Stapel auszuwählen.
5. Füllen Sie die Felder auf der Artikel Erf.-Journalzeile wie erforderlich aus. Beachten Sie, dass die Felder **Chargennr.**, **Seriennr.**, **Ablaufdatum**, **Garantiedatum** und **Paketnr.** zur Verfügung stehen, (wenn das Feature aktiviert ist).
6. Wählen Sie die Aktion **Buchen** aus, um das Lager zu regulieren.

> [!NOTE] 
> [!INCLUDE [prod_short](includes/prod_short.md)] führt einige kleinere Überprüfungen durch, wenn Sie Daten eingeben oder importieren. Eine umfassendere Prüfung findet statt, wenn Sie Daten aus Erfassungsjournalzeilen auf der Seite **Artikeltracking** buchen oder dorthin übertragen. Letzteres geschieht automatisch, wenn Sie die Seite **Artikeltracking** aus der Artikelerfassungsjournal-Zeile öffnen oder die Aktion **Artikeltrackingzeilen aktualisieren** auswählen.

### Logistik Inventur Erf.-Journal für Standorte, für welche die direkte Kommissionierung und Einlagerung aktiviert ist  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Geben Sie **Logistik Inventur Erf.-Journal** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder auf der Artikel Erf.-Journalzeile wie erforderlich aus. Beachten Sie, dass die Felder **Chargennr.**, **Seriennr.**, **Ablaufdatum**, **Garantiedatum** und **Paketnr.** zur Verfügung stehen, (wenn das Feature aktiviert ist).
3. Wählen Sie die Aktion **Journal** aus, die Lagerregulierungen vorzunehmen. Denken Sie daran, dass die korrigierten Lagerplatzposten mit den entsprechenden Lagerposten synchronisieren müssen. Um mehr zu erfahren, gehen Sie zu [Die korrigierten Lagerplatzeinträge synchronisieren](/dynamics365/business-central/inventory-how-count-adjust-reclassify#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

Verwenden Sie für Massenimporte Konfigurationspakete, um Daten in die Erfassungsjournale zu importieren.

> [!NOTE]
> Sie können **In Excel bearbeiten** nicht verwenden, um Erfassungsjournalzeilen mit Trackinginformationen zu erstellen.

## Siehe auch 

[Arbeiten mit Chargennummern und Seriennummern](inventory-how-work-item-tracking.md)  
[Ablaufverfolgung der Artikel mit Artikelverfolgung](inventory-how-to-trace-item-tracked-items.md)  
[Bestand](inventory-manage-inventory.md)  
[Designdetails: Artikeltracking](design-details-item-tracking.md)  
[Designdetails: Artikeltracking und Reservierungen](design-details-item-tracking-and-reservations.md)  
[Artikel reservieren](inventory-how-to-reserve-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
