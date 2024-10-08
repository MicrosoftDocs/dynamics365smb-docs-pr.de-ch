---
title: 'Einrichten von Projekten, Preisen und Projektbuchungsgruppen'
description: 'Beschreibt, wie allgemeine Informationen zu Projekten eingerichtet werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/19/2024
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.service: dynamics-365-business-central
---
# <a name="set-up-projects-prices-and-project-posting-groups"></a>Einrichten von Projekten, Preisen und Projektbuchungsgruppen

Als Projektmanager können Sie jedes der Projekte, die Sie verwalten, einrichten [!INCLUDE[prod_short](includes/prod_short.md)]. Verwenden Sie die Seite **Projekteinrichtung**, um festzulegen, wie Sie Projektfeatures verwenden.

Geben Sie für jedes Projekt verschiedene Informationen an:

* Preise für Projektartikel
* Projektressourcen
* Projektfibukonten
* Projektbuchungsgruppen (erforderlich)

## <a name="to-set-general-information-for-projects"></a>So richten Sie allgemeine Informationen für Projekte ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Projekteinrichtung** ein und wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Der Umschalter **Verbrauchslink standardmässig anwenden** auf der Seite **Projekteinrichtung** zeigt an, ob Projektsachkontoeinträge standardmässig mit Projektplanungszeilen verknüpft werden. Aktivieren Sie den Umschalter, um diese Einstellung auf alle neuen Projekte anzuwenden. Sie können das Tracking des Projektverbrauchs für ein bestimmtes Projekt aktivieren oder deaktivieren, indem Sie den Umschalter **Verbrauchslink anwenden** auf der Seite **Projektkarte** ein- oder ausschalten. Mit dem Schalter  **Verwendung anwenden verknüpfen**  werden auch die Funktionen für Lagerabwicklung, Planung, Auftragsfertigung, Artikelverfolgung und Reservierung für Projekte aktiviert.

### <a name="to-set-up-project-usage-tracking"></a>So richten Sie das Projektverbrauch-Tracking ein

Wenn Sie an einem Projekt arbeiten, möchten Sie vielleicht wissen, wie sich Ihr Verbrauch im Vergleich zu Ihrem Plan verhält. Um den Verbrauch herauszufinden, können Sie einen Link zwischen Ihren Projektplanungszeilen und dem tatsächlichen Verbrauch erstellen. Über den Link können Sie Ihre Kosten verfolgen und nachvollziehen, wie viel Arbeit noch übrig ist. Standardmässig ist der Projektplanungszeilentyp **Plan**, aber die Verwendung der Zeilenart **Budgetiert und verrechenbar** hat ähnliche Effekte.

Nachdem Sie das Verbrauchstracking über den Umschalter **Verbrauchsverknüpfung standardmässig anwenden** aktiviert haben, können Sie die Informationen der Projektplanungszeile überprüfen. Beispielsweise können Sie die Menge der Ressource, des Artikels oder des Fibukontos festlegen. Sie können auch die Menge festlegen, die Sie an das Projekterfassungsjournal übertragen möchten. Das Feld **Restmenge** auf der Projektplanungszeile zeigt Ihnen an, was noch übertragen und in das Projekterfassungsjournal gebucht werden muss.

