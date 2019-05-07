---
title: Debitoren-Einrichtungswerte sammeln | Microsoft Docs
description: Verwenden Sie den Einrichtungsfragebogen, um Ihre Implementierungsarbeitslast zu verringern, indem Sie die Aufgabe des Einrichtens neuer Mandanten rationalisieren. Sie können den Einrichtungsfragebogen in Business Central erstellen und Ihrem Debitor als Excel (.xls) oder XML-Datei zur Verfügung stellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6df4963c18e12efe4ddad68c6050776b45e7614c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "920812"
---
# <a name="gather-customer-setup-values"></a>Sammeln von Einrichtungswerten für Debitoren
Verwenden Sie den Einrichtungsfragebogen, um Ihre Implementierungsarbeitslast zu verringern, indem Sie die Aufgabe des Einrichtens neuer Mandanten rationalisieren. Sie können den Einrichtungsfragebogen in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen und Ihrem Debitor als Excel (.xls) oder XML-Datei zur Verfügung stellen.  

Sie können alle Vorgabewerte in einem Fragebogen ändern, um sie an die Anforderungen des Debitors anzugleichen.  

> [!TIP]  
>  Weitere Informationen zum Definieren von Einrichtungswerten auf den Beschaffungsplanungsgebieten, siehe [Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md).  

Wenn Ihr Debitor den Fragebogen ausgefüllt hat, importieren Sie die Datei in den neuen Mandanten [!INCLUDE[d365fin](includes/d365fin_md.md)] des Debitors. Sie und Ihr Debitor validieren die Antworten aus dem Fragebogen, bevor Sie ihn für das Unternehmen anwenden.

## <a name="to-create-a-configuration-questionnaire"></a>So erstellen Sie einen benutzerdefinierten Konfigurationsfragebogen
Sie können einen Fragebogen verwenden, um den Umfang und die Anforderungen der Konfiguration zu bestimmen. Sie können eine neue Befragung erstellen oder ändern eine bestehende Befragung ändern, indem Sie auch neue Fragen oder Fragenbereiche hinzufügen.  

 Sie können Fragebögen nur für Setup-Typ-Tabellen erstellen. Beispielsweise können Sie das Werkzeug verwenden, um Informationen auf den folgenden Seiten bereitzustellen:  

-   Unternehmensdaten  
-   Anlageneinrichtung  
-   Finanzbuchhaltung Einrichtung  
-   Lagereinrichtung  
-   Montageeinrichtung
-   Fertigung Einrichtung  
-   Kreditoren und Einkauf Einr.  
-   Marketingeinrichtung  
-   Service Einrichtung  
-   Debitoren und Verkauf Einr.  
-   Logistik Einrichtung  

> [!NOTE]  
>  Um eine vollständige Liste von Tabellen-Einrichtungen zu sehen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion Wie möchten Sie weiter verfahren geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben Sie **Einrichtung** ein und wählen dann den zugehörigen Link aus. Um den Umfang der Migration von Daten zu ermitteln, verwenden Sie Migrationsfunktionen. Weitere Informationen finden Sie unter [Gewusst wie: Debitorendaten zusammenführen](admin-migrate-customer-data.md).  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Frageboen-Konfiguration** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus. Die Seite **Profilbefragung konfigurieren** wird geöffnet.  
3. Wählen Sie die Aktion **Fragenbereiche** aus. Die Seite **Fragenbereiche** wird geöffnet.  
4. Wählen Sie die Aktion **Neu** aus. Die Seite **Fragenbereiche konfigurieren** wird geöffnet.  
5. Wählen Sie im Feld **Tabellen-ID** die ID der Tabelle aus, für die Sie Daten erfassen möchten. Das Feld **Tabellennamen** wird automatisch ausgefüllt.  
6. Wählen Sie die **Fragen aktualisieren** Aktion aus. Jedes Feld in der Tabelle wird der Befragung mit einem Fragezeichen hinter seiner Beschriftung hinzugefügt.

