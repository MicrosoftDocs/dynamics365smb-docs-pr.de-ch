---
title: Informationen zur Kostenrechnung
description: 'Kostenrechnung wird verwendet, um Ihnen dabei zu helfen, die Kosten des Betriebs eines Geschäftes zu erkennen. Die Kostenrechnung dient dazu, verschiedene Sachverhalte zu analysieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-cost-accounting"></a>Informationen zur Kostenrechnung

Kostenrechnung wird verwendet, um Ihnen dabei zu helfen, die Kosten des Betriebs eines Geschäftes zu erkennen. Kostenrechnungsinformationen sollen Folgendes analysieren:  

- Die Arten von Kosten, die in Ihrem Unternehmen anfallen  
- Wo die Kosten anfallen
- Wer die Kosten trägt

In der Kostenrechnung weisen Sie aktuelle und geplante Kosten für Betrieb, Abteilungen, Produkte und Projekte zu, um die Profitabilität Ihres Unternehmens zu analysieren.  

## <a name="workflow-in-cost-accounting"></a>Workflow in der Kostenrechnung

Kostenrechnung hat folgende Hauptkomponenten:  

- Kostenarten, Kostenstellen und Kostenträger  
- Kostenposten und Kosten-Erfassungsjournale  
- Kostenumlagen  
- Kostenbudgets
- Kostenberichte  

Das folgende Diagramm zeigt den Workflow der Kostenrechnung.  

![Kostenrechnung im Überblick](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Kostenarten, Kostenstellen und Kostenträger

Sie definieren Kostenarten, Kostenstellen und Kostenträger, um zu analysieren, worin die Kosten bestehen, woher die Kosten stammen und wer die Kosten trägt.  

Zunächst definieren Sie einen Kostenartenplan mit einer Struktur und Funktionalität, die dem Kontenplan des Fibupostens ähnelt. Sie können einen eigenen Kostenartenplan erstellen oder die Konten der Erfolgsrechnung des Fibuposten übernehmen.  

Kostenstellen sind Abteilungen und Gewinne, die für Kosten und Erträge verantwortlich sind. Häufig sind mehr Kostenstellen in der Kostenrechnung als in jeder Dimension eingerichtet, die im Sachkonto eingerichtet ist. Im Fibukonto werden in der Regel nur die Kostenstellen der ersten Ebene für direkte Kosten und die ursprünglichen Kosten verwendet. In der Kostenrechnung werden mehr Kostenstellen für zusätzliche Zuteilungsebenen erstellt.  

Kostenobjekte sind Produkte, Produktgruppen oder Dienstleistungen, die eine Firma anbietet. Diese Objekte sind die „fertigen Waren“ einer Firma, die die Kosten tragen.  

Sie können Kostenstellen mit Abteilungen und Kostenträger mit Projekten in Ihrem Unternehmen verknüpfen. Über den Fibuposten können Sie Kostenstellen und Kostenobjekte mit beliebigen Dimensionen verknüpfen und diese Informationen durch Zwischensummen und Titel ergänzen.  

## <a name="cost-entries-and-cost-journals"></a>Kostenposten und Kosten-Erfassungsjournale

Betriebskosten können aus dem Sachkonto übertragen werden. Sie können die Kostenposten aus dem Sachkonto automatisch auf Kostenposten bei jeder Buchung übertragen. Sie können auch einen Batchauftrag verwenden, um Fibuposten auf der Grundlage einer täglichen oder monatlichen Summenbuchung in Kosteneinträge zu übertragen.  

In Kostenerfassungsjournalen können Sie Kosten und Aktivitäten buchen, die weder aus dem Fibukonto stammen noch durch Zuteilungen erzeugt werden. Beispielsweise können Sie reine Betriebskosten, Inlandsabgaben, Zuordnungen und Korrekturposten einzeln zwischen Kostenarten, Kostenstellen und Kostenträgern oder auf wiederkehrender Basis buchen.  

## <a name="cost-allocations"></a>Kostenumlagen

Zuteilungen verschieben Kosten und Einnahmen zwischen Kostenarten, Kostenstellen und Kostenträgern. Gemeinkosten werden zuerst auf den Kostenstellen gebucht und zu einem späteren Zeitpunkt auf Kostenträger berechnet. Ein Beispiel wäre eine Verkaufsabteilung, die mehrere Produkte gleichzeitig verkauft. Die Gemeinkosten der Abteilung, wie Gehälter, Verbrauchsmaterial und Reisekosten, werden zunächst der Verkaufskostenstelle zugeordnet. Die Kosten werden dann auf die verschiedenen verkauften Produkte (Kostenträger) sowie auf die eingekauften Materialien (direkte Kosten) aufgeteilt.

Die Verrechnungsbasis und die Genauigkeit der Verrechnungsdefinition beeinflussen die Ergebnisse der Kostenumlagen. Die Zuteilungsdefinition wird verwendet, um Kosten zuerst von so genannten Vor-Kostenstellen zu den Hauptkostenstellen und dann von Kostenstellen zu Kostenträgern zuzuordnen.  

Jede Zuordnung besteht aus einer Zuordnungsquelle und einer oder mehreren Zuordnungszielen. Mit der Methode der statischen Umlage können Sie Istwerte oder Budgetwerte auf Basis eines bestimmten Wertes zuweisen. Beispielsweise die Quadratmeterzahl oder ein festgelegtes Aufteilungsverhältnis von 5:2:4. Sie können auch tatsächliche Werte oder geplante Werte zuordnen, indem Sie die Methode der dynamischen Umlage mit neun vordefinierten Zuteilungsgrundlagen und 12 dynamischen Datenbereichen verwenden.  

## <a name="cost-budgets"></a>Kostenbudgets

Ähnlich wie bei der Budgetierung im Fibuposten können Sie Budgets erstellen, um Kosten für einen bestimmten Zeitraum (z. B. ein Geschäftsjahr) zu planen, die auf eine Kostenstelle (Unternehmensabteilung) oder einen Kostenträger (Produkt oder Dienstleistung) angewendet werden können. Sie können so viele Kalkulationen erstellen, wie Sie benötigen. Sie können dann die Kalkulation in das Budget des Fibupostens kopieren und umgekehrt. Und Sie können kalkulierte Kosten als Ist-Kosten übernehmen.

## <a name="cost-reporting"></a>Kostenberichte

Die meisten Berichte und Statistiken basieren auf den gebuchten Kostenposten. Sie können die Sortierung der Ergebnisse einrichten und Filter verwenden, um zu definieren, welche Daten angezeigt werden müssen. Sie können Berichte für eine Kostenaufteilungsanalyse erstellen. Darüber hinaus können Sie mit den Standard-Finanzberichten festlegen, wie Ihre Berichte für den Kostenartenplan angezeigt werden.  

## <a name="see-also"></a>Siehe auch

[Kostenrechnung](finance-manage-cost-accounting.md)  
[Finanzen](finance.md)  
[Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
