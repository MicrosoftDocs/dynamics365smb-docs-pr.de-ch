---
title: Ordnen Sie Einnahmen und Kosten mehreren Fibukonten zu
description: 'Erfahren Sie, wie Sie Kosten einem oder mehreren Konten in Ihrer Finanzbuchhaltung zuordnen.'
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
---

# Ordnen Sie Einnahmen und Kosten mehreren Fibukonten zu

In diesem Artikel wird beschrieben, wie Sie Umlagekonten verwenden, um Beträge in Verkaufs- und Einkaufsbelegen und Erf.-Journalzeilen auf verschiedene Fibukonten zu verteilen. Sie können Beträge durch eine feste oder variable Verteilung verteilen.  

Durch die Zuordnung wird eine Fibu-Journalzeile in die auf der Seite **Umlagekonto** definierten Zeilen aufgeteilt. Wenn Sie beispielsweise einen Mietaufwand mithilfe von Dimensionen auf drei Arten aufteilen, müssen Sie drei Zeilen für die Zuordnung buchen. Daher verfügen Sie über sechs Hauptbuchzeilen (oder möglicherweise mehr, wenn Sie MWST oder Umsatzsteuer verwenden). Obwohl dadurch mehr Fibuposten gebucht werden, als Sie möglicherweise benötigen, können Sie einzelne Zeilen stornieren, anstatt die gesamte Umlage umzukehren.

Umlagekonten funktionieren auch mit Stundungen. Weitere Informationen zu Stundungen finden Sie unter [Einnahmen und Ausgaben aufschieben](finance-how-defer-revenue-expenses.md).

In der folgenden Tabelle werden die Zuordnungsmethoden vorgestellt, die Sie verwenden können.

|Zuordnungsmethode  |Description  |
|---------|---------|
|Behoben     | Wenn Sie Ausgaben so aufteilen möchten, dass sie sich über einen längeren Zeitraum wiederholen, können Sie eine feste Zuweisung verwenden. Mit einer festen Zuteilung können Sie die Aufteilung der Zuteilung definieren. Diese Aufteilung ändert sich nur, wenn Sie die Einrichtung auf der Seite **Umlagekonto** ändern.        |
|Variabel     | Um Einnahmen oder Ausgaben auf der Grundlage von Werten zu verteilen, die sich im Laufe der Zeit ändern, verwenden Sie die Methode der variablen Zuweisung. Mit variablen Zuteilungen können Sie die Quellen angeben, die zur Berechnung der Zuteilungsprozentsätze verwendet werden sollen. Diese Methode eignet sich beispielsweise für die Aufteilung der Personalkosten nach unterschiedlichen Personalbeständen in Abteilungen oder Abteilungen. Ein weiteres Beispiel ist die Verteilung der Mietkosten auf der Grundlage der Produktionsfläche, die je nach Produktionslinie im Laufe der Zeit variieren kann. Variable Zuordnungen verwenden eine Kombination aus Dimensionen und statistischen Konten, um zu bestimmen, wie sich Beträge über einen bestimmten Zeitraum verteilen. Weitere Informationen zu statistischen Konten finden Sie unter [Daten mit statistischen Konten analysieren](bi-use-statistical-accounts.md). Um mehr über Dimensionen zu erfahren, gehen Sie zu [Arbeiten mit Dimensionen](finance-dimensions.md).        |

## Verwenden Sie für die Zuweisung von Beträgen eine feste Anteils- oder Prozentmethode

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Umlagekonto** ein und wählen Sie dann den entsprechenden Link.  
1. Wählen Sie auf der Seite **Umlagekonten** die Aktion **Neu** aus.
1. Füllen Sie die **Felder Nr.** und **Name** Felder.
1. Wählen Sie im Feld **Kontoart** die Option **Fixiert** aus.
1. Wählen Sie im Feld **Zielkontoart** die Option **Fibukonto** oder **Bankkonto** aus.
1. Wählen Sie im Feld **Zielkontonummer** das Sachkonto zum Buchen des Werts aus.
1. Optional: Wählen Sie die Aktion **Dimensionen** und geben Sie dann die Dimensionen an, die für die Zeile gebucht werden sollen.
1. Geben Sie in den Feldern **Teilen** und **Prozent** an, wie Beträge auf das Zielkonto verteilt werden sollen.
  
   > [!TIP]
   > Wenn Sie den tatsächlichen Betrag, der für eine feste Zuteilung zugewiesen werden soll, in das Feld **Teilen** eingeben, wird im Feld **Prozent** der Prozentsatz des Gesamtbetrags angezeigt.
1. Wiederholen Sie diesen Vorgang für jedes Konto, das in die Zuweisung einbezogen werden soll.

