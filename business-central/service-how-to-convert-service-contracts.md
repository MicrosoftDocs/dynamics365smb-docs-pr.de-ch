---
title: "Vorgehensweise: Konvertieren von Serviceverträgen | Microsoft Docs"
description: "Da das Werkzeug zum Ändern des MWST.-Satzes keine Serviceverträge konvertieren, müssen diese Verträge manuell konvertiert werden. In diesem Thema werden mehrere alternative Methoden beschrieben, die Sie für die Servicevertragkonvertierung verwenden können."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 64f3f214d014faff6ee0e71180b1cb928bb15d86
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="convert-service-contracts-that-include-vat-amounts"></a>Konvertieren von Serviceverträgen, die MWST-Beträge enthalten
Da das Werkzeug zum Ändern des MWST.-Satzes keine Serviceverträge konvertieren, müssen diese Verträge manuell konvertiert werden. In diesem Thema werden mehrere alternative Methoden beschrieben, die Sie für die Servicevertragkonvertierung verwenden können.  

> [!NOTE]  
>  Dieses Thema stellt einen High-Level-Workflow bereit.  

 Nachfolgend wird beschrieben, wie eine Rechnung für einen vorausbezahlten Service-Vertrag korrigiert wird, die ein Jahr im Voraus erstellt wurde.  

> [!NOTE]  
>  Für dieses Beispiel müssen Sie Ihr Arbeitsdatum in 01.01.2017 ändern.  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a>So korrigieren Sie eine Rechnung für einen vorausbezahlten Servicevertrag  
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Vertragsverwaltung** ein und wählen den zugehörenden Link aus.  
2. Wählen Sie unter **Listen** die Option **Serviceverträge** aus.  
3. Erstellen Sie eines neuen vorausbezahlten Servicevertrags. Geben Sie als Startdatum **01.01.2017** und als Fakturierungsjahr für Debitor **20000** ein.  
4. Dieser Vertrag muss signiert werden. Wählen Sie auf der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Vertrag unterzeichnen** aus.  
5. Erstellen Sie eine Servicerechnung.
6. Die Rechnung wird als nicht gebuchte Servicerechnung aufgelistet. Um die Servicerechnung einzusehen, wählen Sie **Service**, **Vertragsverwaltung** und dann **Servicerechnungen** aus.  
7. Buchen Sie die Servicerechnung.  

> [!NOTE]  
>  Ändern Sie nicht die nicht gebuchte Servicerechnung. Da die Serviceposten erstellt werden, wenn die Rechnung erstellt wird, ändert eine Änderung in der nicht gebuchten Rechnung nicht die bereits erstellten Serviceposten. Die MWST.-Posten werden allerdings erstellt, wenn die Rechnung gebucht wird. So können Sie die allgemeine Produktbuchungsgruppe und die GSP-Produktbuchungsgruppe auf der nicht gebuchten Servicerechnung ändern.  

### <a name="to-create-a-credit-memo-for-vat-difference"></a>So erstellen Sie eine Gutschrift für MWST.-Differenzen  
Nachfolgend wird beschrieben, wie eine Gutschrift erstellt wird, die nur die MWST.-Differenz für die bereits fakturierte Periode enthält, die am **01.07.2017** beginnt. In diesem Beispiel wird der MWST.-Betrag nur auf das Finanzmanagement-Modul gebucht, nicht auf das Service-Modul. Die MWST.-Posten, die mit dem Serviceposten verknüpft sind, werden nicht korrigiert.  

1. Erstellen Sie ein neues Fibukonto für die MWST.-Differenz. Dieses Konto wird für die direkte Buchung der MWST.-Korrektur verwendet.  
2. Fügen Sie der MWST.-Buchung eine neue Zeile hinzu.  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a>So erstellen Sie Vertragsablaufdaten in Vertragszeilen  
Die folgende Vorgehensweise beschreibt, wie Sie neue Verträge erstellen, indem sie in Servicevertragszeilen mit Kontaktablaufdaten arbeiten.  

1. Im Fenster **Servicevertag** legen Sie das Vertragsablaufdatum auf **30.06.2017** fest.  
2. Wählen Sie die Aktionen **Verkaufsgutschrift erstellen** aus, um automatisch eine Gutschrift für Juli 2017 bis Dezember 2017 zu erstellen.  
3. Da der Vertrag abgelaufen ist, müssen Sie einen neuen Vertrag für die Periode mit dem neuen Mehrwertsteuersatz für 1. Juli 2017 bis 31. Dezember 2017 erstellen.  

### <a name="to-create-a-new-credit-memo"></a>Eine neue Gutschrift erstellen:  
Nachfolgend wird beschrieben, wie eine neue Gutschrift mithilfe des Batchauftrags **Vorausbez. Vertragsposten holen** erstellt wird. Posten, die Sie nicht von Januar 2017 bis Juni 2017 korrigieren möchten, werden gelöscht.  

1. Führen Sie das Werkzeug zum Ändern des MWST-Satzes am 1. Juli 2017 aus. Die allgemeine Produktbuchungsgruppe oder die MwSt-Produktbuchungsgruppe werden geändert. Weitere Informationen Sie unter [Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md).  
2. Nachdem Sie das Werkzeug zum Ändern des MWST.-Satzes ausgeführt haben, können Sie ein Vertragsablaufdatum für den Servicevertrag eingeben. Sie können die Servicevertragszeile jetzt löschen und eine neue Zeile erstellen, die mit der alten identisch ist.  
3. Erstellen Sie eine neue Rechnung für die Periode von Januar 2017 bis Dezember 2012 unter Verwendung des neuen Mehrwertsteuersatzes.  
4. Um eine andere Gutschrift zu erstellen, wählen Sie im Fenster **Servicegutschriften** die Option **Neu** aus, um eine neue Servicegutschrift zu erstellen.  
5. Wählen Sie die **Vorausbez. Vertragsposten holen** Aktion aus.  
6. Nachdem die Konvertierung abgeschlossen ist, sind MWST.- und Serviceposten korrekt.  

## <a name="see-also"></a>Siehe auch  
[Arbeiten mit Serviceverträgen und Servicevertragsofferten](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Finanzen](finance.md)  
[Melden der MWST an die Steuerbehörden](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  

