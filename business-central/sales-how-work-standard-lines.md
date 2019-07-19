---
title: Einrichten und Verwenden von Standardzeilen für Wiederverkäufe und -einkäufe| Microsoft Docs
description: Sie können Verkaufszeilen und Einkaufszeilen einrichten, die Sie häufig machen und diese dann in Verkaufs- und Einkaufsbelegen einfügen, um die Zeilen mit Standardinformationen schnell auszufüllen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 04/24/2019
ms.author: sgroespe
ms.openlocfilehash: 83f6a24fc066faef49de456e18673f8059a9831d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252276"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen
Wenn Sie häufiger Verkaufs- und Einkaufszeilen mit ähnlichen Daten erstellen müssen, können Sie die Standardzeilen einrichten, die Sie in wiederkehrenden Verkaufs- und Einkaufsbelegen, z. B. für wiederkehrende Ersatzaufträge benötigen.  

Der folgende Ablauf zeigt, wie man Standardverkaufszeilen in einer Verkaufsrechnung einrichtet. Das funktioniert ähnlich bei allen anderen Verkaufsbelegen und Einkaufsbelegen.  

## <a name="to-set-up-standard-sales-lines"></a>So richten Sie eine Standard-Verkaufszeile ein  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standard-Verkaufszeilen** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie auf der Seite **Standardverkaufszeile** die Aktion **Neu** aus.  
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Im Inforegister **Zeilen** können Sie Informationen in die Felder eingeben, um Verkaufszeilen vorzubereiten, die die Standardzeilen widerspiegeln, von der Sie erwarten, wiederkehrende Zeilen in Einkaufsbelegen zu verwenden.  

> [!NOTE]
> Sie können keine Preise auf Standardverkaufszeilen definieren, da Preise, Rabatte usw. auf den tatsächlichen Verkaufsbelegen berechnet werden, nachdem Sie die Standardverkaufszeilen eingefügt haben.

## <a name="to-assign-standard-sales-lines-to-a-customer"></a>So weisen Sie Debitoren Standardverkaufszeilen hinzu
Weisen Sie einem Debitor mindestens eine Standardverkaufszeile zu, sodass sie auf Verkaufsbelegen für diesen Debitor eingefügt werden können.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitor** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die Karte für einen entsprechendes Debitor.
3. Wählen Sie die **Wiederkehrende Verkaufszeilen** Aktion aus.
4. Auf der Seite **Wiederkehrende Verkaufszeilen** wählen Sie Codes für die wiederkehrenden Verkaufszeilen aus, die Sie auf den Verkaufsbelegen für den Debitor einfügen können möchten.
5. Füllen Sie die weiteren Felder aus, um festzulegen, wann, wie und wo die wiederkehrenden Verkaufszeilen verwendet werden sollen.
6. In den vier Feldern, in denen Sie angeben, wie die Zeilen auf vier Belegarten eingefügt werden, wählen Sie eine der folgenden Optionen aus:

|Option|Beschreibung|
|-|-|
|**Manuell**|Sie müssen eine wiederkehrende Verkaufszeile, die bereits für den Debitor vorhanden ist, manuell suchen.|
|**Automatisch**|Wenn wiederkehrende Verkaufszeilen für den Debitor vorhanden sind, erhalten Sie eine Benachrichtigung, in der Sie auswählen können, welche eingefügt werden soll. Wenn nur eine wiederkehrende Verkaufszeile existiert, wird sie automatisch eingefügt.|
|**Immer bestätigen**|Eine Benachrichtigung erscheint und alle vorhandenen wiederkehrenden Verkaufszeilen werden angezeigt, sodass Sie eine auswählen können.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Um auf einer wiederkehrenden Verkaufsrechnung Standardverkaufszeilen einfügen
Wenn Sie wiederkehrende Verkaufszeilen für den Debitor vorhanden sind, können Sie diese auf allen Arten von Verkaufsbelegen, wie einer Verkaufsrechnung, einfügen. Wenn Sie die fragliche Benachrichtigung aktiviert haben, werden Sie informiert, wenn eine wiederkehrende Verkaufszeile vorhanden ist.
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Rechnung** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die Verkaufsrechnung, in die Sie eine oder mehrere Standard-Verkaufszeilen einfügen möchten.
3. Wählen Sie die **Wiederkehrende Verkaufszeilen abrufen** Aktion aus.
4. Auf der Seite **Wiederkehrende Verkaufszeilen** wählen Sie die Suchschaltfläche im Feld **Code**, und wählen einen Satz von Standardverkaufszeilen aus.

    > [!NOTE]
    > Um wiederkehrenden die Verkaufszeilen zu verwenden, die bei der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen erstellen** festgelegt werden, müssen Sie die Felder **Gültig ab-Datum** und **Gültig bis-Datum** auf der Seite **Wiederkehrende Verkaufszeilen** ausfüllen. Weitere Informationen finden Sie unter [Mehrere Verkaufsrechnungen auf der Grundlage von Standardverkaufscodes erstellen](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-standard-sales-lines)

5. Wählen Sie die Schaltfläche **OK**, um die Standardverkaufszeilen in die Rechnung einzufügen, in die Sie Informationen verwenden ist beim oder bearbeiten können.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Mehrere Verkaufsrechnungen auf der Grundlage von Standardverkaufscodes erstellen
Sie können mit der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen erstellen** die Verkaufsrechnungen gemäss Standardverkaufscodes erstellen, die den Debitoren zugeordnet sind und Buchungsdaten enthalten, die innerhalb der Gültigkeitszeiträume liegen, die Sie im Standardverkaufscode festgelegt haben.

> [!NOTE]
> Auf der Seite **Wiederkehrende Verkaufszeilen** können Sie auch eine Einzugsmethode und ein Lastschrift-Mandat angeben. Die Verkaufsrechnungen, die mit der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen** erstellt werden, enthalten dann Informationen, die für den Einzug der Zahlungen für die Verkaufsrechnungen per SEPA-Lastschrift benötigt werden. Weitere Informationen finden Sie unter [Einziehen von Zahlungen mit Abbuchung SEPA](finance-collect-payments-with-sepa-direct-debit.md).

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Wiederk. Verkaufsrechnungen** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie auf der Seite **Wiederkehrende Verkaufsrechnung** die Felder wie benötigt aus.
3. In dem Feld **Code** geben Sie den Code der Standardverkaufscode ein, die einem Debitor zugewiesen sind, für den Verkaufsrechnungen erstellen möchten.
4. Wählen Sie die Schaltfläche **OK** aus.

Verkaufsrechnungen werden für die Debitoren mit dem angegebenen Standard-Debitorenvertriebscode und allen angegebenen Direkteinzugsinformationen zur Buchung am angegebenen Datum erstellt.

## <a name="see-also"></a>Siehe auch  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
