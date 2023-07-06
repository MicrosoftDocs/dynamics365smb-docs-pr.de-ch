---
title: 'Importieren von Schweizer Bankenclearingnummern [CH]'
description: 'In diesem Artikel wird erläutert, wie Sie Schweizer Bank-Clearing-Nummern in der Schweizer Version von Business Central importieren.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 11501
ms.date: 06/21/2021
ms.author: edupont
---
# <a name="import-swiss-bank-clearing-numbers-in-the-swiss-version"></a><a name="import-swiss-bank-clearing-numbers-in-the-swiss-version"></a><a name="import-swiss-bank-clearing-numbers-in-the-swiss-version"></a>Schweizer Bank-Clearing-Nummern importieren in der Schweizer Version

Bankenclearingnummern sind eindeutige Nummern zur Kennzeichnung der einzelnen Bankagenturen oder Filialen im Bankenstamm. Diese Informationen sind Voraussetzung für elektronische Zahlung. Die Datei kann auf der Website von [SIX Interbank Clearing](https://go.microsoft.com/fwlink/?LinkId=145121) heruntergeladen werden.  

Die BC-Bankstammdatei (TXT) – die offizielle Schweizer Bankenclearingnummer-Datei – kann importiert werden, um die Bankenclearingnummer-Informationen im Bankenstamm zu aktualisieren. Wenn Sie die Bankenclearingnummer-Datei importieren, werden die Daten in die Tabelle **Bankenstamm** importiert, und die vorhandenen Daten werden überschrieben. Nach dem Importieren der Bankenclearingnummer-Datei können Sie die aktualisierte Bankfilialnummer für Debitoren und Kreditoren definieren. Weitere Informationen finden Sie in den Tabellen "Debitor Bankkonto" und "Kreditor Bankkonto".  

## <a name="to-import-swiss-bank-clearing-numbers"></a><a name="to-import-swiss-bank-clearing-numbers"></a><a name="to-import-swiss-bank-clearing-numbers"></a>So importieren Sie Bankenclearingnummern für Schweiz

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **Bankverzeichnis** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Bankverzeichnis importieren** aus.  
3. Wählen Sie die Schaltfläche **...**, um die TXT-Datei mit der Bankenclearingnummer zu öffnen.
4. Aktivieren Sie auf der Seite **Bankenstamm einlesen** auf dem Inforegister **Optionen** das Feld **Clearingnummern automatisch aktualisieren**, um die Bankenclearingnummern automatisch zu aktualisieren.  
5. Klicken Sie auf die Schaltfläche **Drucken** oder auf **Seitenansicht**, um die Bankenclearingnummern zu importieren, und suchen Sie anschliessend auf der Seite **Öffnen** die Datei, die Sie von der Website von SIX Interbank Clearing heruntergeladen haben.
6. Wählen Sie die Schaltfläche **Öffnen** aus.  

   Falls Sie die Schaltfläche **Drucken** wählen, werden die Inhalte der Datei gedruckt. Falls Sie auf die Schaltfläche **Seitenansicht** klicken, wird die Tabelle **Bankenstamm** aktualisiert und ein Bericht, dessen Clearingnummern geändert wurden, wird angezeigt.  

Im folgenden Verfahren wird beschrieben, wie Sie Bankfilialnummern für Debitorenbankkonten definieren. Dieselben Schritte gelten auch für die Definition von Bankfilialnummern für Debitorenbankkonten.  

## <a name="to-define-bank-branch-numbers-for-customer-bank-accounts"></a><a name="to-define-bank-branch-numbers-for-customer-bank-accounts"></a><a name="to-define-bank-branch-numbers-for-customer-bank-accounts"></a>So definieren Sie Bankfilialnummern für Debitorenbankkonten

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Tell me-Funktion") Geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie den Debitor, für den Sie Bankkontoeninformationen erstellen möchten, und wählen die Aktion **Bankkonten**.  
3. Auf der Seite **Debitor Bankkontenliste** wählen Sie das gewünschte Bankkonto aus, und wählen Sie die **Bearbeiten** Aktion aus.  
4. Wählen Sie auf dem Inforegister **Allgemein** im Feld **BLZ** die Nummer der Bankagentur oder -filiale aus.  
5. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Elektronische Zahlungen (Schweiz)](swiss-electronic-payments.md)  
[Bankkonten einrichten](../../bank-how-setup-bank-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
