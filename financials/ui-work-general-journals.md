---
title: "Arbeiten mit Fibu Buch.-Blättern | Microsoft Docs"
description: "Vorgehensweise: Arbeit mit Fibu-Buch.-Blättern"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 13257a5d82d742d92fb22da9da7ff7f773d7d2f8
ms.contentlocale: de-ch
ms.lasthandoff: 05/04/2017


---
# <a name="working-with-general-journals"></a>Arbeiten mit Fibu Buch.-Blättern
Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten. Bei der Buchung mit einem Fibu Erf.-Journal werden immer Posten für Fibukonten erstellt. Dies gilt auch, wenn beispielsweise eine Erfassungsjournalzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird.

[!INCLUDE[d365fin](includes/d365fin_md.md)] enthält auch nichtfinanzielle Buch.-Blätter, beispielsweise das Artikel Buch.-Blatt und das Inventur Buch.-Blatt, doch diese Buch.-Blätter sind nicht auf der Benutzeroberfläche sichtbar.

Die in ein Erf.-Journal eingegebenen Informationen sind temporär und können geändert werden, solange sie sich im Erf.-Journal befinden. Durch Buchen des Erf.-Journals werden die Informationen in Posten auf Konten übertragen und können nicht mehr geändert werden. Der Ausgleich gebuchter Posten kann jedoch aufgehoben werden, und Sie haben die Möglichkeit zum Buchen von Storno- oder Korrekturposten.

## <a name="journal-templates-and-batches"></a>Buch-Blattvorlagen und -namen
Es gibt mehrere Fibu Erfassungsjournalvorlagen. Jede Erfassungsjournalvorlage wird durch ein spezifisches Fenster mit bestimmten Funktionen und den Feldern dargestellt, die benötigt werden, um diese Funktionen zu unterstützen, wie das Fenster **Zahlungsabstimmungs-Erfassungsjournal**, um Bankzahlungen und das Fenster **Zahlungsausgangs-Erfassungsjournal** zu verarbeiten, um Ihre Kreditoren zu bezahlen.

**Hinweis**: Wenn Sie Zahlungsdateien an Ihre Bank aus dem Zahlungsausgangs Buch.-Blatt exportieren, müssen Sie das Kontrollkästchen **Zahlungsexport erlauben** für den Buch.-Blattnamen auswählen, der im Fenster **Fibu Buch.-Blattnamen** angezeigt wird. Weitere Informationen finden Sie unter [So gehts: Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md).

Sie können zu jeder Erfassungsjournalvorlage mehrere Erfassungsjournalnamen als Buch-Stapel erstellen. Beispielsweise können Sie Ihre eigenen Buch-Stapel für das Zahlungserfassungsjournal erstellen, das Ihr persönliches Layout und Ihre Einstellungen hat.

Ein Beispiel einer persönlichen Einstellungen, die Sie in Ihrem Fibu Buch.-Stapel festlegen können, ist es, mit der Systemhilfe die Betrag-Felder auszufüllen. Wenn Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu Erfassungsjournalnamen** auswählen, dann werden das Feld **Betrag**, beispielsweise Fibu Erfassungsjournalzeilen für dieselbe Belegnummer automatisch mit dem Wert, der zum Ausgleichen des Belegs erforderlich ist, ausgefüllt. Weitere Informationen finden Sie unter [!INCLUDE[d365fin](includes/d365fin_md.md)] Werte vorschlagen lassen (ui-let-system-suggest-values.md).

## <a name="main-accounts-and-balancing-accounts"></a>Hauptkonten und Gegenkonten
Wurden Standardgegenkonten für die Erfassungsjournalnamen eingerichtet, wird das Gegenkonto beim Ausfüllen des Felds **Kontonr.** automatisch ausgefüllt. Feld Sie müssen auch das Feld **Kontonr.**ausfüllen, Feld und **Gegenkonto-Nummer** Feld manuell. Bei einem positiven Betrag im Feld **Betrag** wird das Hauptkonto belastet, und auf dem Gegenkonto erfolgt eine Gutschrift. Bei einem negativen Betrag erfolgt eine Gutschrift auf dem Hauptkonto, und das Gegenkonto wird entsprechend belastet.

**Hinweis**: Die MWST für Haupt- und Gegenkonto wird getrennt berechnet, damit für die Konten unterschiedliche MWST-Prozentsätze verwendet werden können.

## <a name="recurring-journals"></a>Wiederkehrende Erfassungsjournale
Bei einem wiederkehrenden Erfassungsjournal handelt es sich um ein Fibu Erfassungsjournal mit speziellen Feldern für die Verwaltung von Transaktionen, die häufig mit geringen oder keinen Änderungen gebucht werden. Mithilfe dieser speziellen Felder für wiederkehrende Transaktionen können Sie feste und variable Beträge buchen. Sie können auch ein automatisches Storno für den Tag nach dem Buchungsdatum festlegen und wiederkehrende Posten zusammen mit Verteilungsschlüsseln verwenden.

## <a name="see-also"></a>Siehe auch
[Vorgehensweise: Verwenden von Verteilungsschlüsseln in Fibu Buch.-Blättern](ui-how-use-allocation-keys-general-journals.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

