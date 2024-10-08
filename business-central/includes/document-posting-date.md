---
author: brentholtorf
ms.topic: include
ms.date: 11/14/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

Die Felder **Belegdatum** und **Buchungsdatum** in Verkaufs- und Einkaufsbelegen helfen Ihnen dabei, Buchhaltungsstandards einzuhalten und genaue Finanzberechnungen zu erhalten. Die Felder dienen unterschiedlichen Zwecken:

- Dass [!INCLUDE [prod_short](prod_short.md)] die Finanzierungskosten und den auf Verkaufsrechnungen fälligen Betrag korrekt berechnet, muss das **Belegdatum** mit einem der folgenden Daten übereinstimmen:

   - Das Datum auf der Verkaufsrechnung, die Sie an den Kunden gesendet haben. 
   - Das Datum auf der Kaufrechnung, die Sie von Ihrem Lieferanten erhalten haben.
- Das **Buchungsdatum** zeigt an, wann ein Beleg in [!INCLUDE [prod_short](prod_short.md)] registriert wurde. Viele Rechnungslegungsstandards und -vorschriften verlangen von Unternehmen, Finanztransaktionen basierend auf dem Datum, an dem sie stattgefunden haben, aufzuzeichnen und zu melden.

Abhängig von Ihren Geschäftsprozessen können diese Daten identisch sein oder auch nicht. Wenn sie gleich sind, können Sie [!INCLUDE [prod_short](prod_short.md)] einrichten, um das Belegdatum auf Verkaufs- und Einkaufsbelegen mit dem Datum zu aktualisieren, an dem Sie sie gebucht haben.  
  
Um Belegdaten automatisch auf Buchungsdaten festzulegen, aktivieren Sie auf den Seiten **Debitoren & Verkauf Einr.** und **Kreditoren & Einkauf Einr.** den Schalter **Belegdatum mit Buchungsdatum verknüpfen**.

> [!NOTE]
> Die Einstellung wirkt sich nicht auf Verkaufs- oder Einkaufsjournale aus.