---
title: 'So gehts: Einrichten von Bankkonten| Microsoft Docs'
description: 'Gewusst wie: Bankkonten einrichten'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 665c07a7242796718cfb01a1eb901d4df04ef8c9
ms.contentlocale: de-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-bank-accounts"></a>Gewusst wie: Bankkonten einrichten
In [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden Sie Bankkonten, um Ihre Banktransaktionen nachzuvollziehen. Konten können in Mandantenwährung oder in Fremdwährung geführt werden. Nachdem Sie Bankkonten eingerichtet haben, können Sie auch Checks drucken.

## <a name="to-set-up-bank-accounts"></a>Bankkonten einrichten:
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen **aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen.") Geben Sie **Bankkonten** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie im Fenster **Bankkonten** die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Um Ihre Bankkonten zum Importieren und Exportieren von Bankdateien einzurichten
Felder auf dem Inforegister **Transfer** im Fenster **Bankkontenkarte** beziehen sich auf den Import und den Export von Bankfeeds und Dateien. Weitere Informationen finden Sie unter [So gehts: Einrichten des Bankdatenkonvertierungsdienstes](bank-how-setup-bank-data-conversion-service.md) und [So gehts: Einrichten des Envestnet Yodlee Bankfeed-Diensts](bank-how-setup-bank-statement-service.md).

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen **aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen.") Geben Sie **Bankkonten** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die Karte für ein Bankkonto, mit dem Sie Bankdateien exportieren oder importieren, indem Sie den Bankdatenkonvertierungs-Service verwenden.
3. Füllen Sie im Inforegister **Übertrag** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Hinweis**: Verschiedene Dateiexportdienstleistungen und deren Formaten benötigen verschiedene Einrichtungswerte im Fenster **Bankkontokarte** Sie werden über die falschen oder fehlende Einrichtungswerte informiert, wenn Sie versuchen, die Datei zu exportieren. Lesen die Kurzbeschreibungen der Felder sorgfältig durch oder gehen Sie zu den entsprechenden Verfahrensthemen. Beispielsweise benötigt das Exportieren einer Zahlungsdatei für nordamerikanische elektronische Geldüberweisungen (EFT), dass die **Letzte Zahlungsanweisungs-Nr.** Feld und **Transitnr.** ausgefüllt ist. Weitere Informationen finden Sie unter [So gehts: Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Um Ihre Bankkonten zum Importieren und Exportieren von Bankdateien einzurichten
Felder auf dem Inforegister **Transfer** im Fenster **Bankkontenkarte** beziehen sich auf den Import und den Export von Bankfeeds und Dateien. Weitere Informationen finden Sie unter [So gehts: Einrichten des Bankdatenkonvertierungsdientes](bank-how-setup-bank-data-conversion-service.md) und [So gehts: Einrichten einer Exportzahlung an eine Bankdatei](payables-how-export-payments-bank-file.md).

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus**![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "") Symbol nach Seite oder Bericht suchen. Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die Karte für einen Kreditor, dem Sie Zahlungsbankdateien auf das Bankkonto exportieren möchten.
3. Wählen Sie die **Bankkonten** Aktion aus.
3. Füllen Sie im Fenster **Kreditoren-Bankkontokarte** im Inforegister **Übertragung** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Siehe auch
[Einrichten von Banken](bank-setup-banking.md)  
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

