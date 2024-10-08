---
title: 'Saldo [CH]'
description: 'In diesem Artikel wird die Nutzung der Seite „Fibukonto Vorläufige Bilanz“ erläutert, um gebuchte Fibuposten anzuzeigen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 11500
ms.date: 12/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="general-ledger-balance-in-the-swiss-version"></a>Fibupostensaldo in der Schweizer Version

Wenn Sie die **Saldo** Aktion auf der Seite **Fibukonten** auswählen, wird die Seite **Fibukonto Vorläufige Bilanz** geöffnet. Es enthält den Saldo der definitiv gebuchten Fibuposten sowie den Saldo der Posten, die im aktuellen Fibu-Erfassungsjournal gebucht wurden.  

Der Saldo des Erfassungsjournals berücksichtigt alle Zeilen vom Anfang des Erfassungsjournals bis einschl. zur aktuellen Zeile.

Beispielsweise können Sie damit nach dem Erfassen der Debitorenzahlungen überprüfen, ob der Banksaldo stimmt.

Sie haben die Wahl zwischen zwei Optionen:

* **Alle Journale**

    Der nicht gebuchte Saldo wird für alle Fibujournale berechnet. Dieser berücksichtigt auch Werte aus Erfassungsjournalen mit anderen Namen, die zum aktuellen Zeitpunkt nicht angezeigt werden.

* **Aktuelles Journal**

    Der ungebuchte Saldo wird nur für das zum aktuellen Zeitpunkt geöffnete Fibu-Erfassungsjournal berechnet.

## <a name="see-also"></a>Siehe auch

[Vorläufige Salden in den Fibu.-Erfassungsjournalen anzeigen](how-to-view-temporary-balances-in-general-ledger-journals.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
