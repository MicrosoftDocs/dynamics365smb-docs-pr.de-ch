---
title: Abstimmen von Zahlungen mithilfe der automatischen Anwendung | Microsoft Docs
description: Beschreibt, wie die automatische Anwendungsfunktion verwendet wird, um Zahlungseingänge Zahlungen oder in ihre entsprechenden offenen Posten anwenden und Zahlungen auszugleichen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 121212f41d5dadff53a10f828c88279865828788
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316586"
---
# <a name="reconcile-payments-using-automatic-application"></a>Abstimmen von Zahlungen mithilfe der automatischen Anwendung
Die Seite **Zahlungsabstimmungserf.-Journal** gibt Zahlungen an, entweder eingehend von Debitoren oder ausgehend an Kreditoren, die als Transaktionen in Ihrem Bankkonto erfasst wurden und die auf ihre entsprechenden unbezahlten Rechnungen und Gutschriften oder andere offene Posten angewendet werden können. Die Zeilen im Erfassungsjournal werden ausgefüllt, indem ein Bankkontoauszug als Bankfeed oder -Datei importiert wird.

> [!NOTE]
> Die Seite bietet automatisch entsprechende Funktionen an, die für Zahlungen in ihre entsprechenden offenen Postens darstellte eine Zuordnung des Textes in einer Bankkontoauszugszeile (Erf.-Journalzeile) mit Text auf einer oder mehreren offenen Posten ausgeglichen werden soll. Beachten Sie, dass die vorgeschlagenen automatischen Anwendungen überschrieben können, und Sie können wählen, dass die Anwendung nicht automatisch verwendet wird. Weitere Informationen finden Sie unter Schritt 7.

Ein Zahlungsabstimmungsbuch.-Blatt wird mit einem Bankkonto in [!INCLUDE[d365fin](includes/d365fin_md.md)] verknüpft, das das elektronischen Bankkonto widerspiegelt, in der die Zahlungsbuchungen erfasst werden. Alle offnen Bankposten, die sich auf ausgeglichene Debitoren- oder Kreditorenposten beziehen, werden geschlossen, wenn Sie die Aktion **Zahlungen buchen und Bankkonto abstimmen** auswählen. Dies bedeutet, dass das Bankkonto mit Zahlungen abgestimmt wird, die Sie mit dem Erfassungsjournal buchen.

Um den Import von Bankkontoauszügen als Bankfeed zu aktivieren, müssen Sie den Dienst „Envestnet Yodlee Bank Feeds“ einrichten und aktivieren und dann Ihr Bankkonto mit den entsprechenden Onlinebankkonten verbinden. Das Zahlungsabstimmungs-Erfassungsjournal erkennt dann automatisch Bankfeeds, wenn Sie die Aktion **Import-Bankbuchungen** auswählen. Darüber hinaus können Sie in einem Bankkonto beliebig viele automatisch festgelegt Importe für neue Bankkontoauszugsfeeds jede Stunde festlegen. Transaktionen für Zahlungen, die bereits als ausgeführt und/oder abgestimmt im Fenster Zahlungsabstimmungsbuch.-Blatt gebucht wurden, werden nicht importiert. Weitere Informationen finden Sie unter [Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md).

Im Fenster **Text zu Konto zuordnen**, können Sie schnell Zuordnungen zwischen Text in Zahlungen und bestimmten Soll-, Haben- und Gegenkonten eingeben, sodass solche Zahlungen auf die angegebenen Konten gebucht werden, wenn Sie Zahlungen im Zahlungsabstimmungs-Erfassungsjournal buchen. Siehe dazu auch Schritt 8. Weitere Informationen finden Sie unter [Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

Ähnliche Funktionen sind vorhanden, um Mehrbeträge auf Zahlungsabstimmungsbuch.-Blattzeilen fallweise abzustimmen. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-cannot-apply-auto.md).

