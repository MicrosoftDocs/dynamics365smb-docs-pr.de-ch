---
title: Einrichten von Intercompanytransaktionsbuchungen | Microsoft Docs
description: Erstellen Sie Ihre Intercompanykreditoren und -debitoren als so genannte Intercompanypartner, und richten Sie einen Intercompanykontenplan ein.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 12/15/2020
ms.author: edupont
ms.openlocfilehash: 81e19144e309e98c7887f264ac914202690977cc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750144"
---
# <a name="set-up-intercompany"></a>Intercompany einrichten

Wenn Sie eine Transaktion (beispielsweise eine Verkaufs-Erf.-Journalzeile) von einem Unternehmen an ein anderes Unternehmen senden möchten und im Partnerunternehmen automatisch die entsprechende Transaktion (beispielsweise eine Einkaufs-Erf.-Journalzeile) erstellt werden soll, müssen sich die Unternehmen auf einen gemeinsamen Kontenplan sowie auf eine Gruppe von Dimensionen für Intercompanytransaktionen einigen. Bei dem Intercompanykontenplan kann es sich beispielsweise um eine vereinfachte Version des Kontenplans der Muttergesellschaft handeln. In jedem Unternehmen wird der eigene vollständige Kontenplan dem gemeinsam genutzten Intercompanykontenplan zugeordnet, und auch die Dimensionen des jeweiligen Unternehmens werden den Intercompanydimensionen zugeordnet.  

Sie müssen einen Intercompanypartnercode für jedes Partnerunternehmen einrichten, der zwischen allen Unternehmen vereinbart wurde, und diese dann Kreditorenkarten bzw. Debitorkarten zuweisen, indem Sie das Feld **Intercompanypartnercode** ausfüllen.  

Wenn Sie Intercompanyzeilen mit Artikeln erstellen oder erhalten, können Sie entweder eigene Artikelnummern verwenden oder für die betreffenden Artikel jeweils die Artikelnummern des Partners einrichten, indem Sie das **Feld Kred.-Artikelnr.** oder das Feld **Gemeinsame Artikelnr.** auf der Artikelkarte verwenden. Sie können auch die Funktion **Artikelreferenz** verwenden, um die Artikelnummern den Artikelbeschreibungen des Intercompanypartners zuzuordnen. Öffnen Sie die Karte eines jeden Artikels und wählen Sie dann die Aktion **Referenzen** aus, um Referenzen zwischen Ihren Artikelbeschreibungen und denen des Intercompanypartners einzurichten. Weitere Informationen finden Sie unter [Verwenden von Artikelquerverweisen](inventory-how-use-item-cross-refs.md). 

Wenn Sie Intercompany-Verkaufstransaktionen vornehmen, die Ressourcen beinhalten, müssen Sie auf der Ressourcenkarte der entsprechenden Ressourcen das Feld **IC-Partner Eink.-Sachkontonr.** ausfüllen. Das Feld enthält die Nummer des Intercompanyfibukontos im Unternehmen Ihres Partners, auf das die Ressource gebucht wird. Weitere Informationen finden Sie unter [Ressourcen einrichten](projects-how-setup-resources.md).

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Unternehmen für Intercompanytransaktionen einrichten
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Firmeninformationen** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie auf der Seite **Unternehmensdaten** die Felder **Intercompanypartnercode**, **Intercompanyeingangsart** und **Intercompanyeingangsdetails** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>So legen Sie Intercompanypartner fest
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Intercompanypartner** ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie auf der Seite **Intercompanypartner** die Felder nach Bedarf aus.

