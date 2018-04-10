---
title: Kundendatenmigration vorbereiten | Microsoft Docs
description: "Nachdem Sie die Einrichtungsdaten in die neue Datenbank importiert und dort angewendet haben, können Sie mit dem Migrieren der vorhandenen Stammdaten des Debitors beginnen, beispielsweise Artikel- und Debitorennummern sowie Namen. Um sicherzustellen, dass diese Daten schnell und genau im neuen Mandanten erstellt werden, sollten Sie Vorlagen verwenden, um die Daten zu strukturieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 260f9c87f3c824e2eeced45fb4943784a03cb641
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="prepare-to-migrate-customer-data"></a>Vorgehensweise: Migrieren von Debitorendaten
Nachdem Sie die Einrichtungsdaten in die neue Datenbank importiert und dort angewendet haben, können Sie mit dem Migrieren der vorhandenen Stammdaten des Debitors beginnen, beispielsweise Artikel- und Debitorennummern sowie Namen. Um sicherzustellen, dass diese Daten schnell und genau im neuen Mandanten erstellt werden, sollten Sie Vorlagen verwenden, um die Daten zu strukturieren.  

Normalerweise erstellen Sie Datenvorlagen für die folgenden Stammdatentabellen:  

-   **Kontakte**  
-   **Debitor**  
-   **Artikel**  
-   **Kreditor**  

Sie können jedoch eine Vorlagenstruktur erstellen und diese auf jede beliebige Tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)] anwenden.  

> [!TIP]  
>  Sie können auch Datenvorlagen für tägliche Arbeitsgänge verwenden, um neue Datensätze zu erstellen, die auf Vorlagen basieren. Diese Datenvorlagen funktionieren nur für die unterstützten Stammdatentabellen. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).  

Wenn Sie Debitorendaten aus einer Datei importieren, z. B. für Artikel, werden die Daten, die Sie angegeben haben, aus der verknüpften Datenvorlage entnommen. Wenn Sie einen neuen Artikel erstellen, geben Sie nur allgemeine Informationen wie Artikelname, Beschreibung und Preis ein und erfassen dann die restlichen Pflichtfelddaten aus einer ausgewählten Datenvorlage.  

Wenn Sie einen neuen Masterdatensatzes wie eine Debitorenkarte erstellen, sind einige Felder zwingend und müssen ausgefüllt werden. Sie können die meisten Pflichtfelder wie Buchungsgruppen und Zahlungsbedingungen gruppieren, damit die Erstellung von Masterdatensätzeb einfacher und stabiler ist,. Beispielsweise können Sie Pflichtfelder für Tabelle 18, **Debitor**, unter der Art **Inland**, **Ausland** oder **Exportieren** gruppieren.

## <a name="to-select-a-data-template"></a>So wählen Sie eine Datenvorlage aus
Wenn Sie eine vorhandene Datenvorlage auswählen, müssen Sie bewerten, ob die Vorlagen, die für den neuen Mandanten erstellt wurden, für den Debitoren ausreichen. Sehen Sie sich die bereitgestellten Felder und Werte an, um zu ermitteln, welche Vorlagen sich für ein neues Unternehmen eignen.  

> [!TIP]  
>  Datenvorlagen ermöglichen jedoch auch das schnelle Erstellen neuer Datensätze. Verwenden Sie diese für eine schnellere und genauere Erstellung von Daten. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Vorlage konfiguriern** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Im Fenster **Config. Vorlagen-Liste** wählen Sie aus der Liste eine Datenvorlage, und wählen die **Bearbeiten** Aktion aus.  

Wenn die Standardvorlagen nicht Ihren Anforderungen entsprechen, können Sie neue Vorlagen erstellen oder einer vorhandenen Vorlage Felder hinzufügen. Wenn die Standardvorlagen ausreichen, können Sie sie zum Erstellen von Datensätzen verwenden, die auf Stammdatenvorlagen basieren.

## <a name="to-create-a-data-template"></a>Erstellen Sie eine Datenvorlage
Sie können eine neue Datendatensatzvorlage erstellen, wenn die Standardvorlagen nicht den Anforderungen des neuen Mandanten entsprechen. Wenn Sie mehr als eine Vorlage erstellen, ist es nützlich, für das Feld **Code** eine Benennungskonvention zu verwenden.