Sie verwenden die Funktion **Automatisch anwenden** entweder automatisch, wenn Sie die Bankdatei importieren mit Zahlungstransaktionen, oder wenn Sie sie aktivieren, um Zahlungen auf ihre entsprechenden offenen Posten im Rahmen eines Datenabgleichs in einer Erf.-Journalzeile mit Daten für einen oder mehrere offene Posten anzuwenden.

In Erfassungsjournalzeilen, bei denen eine Zahlung automatisch auf einen oder mehrere offene Posten angewendet wurde, hat das Feld **Passende Werte** einen Wert zwischen Niedrig und Hoch, um die Qualität des Datenabgleichens anzugeben, auf der die vorgeschlagenen Zahlungsanwendung basiert. Darüber hinaus werden -**Kontoart** und **Konto-Nr.**-Felder mit Informationen über den Debitor oder Kreditor ausgefüllt, auf die die Zahlung angewendet wird. Wenn Sie eine Text-zu-Konto-Zuordnung eingerichtet haben, kann die automatische Anwendung einen Abgleichungsvertrauenswert von **Hoch - Text-zu-Konto-Zuordnung** ergeben.

Für jede Erf.-Journalzeile, die ein Zahlung auf der Seite **Zahlungsabstimmungserf.-Journal** darstellt, können Sie die Seite **Zahlungsanwendung** öffnen, um alle offenen Kandidatenposten für die Zahlung anzuzeigen und detaillierte Informationen für jeden Posten zum Datenabgleich anzuzeigen, auf denen eine Zahlungsanwendung basiert. Hier können Sie manuell Zahlungen ausgleichen, oder Zahlungen erneut ausgleichen, die automatisch auf einen falschen offenen Posten angewendet wurden,. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Sie können den Banktransaktionsimport automatisch starten, wenn Sie dafür ein vorhandenes **Zahlungsabstimmungserf.-Journal** auf der Seite **Zahlungsabstimmungserf.-Journal** öffnen. Nachfolgend wird beschrieben, wie Banktransaktionen auf die Seite **Zahlungsabstimmungserf.-Journal** importiert werden, nachdem Sie ein neues Erf.-Journal erstellt haben.

## <a name="to-reconcile-payments-using-automatic-application"></a>Vorgehensweise zum Abstimmen von Zahlungen mithilfe der automatischen Anwendung
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zahlungsabstimmungsbuch.-Blatt** ein, und wählen dann den zugehörigen Link aus.
2. Um in einem neuen Zahlungsabstimmungs-Erfassungsjournal zu arbeiten, wählen Sie die Aktion **Neues Erfassungsjournal** aus.
3. Wählen Sie auf der Seite **Zahlung Bankkontenliste** das Bankkonto aus, für das Sie Zahlungen abstimmen möchten, und klicken Sie anschliessend auf **OK**.
   Die Seite **Zahlungsabstimmungserf.-Journal** wird für das ausgewählte Bankkonto vorbereitet geöffnet.
4. Wählen Sie die Aktion **Import-Bankbuchungen** aus.
   Wenn das Bankkonto für das gewählte Erf.-Journal nicht zum Importieren von Banktransaktionen eingerichtet ist, dann öffnet sich ein Dialogfeld, um Ihnen dabei zu helfen, die entsprechenden Felder einzutragen.
5. Auf der Seite **Datei für den Import auswählen** wählen Sie die Datei aus, die die Banktransaktionen für Zahlungen enthält, die abgestimmt werden sollen, und wählen Sie dann die Schaltfläche **Öffnen**.  
6. Wenn der Bankkontoauszugs-Service ausgeführt wird, öffnet sich die Seite **Bankkontoauszugs-Filter** automatisch. Geben Sie ein Datumsintervall an, sodass die Bankkontoauszüge importiert werden können.

    Die Seite **Zahlungsabstimmungserf.-Journal** enthält Zeilen für die Zahlungen, die Banktransaktionen in der importierten Datei darstellen.

    In Zeilen, bei denen eine Zahlung automatisch auf den zugehörigen offenen Posten angewendet wurde, hat das Feld **Übereinstimmungsgenauigkeit** einen Wert zwischen **Niedrig** und **Hoch**, um die Qualität des Datenabgleichens anzugeben, auf der die vorgeschlagenen Zahlungsanwendung basiert. Darüber hinaus werden -**Kontoart** und **Konto-Nr.**-Felder mit Informationen über den Debitor oder Kreditor ausgefüllt, auf die die Zahlung angewendet wird.
