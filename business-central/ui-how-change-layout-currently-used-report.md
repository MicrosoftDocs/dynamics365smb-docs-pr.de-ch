---
title: Ändern Sie die Art, wie Berichte dargestellt werden, indem Sie ein anderes Layout auswählen| Microsoft Docs
description: Sie können unterschiedliche Layouts für einen Bericht auswählen und zwischen Layouts wechseln, um das Aussehen des Berichts zu ändern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 07de4be7bc516cf9f4b802a48dc59293b1992f5f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315266"
---
# <a name="change-the-current-report-layout"></a>Ändern Sie das aktuelle Berichtslayout
Ein Bericht kann mit mehreren Berichtlayouts eingerichtet werden, die bei Bedarf ausgewechselt werden können.

Abhängig von den Layouts, die für einen Bericht verfügbar sind, können Sie ein integriertes RDLC-Berichtlayout, ein integriertes Word-Berichtlayout oder ein kundenspezifisches Layout verwenden. Weitere Informationen zu RDLC- und Word-Berichtlayouts, integrierten und benutzerdefinierten Layouts und mehr finden Sie unter [Verwalten von Berichtslayouts](ui-manage-report-layouts.md).

> [!TIP]  
> Belegberichte (keine Listen), die ein Word-Berichtslayout verwenden, sind normalerweise schneller als diejenigen, die ein RDLC-Berichtslayout verwenden. Wenn Sie also die Option haben, zwischen einem Word- oder einem RDLC-Berichtslayout für einen Belegbericht zu wählen, verwenden Sie das Word-Berichtslayout für optimale Leistung.  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Um das Layout ändern, das in einem Bericht verwendet wird
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Berichtslayout-Auswahl** ein, und wählen dann den zugehörigen Link aus.  
   Auf der Seite sind alle Berichte aufgelistet, die für das Unternehmen verfügbar sind, das auf der Seite **Bericht-Layout-Auswahl** oben verfügbar ist. Das ausgewählte Layout-Feld gibt das Layout an, das momentan in dem Bericht verwendet wird.
2. Legen Sie das Feld **Unternehmen** oben auf der Seite auf das Unternehmen fest, das den Bericht umfasst.
3. Um das Layout, das von einem Bericht verwendet wird, zu ändern, wählen Sie die Zeile für den Bericht aus der Liste, und legen Sie dann das Feld **Ausgewähltes Layout** auf eine der folgenden Optionen fest:
   * RDLC (integriert) verwendet im Bericht das integrierte RDLC-Berichtlayout.
   * Word (integriert) verwendet im Bericht das integrierte Word-Berichtlayout.
   * Benutzerdefiniert, verwendet ein kundenspezifisches Layout im Bericht.  

Sie können sehen, welche benutzerdefinierten Layouts für den Bericht im **Teil Berichtslayout** verfügbar sind. Falls es keine benutzerdefinierten Layouts für den Bericht gibt, müssen Sie zunächst welche erstellen. Wenn Sie diese Option auswählen, gehen Sie zum folgenden Verfahren, um das benutzerdefinierte Layout anzugeben, die Sie verwenden möchten.

> [!NOTE]
> Wenn Sie **RDLC (integriert)** oder **Word (integriert)** auswählen und Sie eine Fehlermeldung erhalten, dass der Bericht kein Layout der angegebenen Art hat, müssen Sie eine andere Darstellungsoption auswählen oder ein kundenspezifisches Berichtlayout der Art erstellen, die Sie verwenden möchten.

Wenn Sie ein inztegriertes RDLC- oder Word-Berichtslayout ausgewählt haben, ist keine weitere Aktionen erforderlich, und das Layout wird verwendet, wenn der Bericht zum nächsten Mal ausgeführt wird.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Um ein kundenspezifisches Layout in einem Bericht festzulegen
1. Sie bestimmen, welches benutzerdefinierte Layout im Bericht aus der Seite **Debitorenspezifischen Berichtlayout**-verwendet werden soll. Wenn die Seite **Debitorenspezifisches Layout** nicht offen ist, dann wählen Sie im Feld **Berichtlayout-Beschreibung** die Suchschaltfläche aus.
2. Wählen Sie auf der Seite **Debitorenspezifisches Layout** die Zeile für das benutzerdefinierte Layout, das Sie verwenden möchten, und schliessen Sie dann die Seite.

Sie kehren zur Seite **Berichtslayout-Auswahl** zurück. Der Name des ausgewählten benutzerdefinierten Layouts wird im Feld **Benutzerdefinierte Beschreibung** angezeigt. Das benutzerdefinierte Layout wird das nächste Mal verwendet, wenn Sie den Bericht ausführen.

## <a name="see-also"></a>Siehe auch
[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
