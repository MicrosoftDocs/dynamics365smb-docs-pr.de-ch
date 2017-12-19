---
title: Erweiterungen installieren um Dynamics 365 Business edition anzupassen | Microsoft Docs
description: "Informationen zum Hinzufügen von Funktionalität und Anpassungen für Dynamics 365 Business edition erhalten durch die Installation von Erweiterungen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 07/07/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: fb13cfe2d5e5a397d33f66b9fd4db14e46dcc5e1
ms.contentlocale: de-ch
ms.lasthandoff: 12/14/2017

---
# <a name="customizing-dynamics-365-business-edition-using-extensions"></a>Anpassen von Dynamics 365, Business edition mit Erweiterungen
Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] ändern, indem Sie beispielsweise Erweiterungen installieren, die Funktionalität hinzufügen, das Verhalten ändern oder Zugriff auf die neuen Onlinediensten geben.
Wenn Sie das [!INCLUDE[d365fin](includes/d365fin_md.md)] zuerst starten, werden bestimmte Erweiterungen bereits eingerichtet. Im Zeitverlauf werden mehr Erweiterungen für Sie zugänglich und Sie können auswählen, ob Sie die Erweiterung verwenden möchten oder nicht.

Beispielsweise bietet Microsoft eine Erweiterung an, die die Integration mit Standard Paypal-Zahlungen ermöglicht. Diese Erweiterung wird standardmäßig eingerichtet.
Wenn aber keine andere Erweiterung bereitgestellt wird, die die Integration mit einem anderen Zahlungsservice anbietet, können Sie die neue Erweiterung einrichten und dann auswählen, welcher der beiden Services verwendet werden soll.  

Sie verwalten die Erweiterung des **Erweiterungs-Verwaltungs**-Fenster. Sie können vom Startbildschirm auf dieses Fenster zugreifen. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus**![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Erweiterung** ein und wählen Sie dann den entsprechenden Link aus.  

> [!NOTE]  
>   Wenn Sie der Meinung sind, Sie sollten Zugriff zu einer Erweiterung haben, können die Funktionalität aber nicht finden, überprüfen Sie das Fenster **Erweiterungsverwaltung**, wenn die Erweiterung dort nicht aufgeführt wird, können Sie sie einrichten, wie im folgenden Abschnitt erläutert.  

## <a name="installing-an-extension"></a>Eine Erweiterung wird installiert
Sie können neue Erweiterungen vom Marketplace abrufen unter [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1). Hier können Sie alle verfügbaren Erweiterungen anzeigen für [!INCLUDE[d365fin](includes/d365fin_md.md)] und Sie können Apps, Erweiterungen und Inhaltpakete für andere Microsoft-Produkte abrufen. Legen Sie die gewünschten Filter fest, werfen Sie einen Blick auf die Informationen für jede Erweiterung, und rufen Sie eine Erweiterung für Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] ab.  
> [!NOTE]  
>   Melden Sie sich auf [AppSource.microsoft.com](https://appsource.microsoft.com/)über Ihr E-Mail- Konto an, das Sie für [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden. Verwenden Sie dasselbe E-Mail-Konto für andere Produkte und Dienste für eine reibungslose Nutzung.  

Sie können auch auf den Marketplace aus [!INCLUDE[d365fin](includes/d365fin_md.md)]zugreifen. Im Fenster **Erweiterungsverwaltung** können Sie die Erweiterungen sehen, die zur Zeit installiert sind, und Sie können die Seite **Marketplace für Erweiterungen** öffnen, die die [!INCLUDE[d365fin](includes/d365fin_md.md)]Erweiterungen anzeigen, die aktuell über die AppSource verfügbar sind. Wenn Sie den Link *Weitere Apps* auswählen, werden Sie auf [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1) weitergeleitet.  

Wenn Sie eine Erweiterung auswählen, können Sie erfahren, was die Erweiterung ausführt, und auf die Hilfe für die Erweiterung zugreifen, um mehr darüber zu erfahren. Wenn Sie eine Erweiterung erhalten möchten, müssen Sie die Nutzungsbedingungen zustimmen. Wenn Sie Erweiterungen von der AppSource-Website abrufen, werden Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] angemeldet, um die Installation abzuschließen.  

Wenn Sie eine Erweiterung installieren, müssen Sie diese möglicherweise einrichten, wie ein Konto zur Verwendung mit Erweiterung für **Paypal-Zahlungen Standard** für [!INCLUDE[d365fin](includes/d365fin_md.md)] definieren.
Andere Erweiterungen fügen einfach Felder einer vorhandenen Seite hinzu, oder sie fügen beispielsweise eine neue Seite hinzu.   

Wenn Sie eine Erweiterung deinstallieren und Sie dann Ihre Absicht ändern, können Sie sie wieder einrichten. Wenn Sie eine Erweiterung deinstallieren, die Sie verwendet haben, werden die Daten beibehalten, sodass, wenn Sie die Erweiterung erneut einrichten, die Daten noch verfügbar sind.  

Einige Erweiterungen werden von Microsoft bereitgestellt, und andere Erweiterungen werden von anderen [anderen Unternehmen](ui-extensions-other.md) bereitgestellt. Alle Erweiterungen werden getestet, bevor sie zugänglich gemacht werden, aber wir empfehlen, dass Sie auf die Links zugreifen, die mit jeder Erweiterung zur Verfügung gestellt wurden, um mehr über die Erweiterung zu erfahren, bevor Sie entscheiden, sie einzurichten.  

Microsoft stellt die folgenden Erweiterungen bereit:  

* [Dynamics GP Datenmigration](ui-extensions-dynamicsgp-data-migration.md)  
* [Bank-Feeds Envestnet Yodlee](ui-extensions-yodlee-bank-feeds.md)  
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [QuickBooks Datenmigration](ui-extensions-quickbooks-data-migration.md)  
* [Umsatz- und Lagerbestandsplanung](ui-extensions-sales-forecast.md)  
* [Ceridian-Gehaltsliste](ui-extensions-ceridian-payroll.md)  
* [Import von QuickBooks-Lohndatei](ui-extensions-quickbooks-payroll.md)  
* [WorldPay Zahlungsstandard](ui-extensions-worldpay-payments-standard.md)
* [GetAddress.io Postleitzahlen Großbritannien](ui-extensions-getaddressio.md)
* [QuickBooks Onlin Datenmigration](ui-extensions-quickbooks-online-data-migration.md)
* [Buchhaltungsportal](ui-extensions-accountant-portal.md)  
* [Schliffbildanalysator](ui-extensions-image-analyzer.md)
* [Zahlungen und gebuchte Abstimmungen (DK)](ui-extensions-payments-reconciliation-formats-dk.md)
* [C5-Datenmigration](ui-extensions-c5-data-migration.md)

> [!NOTE]  
>  Neue Erweiterungen sind nicht in AppSource verfügbar, sofort nachdem wird ein ankündigen aktualisieren. Sie können die Erweiterung [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1) im Auge behalten.

## <a name="see-also"></a>Siehe auch
[Gewusst wie: Einrichten des Envestnet Yodlee Bank-Feed-Service](bank-how-setup-bank-statement-service.md)  
[Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Paypal](sales-how-enable-payment-service-extensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen migrieren](upload-data.md)  
[Einrichten der britischen Postleitzahlerweiterung GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]Erweiterungen für andere Anbieter](ui-extensions-other.md)E  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

