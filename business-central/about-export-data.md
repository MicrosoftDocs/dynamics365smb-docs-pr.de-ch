---
title: Business Central-Daten nach Excel exportieren
description: 'Sie können Ihre Finanzberichte und Intelligence-Daten von Business Central nach Excel exportieren, oder Ihre Financials Daten in Excel öffnen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'analysis, reporting, financial report, business intelligence, BI, Excel'
ms.search.form: '9901,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---
# <a name="export-your-business-data-to-excel"></a>Ihre Geschäftsdaten in Excel exportieren

Excel ist ein leistungsstarkes Tool, um mit Daten zu arbeiten. Sie können jede Liste in Excel über [!INCLUDE[prod_short](includes/prod_short.md)] öffnen. Sie können sogar Daten in Excel ändern und dann an [!INCLUDE [prod_short](includes/prod_short.md)] zurücksenden. Mit derselben Funktion können Sie Ihre Daten mühelos mitnehmen, wenn Sie sich entscheiden, Ihr Abonnement zu kündigen.

## <a name="opening-lists-in-excel"></a>Öffnen von Listen in Excel

Sie können Daten aus jeder Liste, jedem Arbeitsblatt oder jedem Eintrag in Excel öffnen. Sie öffnen einfach die Seite, die Sie anzeigen möchten, und wählen dann **In Excel öffnen**. Beispielsweise öffnen Sie die Liste der Debitoren (nach **Debitoren** suchen) und wählen Sie dann **In Excel öffnen** aus. Ihr Browser fordert Sie auf, das generierte Excel-Arbeitsblatt zu öffnen oder zu speichern.  

> [!NOTE]
> Verwenden Sie diese Option, wenn Sie Ihre Änderungen nicht wieder in [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlichen möchten.  

Jede Liste enthält einige Spalten. Der Export nach Excel umfasst alle Spalten, die sich in Ihrer aktuellen Ansicht befinden. Ändern Sie die Spalten, indem Sie das Kontextmenü für eine beliebige Spalte öffnen und dann angeben, welche Spalten Sie anzeigen möchten. Die Liste der Spalten ist bei den meisten Listen unterschiedlich. Die Spalten spiegeln die Struktur in der Datenbank wider, in der Ihre Daten gespeichert sind. Wenn Sie nicht sicher sind, welchen Datentyp eine bestimmte Spalte enthält, fügen Sie sie Ihrer Ansicht hinzu. Sie können sie jederzeit wieder entfernen.  

### <a name="edit-data-in-excel"></a>Daten in Excel bearbeiten

Ihre [!INCLUDE[prod_short](includes/prod_short.md)] Benutzeroberfläche wird das Add-In für Excel integrieren, sodass Sie Daten in Excel bearbeiten können. Weitere Informationen finden Sie unter [Finanzauswertungen analysieren in Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Daten in andere Finanzsysteme exportieren

Wenn Sie Ihre Abonnement für [!INCLUDE[prod_short](includes/prod_short.md)] stornieren möchten, können Sie die Daten in Excel exportieren, damit Sie in Ihrem nächsten Finanzsystem bereitstehen.  

Sie können alle Seiten exportieren, aber möglicherweise benötigen Sie nicht alles. Ziehen Sie in Betracht, nur die wesentlichen Seiten zu exportieren, und denken Sie daran, alle Spalten hinzuzufügen:  

* Kontenplan  
* Debitoren  
* Kreditoren  
* Banken  
* Arti&kel  

Wenn Sie alle Ihre Finanztransaktionen exportieren möchten, sind dies sehr viele Daten. Der Export dauert deshalb mehrere Minuten. Die Finanztransaktionen werden auf der Seite **Fibuposten** angezeigt.  

Es ist empfehlenswert, dass Sie auch erwägen, Daten von den nächsten Seiten zu exportieren:  

* Debitorenposten  
* Kreditorenposten  
* Bankposten  
* Lagerposten  
* Buchungsmatrix Einrichtung  
* Debitorenbuchungsgruppen  
* Kreditorenbuchungsgruppen  
* Artikelbuchungsgruppen  
* Bankbuchungsgruppe  
* Sachkontenbudgets  
* Finanzbudgetposten  
* Verkaufsofferten  
* Verkaufsrechnungen  
* Einkaufsrechnungen  
* Kontakte  
* Verkäufer  

> [!NOTE]  
> Wenn Sie mehr als einen Mandanten in [!INCLUDE[prod_short](includes/prod_short.md)] erfasst haben, müssen Sie die entsprechenden Daten der einzelnen Unternehmen exportieren.

> [!NOTE]
> Sie müssen über mindestens eine der folgenden Berechtigungen verfügen, um Daten in Excel zu öffnen oder zu bearbeiten:
>
> * Berechtigungssatz *D365 Excel-Exportaktion*  
> * Systemberechtigung 6110 *Aktionsexport nach Excel zulassen*.  

Weitere Informationen finden Sie unter [Eine Übersicht der Benutzerberechtigungen erhalten](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).

## <a name="see-also"></a>Siehe auch

[Abbrechen des Abonnements für [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Geschäftsdaten aus anderen Finanzsystemen migrieren](across-import-data-configuration-packages.md)  
[Finanzauswertungen analysieren in Microsoft Excel](finance-analyze-excel.md)  
[Finanzen](finance.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
