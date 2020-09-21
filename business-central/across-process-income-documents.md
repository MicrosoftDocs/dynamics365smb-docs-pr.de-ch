---
title: Verarbeiten von eingehenden Belegen| Microsoft Docs
description: Um einen externen Beleg, wie beispielsweise eine PDF, in Business Central aufzuzeichnen, müssen Sie zuerst einen eingehenden Belegdatensatz erstellen oder fertig stellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 9e6ce88485fcceeba9b35d8a309e9c7d73b40dae
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778898"
---
# <a name="processing-incoming-documents"></a>Eingehende Belege verarbeiten
Um einen externen Beleg in [!INCLUDE[d365fin](includes/d365fin_md.md)] aufzuzeichnen, müssen Sie zuerst einen Datensatz des eingehenden Belegs anlegen oder ausfüllen. Dies kann manuell erfolgen, oder Sie können ein Foto des externen Belegs machen und einen Datensatz für einen eingehenden Beleg mit der angehängten Bilddatei erstellen.

Mithilfe eines externen OCR-Dienstes (optische Zeichenerkennung) können Sie aus PDF- oder Bilddateien, die Sie von Ihren Handelspartnern erhalten, elektronische Belege erstellen, die Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] in Belegdatensätze konvertieren können. Wenn Sie beispielsweise eine Rechnung in PDF-Format von Ihrem Kreditor erhalten, können Sie diese über die Seiter **Eingehende Belege** zum OCR-Dienst senden. Alternativ können Sie die Datei per E-Mail an den OCR-Dienst senden. Wenn Sie dann den elektronischen Beleg zurückerhalten, wird automatisch ein damit zusammenhängener Datensatz zum eingehenden Beleg erstellt. Nach einigen Sekunden erhalten Sie die Datei vom OCR-Dienst als elektronische Rechnung zurück, die zu einer Einkaufsrechnung für den Kreditor umgewandelt werden kann.

| Aktion | Informationen |
| --- | --- |
| Erstellen Sie eingehende Belegdatensätze manuell oder automatisch, indem Sie zum Beispiel ein Foto eines Papierbelegs erstellen. |[Erstellen von eingehenden Belegen](across-how-create-income-document-records.md) |
| Verwenden Sie einen OCR-Dienst, um PDF und Bilddateien zu elektronische Belege umzuwandeln, die beispielsweise zu Einkaufsrechnungen im [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertiert werden können. Schulen Sie den OCR-Dienst, Fehler zu vermeiden,wenn er das nächste Mal ähnliche Daten verarbeitet. |[Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln](across-how-use-ocr-pdf-images-files.md) |
| Verbinden oder entfernen Sie einen eingehenden Beleg mit einem beliebigem nicht gebuchten Verkaufs- oder Einkaufsbeleg, sowie mit jedem Debitor-, Kreditor- oder Fibuposten in dem Beleg oder Posten. |[Erstellen und Verknüpfen von eingehenden Belegen aus Belegen und Posten](across-how-connect-disconnect-income-document-records.md) |
| Auf der Seiten **Kontenplan** und **Fibuposten** können Sie eine Suchfunktion verwenden, um Fibuposten für gebuchte Belege zu finden, für die keine eingehende Belegdatensätze vorhanden sind, und dann zentral eine Verknüpfung zu vorhandenen Datensätzen herstellen oder neue mit angefügten Belegdateien erstellen. |[So finden Sie gebuchte Belege ohne zugehörige eingehende Belege](across-how-find-posted-documents-without-income-document-records.md) |
| Verschaffen Sie sich einen besseren Überblick, indem Sie eingehende Belegdatensätze auf "Verarbeitet" festlegen, um sie aus der Standardansicht zu entfernen. |[Mehrere eingehende Belegdatensätze verwalten](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Siehe auch
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