Sie können die Beschriftung neu formulieren, um zu verdeutlichen, wie die Frage beantwortet werden soll. Beispielsweise können Sie ein Feld mit der Bezeichnung "Name" so bearbeiten, dass seine Beschriftung "Wie ist der Name von zu erfassende Daten" <data being collected>  lautet. Sie können aucn eine Anleitung im Feld **Referenz** angeben, einschliesslich einer URL auf einer Seite angeben, die zusätzliche Informationen angibt.  

Bei Bedarf können Sie Fragen auch löschen, die nicht im Fragebogen berücksichtigt werden sollen.  

> [!NOTE]  
>  Das Feld **Antwortoption** beschreibt die Art und das Format der geeigneten Antwortdaten. Das Feld **Antworten** enthält vom Benutzer bereitgestellte Informationen.  
>   
>  Bei Bedarf können Sie im Feld **Antworten** auch Standardantworten definieren. Diese Werte werden standardmässig für benutzerdefinierte Einrichtungen verwendet. Jedoch kann die Person, die den Fragebogen ausfüllt, die Antwort ändern und aktualisieren.  

## <a name="to-complete-the-configuration-questionnaire"></a>Vorgehensweise: Abschliessen des Konfigurationsfragebogens
Verwenden Sie den Einrichtungsfragebogen, um eine detaillierte Erörterung der speziellen Anforderungen des Debitors zu strukturieren und zu dokumentieren. Verwenden Sie sie auch, um Einrichtungsdaten vom Debitoren zu erfassen, um die relevanten [!INCLUDE[d365fin](includes/d365fin_md.md)]-Einrichtungstabellen, wie die Fibuposten, die Lagerbestandsdaten und die Debitoren zu konfigurieren.  

> [!NOTE]  
>  Sie können auch einen eigenen Einrichtungsfragebogen erstellen, der ihre speziellen Bedürfnisse erfüllt.  

1. Wählen Sie im Feld Mandanten den gewünschten Mandanten aus, für dten.en Sie den Fragebogen beenden möchten.
2. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Frageboen-Konfiguration** ein, und wählen dann den zugehörigen Link aus.  
3. Wählen Sie die Befragung für Unternehmen, und wählen die **In Excel exportieren** Aktion, optional die **In XML exportieren** Aktion aus.
4. Lassen Sie den Debitoren den Konfigurationsfragebogen ausfüllen, indem Sie die Antworten in die Excel-Arbeitsmappe eingeben. Es gibt Arbeitsblätter für jeden der Fragenbereiche, die für die Befragung erstellt wurden.   
5. Wählen Sie die **Aus Excel importieren** Aktion aus, und wählen Sie die XLSX-Datei mit die Antworten des Debitors aus.  
6. Klicken Sie auf der Registerkarte Start in der Gruppe Vorgang auf **Fragenbereiche**, um die Validierung und die Anwendung der Antworten auf den Einrichtungsfragebogen zu starten.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>So füllen Sie einen Fragebogen aus dem Konfigurationsarbeitsblatt aus  
Das nächste Verfahren ist eine alternative Möglichkeit für den Zugriff auf Konfigurationsfragebögen. Dabei wird davon ausgegangen, dass das Konfigurationspaket, das Sie bereitgestellt haben, Fragebögen enthält.  

1. Nachdem Sie ein Konfigurationspaket importiert haben, öffnen Sie das Konfigurationsarbeitsblatt.  
2. Für jede Tabelle, für die ein Fragenbereich vorhanden ist, wählen Sie die Aktion **Fragen** aus. Die Fragebogenseite wird geöffnet.  
3. Beantworten Sie die Fragen, und wählen Sie die **Antworten übernehmen** Aktion aus.  
4. Wählen Sie die Schaltfläche **OK**, um den Fragebogen zu schliessen.

