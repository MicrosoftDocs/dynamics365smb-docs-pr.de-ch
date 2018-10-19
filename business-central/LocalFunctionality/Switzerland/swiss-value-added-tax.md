---
title: Mehrwertsteuer (Schweiz)
description: Schweizer Erweiterungen enthalten spezielle Mehrwertsteuerberichterstellungsfunktionen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 66ac3a70ee4f40ab1b4c86afcc8ad28357c7a543
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="swiss-value-added-tax"></a>Mehrwertsteuer (Schweiz)
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] enthält die folgenden Erweiterungen für die Schweizer Mehrwertsteuerberichterstellung:  

- Automatische Regulierung von MWST-Beträgen für Rechnungen entsprechend dem Rabatt  
- Zusätzliche MWST-Wechselkurse für Rechnungen in Fremdwährungen  

Weitere Informationen über die Schweizer Mehrwertsteuerberichterstellung und die Codierungsanforderungen finden Sie unter [Schweizer MWST-Informationen](https://www.estv.admin.ch/estv/en/home.html). Die Information ist für Französisch, Deutsch und Italienisch verfügbar.  

## <a name="vat-amounts-and-vat-exchange-rates"></a>MWST-Beträge und MWST-Wechselkurse  
Entsprechend den lokalen Mehrwertsteuer-Gesetzen kann der MWST Basisbetrag um den Skontobetrag reduziert werden, wenn Skonto gewährt wird. Um automatische Mehrwertsteueranpassungen für einen Zahlungsrabatt einer Rechnung zuzulassen wir das Feld **Skonto berichtigen** standardmässig im Fenster **Fibuposten Einrichtung** ausgeführt. Sie können diese Funktion in der MWST-Buchungsmatrix-Einrichtung " aktivieren. Weitere Informationen finden Sie in der Tabelle "Fibuposten einrichten" und "MWST-Buchungsmatrix einrichten".  

### <a name="currency-exchange-rates-for-vat-reporting"></a>Währungswechselkurse für die MWST-Abrechnung  
Für Rechnungen in Fremdwährungen muss der offizielle Wechselkurs der Regierung für die MWST-Berechnung verwendet werden. Sie können zusätzliche MWST-Wechselkurse einrichten, die für andere Rechnungsbelange als die MWST-Berechnung verwendet werden können. Der korrekte offizielle MWST-Wechselkurs kann für jede relevante Fremdwährung in der Wechselkurseinrichtung für Rechnungen angegeben werden. Weitere Informationen finden Sie in der Tabelle "Wechselkurse".  

Es ist auch möglich, alle aus Fremdwährungstransaktionen resultierenden MWST-Beträge in MWST-Posten zu regulieren. Wenn Sie die Funktion für die MWST-Wechselkursregulierung aktivieren, werden die MWST-Wechselkurse automatisch reguliert. Die durch Wechselkurse verursachten positiven Differenzen werden auf Kursgewinnkonten gebucht. Die durch Wechselkurse verursachten negativen Differenzen werden auf Kursverlustkonten gebucht. Weitere Informationen finden Sie unter Stapelverarbeitungsauftrag "Wechselkurse regulieren".  

In die MWST-Posten werden weitere Angaben übertragen, z. B. der MWST-Satz und der ursprüngliche Währungsbetrag. Weitere Informationen finden Sie in der MWST-Postentabelle.  

## <a name="see-also"></a>Siehe auch  
 [MWST-Sätze für die Schweiz](vat-rates-for-switzerland.md)   
 [Erstellen und Drucken einer Schweizer MWST-Abrechnung](how-to-create-and-print-a-swiss-vat-statement.md)   
 [Lokale Funktion (Schweiz)](switzerland-local-functionality.md)   