>[!NOTE]
> Wenn **Verbrauchsverknüpfung anwenden** auf dem einzelnen Projekt gewählt wird und das Feld **Zeilentyp** in der Projektbuchungszeile oder Einkaufszeile **Fakturierbar** ist, dann werden neue Projektplanungszeilen des Zeilentyps **Budgetiert und verrechenbar** erstellt, wenn Sie die Projektbuchungszeile oder den Einkaufsbeleg buchen.  
>
> Weitere Informationen finden Sie unter [Den Verbrauch für Projekte erfassen](projects-how-record-job-usage.md) und [Verwalten von Projektmitteln](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Wenn Sie im Feld **Zeilentyp** auf der Zeile für die Projekterfassungsjournal-Zeile oder den Kauf keinen Wert angeben, werden keine Projektplanungszeilen erstellt, wenn Sie das Projekterfassungsjournal oder den Einkaufsbeleg buchen.

### <a name="invoice-multiple-customers-for-project-tasks"></a>Mehrere Debitoren für Projektaufgaben in Rechnung stellen

Wenn an Projekten mehrere Debitoren beteiligt sind, kann es eine Herausforderung sein, dem richtigen Debitor die richtigen Aufgaben in Rechnung zu stellen. [!INCLUDE [prod_short](includes/prod_short.md)] macht die Abrechnung weniger komplex, da Sie in jeder Projektaufgabenzeile die Rechnungsadresse und Rechnung an Debitor angeben können, sodass Sie automatisch Rechnungen für die richtigen Debitoren erstellen können.  Verwenden Sie das Feld  **Standardmäßige Abrechnungsmethode Aufgabe**, um anzugeben, ob Sie standardmäßig einem oder mehreren Kunden eine Rechnung stellen. Sie können die Abrechnungsmethode Aufgabe für ein bestimmtes Projekt ändern, indem Sie das Feld  **Aufgabe-Abrechnungsmethode**  auf der Seite  **Projekt Karte**  verwenden. Weitere Informationen zum Rechnungsstellen an mehrere Debitoren finden Sie unter [Einem oder mehreren Debitoren Projektaufgaben in Rechnung stellen](projects-how-create-jobs.md#invoice-one-or-more-customers-for-project-tasks).

### <a name="synchronize-the-cost-of-used-items"></a>Synchronisieren Sie die Kosten für gebrauchte Artikel

Die Kosten eines Artikels (Inventarwert), den Sie kaufen und später im Projekt verwenden, können sich während seiner Lebensdauer ändern. Beispielsweise weil zu den Anschaffungskosten des Artikels Frachtkosten hinzugerechnet werden, nachdem Sie die Nutzung des Artikels gebucht haben.

In [!INCLUDE [prod_short](includes/prod_short.md)] können Sie Artikelkosten manuell oder automatisch Anpassen. Die Anpassung wird in den Wertbuchungen und im Hauptbuch berücksichtigt. Weitere Informationen finden Sie unter  [Lagerkosten verwalten](finance-manage-inventory-costs.md)

Auch projektbezogen haben Sie Möglichkeiten, diese Anpassungen abzubilden.

Um sicherzustellen, dass sich die Kosten in einem Projekt jedes Mal automatisch ändern, wenn der Stapelverarbeitungsauftrag  **Anpassen „Kosten – Artikeleinträge“** ausgeführt wird, aktivieren Sie den Schalter  **Projektartikelkosten automatisch aktualisieren** .

Wenn Sie es ausgeschaltet lassen, denken Sie daran, die  **Auftragsprojektkosten aktualisieren** Aufgabe manuell oder mithilfe eines Auftragswarteschlangeneintrags auszuführen.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-projects"></a>So erstellen Sie projektspezifische Preise für Ressourcen, Artikel und Fibukonten für Projekte

> [!NOTE]
> In der 2020er Release-Welle 2 haben wir neue Prozesse zum Einrichten und Verwalten von Preisen und Rabatten freigegeben. Wenn Sie ein neuer Kunde sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** in **Funktionsverwaltung** akualisiert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Sie können Preise für die Artikel, Ressourcen und Fibukonten für ein Projekt einrichten. 

#### [Aktuelle Erfahrung](#tab/current-experience)

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Projekt** ein und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie das Projekt und dann die Aktion **Ressource**, **Artikel** oder **Fibukonto** aus.
3. Füllen Sie auf den Seiten **Res.-VK-Preise Projekt**, **Projektartikelpreise** oder **Projekt-Fibukontopreise** die Felder nach Bedarf aus.

Wenn Sie ein Ressourcen-, Artikel- oder Fibukonto für ein Projekt auswählen, verwendet [!INCLUDE [prod_short](includes/prod_short.md)] Informationen in den optionalen Feldern in Projektplanungszeilen und Projekterfassungsjournalen. Die folgende Tabelle erläutert, wie.

|Spalte1  |Spalte2  |
|---------|---------|
|**Projektartikel**|Die Felder **Projektaufgabennr.**, **Währungscode** und **Zeilenrabatt %%**. Dies ist der Wert im Feld **VK-Preis** der in den Projektplanungszeilen und Projekterfassungsjournalen verwendet wird, wenn dieser Artikel eingegeben wird. Dieser Preis hat Vorrang vor dem regulären Debitorenpreis (Mechanismus für „bester Preis“) für Artikel. Um den regulären Debitorenpreis zu verwenden, geben Sie keine Projektartikelpreise für das Projekt an.|
|**Fibukonten**|Die Informationen in den Feldern **Projektaufgaben-Nr.**, **Währungscode**, **Zeilenrabatt %**, **Einheitskostenfaktor** und **Einheitskosten** werden auf den Projektplanungszeilen und in Projekterfassungsjournalen verwendet, wenn dieses Fibukonto eingegeben und einem Projekt hinzugefügt wird. Wenn Sie ein Fibukonto auswählen, verwenden Projektplanungszeilen und Projekterfassungsjournale den Wert im Feld **Einzelpreis** für das Aufwandsfibukonto.|
|**Projektressourcen**|Die Felder **Projektaufgabennr.**, **Arbeitstyp**, **Währungscode**, **Zeilenrabatt %%** und **Einstandspreis**. Der Wert im Feld **Einzelpreis** für die Ressource wird in den Projektplanungszeilen und Projekterfassungsjournalen verwendet, wenn Sie eine Ressource oder eine der Ressourcengruppe zugeordnete Ressource eingeben. Dieser Preis überschreibt immer die auf der Seite **Ressourcen-VK-Preis/Ressourcengruppen-VK-Preise** angegebenen Preise.|

#### [Neue Erfahrung](#tab/new-experience)

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") und geben Sie **Projekte** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Markieren Sie das entsprechende Projekt und wählen Sie dann die Aktion **Verkaufspreislisten** aus.

---

## <a name="to-set-up-project-posting-groups"></a>So richten Sie Projektbuchungsgruppen ein

Ein Aspekt der Planungsprojekte besteht darin, zu entscheiden, welche Buchungskonten für die Projektkalkulation verwendet werden. Damit Projekte gebucht werden können, müssen Sie Konten für die Buchung für jede Projektbuchungsgruppe einrichten. Eine Buchungsgruppe stellt eine Verknüpfung zwischen dem Projekt und der Art dar, wie es im Fibukonto zu behandeln ist. Wenn Sie ein Projekt erstellen, geben Sie eine Buchungsgruppe an, und standardmässig wird jede Aufgabe, die Sie für das Projekt erstellen, dieser Buchungsgruppe zugeordnet. Wenn Sie Aufgaben erstellen, können Sie jedoch die Voreinstellung überschreiben und eine Buchungsgruppe auswählen, die geeigneter ist.  

> [!NOTE]  
> Sie müssen die Konten in den Kontenplan eingegeben, bevor Sie Buchungsgruppen einrichten können. Weitere Informationen finden Sie unter [Einrichten oder ändern des Kontenplans](finance-setup-chart-accounts.md).  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Projektbuchungsgruppen** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

| Das Feld "Konto" | Description | In WIP-Typ verwendet |
| --- | --- |  --- |
| **Code** |Eine Kennung für die Buchungsgruppe. Sie können bis zu 10 Zeichen, einschliesslich Leerzeichen, eingeben. | |
| **Konto f. Kosten n. abgs. Arb.** |Das WIP-Konto für die berechneten Kosten der Projekt-WIP, bei dem es sich um ein Bilanz-Aktivkonto für Kapital handelt. | Verrechnete Kosten, deklarierte Kosten|
| **Konto f. aufgel. Kosten n. abgs. Arb.** |Ein Konto für die Einstandswert- oder Vertriebskostenmethode der WIP-Berechnung. Dieses Konto ist für die aufgelaufene Kosten in Ihrer Bilanz. Wenn die WIP-Regulierung erfordert, dass Sie die Verbrauchsosten, die Sie in Ihrer Erfolgsrechnung buchen, erhöhen, buchen Sie dies auf dieses Konto. | Aufgelaufene Kosten|
| **Projektkostenausgleich-Konto** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. Wird verwendet, wenn **Verwendete WIP-Buchungsmethode** auf *Projekt* eingestellt ist. | Verrechnete Kosten, deklarierte Kosten|
| **Konto für ausgeglichene Artikelpreise** |Dasselbe wie **Projektkostenausgleich-Konto**, wird aber verwendet, wenn **Verwendete WIP-Buchungsmethode** auf *Projektposten* eingestellt ist.| |
| **Konto für ausgeglichene Ressourcenpreise** |Dasselbe wie **Projektkostenausgleich-Konto**, wird aber verwendet, wenn **Verwendete WIP-Buchungsmethode** auf *Projektposten* eingestellt ist.| |
| **Konto für ausgeglichene Fibu-Kosten** |Dasselbe wie **Projektkostenausgleich-Konto**, wird aber verwendet, wenn **Verwendete WIP-Buchungsmethode** auf *Projektposten* eingestellt ist.| |
| **Projektkostenregulierung-Konto** |Das Gegenkonto zum WIP-Konto für aufgelaufene Kosten, bei dem es sich um ein Aufwandskonto handelt. | Aufgelaufene Kosten|
| **Aufwandssachkonto (Budget)** |Das Verkaufskonto, das für Aufwands-Fibuposten in Projektaufgaben mit dieser Buchungsgruppe verwendet werden soll. Wenn dieses Feld leer gelassen wird, wird das für die Projektplanungszeile eingegebene Fibukonto verwendet. | |
| **Konto f. aufgel. Verkäufe n. abgs. Arb.** |Das WIP-Konto für den berechneten Verkaufswert der WIP, bei dem es sich um ein Konto für aufgelaufene Umsätze für Ihre Bilanz handelt. Wenn eine WIP-Regulierung erfordert, dass Sie die anerkannten Umsätze erhöhen, buchen Sie dies auf dieses Konto. | Aufgelaufene Verkäufe, deklarierte Verkäufe|
| **Konto f. fakt. Verkäufe n. abgs. Arb.** |Das Konto für den fakturierten WIP-Verkaufswert, der nicht deklariert werden kann. Es handelt sich dabei um ein Bilanzblatt für nicht realisierte Einnahmen. | Deklarierte Verkäufe, ausgeglichene Verkäufe|
| **Projektverkaufsausgleich-Konto** |Das Gegenkonto zum WIP-Konto für fakturierte Verkäufe, bei dem es sich um ein Ertragsgegenkonto handelt. | Ausgeglichene Verkäufe, deklarierte Verkäufe|
| **Projektverkaufsregulierungs-Konto** |Das Gegenkonto zum WIP-Projektkonto für den Umsatz, bei dem es sich um ein Ertragskonto handelt. | Aufgelaufene Verkäufe|
| **Konto deklarierte Kosten** |Das Aufwandskonto, das die deklarierten Kosten für das Projekt enthält. Dabei handelt es sich normalerweise um ein Soll-Aufwandskonto. | Deklarierte Kosten|
| **Konto deklarierte Verkäufe** |Das Ertragskonto, das den deklarierten Umsatz für das Projekt enthält. Dabei handelt es sich normalerweise um ein Haben-Ertragskonto. | Deklarierte Verkäufe|

## <a name="see-also"></a>Siehe auch

[Projektmanagement einrichten](projects-setup-projects.md)  
[Video: Wie man ein Projekt in Dynamics 365 Business Central erstellt](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projekte verwalten](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
