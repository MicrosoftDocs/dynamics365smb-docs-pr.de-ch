---
title: Buchungsgruppen-Einrichtung| Microsoft Docs
description: "Übersicht der Buchungsgruppen, die Sie verwenden können, um die Zeit zu sparen und Fehler zu vermeiden, wenn Sie Transaktionen buchen."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 732b69df44681d3cc63391bc87c0645ed7e5e1a5
ms.contentlocale: de-ch
ms.lasthandoff: 11/26/2018

---
# <a name="setting-up-posting-groups"></a>Buchungsgruppen einrichten
Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Fibukonten. Sie sparen Zeit und helfen, Fehler zu vermeiden, wenn Sie Transaktionen buchen. Die Umsatzwerte wechseln zu den Konten, die in der Buchungsgruppe für diese bestimmte Einheit angegeben werden. Die einzige Anforderung ist, dass Sie einen Kontenplan haben. Weitere Informationen finden Sie unter [Einrichten des Kontenplans](finance-setup-chart-accounts.md).  

Buchungsgruppen werden unter drei Schlüsseln abgedeckt:  

* Allgemein - definiert, an wen Sie verkaufen und von wem Sie kaufen und was Sie verkaufen und was Sie kaufen. Sie können Gruppen kombinieren, um Elemente wie die Erfolgsrechnung-Konten festzulegen, um zu buchen, oder Sie verwenden Gruppen Berichte zum Filtern.  
* Benutzerdefiniert - Auf diese Weise erhalten Sie die Möglichkeit, beispielsweise Verkaufsbelege zu verwenden, statt die Posten direkt in der Fibuposten zu buchen. Wenn Debitorenposten erstellt werden, wird durch die Buchungsgruppen gewährleistet, dass die entsprechenden Posten in der Fibuposten gebucht werden.  
* Steuer- definieren Sie die Steuerprozentsätze und -Berechnungsarten, die anwenden, an wen Sie verkaufen und kaufen und was Sie verkaufen und was Sie kaufen.

Die folgenden Tabellen beschreiben die Buchungsgruppen nach den Schlüsseln.  

| Allgemeine Buchungsgruppen | Description |
| --- | --- |
| Allgemeine Geschäftsbuchungsgruppen |Weisen Sie diese Gruppen den Debitoren und Kreditoren zu, um anzugeben, von wem Sie kaufen und an wen Sie verkaufen. Richten Sie dies auf der Seite **Geschäftsbuchungsgruppen erstellen** ein Wenn Sie dies tun, überlegen Sie, in wie viele Gruppen die Verkäufe und Einkäufe aufgeschlüsselt werden müssen. Beispielsweise Gruppendebitoren und Kreditoren nach bestimmten Feld oder nach Art des Geschäfts. |
| Allgemeine Produktbuchungsgruppen |Weisen Sie diese Gruppe Artikeln und Ressourcen zu, um festzulegen, was Sie verkaufen und was Sie kaufen. Richten Sie dies auf der Seite **Produktbuchungsgruppen erstellen** ein Wenn Sie dies tun, berücksichtigen Sie die Gruppen, in die Sie Verkäufe nach Produkt (Artikel und Ressourcen) und Verkäufe nach Artikeln aufschlüsseln müssen. Beispielsweise  teilen Sie diese Gruppen nach Rohmaterial, Einzelhandel, Ressourcen, Kapazität, usw. auf. |
| Buchungsmatrix Einrichtung |Kombinieren von Geschäfts- und Produktbuchungsgruppen, und aktivieren Sie die Konten, um zu buchen. Jeder Kombination aus Geschäfts- und Produktbuchungsgruppen können Sie einen anderen Satz von Fibukonten zuweisen. So können Sie beispielsweise den Verkauf eines Artikels in der Fibuposten auf unterschiedliche Verkaufskonten buchen, indem den Debitoren verschiedene Geschäftsbuchungsgruppen zugewiesen werden. Richten Sie die Seite **Buchungsmatrix Einrichtung** ein. |