## <a name="to-validate-the-configuration-questionnaire"></a>Vorgehensweise: Überprüfen des Konfigurationsfragebogens
Es ist wichtig, dass der Konfigurationsfragebogen geprüft wird, bevor Sie ihn auf das [!INCLUDE[d365fin](includes/d365fin_md.md)]-Format anwenden. Damit prüfen Sie auch, ob die Datenformatierung während des Imports aus Excel beibehalten wurde.  

Ein typischer Validierungsvorgang ist die Prüfung, ob keine Textzeichenfolgen in Datumsfelder eingegeben wurden. Dieser Reviewprozess ist notwendig, da das Format der Antwort im Fragebogen nicht automatisch überprüft wird, wenn die Funktion **Antworten übernehmen** ausgeführt wird.  

> [!NOTE]  
>  Im Allgemeinen ist die Konfiguration des Einrichtungsfragebogens nur ein manueller Prozess. Es gibt jedoch Prüfungen für regionale Formatierungsinkonsistenzen. Darüber hinaus erhalten Sie Fehler, wenn die Struktur Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank nicht der Struktur der Migrationsdatenbank entspricht.  

1. Auf der Seite **Konfigurationsfragebogen** wählen Sie den gewünschten Fragebogen aus, und wählen Sie die **Fragenbereiche** Aktion aus.  
2. Öffnen Sie den relevanten Fragenbereich.  
3. Prüfen Sie für jede Frage, dass der Wert im Feld **Antwort** dem Format entspricht, das im Feld **Antwortoption** bereitgestellt wird. Prüfen Sie etwa, dass die Adresse eines Mandanten im Textformat ist.  
4. Wenn Sie Fehler finden, können Sie Korrekturen in Excel vornehmen; dazu exportieren Sie den Fragebogen und importieren ihn anschliessend wieder. Alternativ können Sie Fehler auch direkt in [!INCLUDE[d365fin](includes/d365fin_md.md)] korrigieren, während Sie die Antworten auf der Seite **Fragenbereich konfigurieren** prüfen.  
5. Wiederholen Sie diese Schritte für jeden Fragenbereich.  

Nachdem Sie Ihre Prüfung abgeschlossen haben, sind die Daten bereit, um zur Datenbank ausgeglichen werden.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Anwenden von Antworten aus dem Konfigurationsfragebogen
Nachdem Sie und Informationen aus einem Konfigurationsfragebogen importiert und validiert haben, können Sie die Einrichtungsdaten übertragen, oder Sie auf die entsprechenden Tabellen in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank anwenden.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Frageboen-Konfiguration** ein, und wählen dann den zugehörigen Link aus. Die Seite **Profilbefragung konfigurieren** wird geöffnet.  
2. Wählen Sie einen Konfigurationsfragebogen aus der Liste und wählen Sie **Liste bearbeiten** aus.  
3. Sie können Antworten auf eine von zwei Arten anwenden.  

- Um den gesamten Fragebogen anzuwenden, wählen Sie auf der Registerkarte Vorgang die Option **Antworten übernehmen**.  
- Um Antworten aus einem bestimmten **Fragenbereich** anzuwenden, aktivieren Sie **Fragebereiche**, wählen Sie einen **Fragenbereich** aus der Liste, und wählen Sie anschliessend auf der Registerkarte Start die Option **Antworten anwenden** aus.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>So überprüfen Sie, ob Antworten erfolgreich angewendet wurden  
1. Prüfen Sie die Einrichtungsseiten für die verschiedenen Funktionsbereiche aus [!INCLUDE[d365fin](includes/d365fin_md.md)]. Um die Seite zu suchen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie den Namen des Einrichtungsfensters ein, und wählen dann den zugehörigen Link aus.  
2. Vergewissern Sie sich, dass die Felder mit den richtigen Daten aus den verschiedenen Fragenbereichen im Konfigurationsfragebogen gefüllt wurden.  

Sie haben nun die Einrichtung mit den Geschäftsinformationen und den Regeln des Debitors konfiguriert.

## <a name="see-also"></a>Siehe auch  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
