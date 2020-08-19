---
title: QR-Bill Management | Microsoft Docs
description: QR-Bill Management-Erweiterung einrichten und QR-Rechnungen einfach generieren, senden und importieren.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: QR-bill, invoice, incoming documents, payment reference
ms.date: 05/05/2020
ms.author: soalex
ms.openlocfilehash: 6c3f1a2209db2ff3e1f82e0b24d44281c661a9f5
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676841"
---
# <a name="qr-bill-management-in-d365fin"></a>QR-Bill Management in [!INCLUDE[d365fin](../../includes/d365fin_md.md)]
Ab dem 1. Juli 2020 müssen Unternehmen in der Schweiz QR-Rechnungen empfangen können. QR-Rechnungen sind Zahlungsscheine für Rechnungen und eine landesweite Initiative zur Optimierung von Zahlungsprozessen. QR-Rechnungen ersetzen alle vorhandenen Zahlungsscheine und ESR-bezogene Funktionen. Sie enthalten alle erforderlichen Informationen zum Vornehmen von Zahlungen. Ein QR-Code auf dem Zahlungsschein erleichtert das Importieren der Informationen in [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. Alle relevanten Informationen werden importiert und zum Generieren von Zahlungen für den Kreditor verwendet, der die QR-Rechnung gesendet hat, einschliesslich der Zahlungsreferenz, die automatisch in Kreditorenposten eingefügt und in Zahlungsdateien an die Bank exportiert wird.

## <a name="get-started-with-the-qr-bill-management-extension"></a>Erste Schritte mit der QR-Bill Management-Erweiterung
Die QR-Bill Management-Erweiterung ist in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] enthalten und automatisch installiert. Für die ersten Schritte mit der Erweiterung müssen Sie ein paar Konfigurationsänderungen in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] vornehmen. Eine einfache Möglichkeit dafür ist die Verwendung der unterstützten Einrichtung 'QR-Rechnung einrichten'. Die Anleitung hilft Ihnen bei der Eingabe von Informationen, wie etwa:

* Angeben, ob Ihre IBAN oder QR-IBAN verwendet werden soll.
* Definieren, wie Namen und Adressen auf QR-Rechnungen angezeigt werden und wie die Codierung für deutsche Umlaute verwendet werden soll. Wir empfehlen, dass Sie die Standardwerte verwenden.
* Wählen Sie das Standardlayout aus, das Sie für QR-Rechnungen verwenden. Das Layout bestimmt, ob IBAN oder QR-IBAN verwendet werden soll, ob der Referenztyp Kreditor oder QR-Referenz ist und ob die Abrechnungsinformationen im SWICO-Format enthalten sein sollen.
* Aktivieren Sie Verkaufs- und Servicerechnungstypen sowie Zahlungsmethoden für die QR-Rechnungen.
* Geben Sie die Erf.-Journalvorlage und das Erfassungsjournal an, die verwendet werden sollen, wenn Einkaufserfassungsjournale aus gescannten oder importierten QR-Rechnungen generiert werden.

Bei Bedarf können Sie diese Einstellungen auf den folgenden Seiten ändern. 

* **Einrichtung der QR-Rechnung**, um allgemeine Einstellungen zu ändern. 
* **QR-Rechnungslayout**, um Layouteinstellungen zu ändern.

## <a name="issuing-qr-bills"></a>Ausstellen von QR-Rechnungen
Sie können QR-Rechnungen für Verkaufs- und Servicerechnungen aktivieren. Dadurch wird ein Eintrag zu **Berichtsauswahl - Verkauf** hinzugefügt, der beim Generieren der Rechnungen eine zusätzliche PDF-Datei mit der QR-Rechnung generiert. 

## <a name="adding-billing-information-to-qr-bills"></a>Hinzufügen von Abrechnungsinformationen zu QR-Rechnungen
Beim Erstellen einer QR-Rechnung können Sie Abrechnungsinformationen im SWICO-Format einfügen, wie von SIX, dem Schweizer Anbieter für Zahlungsinfrastruktur, empfohlen. Im Idealfall können Geschäftsanwendungen, die QR-Rechnungen erstellen oder importieren, Informationen, wie den MWST-Betrag, die Rechnungsnummer des Kreditors usw., verarbeiten, weil diese für die zu zahlende Rechnung wertvoll sein können. In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] importieren wir diese Informationen, verwenden allerdings nur die Rechnungsnummer des Kreditors. Falls Sie die anderen Informationen verwenden möchten, können Sie Ihre eigene Anpassung erstellen.