7. Wählen Sie eine Erf.-Journalzeile, und wählen Sie dann **Manuell anwenden** oder Zahlung manuell anwenden auf der Seite **Zahlungsanwendung**. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-review-apply-payments-auto-application.md).

    Wenn Sie den manuellen Ausgleich abgeschlossen haben, enthält das Feld **Übereinstimmungsgenauigkeit** in der Erfassungsjournalzeile, die Sie manuell verarbeitet haben **Akzeptiert**.
8. Wählen Sie eine nicht ausgeglichene Buch.-Blattzeile für einen wiederkehrende Zahlungseingang oder Ausgabe aus, wie einen Autobenzineinkauf, und wählen Sie dann auf der Registerkarte Start in der Gruppe Anwendungen **Text-zu-Kontenzuordnung** aus. Weitere Informationen finden Sie unter [Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
9. Wenn Sie Ihre manuelle Zuordnung von Zahlungstext zu Konten abgeschlossen haben, wählen Sie die Aktion **Manuell anwenden** aus.
10. Wenn Sie sicher sind, dass alle Zahlungen der Erfassungsjournalzeilen korrekt angewendet oder zur direkten Erfassungsjournalzeilenerfassung festgelegt werden, wählen Sie die Aktion **Buchen** aus und wählen Sie dann eine der Optionen:

    - **Buchen von Zahlungen und Abstimmen von Bankkonten** - Um die Zahlung zu buchen und den entsprechenden Bankposten als ausgeglichen zu schliessen.
    - **Nur Zahlungen buchen** -, Um nur Zahlungen als übernommen zu buchen aber den entsprechenden Bankposten offen lassen. Erforderlich, dass Sie das Bankkonto separat abstimmen, zum Beispiel: Weitere Informationen finden Sie unter [Abstimmen von Bankkonten separat](bank-how-reconcile-bank-accounts-separately.md).
    - Um das Ergebnis der Buchung erneut durchzuführen bevor Sie buchen, wählen Sie die **Bericht testen** Aktion. Der Bericht **Bankkontoauszug** wird geöffnet und zeigt die gleichen Felder wie der Kopf der Seite **Zahlungsabstimmungserfassungsjournal** an.

Wenn Sie das Zahlungsabstimmungserf.-Journal buchen, werden die saldierten offenen Posten geschlossen und die zugehörigen Debitoren-, Kreditoren- oder Fibukonten werden aktualisiert. Für Zahlungen in Erf.-Journalzeilen basierend auf der Text-zu-Kontenzuordnung werden die angegebenen Debitoren-, Kreditoren- und Fibukonten aktualisiert. Für alle Buch.-Blattzeilen werden Bankposten erstellt. Alle offenen Bankposten, die sich auf ausgeglichene Debitoren- oder Kreditorenposten beziehen, werden geschlossen, wenn Sie die Aktion **Zahlungen buchen und Bankkonto abstimmen** auswählen. Dies bedeutet, dass das Bankkonto mit Zahlungen abgestimmt wird, die Sie mit dem Erfassungsjournal buchen.

Sie können den Wert im Feld **Saldo auf Bankkonto nach dem Buchen** zusammen mit dem Wert im Feld **Auszug Schluss-Saldo** verwenden, um zu kontrollieren, wenn das Bankkonto basierend auf den gebuchten Zahlungen abgestimmt wird.

> [!NOTE]  
>   Wenn Sie nicht das Bankkonto aus der Seite **Zahlungsabstimmungserfassungsjournal** abstimmen, müssen Sie das Fenster **Bankkonto-Abstimmung** verwenden. Weitere Informationen finden Sie unter [Einrichten von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Siehe auch
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
