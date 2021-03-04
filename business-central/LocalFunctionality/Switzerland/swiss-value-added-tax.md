---
title: Mehrwertsteuer (Schweiz)
description: Schweizer Erweiterungen enthalten spezielle Mehrwertsteuerberichterstellungsfunktionen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 67617e389d20e2e57cf13dd5ecb6031341509dca
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753149"
---
# <a name="swiss-value-added-tax"></a>Mehrwertsteuer (Schweiz)
[!INCLUDE[prod_short](../../includes/prod_short.md)] enthält die folgenden Erweiterungen für die Schweizer Mehrwertsteuerberichterstellung:  

- Automatische Regulierung von MWST-Beträgen für Rechnungen entsprechend dem Skonto  
- Zusätzliche MWST-Wechselkurse für Rechnungen in Fremdwährungen  

Weitere Informationen über die Schweizer Mehrwertsteuerberichterstellung und die Codierungsanforderungen finden Sie unter [Schweizer MWST-Informationen](https://www.estv.admin.ch/estv/en/home/estv-suissetax/sw-hersteller.html). Die Information ist für Französisch, Deutsch und Italienisch verfügbar.  

## <a name="vat-amounts-and-vat-exchange-rates"></a>MWST-Beträge und MWST-Wechselkurse  
Entsprechend den lokalen Mehrwertsteuer-Gesetzen kann der MWST Basisbetrag um den Skontobetrag reduziert werden, wenn Skonto gewährt wird. Um automatische Mehrwertsteueranpassungen für ein Skonto einer Rechnung zuzulassen wir das Feld **Skonto berichtigen** standardmässig auf der Seite **Fibuposten Einrichtung** ausgeführt. Sie können diese Funktion in der MWST-Buchungsmatrix-Einrichtung " aktivieren. Weitere Informationen finden Sie in der Tabelle "Fibuposten einrichten" und "MWST-Buchungsmatrix einrichten".  

### <a name="currency-exchange-rates-for-vat-reporting"></a>Währungswechselkurse für die MWST-Abrechnung  
Für Rechnungen in Fremdwährungen muss der offizielle Wechselkurs der Regierung für die MWST-Berechnung verwendet werden. Sie können zusätzliche MWST-Wechselkurse einrichten, die für andere Rechnungsbelange als die MWST-Berechnung verwendet werden können. Der korrekte offizielle MWST-Wechselkurs kann für jede relevante Fremdwährung in der Wechselkurseinrichtung für Rechnungen angegeben werden. Weitere Informationen finden Sie in der Tabelle "Wechselkurse".  

Es ist auch möglich, alle aus Fremdwährungstransaktionen resultierenden MWST-Beträge in MWST-Posten zu regulieren. Wenn Sie die Funktion für die MWST-Wechselkursregulierung aktivieren, werden die MWST-Wechselkurse automatisch reguliert. Die durch Wechselkurse verursachten positiven Differenzen werden auf Kursgewinnkonten gebucht. Die durch Wechselkurse verursachten negativen Differenzen werden auf Kursverlustkonten gebucht. Weitere Informationen finden Sie unter Stapelverarbeitungsauftrag "Wechselkurse regulieren".  

In die MWST-Posten werden weitere Angaben übertragen, z. B. der MWST-Satz und der ursprüngliche Währungsbetrag. Weitere Informationen finden Sie in der MWST-Postentabelle.  

## <a name="see-also"></a>Siehe auch  
 [MWST-Sätze für die Schweiz](vat-rates-for-switzerland.md)   
 [Erstellen und Drucken einer Schweizer MWST-Abrechnung](how-to-create-and-print-a-swiss-vat-statement.md)   
 [Lokale Funktion (Schweiz)](switzerland-local-functionality.md)   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]