> [!NOTE]
> In [!INCLUDE[prod_short](includes/prod_short.md)] online können Sie keine Dateispeicherorte verwenden, um Transaktionen an Ihre Partner zu übertragen, da [!INCLUDE[prod_short](includes/prod_short.md)] keinen Zugriff auf Ihr lokales Netzwerk hat. Daher ist bei Auswahl von **Dateispeicherort** im Feld **Transfertyp** das Feld **Ordnerpfad** nicht verfügbar. Stattdessen wird die Datei in den Ordner „Downloads“ auf Ihrem Computer heruntergeladen. Anschliessend senden Sie die Datei per E-Mail an eine Person in der Partnerfirma. Für einen direkteren Prozess empfehlen wir stattdessen die Auswahl von **E-Mail**.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Einrichten von Intercompanykreditoren und Intercompanydebitoren
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Anbieter** ein und wählen Sie dann den entsprechenden Link.
2. Alternativ können Sie auf den Kreditor über das Feld **Kreditorennr.** auf der Seite **Intercompanypartner** zugreifen.
3. Öffnen Sie die Karte für den Kreditor, der ein Intercompanypartner ist. Weitere Informationen finden Sie unter [Neue Kreditoren registrieren](purchasing-how-register-new-vendors.md).
4. Wählen Sie im Feld **Intercompanypartnercode** den relevanten Intercompanypartnercode aus.
5. Wiederholen Sie die Schritte 1 bis 4 für Debitoren.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Einrichten von Intercompanykontenplänen
Damit innerhalb einer Gruppe von Unternehmen Intercompanytransaktionen vorgenommen werden können, müssen sich die Unternehmen auf einen Kontenplan einigen, der allgemein zur Referenz dient. Bei der Erstellung von Intercompanytransaktionen müssen Sie sich mit den Partnerunternehmen auf die zu verwendenden Kontonummern einigen. Die Muttergesellschaft der Gruppe muss beispielsweise eine vereinfachte Version des eigenen Kontenplans erstellen, diesen Intercompanykontenplan aus der Datenbank in eine XML-Datei exportieren und an alle Unternehmen in der Gruppe verteilen.  

Wenn das Unternehmen das übergeordnete Unternehmen ist und über den definierenden Intercompanykontenplan verfügt, der von der Gruppe zur Referenz verwendet wird, folgen Sie den Schritten unter [Einrichten des definierenden Intercompanykontenplans](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts).  