Jede Vorlage besteht aus einem Kopf und aus Zeilen. Wenn Sie eine Vorlage erstellen, können Sie angeben, welche Felder immer Daten eines bestimmten Typs anwenden sollen. Beispielsweise können Sie Vorlagen eines anderen Debitors erstellen, um auf Arten eines anderen Debitors angewendet wird. Wenn Sie den Debitor mithilfe einer Vorlage erstellen, können Sie die Daten der Vorlage verwenden, um bestimmte Felder vorab auszufüllen.

### <a name="to-create-a-data-template-header"></a>So erstellen Sie einen Datenvorlagenkopf
1. Öffnen Sie das Fenster **Vorlagenliste**.
2. Wählen Sie die Aktion **Neu** aus.
3. Geben Sie im Feld **Tabellen-ID** die Tabelle ein, zu der diese Vorlage gehört. Das Feld wird nach der Eingabe im Feld **Tabellenname** automatisch ausgefüllt, wenn das Feld **Tabellen-Id** festgelegt ist.

### <a name="to-create-a-data-template-line"></a>So erstellen Sie einen Datenvorlagenzeile:
1. Wählen Sie in der ersten Zeile im Feld den **Feldnamen** aus. Das Fenster **Felderliste** zeigt die Liste der Felder in der Tabelle an.
2. Wählen Sie ein Feld aus, und wählen Sie dann die Schaltfläche **OK**. Das Feld **Felderfassun g** wird mit dem Feldnamen ausgefüllt.
3. Geben Sie im Feld **Standardwert** einen geeigneten Wert ein. In einigen Fällen möchten Sie möglicherweise einen Wert verwenden, der nicht einem in der Datenbank vorhandenen Wert entspricht. In diesem Fall können Sie das Kontrollkästchen **Relationenprüfung überspringen** aktivieren, um zu ermöglichen, Daten ohne Fehler zu verwenden.

    > [!TIP]  
    > Da das Feld **Standardwert** keinen Lookup zu den entsprechenden [!INCLUDE[d365fin](includes/d365fin_md.md)]-Feldoptionen hat, kopieren Sie den gewünschten Wert von der entsprechenden Seite in die Vorlage.

    > Aktivieren Sie das Kontrollkästchen ‌**Zwingend**. Das Kontrollkästchen dient nur zur Information. Es gibt an, dass der Benutzer Informationen in das Feld eingeben muss, es wird jedoch keine Geschäftslogik erzwungen. So können Sie beispielsweise einen Auftrag erst fakturieren und buchen, wenn Buchungsgruppen eingerichtet wurden. Da Buchungsgruppen erforderlich sind, können Sie das Kontrollkästchen **Notwendig** für diese Felder markieren.

3. Geben Sie im Feld **Referenz** nach Bedarf Informationen zu dem Feld ein.
4. Wählen Sie die Schaltfläche **OK**.