## <a name="understanding-the-payment-reference"></a>Informationen über die Zahlungsreferenz
Bei Zahlungsprozessen geht es um das Bezahlen des richtigen Betrags an die richtige Partei. Dadurch können sie Zahlungen leichter abstimmen und ausstehende Konten schliessen. Die QR-Bill Management-Erweiterung erledigt dies durch Generieren einer Zahlungsreferenz für QR-Rechnungen, die für Rechnungen in einem bestimmten Unternehmen eindeutig sind. Dies bedeutet, dass dieselbe Zahlungsreferenz nicht mehrmals ausgestellt werden kann. Falls Ihr Kunde zudem [!INCLUDE[d365fin](../../includes/d365fin_md.md)] verwendet, wird die Zahlungsreferenz importiert, wenn Sie QR-Rechnungen erhalten, an die Seite 'Kreditorenposten' übertragen und als Referenz beim Erstellen von Kreditorenzahlungen verwendet. Weitere Informationen finden Sie unter [Empfang von QR-Rechnungen](ui-extensions-qr-bill-management.md#receiving-qr-bills). Der Ablauf ist ähnlich wie bei der vorherigen ESR-Referenzfunktion, die die QR-Rechnungen ersetzen. Schliesslich werden die Zahlungsdateien (pain.001) von der Geschäftsanwendung des Kunden mit der Nachricht an seine Bank gesendet, die Beträge an das Konto des Kreditors zu überweisen. Die Bank erstellt eine Kontoauszugsdatei (camt.054), die der Kreditor importieren kann, um die Konten abzustimmen. Diese Datei enthält die Zahlungsreferenz und wird über das Datenaustauschframework importiert, das von der QR-Bill Management-Erweiterung aktualisiert wird, um camt.054-Dateien zu importieren.  
Für ESR-Referenzen konnten Sie Informationen konfigurieren, damit sie beispielsweise die Kundennummer und Rechnungsnummer enthielten. Sie können in QR-Rechnungen die Zahlungsreferenz nicht konfigurieren. Es besteht immer eine direkte Relation zwischen ausgestellter QR-Rechnung und einer Zahlung. Dadurch wird die Abstimmung erleichtert und die Zahlungsreferenz muss auf QR-Rechnungen nicht mehr konfiguriert werden. Stattdessen verwendet [!INCLUDE[d365fin](../../includes/d365fin_md.md)] einen eindeutigen Zähler für die Zahlungsreferenz. Außerdem ist eine Logik implementiert, die den zweimaligen Import oder Scan derselben Zahlungsreferenz sperrt.

## <a name="scanning-and-importing-qr-bills"></a>Scannen und Importieren von QR-Rechnungen
Zum Scannen oder Importieren einer QR-Rechnung müssen Sie einen der folgenden Typen von Scangeräten verwenden:

* Ein Eingangsscanner, der den QR-Code entschlüsselt und die Tastatur simuliert, um den entschlüsselten Wert direkt in ein Feld in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] einzugeben.
* Ein Scanner, der den QR-Code entschlüsseln und in einer TXT-Datei speichern kann, die Sie in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] importieren. 

> [!Note]
> Sie können keine QR-Rechnungen, die Sie als PDF-Dateien erhalten haben, direkt in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] importieren, weil [!INCLUDE[d365fin](../../includes/d365fin_md.md)] keine QR-Codes interpretieren kann. Sie müssen eine der folgenden Scanmethoden verwenden.

## <a name="receiving-qr-bills"></a>Empfang von QR-Rechnungen
Sie können QR-Rechnungen an mehreren Orten in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] empfangen:

* **Eingehende Belege**, wenn eine QR-Rechnung das Erstellen eines neuen Kaufbelegs oder eines Einkauf Erf.-Journals initiieren soll.
* **Einkaufsbestellungen und Einkaufsrechnungen**, wenn Sie Informationen aus einer QR-Rechnung in einen vorhandenen Einkaufsbeleg importieren und zur Überprüfung von Betrag und Währung sowie zum Aufbewahren der Zahlungsreferenz verwenden möchten.
* **Einkaufserfassungsjournale**, wenn Sie neue Einkaufserfassungsjournalzeilen auf Grundlage von QR-Rechnungen erstellen möchten. 

### <a name="to-receive-a-qr-bill-through-an-incoming-documents"></a>So empfangen Sie eine QR-Rechnung über eingehende Belege
Der Empfang einer QR-Rechnung über eingehende Belege ist insbesondere hilfreich, wenn der Prozess automatisiert ist. Sie können QR-Rechnungen durch eingehende Belege allerdings auch manuell empfangen.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell me-Funktion") aus, geben Sie **Eingehende Belege** ein, und wählen Sie dann den zugehörigen Link.
2. Erstellen Sie in der Liste **Eingehende Belege** einen neuen Eintrag, indem Sie **Neu** und dann **Neu** wählen. 
3. Geben Sie auf der Seite **Eingehender Beleg** eine Beschreibung in das Feld **Beschreibung** ein.
4. Zum Importieren der QR-Rechnung wählen Sie **Aktionen**, **QR-Rechnung** und dann **QR-Rechnung scannen** aus, um eine QR-Rechnung in den Eintrag des eingehenden Belegs zu scannen.
 
> [!TIP]
> Nach dem Importieren der QR-Rechnung können Sie sie im Inforegister **Detailabgleich** auf Fehler überprüfen.