Wenn das Unternehmen ein untergeordnetes Unternehmen ist und Sie eine XML-Datei mit dem gemeinsamen Intercompanykontenplan erhalten, folgen Sie den Verfahren unter [So importieren Sie den Intercompanykontenplan](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Einrichten des definierenden Intercompanykontenplans
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **IC-Kontenplan** ein, und wählen Sie dann den entsprechenden Link aus.
2. Geben Sie auf der Seite **IC-Kontenplan** die einzelnen Konten zeilenweise in das Fenster ein.  
3. Wenn der Intercompanykontenplan dem üblichen unternehmenseigenen Kontenplan gleicht oder ähnelt, können Sie die Werte automatisch in das Fenster eingeben, indem Sie die Aktion **Aus Kontenplan kopieren** wählen. Sie können die neuen Zeilen bei Bedarf bearbeiten.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>So exportieren Sie einen Intercompanykontenplan
Um Ihren Intercompanypartner zu gestatten, den definierenden Kontenplan zu importieren, müssen Sie ihn in eine Datei exportieren.      
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **IC-Kontenplan** ein, und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie auf der Seite **IC-Kontenplan** die **Exportieren**-Aktion aus, und wählen Sie dann die Schaltfläche **Speichern** aus.
3. Geben Sie zum Speichern der XML-Datei einen Namen und einen Verzeichnispfad an, und wählen Sie dann die Schaltfläche **Speichern**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Den Intercompanykontenplan importieren:  
Wenn eine Datei für den definierenden Intercompanykontenplan vorhanden ist, können Intercompanypartner diesen importiern, um sicherzustellen, dass sie dieselben Konten haben.  
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **IC-Kontenplan** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie auf der Seite **IC-Kontenplan** die **Importieren**-Aktion aus.  
3. Wählen Sie den Dateinamen und Verzeichnispfad der XML-Datei aus, und wählen Sie **Öffnen**.  

Die Seite **IC-Kontenplan** wird mit den neuen oder bearbeiteten Fibukontozeilen entsprechend dem Intercompanykontenplan in der Datei ausgefüllt. Jede möglicherweise vorhandene Zeile auf der Seite bleibt unverändert.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Den Intercompanykontenplan dem unternehmenseigenen Kontenplan zuordnen:  
Nachdem Sie den Kontenplan definiert oder importiert haben, auf den Sie sich mit den Intercompanypartnern geeinigt haben, müssen Sie den einzelnen Intercompanyfibukonten unternehmenseigene Fibukonten zuordnen. Auf der Seite **IC-Kontenplan** legen Sie fest, wie IntercompanyFibukonten bei eingehenden Transaktionen in Fibukonten des unternehmenseigenen Kontenplans übersetzt werden.

Wenn die Kontonummern im Intercompanykontenplan mit Kontonummern des unternehmenseigenen Kontenplans übereinstimmen, können diese Konten automatisch einander zugeordnet werden.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **IC-Kontenplan** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie die Zeilen aus, die automatisch zugeordnet werden sollen, und klicken Sie auf die Aktion **Zuordn. zu Kto. m. selb. Nr.**.  
3. Für jedes Intercompanyfibukonto, das nicht automatisch zugeordnet werden kann, füllen Sie das Feld **Zuordnen zu Fibukontonr.** aus.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Vorgegebene IC-Partner-Sachkonten einrichten:  
Bei der Erstellung von Intercompanyverkaufs- oder -einkaufszeilen, die als ausgehende Transaktion gesendet werden sollen, geben Sie ein Konto aus dem Intercompanykontenplan vor, auf das der Betrag im Partnerunternehmen gebucht werden soll. Auf der Seite **Kontenplan** können Konten, die häufig für ausgehende Intercompanyverkaufs- oder -einkaufszeilen verwendet werden, als vorgegebene Intercompanypartner-Fibukonten festgelegt werden. Für Debitorensammelkonten können beispielsweise die zugeordneten Kreditorensammelkonten aus dem Intercompanykontenplan als vorgegebene Konten festgelegt werden.  

Wenn Sie jetzt im Feld **Gegenkontonr.** in einer Intercompanyzeile mit dem Eintrag **Intercompanypartner** im Feld **Kontoart** ein Fibukonto eingeben, wird das Feld **IC-Partner-Fibukonto** automatisch ausgefüllt.  

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.  
2. Geben Sie in der Zeile für ein Fibukonto, das für Intercompanytransaktionen verwendet wird, im Feld **Vorgegebene IC-Partner-Fibukonten** das Intercompanyfibukonto ein, auf das Ihr Partner buchen soll, wenn Sie auf das Fibukonto in der Zeile buchen.  
3. Wiederholen Sie Schritt 2 für jedes Konto, das Sie häufig im Feld **Gegenkontonr.** einer Zeile in einem Intercompany-Erf.-Journal oder -Beleg eingeben.

## <a name="to-set-up-intercompany-dimensions"></a>So richten Sie Intercompanydimensionen ein

Wenn Transaktionen mit entsprechend verknüpften Dimensionen zwischen dem Unternehmen und den Intercompanypartern übertragen werden sollen, müssen Sie die Dimensionen vereinbaren, die von allen verwendet werden. Die Muttergesellschaft der Gruppe erstellt beispielsweise eine vereinfachte Version des eigenen Dimensionssatzes, exportiert diese Intercompanydimensionen in eine XML-Datei und verteilt diese an alle Unternehmen der Gruppe. Anschliessend wird die XML-Datei von allen Tochtergesellschaften auf der Seite **Intercompanydimensionen** importiert, und die Intercompanydimensionen werden den Dimensionen im eigenen Fenster **Dimensionen** zugeordnet.  

> [!NOTE]
> Jedes Unternehmen in [!INCLUDE [prod_short](includes/prod_short.md)] muss Intercompany-Dimensionen für ausgehende Belege und Intercompany-Dimensionen für eingehende Belege den eigenen Dimensionen zuordnen. Diese Zuordnung trägt dazu bei, die Konsistenz zwischen den Unternehmen sicherzustellen. Weitere Informationen finden Sie im Abschnitt [So ordnen Sie konzerninterne Dimensionen den Dimensionen Ihres Unternehmens zu](#to-map-intercompany-dimensions-to-your-companys-dimensions).

Wenn das Unternehmen die Muttergesellschaft ist und den IC-Dimensionssatz definiert, der von der Gruppe zur Referenz verwendet wird, verwenden Sie die Schrittfolge unter [Definieren von Intercompanydimensionen](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Wenn das Unternehmen eine Tochtergesellschaft ist und Sie eine XML-Datei mit den IC-Dimensionen erhalten, die von der Gruppe zur Referenz verwendet werden, verwenden Sie die Schrittfolge unter [Importieren von Intercompanydimensionen](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### <a name="to-define-the-intercompany-dimensions"></a>Definieren von Intercompanydimensionen
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Intercompany-Dimensionen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie die Dimensionen zeilenweise auf der Seite **Intercompanydimensionen** ein.

    Wenn die Intercompanydimensionen den unternehmenseigenen Dimensionen gleichen oder ähneln, können Sie die Seite automatisch ausfüllen, indem Sie die Funktion **Aus Dimensionen kopieren** benutzen. Anschliessend können Sie die ausgefüllten Zeilen bearbeiten.  
3. Die Intercompanydimensionen können mit der Aktion **Exportieren** in eine XML-Datei exportiert und auf diese Weise an die Partnerunternehmen verteilt werden.  
4. Geben Sie zum Speichern der XML-Datei einen Namen und einen Verzeichnispfad an, und wählen Sie dann die Schaltfläche **Speichern**.  

### <a name="to-import-the-intercompany-dimensions"></a>Importieren der Intercompanydimensionen  
Wenn eine Datei für die definierenden Intercompanydimensionen vorhanden ist, können Intercompanypartner diesen importiern, um sicherzustellen, dass sie dieselben Dimensionen haben.  
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Intercompany-Dimensionen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie auf der Seite **Intercompany-Dimensionen** die **Importieren**-Aktion aus.  
3. Legen Sie den Dateinamen und Verzeichnispfad der XML-Datei fest, und wählen Sie **Öffnen**.  

Die Zeilen auf der Seite **Intercompanydimensionen** und **Intercompanydimensionendimensionswerte** werden importiert.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Intercompanydimensionen Ihren unternehmenseigenen Dimensionen zuordnen:
Nachdem Sie alle Dimensionen definiert oder importiert haben, die von den Intercompanypartnern laut Übereinkunft verwendet werden, müssen die einzelnen Intercompanydimensionen den unternehmenseigenen Dimensionen zugeordnet werden und umgekehrt. Auf der Seite **Intercompanydimensionen** geben Sie an, wie die Intercompanydimensionen *eingehender Transaktionen* in die unternehmenseigenen Dimensionen aus der Dimensionsliste übersetzt werden. Auf der Seite **Dimension** legen Sie fest, wie die unternehmenseigenen Dimensionen bei *Ausgehenden Transaktionen* in Intercompanydimensionen übersetzt werden.

Wenn Intercompanydimensionen bezüglich ihres Codes mit unternehmenseigenen Dimensionen aus der Dimensionsliste übereinstimmen, können diese Dimensionen durch die Anwendung automatisch einander zugeordnet werden, und anschliessend ordnen Sie die Konten automatisch zu:  

In den folgenden Schritten ordnen Sie zunächst konzerninterne Dimensionen Dimensionen für eingehende Belege auf der Seite **Intercompany-Dimensionen** zu. Anschliessend ordnen Sie Dimensionen Intercompany-Dimensionen für ausgehende Belege auf der Seite **Dimensionen** zu.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Intercompany-Dimensionen** ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie auf der Seite **Intercompanydimensionen** die automatisch zuzuweisenden Zeilen aus, und klicken Sie anschliessend auf die Aktion **Zuordn. zu Dim. m. selb. Code** aus.
3. Füllen Sie für jede Intercompany-Dimensionen, die nicht automatisch zugeordnet wird, das Feld **Zuordnen zu Dimensionscode** aus.

    Möglicherweise müssen Sie Ihrer Ansicht das Feld hinzufügen. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).
4. Wählen Sie die Aktion **Intercompanydimensionswerte** aus.
5. Füllen Sie auf der Seite **Intercompanydimensionswerte** das Feld **Zuordnen zu Dimensionswertcode** aus.

    Fahren Sie mit dem Zuordnen der Intercompanydimensionen fort, indem Sie ähnliche Schritte ausführen.
6. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Dimensionen** ein und wählen Sie dann den entsprechenden Link.
7. Wählen Sie auf der Seite **Intercompanydimensionen** die automatisch zuzuweisenden Zeilen aus, und klicken Sie anschliessend auf die Aktion **Zuordn. zu Dim. m. selb. Code**.
8. Füllen Sie für jede Intercompany-Dimensionen, die nicht automatisch zugeordnet wird, das Feld **Zuordn. zu IC-Dimens.wertcode** aus.
9. Wählen Sie die Aktion **Intercompanydimensionswerte** aus.
10. Füllen Sie auf der Seite **Intercompanydimensionswerte** das Feld **Zuordnen zu IC-Dimensionswertcode** aus.

## <a name="see-also"></a>Siehe auch

[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]