## <a name="to-export-to-a-template-in-excel"></a>Exportieren einer Vorlage in Excel
Sie können schnell eine Excel-Arbeitsmappe erstellen, die als Vorlage dient und auf der Struktur einer vorhandenen Datenbanktabelle basiert. Sie können die Vorlage dann verwenden, um Debitorendaten in einem konsistenten Format für den späteren Import in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu erfassen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurations-Arbeitsblatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Fügen Sie der Liste eine Tabelle hinzu, oder wählen Sie eine vorhandene Tabelle aus. Weitere Informationen finden Sie unter [Verwalten von Mandanten-Konfiguration in einem Arbeitsblatt](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Definieren Sie die Felder aus der Tabelle, die in der Vorlage enthalten sein sollen.
4. Wählen Sie die Aktion **Vorlageninhalt exportieren** aus.
5. Benennen und speichern Sie die .xlsx-Datei. Die Excel-Arbeitsmappe wird automatisch geöffnet.

Sie können jetzt in die Excel-Arbeitsmappe Kundendaten eingeben. Wenn Sie mehrere Tabellen exportiert haben, befindet sich jede Tabelle in einem eigenen Arbeitsblatt. Speichern Sie die Arbeitsmappe, bevor Sie mit der folgenden Vorgehensweise fortfahren.

> [!NOTE]  
> Wenn Sie eine englischsprachige Version von Excel nutzen, Ihre regionalen Einstellungen aber für eine andere Sprache konfiguriert haben, kann der folgende Fehler auftreten: "Old format or invalid type library." Um diesen Fehler zu beheben, prüfen Sie, ob das Language Pack für die andere Sprache installiert ist.

## <a name="to-import-from-a-template-in-excel"></a>So importieren Sie aus einer Vorlage in Excel
1. Im Fenster **Config. Arbeitsblatt** wählen Sie die **Aus Vorlage importieren** Aktion aus.
3. Navigieren Sie zum Vorlagenvorschlag, den Sie erstellt haben, und wählen Sie die Aktion **Öffnen**.
4. Um der gesammelten Debitorendaten der Datenbank hinzuzufügen, wählen Sie die **Daten übernehmen** Aktion.

Wenn Sie Daten aus einer Vorlage in Excel auf eine Tabelle anwenden, der auch im Konfigurationspaket eine Konfigurationstabelle zugeordnet ist, werden auch die Standardfeldwerte aus der Konfigurationstabelle angewendet.

Jeder Datensatz, dessen Daten auf diese Weise angewendet werden, ist vollständig, da er aus den Daten besteht, die von einem Benutzer in Excel eingegeben werden, plus der Standardwerte, die die Konfigurationsvorlage angibt.

## <a name="to-create-a-record-from-a-configuration-template"></a>So erstellen Sie einen Datensatz aus einer Konfigurationsvorlage
Sie können die Struktur der Daten verwenden, die in den Datenvorlagen enthalten ist, um Ihre Informationen nacheinander in Datensätze in der Datenbank umzuwandeln. Verwenden Sie zu diesem Zweck die Funktion **Instanz erstellen**. Dies ist eine abgespeckte Version des Datenmigrationsprozesses und kann für das Erstellen von Prototypen oder für kleinere Aufgaben der Datenerstellung hilfreich sein.  

Die folgenden Schritte veranschaulichen, wie eine Artikelkarte aus einer Artikeldatenvorlage erstellt wird. Mit demselben Verfahren können Sie einen Datensatz aus jeder beliebigen Datenvorlage erstellen.  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Vorlage konfiguriern** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende **Element**-Vorlage und wählen Sie dann die Aktion **Bearbeiten** aus. Weitere Informationen zum Erstellen einer Vorlage finden Sie unter Vorgehensweise: Eine Datenvorlage erstellen.
3. Wählen Sie die Aktion **Instanz erstellen** aus. Eine Artikelkarte wird erstellt.  
4. Wählen Sie die Schaltfläche **OK** aus.  
5. Um das neue Kartenelement zu überprüfen, wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
6. Öffnen Sie eine neue Artikelkarte.  
7. Erweitern Sie verschiedene Inforegister und vergewissern Sie sich, dass die Informationen korrekt in ihnen erstellt wurden.  

## <a name="to-use-a-configuration-template-on-a-record"></a>So verwenden Sie eine Konfigurationsdatenvorlage bei einem Datensatz
Sie können eine Datenvorlage bei jedem beliebigen Datensatz anwenden, der in [!INCLUDE[d365fin](includes/d365fin_md.md)] vorhanden ist, und diese Methode verwenden, um einen Datensatz zu ändern oder zu bearbeiten. Hierbei werden jedoch vorhandene Werte im Datensatz mit denen der Vorlage überschrieben. Deshalb sollten Sie behutsam vorgehen, wenn Sie eine Vorlage bei vorhandenen Datensätzen anwenden.

> [!WARNING]  
>  Die **Vorlage anwenden**-Funktion überschreibt vorhandene Daten in einem Datensatz. Wenn diese Funktion bei der Stammdatenmigration verwendet wird, überschreibt sie die importierten Daten, wenn Sie Datensätze erstellen.

Das folgende Verfahren basiert auf einer Debitorenkarte.  

1. einen Kunden erstellen. Weitere Informationen finden Sie unter [Neue Kunden registrieren](sales-how-register-new-customers.md).
2. Im Fenster **Debitorenkarte** wählen Sie die Aktion **Vorlage anwenden** aus.  
3. Im Fenster **Debitorenvorlagen** wählen Sie eine der Vorlagen aus, und wählen Sie dann die Schaltfläche **OK** aus.  

Die Standardwerte aus der ausgewählten Debitorenvorlage werden in die Debitorenkarte eingefügt.

## <a name="see-also"></a>Siehe auch  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)  
[Registriert einen neuen Debitor.](sales-how-register-new-customers.md)