| Spezielle Buchungsgruppen | Description |
| --- | --- |
| Debitorenbuchungsgruppen |Definieren Sie die Konten, die verwendet werden, wenn Sie buchen. Wenn Sie den Lagerbestand in Verbindung mit Debitoren verwenden, bestimmt die Kombination aus Ihren Debitoren zugewiesener allgemeiner Geschäftsbuchungsgruppe und dem Lagerartikel zugewiesener allgemeiner Produktbuchungsgruppe auf welche Konten die Auftragszeilenposten in der Finanzbuchhaltung gebucht werden. Richten Sie dies auf der Seite **Kundenbuchungsgruppen** ein |
| Kreditorenbuchungsgruppen |Definieren Sie, wo Transaktionen für Kreditorensammelkonten, Zuschlagenkonten und Skontokonten gebucht werden. Dieses ist gleich wie bei den Debitorenbuchungsgruppen. Richten Sie dies auf der Seite **Kundenbuchungsgruppen** ein |
| Lagerbuchungsgruppen |Definieren Sie Bilanzlagerkonten. Lagerbuchungsgruppen stellen darüber hinaus eine ideale Möglichkeit dar, das Lager zu organisieren. Beim Generieren von Berichten können Sie Artikel anhand ihrer Lagergruppen voneinander trennen. Richten Sie dies auf der Seite **Bestandbuchungsgruppen** ein |
| Bankkontobuchungsgruppen |Definieren von Bankkonten. Beispielsweise kann dies die Vorgänge für die Nachverfolgung von Transaktions- und Ausgleichsbankonten vereinfachen, Richten Sie dies auf der Seite **Bankbuchungsgruppen** ein. |
| Anlagenbuchungsgruppen |Sie legen die Konten für die Anschaffungskosten, die kumulierten Abschreibungsbeträge, die Anschaffungskosten bei Verkauf, die kumulierte Abschreibung bei Verkauf, den Gewinn bei Verkauf, den Wartungsaufwand und den Abschreibungsaufwand fest. Richten Sie dies auf der Seite **Buchungsgruppen** ein |

| Steuerbuchungsgruppe | Description |
| --- | --- |
| Geschäftssteuerbuchungsgruppen |Bestimmen, wie Salestax für Debitoren und Kreditoren berechnet und gebucht werden. Richten Sie dies auf der Seite **Steuerbuchungsgruppen erstellen** ein. Wenn Sie dies tun, überlegen Sie, wieviele Gruppen Sie benötigen. Dies ist von verschiedenen Faktoren wie der hiesigen Gesetzgebung ab und ob Sie sowohl im Inland als auch im Ausland Handel treiben. |
| Steuerproduktbuchungsgruppen |Geben Sie die Steuerberechnungen an, die für die Arten von  Artikeln oder Ressourcen erforderlich ist, die Sie kaufen oder verkaufen. |
| Steuerbuchung einrichten |Zeigt Kombinationen aus MwSt.-Geschäftsbuchungsgruppen und MwSt.-Produktbuchungsgruppen an. Wenn Sie eine Erf.-Journalzeile, eine Einkaufszeile bzw. Verkaufszeile ausfüllen, schauen wir die Kombination an, um die zu verwendenden Konten zu identifizieren. |

## <a name="example-of-linking-posting-groups"></a>Beispiel für die Verknüpfung von Buchungsgruppen
Hier ist ein Szenario.  

Diese Buchungsgruppen werden auf der Debitorenkarte aktiviert:  

* Allgemeine Geschäftsbuchungsgruppe
* Debitorenbuchungsgruppe  

Diese Buchungsgruppen werden auf der Artikelkarte aktiviert:  

* Allgemeine Produktbuchungsgruppen  
* Lagerbuchungsgruppe  

Wenn ein Verkaufsbeleg erstellt wird, werden die Informationen auf der Debitorenkarte in den Verkaufskopf übernommen, und die Informationen auf der Artikelkarte werden in die Verkaufszeilen eingefügt.  

* Die Buchung der Einnahmen (Erfolgsrechnung-Konten) wird durch die Kombination der allgemeinen Geschäftsbuchungsgruppe und der allgemeinen Produktbuchungsgruppe bestimmt.  
* Die Debitorenbuchung (Bilanz) wird durch die Debitorenbuchungsgruppe bestimmt.  
* Die Lagerbuchung (Bilanz) wird durch die Lagerbuchungsgruppe bestimmt.  
* Die Buchung der Kosten für verkaufte Waren (Erfolgsrechnung) wird durch die Kombination der allgemeinen Geschäftsbuchungsgruppe und der allgemeinen Produktbuchungsgruppe bestimmt.  

Ihre Einrichtung legt fest, wann die Buchung erfolgt. Beispielsweise wird die zeitliche Steuerung tangiert, wenn Sie "Periodische Aktivitäten" durchführen, wie Buchungslagerkosten oder Anpassung von Kostenfaktorposten.

## <a name="copying-posting-setup-lines"></a>Kopieren von Buchungsmatrix-Einrichtungszeilen
Je mehr Produkt- und Geschäftsbuchungsgruppen vorhanden sind, um so mehr Zeilen werden auf der Seite Buchungsmatrix Einrichtung angezeigt. Für die Einrichtung der Buchungsmatrix des Unternehmens kann daher unter Umständen eine umfangreiche Dateneingabe erforderlich sein. Während unter Umständen viele verschiedene Kombinationen von Geschäfts- und Produktbuchungsgruppen vorhanden sind, buchen möglicherweise unterschiedliche Kombinationen weiterhin auf dieselben Fibukonten. Um den Umfang der erforderlichen manuellen Dateneingabe einzuschränken, kopieren Sie die Fibukonten aus einer vorhandenen Zeile auf der Seite **Buchungsmatrix Einrichtung**.

## <a name="see-also"></a>Siehe auch 
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Finance einrichten](finance-setup-finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

