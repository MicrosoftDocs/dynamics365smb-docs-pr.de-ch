---
title: Einrichten von Bankdatenkonversion| Microsoft Docs
description: "Sie können Bankkonten einrichten, um Geschäftsvorfälle und Import- oder Ausfuhrbankfeeds, wie Yodlee zu verwalten."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 5bf6e0c961e35b2fdb23eb1ba470da0f5c098d81
ms.contentlocale: de-ch
ms.lasthandoff: 06/11/2018

---
# <a name="set-up-the-bank-data-conversion-service"></a>Einrichten des Bankdaten-Konvertierungsdienst
Ein globaler Diensteanbieter, der Bankdaten in das Dateiformat konvertiert, das Ihre Bank verlangt, ist in [!INCLUDE[d365fin](includes/d365fin_md.md)] eingebunden und kann aktiviert werden. Dieses wird in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Bankdaten-Konvertierungsdienst erstellt.

Sie können Zahlungspositionen aus dem Fenster **Zahlungsausgangs Buch.-Blatt** in einen Datenstream oder eine Datei exportieren, den Sie dann für Ihre Bank automatische zum Verarbeiten hochladen, sodass Sie elektronische Zahlungen nicht einzeln ausführen müssen. Weitere Informationen finden Sie unter [Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md).

Sie können Bankkontoauszugsdateien in das **Zahlungsabstimmungsbuch.-Blatt** importieren, indem Sie den Bankdaten-Konvertierungsdienst verwenden, um eine Datei zu erstellen, die Sie von Ihrer Bank mit einem Datenstream erhalten, die in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert werden kann. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Als Alternative zum Importieren von Bankkontoauszügen mit dem Bankdaten-Konvertierungsdienst können Sie den Bank-Feeddienst Envestnet Yodlee verwenden. Für weitere Informationen, siehe [Einrichten des Envestnet Yodlee Bank-Feed-Service](bank-how-setup-bank-statement-service.md).

Um Bankdateien zu importieren oder zu exportieren, müssen Sie Ihre eigenen Bankkonten und jene des Kreditors einrichten. Weitere Informationen finden Sie unter [So gehts: Einrichten von Bankkonten](bank-how-setup-bank-accounts.md).

> [!NOTE]  
>   Der Bankdaten-Konvertierungsdienst legt möglicherweise einen Höchstwert für die Anzahl der Zeilen fest, die in einer Datei exportiert werden können. Sie erhalten eine Fehlermeldung, wenn der Grenzwert überschritten wird. Es wird empfohlen, das Bankkontoauszugsdateien nicht 1000 Zeilen überschreiten, da die Verarbeitungszeit im Bankdaten-Konvertierungsdienst andernfalls sich erheblich erhöht.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Ihr Unternehmen für den Bankdatenkonvertierungs-Service anmelden
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankdaten-Konvertierungsservice einrichten** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Das Fenster **Einrichtung Bankdaten-Konvertierungsservice** wird geöffnet und zeigt drei Felder an, die mit relevanten URLs des Anbieters des Bankdaten-Konvertierungsdienst vorab ausgefüllt sind.

    > [!NOTE]  
    >   In der Demonstrationsdatenbank CRONUS Internationals Ltd. werden die Felder "Benutzername" und "Kennwort" mit Demonstrationsanmeldungsinformationen vorausgefüllt, die Sie mit den tatsächlichen Informationen Ihres Unternehmens ersetzen müssen, wenn Sie sich für den Bankdaten-Konvertierungsdienst anmelden.
3. Wählen Sie im Feld **Registrierungs-URL** die Browserschaltfläche, um die Registrierungsseite des Dienstanbieters zu öffnen.  
4. Geben Sie auf der Registrierungsseite des Bankdatendienstanbieters den Benutzernamen und das Kennwort für das Abonnement Ihres Unternehmens ein, und schliessen Sie dann die Anmeldung ab, wie von dem Dienstanbieter angewiesen.

  Ihr Unternehmen ist jetzt für den Bankdatenkonvertierungs-Dienst registriert. Fahren Sie fort, um den Benutzernamen und das Kennwort einzugeben, die Sie für den Service für die verknüpften Einrichtungsfeldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] angegeben haben.
5. Im Fenster **Einrichtung Bankdaten-Konvertierungsservice** geben Sie im Feld **Benutzername** den gleichen Wert ein, den Sie als Benutzername auf der Seite des Dienstanbieters in Schritt 4 eingegeben haben.
6. Geben Sie im Feld **Kennwort** denselben Wert ein, den Sie im Feld **Kennwort** auf der Seite des Dienstanbieters in Schritt 4 angegeben haben.

> [!NOTE]  
> Sie informieren Daten werden verschlüsselt automatisch an.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Um die Liste der gerade unterstützten Bankdatenformate anzeigen oder zu aktualisieren
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankdaten-Konvertierungsservice einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Einrichtung Bankdaten-Konvertierungsservice** die Aktion **Bankname – Datenkonvertierungsliste**, um die Liste der Banknamen zu öffnen, die die Bankdatenformate darstellen, die von dem Konvertierungs-Service unterstützt werden.
3. Wählen Sie auf der Seite **Bankname – Datenkonvertierungsliste** die Aktion **Banknamenliste aktualisieren** aus.

Die Liste der Bankdatenformaten, die aus dem Bankdatenkonvertierungs-Service unterstützt werden, wird jetzt aktualisiert. Dies ist die Liste der Banknamen, gefiltert nach den Ländern/Regionen, die Sie im Feld **Bankname – Datenkonvertierung** im Fenster **Bankkontokarte** auswählen können.

> [!NOTE]  
>   Die Aktualisierung der unterstützten Bankdatenformate erfolgt auch, wenn Sie einen Wert im Feld **Bankname – Datenkonvertierung** des Bankkontos auswählen oder dort einen Wert eingeben.

Sie sind nun für den Bankdatenkonvertierungs-Dienst registriert. Fahren Sie fort, die Registrierungsinformationen über jedes Bankkonto wiederzugeben, das der Service verwendet.

## <a name="see-also"></a>Siehe auch
[Einrichten von Banken](bank-setup-banking.md)  
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