Im eingehenden Beleg können Sie ein Einkauf Erf.-Journal oder eine Einkaufsrechnung erstellen und die Zahlungsreferenz von der QR-Rechnung wird beiden zugeordnet.

> [!Note]
> Beim Importieren von QR-Rechnungen versucht [!INCLUDE[d365fin](../../includes/d365fin_md.md)], ein Kreditorenbankkonto mit übereinstimmender IBAN oder QR-IBAN zu finden. Beim Importieren von QR-Rechnungen in eingehenden Belegen und damit verbundenen Erstellen eines Belegs oder Einkauf Erf.-Journals bestimmt das Kreditorenbankkonto den zu verwendenden Kreditor. Der Ansatz mit dem eingehenden Beleg hilft zu gewährleisten, dass der richtige Kreditor zugewiesen ist.

### <a name="receiving-a-qr-bill-through-purchase-order-or-purchase-invoice"></a>Empfang einer QR-Rechnung über Einkaufsbestellung oder Einkaufsrechnung
Beim Empfang einer QR-Rechnung über eine Einkaufsbestellung oder eine Einkaufsrechnung wird der Rechnungsbetrag überprüft und die Zahlungsreferenz zu den Posten hinzugefügt. Sie können eine QR-Rechnung wie eingehende Belege scannen oder in eine vorhandene Einkaufsbestellung oder eine Einkaufsrechnung importieren. Dieser Prozess verwendet die QR-IBAN oder IBAN aus der QR-Rechnung, um den Kreditor mit einer übereinstimmenden Nummer zu finden. Falls keine Übereinstimmung gefunden wird, können Sie die QR-Rechnung nicht scannen oder importieren. Falls das geschieht, können Sie das Kreditorenbankkonto erstellen und dann das Hinzufügen der QR-Rechnung zum Kaufbeleg erlauben. Wenn die QR-Rechnung gescannt oder in den Kaufbeleg importiert wird, werden der Betrag, die Zahlungsreferenz und weitere Informationen aus der QR-Rechnung hinzugefügt. Diese werden zur Überprüfung verwendet, bevor der Kaufbeleg gebucht wird. Die Buchung wird gesperrt, wenn der Betrag der Bestellung oder der Rechnung nicht mit dem Betrag der QR-Rechnung übereinstimmt. Die Überprüfung erfolgt ebenso, wenn Sie die QR-Rechnung scannen oder importieren. Falls die Zahlungsreferenz bereits in einem Kreditorenposten für einen Kreditor verwendet wird, wird ein Fehler angezeigt. Kreditoren können nicht mehrere QR-Rechnungen mit derselben Zahlungsreferenz ausstellen. Entsprechend wird ein Fehler angezeigt, wenn die QR-Rechnung und die Zahlungsreferenz bereits in einen offenen Kaufbeleg importiert wurden. 

### <a name="receiving-a-qr-bill-through-a-purchase-journal"></a>Empfang einer QR-Rechnung über ein Einkauf Erf.-Journal
Sie können QR-Rechnungen direkt in ein **Einkauf Erf.-Journal** scannen oder importieren. Dies ist hilfreich, wenn Sie neue Einkauf Erf.-Journale auf Grundlage einer QR-Rechnung erstellen möchten. Durch direktes Scannen oder Importieren in ein Einkauf Erf.-Journal wird eine neue **Einkaufserfassungsjournalzeile** mithilfe des Kreditors und des Betrags aus der QR-Rechnung erstellt. Zudem wird versucht, den Kreditor zu erkennen, indem ein **Kreditor Bankkonto** mit übereinstimmender IBAN oder QR-IBAN gesucht wird. Beispiel: Die Verwendung von Einkaufserfassungsjournalen ist hilfreich, wenn Sie keine Einkaufsbestellungen oder Einkaufsrechnungen verwenden möchten.

## <a name="reconciliation"></a>Abstimmen
Beim Importieren von Banktransaktionen (camt) auf der Seite "Zahlungsabstimmungserfassungsjournal" wird angenommen, dass die Datei die Zahlungsreferenz enthält, die automatisch die entsprechenden **Debitorenposten** sucht, die ausgeglichen werden müssen.    

## <a name="upcoming-capabilities-for-qr-bills"></a>Zukünftige Funktionen für QR-Rechnungen
Wir planen, der QR-Bill Management-Erweiterung in den kommenden Updates der 1. Veröffentlichungsrunde 2020 weitere Funktionen hinzuzufügen. Beispiel: Sie können QR-Rechnungen durch Einkaufsbelege und Einkaufserfassungsjournale empfangen. Dies ermöglicht zusätzliche Validierungen sowie die Automatisierung und Optimierung von Empfangsprozessen. Informationen dazu finden Sie im [Veröffentlichungsplan](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-business-central/qr-bill-management-switzerland).

## <a name="see-also"></a>Siehe auch
[Lokale Funktion (Schweiz)](switzerland-local-functionality.md)  
