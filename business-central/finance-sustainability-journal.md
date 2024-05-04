---
title: Nachhaltigkeitsposten erfassen
description: 'Erfahren Sie, wie Sie Treibhausgasemissionen erfassen.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="how-to-record-sustainability-entries"></a>Nachhaltigkeitsposten erfassen

Derzeit ist die einzige Möglichkeit zur Erfassung von Treibhausgasemissionen im **Nachhaltigkeitssachkonto** die Verwendung von **Nachhaltigkeits-Erfassungsjournalen**.   

## <a name="sustainability-journal"></a>Nachhaltigkeits-Erf.-Journal

**Nachhaltigkeits-Erfassungsjournale** sind für die Nachverfolgung und Erfassung von Nachhaltigkeitsaktivitäten konzipiert und bieten dieselbe Benutzererfahrung wie andere Erfassungsjournale in Business Central. Innerhalb des Erf.-Journals haben Benutzende die Möglichkeit, Emissionen manuell einzugeben, sofern sie über die erforderlichen Informationen verfügen. Falls diese Daten nicht vorliegen, können sie alternativ integrierte Formeln verwenden, um die Emissionen auf der Grundlage spezifischer bekannter Parameter, die verschiedenen Arten von Quellen und Konten entsprechen, genau zu berechnen. 

Die in ein Erf.-Journal eingegebenen Informationen sind temporär und können geändert werden, solange sie sich im Erf.-Journal befinden. Wenn Sie das Erf.-Journal buchen, werden die Informationen in **Nachhaltigkeitsposten** auf einzelnen **Nachhaltigkeitskonten** übertragen, wo sie nicht geändert werden können. Es ist jedoch möglich, Storno- oder Korrekturbuchungen vorzunehmen.  

### <a name="use-journal-templates-and-batches"></a>Erf.-Journalvorlagen und -namen verwenden

Es gibt standardmässig zwei **Nachhaltigkeits-Erf.-Journalvorlagen**: die Standardvorlage und die wiederkehrende Vorlage. Sie können zu jeder Erfassungsjournalvorlage mehrere Erfassungsjournalnamen als Journal-Stapel erstellen. Wählen Sie hierzu auf der Seite **Nachhaltigkeits-Erf.-Journalvorlagen** die Aktion **Batch** aus und erstellen Sie auf der neuen Seite den neuen **Nachhaltigkeits-Erf.-Journalbatch**. So können Sie beispielsweise für jeden Emissionsscope einen eigenen Erf.-Journalbatch festlegen. Hierzu verwenden Sie die Option **Emissionsscope** und können zwischen drei vorhandenen Scopes wählen. Sie können auch den **Quellcode** und den **Ursachencode** für jeden Batch hinzufügen oder ändern. 

>[!TIP]
>Wenn Sie über viele Zeilen verfügen, können Sie für jede Emissionsart einen Erf.-Journalbatch haben, da dies die Fehlerwahrscheinlichkeit verringern kann. Sie können jedoch auch den gemeinsamen Batch für alle Emissionsarten verwenden.   

### <a name="validating-sustainability-journals"></a>Nachhaltigkeits-Erfassungsjournale überprüfen

Sie können auf der Seite **Nachhaltigkeitseinrichtung** eine Hintergrundprüfung einschalten, um Verzögerungen beim Buchen zu vermeiden. Die Prüfung benachrichtigt Sie, wenn bei der Arbeit am **Nachhaltigkeits-Erf.-Journal** ein Fehler aufgetreten ist und dieser das Buchen des Erf.-Journals verhindert.  

Wenn Sie die Prüfung aktivieren, werden in der Infobox **Erf.-Journal Prüfung** Probleme in der aktuellen Zeile und im gesamten Batch angezeigt. Die Überprüfung erfolgt, wenn Sie einen Erf.-Journalbatch laden und eine andere Erfassungsjournalzeile auswählen. Die Kachel **Probleme insgesamt** in der Infobox zeigt die Gesamtanzahl von Problemen, die [!INCLUDE [prod_short](includes/prod_short.md)] gefunden hat. Sie können sie auswählen, um eine Übersicht über die Probleme zu öffnen. 

### <a name="work-with-sustainability-journals"></a>Mit Nachhaltigkeits-Erfassungsjournalen arbeiten

Um mit den **Nachhaltigkeits-Erfassungsjournalen** zu arbeiten, gehen Sie wie folgt vor:   