## Verwenden Sie eine variable Methode zur Zuweisung von Beträgen

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Umlagekonto** ein und wählen Sie dann den entsprechenden Link.  
1. Wählen Sie auf der Seite **Umlagekonten** die Aktion **Neu** aus.
1. Füllen Sie die **Felder Nr.** und **Name** Felder.
1. Wählen Sie im Feld **Kontoart** die Option **Variable** aus.
1. Geben Sie im Feld **Zielkontoart** die Option **Fibukonto** ein.
1. Wählen Sie im Feld **Zielkontonummer** das Sachkonto zum Buchen des Werts aus.
1. Geben Sie im Feld **Aufschlüsselungskontoart** **Statistisches Konto** ein.
1. Wählen Sie im Feld **Berechnungszeitraum** den Zeitraum aus, für den Beträge verteilt werden sollen.
1. Optional: Um nach bestimmten globalen Dimensionswerten zu filtern, wählen Sie die Aktion **Filter für den Saldo des Aufschlüsselungskontos** aus und geben Sie dann die Filterwerte an.
1. Optional: Wählen Sie die Aktion **Dimensionen** und geben Sie dann die Dimensionen an, die für die Zeile gebucht werden sollen.

## Weisen Sie Beträge im Handumdrehen zu

Sie erstellen Umlagekonten zur Aufteilung von Erlösen und Kosten auf Fibukonten und Bankkonten. Durch die Automatisierung der Zuordnung können Sie viel Zeit sparen. Wenn Sie jedoch Umlagekonten verwenden, diese aber nicht für jedes Fibukonto anlegen möchten, können Sie noch mehr Zeit sparen.

Mit der Option «Von übergeordnetem Konto übernehmen» können Sie das Umlagekonto verwenden, um Beträge für ein beliebiges Fibukonto in einer Zeile eines Dokuments oder Journals aufzuteilen. Im Feld **Kontoart** in einem Beleg oder einer Erf.-Journalzeile wählen Sie ein Fibukonto und anschliessend das Umlagekonto im Feld **Umlagekonto-Nr.** aus. Der Betrag in der Zeile wird entsprechend der Einrichtung in Ihrem Umlagekonto für das Fibukonto aufgeteilt. Dies ist eine weniger transparente Art der Zuordung. Sie müssen jedoch kein Umlagekonto speziell für das Fibukonto erstellen.

Ad-hoc-Zuweisungen sind einfach einzurichten. Anstelle der Angabe eines Bank- oder Fibukontos im Feld **Zielkontoart** auf der **Umlagekonto** wählen Sie die Option **Vom übergeordneten Element erben**. Lassen Sie das Feld **Zielkontonummer** leer. Wenn Sie das Fibukonto in der Beleg- oder Journalzeile auswählen, wird dieses Konto für die Umlage von Beträgen verwendet.

## Stellen Sie sicher, dass die Beträge korrekt verteilt werden, bevor Sie sie buchen

Es gibt mehrere Möglichkeiten, die korrekte Verteilung der Beträge zu überprüfen:

* Wählen Sie auf der Seite **Umlagekonto** die Aktion **Verteilung testen** aus. Benutzen Sie das Feld **Zuzuweisender Betrag**, um verschiedene Beträge zu testen.
* Auf der Seite **Fibu-Erfassungsjournale** wählen Sie das Journal aus und verwenden die Aktion **Buchungsvorschau**.

## Passen Sie die Verteilung an

Wenn Sie in einer Zuordnung etwas finden, das Sie ändern möchten, können Sie die Zuordnung anpassen, bevor Sie sie veröffentlichen.  

1. Öffnen Sie das Dokument oder Journal mit der Zuordnung, die Sie ändern möchten.
1. Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **Kontenverteilungen neu verteilen** aus.
1. Auf der **Verteilungen ändern** Seite nehmen Sie Ihre Anpassung vor.

## Buchen Sie eine Zuteilungstransaktion

In den folgenden Schritten wird beschrieben, wie eine Zuordnungstransaktion aus einem Fibu-Erf.-Journal gebucht wird. Die Schritte sind für Verkaufs- und Einkaufsbelege identisch.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Fibu Erfassungsjournale** ein und wählen Sie dann den entsprechenden Link.  
1. Erstellen Sie eine neue Zeile. Füllen Sie die Felder auf die gleiche Weise aus wie bei jeder anderen Art von Fibu-Erf.-Journal.
1. Wenn Sie eine feste oder variable Zuteilung verwenden, füllen Sie die folgenden Felder aus:
    1. Geben Sie im Feld **Kontoart** **Umlagekonto** ein.
    1. Wählen Sie im Feld **Kontonr.** das Umlagekonto aus.
1. Wenn Sie eine Zuordnung verwenden, die die Option „Vom übergeordneten Element erben“ verwendet, gehen Sie wie folgt vor:
    1. Wählen Sie im Feld **Kontoart** die Option **Fibukonto** aus.
    1. Wählen Sie im Feld **Kontonummer** das Fibukonto aus.
    1. Wählen Sie im Feld **Umlagekonto-Nr.** das Umlagekonto aus, das für die Verwendung der Option „Von übergeordnetem Konto erben“ eingerichtet ist. 
1. Wählen Sie **Buchen** aus.

## Siehe auch

[Mit Fibu Erfassungsjournalen arbeiten](ui-work-general-journals.md)  