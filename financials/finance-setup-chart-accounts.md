---
title: Einrichten des Kontenplans | Microsoft Docs
description: "Beschreibt, wie Sie den Kontenplan ändern können."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 48202a9e9a763dcb22bed9975aa9c4a39d2dc4ae
ms.contentlocale: de-ch
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Einrichten oder Ändern des Kontenplans
Der Kontenplan zeigt die Sachkonten an, die Ihre Finanzdaten speichern. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.
Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen.  

## <a name="adding-or-changing-accounts"></a>Konten hinzufügen oder ändern
Im Kontenplan können Sie jedes Fibukonto öffnen und Einstellungen hinzufügen oder ändern.

**Hinweis**: Sie können ein Fibukonto löschen. Bevor es gelöscht wird, müssen allerdings folgende Bedingungen erfüllt sein:  

* Der Saldo des Kontos muss Null betragen.  
* Das Feld **Löschen v. Sachkonten zul. vor** im Fenster **Finanzbuchhaltung Einrichtung** muss ausgefüllt sein, und das Konto darf keine Posten an oder nach diesem Datum enthalten.  
* Ist das Feld **Fibukontoverwendung prüfen** im Fenster **Finanzbuchhaltung Einrichtung** ausgewählt, darf dieses Konto nicht in Buchungsgruppen oder der Buchungsmatrix Einrichtung verwendet werden.  

[!INCLUDE[d365fin](includes/d365fin_md.md)]verhindert, dass Sie ein Sachkonto löschen, in dem Daten gespeichert werden, die im Kontenplan erforderlich sind.  

## <a name="see-also"></a>Siehe auch
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Dimensionen](finance-dimensions.md)  
[Aus anderen Finanzsystemen importieren](upload-data.md)  
[So gehts: Arbeiten mit GIFI-Codes in Kanada](ca-finance-work-gifi-codes.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
