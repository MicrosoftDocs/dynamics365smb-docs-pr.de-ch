---
title: Importieren von Bankenclearing-Nummern (Schweiz)
description: Bankenclearingnummern sind eindeutige Nummern zur Kennzeichnung der einzelnen Bankagenturen oder Filialen im Bankenstamm. Diese Informationen sind Voraussetzung für elektronische Zahlung. Die Datei kann auf der Website von SIX Interbank Clearing heruntergeladen werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: fac98b748ef7adfbad06ddeb659dabecca4eed50
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779835"
---
# <a name="import-swiss-bank-clearing-numbers"></a>Importieren von Schweizer Bankenclearingnummern
Bankenclearingnummern sind eindeutige Nummern zur Kennzeichnung der einzelnen Bankagenturen oder Filialen im Bankenstamm. Diese Informationen sind Voraussetzung für elektronische Zahlung. Die Datei kann auf der Website von [SIX Interbank Clearing](https://go.microsoft.com/fwlink/?LinkId=145121) heruntergeladen werden.  

Die BC-Bankstammdatei – die offizielle Schweizer Bankenclearingnummer-Datei – kann importiert werden, um die Bankenclearingnummer-Informationen im Bankenstamm zu aktualisieren. Wenn Sie die Bankenclearingnummer-Datei importieren, werden die Daten in die Tabelle **Bankenstamm** importiert, und die vorhandenen Daten werden überschrieben. Nach dem Importieren der Bankenclearingnummer-Datei können Sie die aktualisierte Bankfilialnummer für Debitoren und Kreditoren definieren. Weitere Informationen finden Sie in den Tabellen "Debitor Bankkonto" und "Kreditor Bankkonto".  

## <a name="to-import-swiss-bank-clearing-numbers"></a>So importieren Sie Bankenclearingnummern für Schweiz  

1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](../../media/ui-search/search_small.png "Tell me-Funktion"), geben Sie **Bankverzeichnis** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Bankverzeichnis importieren** aus.  
3.  Aktivieren Sie auf der Seite **Bankenstamm einlesen** auf dem Inforegister **Optionen** das Feld **Clearingnummern automatisch aktualisieren**, um die Bankenclearingnummern automatisch zu aktualisieren.  
4.  Klicken Sie auf die Schaltfläche **Drucken** oder auf **Seitenansicht**, um die Bankenclearingnummern zu importieren, und suchen Sie anschliessend auf der Seite **Öffnen** die Datei, die Sie von der Website von SIX Interbank Clearing heruntergeladen haben.
5. Wählen Sie die Schaltfläche **Öffnen** aus.  

    Falls Sie die Schaltfläche **Drucken** wählen, werden die Inhalte der Datei gedruckt. Falls Sie auf die Schaltfläche **Seitenansicht** klicken, wird die Tabelle **Bankenstamm** aktualisiert und ein Bericht, dessen Clearingnummern geändert wurden, wird angezeigt.  

Nachfolgend wird beschrieben, wie Bankfilialnummern für Debitorenbankkonten definiert werden. Diese Schritte gelten jedoch auch für die Definition von Bankfilialnummern für Kreditorenbankkonten.  

## <a name="to-define-bank-branch-numbers-for-customer-bank-accounts"></a>So definieren Sie Bankfilialnummern für Debitorenbankkonten  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie den Debitor, für den Sie Bankkontoeninformationen erstellen möchten, und wählen die Aktion **Bankkonten**.  
3.  Auf der Seite **Debitor Bankkontenliste** wählen Sie das gewünschte Bankkonto aus, und wählen Sie die **Bearbeiten** Aktion aus.  
4.  Wählen Sie auf dem Inforegister **Allgemein** im Feld **BLZ** die Nummer der Bankagentur oder -filiale aus.  
5.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
 [Elektronische Zahlungen (Schweiz)](swiss-electronic-payments.md)   
 [Bankkonten einrichten](../../bank-how-setup-bank-accounts.md)