1. Wählen Sie die ![Glühbirne, welche die 3. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Nachhaltigkeits-Erf.-Journal** ein und wählen Sie dann den zugehörigen Link. 
2. Auf der Seite **Nachhaltigkeits-Erf.-Journal** können Sie so viele Zeilen eingeben, wie Sie mit demselben Batch buchen möchten.  
3. Sie können die Option **Belegart** leer lassen oder sich für die Verwendung von **Rechnung** oder **Gutschrift** entscheiden.  
4. Im Feld **Kontonr.** können Sie **Nachhaltigkeitskonten** nur auswählen, wenn das Feld **Direktbuchung** aktiv ist, **Buchung** als **Buchungsart** festgelegt und das Konto nicht gesperrt ist. Ausserdem muss für Konten die Kategorie und Unterkategorie konfiguriert sein.  

>[!NOTE]
>Wenn Sie den Batch verwenden, bei dem der Emissionsscope konfiguriert ist, muss der **Emissionsscope** im **Nachhaltigkeitskonto** mit dem **Emissionsscope** in dem verwendeten Batch übereinstimmen.  

5. Sie haben zwei Möglichkeiten: Entweder Sie buchen die Beträge manuell oder Sie verwenden Formeln.   

    1. Wenn Sie über genaue Informationen zu den Emissionen verfügen und diese buchen möchten (d. h., sie stehen auf der erhaltenen Rechnung), müssen Sie das Feld **Manuelle Eingabe** auswählen, um anzugeben, dass die Beträge manuell eingegeben werden. In diesem Fall können Sie Ihre Daten nicht in die Felder **Kraftstoff/Strom**, **Entfernung**, **Benutzerdefinierter Betrag**, **Installationsmultiplikator** und **Zeitfaktor** eingeben, da sie für diese Auswahl nicht bearbeitet werden können. Die Felder **CO2-Emission**, **CH4-Emission** und **N2O-Emission** sind jedoch editierbar und Sie können Ihre Daten direkt dort eingeben. 
    2. Wenn Sie Ihre Emissionen nicht genau kennen, müssen Sie sie berechnen. Dabei darf das Feld **Manuelle Eingabe** nicht ausgewählt sein. In diesem Fall können die Felder **CO2-Emission**, **CH4-Emission** und **N2O-Emission** nicht bearbeitet werden. Sie können Ihre Berechnungsdetails jedoch basierend auf der von Ihnen verwendeten Formel eingeben. Weitere Informationen zu den verwendeten Formeln und Definitionen in der **Kategorie des Nachhaltigkeitskontos** finden Sie unter [Diagramm der Nachhaltigkeitskonten und Nachhaltigkeitssachkonto](finance-sustainability-accounts-ledger.md#account-categories).
    
7. Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Erfassungsjournal zu buchen. Beim Buchen in einem **Nachhaltigkeits-Erf.-Journal** werden Posten im **Nachhaltigkeitssachkonto** generiert. 

Falls Ihre Formel auf der Option **Aus Finanzbuchhaltung berechnen** in der **Kategorie des Nachhaltigkeitskontos** beruht, müssen Sie die Aktion **Betrag aus Fibuposten erfassen** vor der Buchung des Erf.-Journals verwenden, um die Emissionen basierend auf dieser Datenquelle zu berechnen. Wenn Sie nach dem Ausfüllen der Buchblattzeilen Änderungen an den Emissionsfaktoren vorgenommen haben, müssen Sie ausserdem die Aktion **Neu berechnen** auswählen, um den richtigen Betrag im Erf.-Journal zu erhalten.  

### <a name="recurring-journals"></a>Wiederkehrende Erfassungsjournale

Ein wiederkehrendes Erfassungjournal ist ein **Nachhaltigkeits-Erf.-Journal** mit spezifischen Feldern zur Verwaltung von Transaktionen, die Sie häufig mit wenigen oder gar keinen Änderungen buchen. Zum Beispiel Nachhaltigkeitstransaktionen wie Strom, Wärme oder andere ähnliche Transaktionen. Mithilfe wiederkehrender Erfassungsjournale können Sie feste und variable Beträge buchen. Mit einem wiederkehrenden Erf.-Journal erstellen Sie die Posten, die regelmässig nur einmal gebucht werden sollen. So bleiben beispielsweise die Konten, Dimensionen, Dimensionswerte usw. nach der Buchung im Journal erhalten. Falls Änderungen erforderlich sind, können Sie diese bei jeder Buchung vornehmen. 

Das Feld **Wiederkehrende Methode** ist wichtig. Es bestimmt, wie der Betrag in der Erfassungsjournalzeile nach der Buchung behandelt werden soll. Wenn Sie beispielsweise bei jeder Buchung der Zeile den gleichen Betrag verwenden, können Sie den Betrag unverändert lassen. In diesem Fall sollten Sie **F Fest** als eine Option verwenden. Wenn Sie dieselben Konten und denselben Text in der Zeile verwenden, der Betrag aber bei jeder Buchung variiert, können Sie den Betrag nach der Buchung löschen. In diesem Fall wählen Sie die Option **V Variable** aus. 

Darüber hinaus müssen Sie das Feld **Wiederholungsrate** konfigurieren, da diese Datumsformel bestimmt, wie oft der Posten in der Erfassungsjournalzeile gebucht werden soll, und somit ausgefüllt werden muss. Mehr dazu erfahren Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#use-date-formulas).  

Das Feld **Ablaufdatum** bestimmt das Datum, an dem die Zeile letztmalig gebucht werden soll. Die Zeile wird nach diesem Datum nicht mehr gebucht. Die Verwendung des Feldes **Ablaufdatum** hat den Vorteil, dass die Zeile nicht sofort aus dem Erf.-Journal gelöscht wird. Sie können ein späteres Datum eingeben, so dass Sie die Zeile auch in der Zukunft verwenden können. Wenn das Feld leer ist, wird die Zeile jedes Mal gebucht, bis sie aus dem Journal gelöscht wird.  

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)    
[Nachhaltigkeitsverwaltung – Übersicht](finance-manage-sustainability.md)   
[Nachhaltigkeitseinrichtung](finance-sustainability-setup.md)   
[Diagramm der Nachhaltigkeitskonten und -posten](finance-sustainability-accounts-ledger.md)   
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
