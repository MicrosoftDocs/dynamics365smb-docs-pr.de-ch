---
title: Einrichten von eingehenden Belegen| Microsoft Docs
description: Verwenden Sie die Funktion der eingehenden Belege, um elektronische Belege zu erstellen, verwalten Sie OCRaufgaben, importieren Sie Rechnungen und wandeln Sie Bilddateien um.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f7d0741f3ead748867a52cb399967c196748c479
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305538"
---
# <a name="set-up-incoming-documents"></a>Einrichten von eingehenden Belegen
Wenn Sie Fibu Erfassungsjournalzeilen für eingehende Belegdatensätze erstellen, müssen Sie auf der Seite **Einrichtung für eingehende Belege** angeben, welche Erf.-Journalvorlage und welches Erf.-Journal verwendet werden sollen.

Wenn Sie nicht möchten, dass Benutzer Rechnungen oder Fibu Erfassungsjournalzeilen anhand von eingehenden Belegdatensätzen erstellen können, ausser, wenn diese genehmigt sind, müssen Sie Genehmiger auf der Seite **Genehmiger für eingehenden Beleg** einrichten.

Um PDF und Bilddateien in elektronische Belege umzuwandeln, die in Belegdatensätze in Project '[!INCLUDE[d365fin](includes/d365fin_md.md)]' konvertiert werden, müssen Sie die OCR-Funktion einrichten und den Dienst aktivieren.

Wenn die Funktion „Eingehende Belege“ eingerichtet ist, können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren eingehender Belege, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden. Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten. Weitere Informationen finden Sie unter [Eingehende Belege verarbeiten](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>So richten Sie die Funktion „Eingehende Belege“ ein
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Einrichtung für eingehende Belege** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>So richten Sie Genehmiger für eingehende Belege ein
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Einrichtung für eingehende Belege** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie auf der Seite **Einrichtung für eingehende Belege** die Aktion **Genehmiger** aus.

    Auf der Seite **Genehmiger für eingehende Belege** werden alle Benutzer, die in Ihrem Project [!INCLUDE[d365fin](includes/d365fin_md.md)] eingerichtet sind, angezeigt.  
3. Wählen Sie mindestens einen Benutzer aus, der einen eingehenden Beleg genehmigen kann, bevor eine zugehörige Beleg- oder Erf.-Journalzeile erstellt werden kann.

Nachdem Sie Genehmiger auf der Seite **Genehmiger für eingehende Belege** eingerichtet haben, können nur diese Benutzer einen eingehenden Beleg genehmigen, wenn auf der Seite **Einrichtung für eingehende Belege** das Kontrollkästchen **Genehmigung zum Erstellen anfordern** aktiviert ist.

> [!NOTE]  
>   Diese Genehmigungseinrichtung ist nicht mit den Genehmigungsworkflows verknüpft. Weitere Informationen erhalten Sie unter [Genehmigungsworkflow verwenden](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>So richten Sie einen OCR-Service ein
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **OCR Service einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Sie informieren Daten werden verschlüsselt automatisch an.

## <a name="see-also"></a>Siehe auch
[Eingehende Belege verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
