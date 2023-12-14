---
title: Tabelleninformationen anzeigen
description: 'Erfahren Sie, wie Sie Informationen über Datenbanktabellen in Business Central anzeigen können.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 10/11/2023
ms.author: jswymer
---

# <a name="viewing-table-information"></a>Tabelleninformationen anzeigen

Auf der Seite **8700 Tabelleninformationen** erhalten Sie Informationen über die Anzahl der Datensätze in allen System- und Geschäftstabellen in [!INCLUDE[prod_short](includes/prod_short.md)], und wie viele Daten jede Tabelle enthält.

Diese Informationen sind hilfreich bei der Behebung von Leistungsproblemen, da Sie die Verteilung der Datengrösse auf Tabellen anzeigen können.

## <a name="view-table-information"></a>Tabelleninformationen anzeigen

Um diese Seite zu öffnen, wählen Sie das ![Suche nach Seite oder Bericht.](media/ui-search/search_small.png "Symbol 'Nach Seite oder Bericht suchen'") Symbol. Geben Sie **Tabelleninformationen** ein und wählen Sie dann den entsprechenden Link.

In der folgenden Tabelle werden die für jede Tabelle bereitgestellten Informationen beschrieben:

|Spalte|Beschreibung|
|------|-----------|
|Unternehmensname|Name des Unternehmens (sofern zutreffend), zu dem die Tabelle gehört.|
|Tabellenname|Der Name der Tabelle.|
|Tabellennr.|Die ID der Tabelle.|
|Anz. der Datensätze|Die Gesamtzahl der in der Tabelle gespeicherten Datensätze.|
|Datensatzgrösse|Die durchschnittliche Datensatzgrösse in KB/Datensatz. Der Wert wird nach folgender Formel berechnet: 1024 (Grösse)/(Anzahl der Datensätze). |
|Grösse (KB)|Wie viel Platz ingesamt die Tabelle in der Datenbank belegt. Dieser Wert stammt aus der Summe der Werte in den Feldern Datengrösse und Indexgrösse.|
|Datengrösse (KB)|Wie viel Platz die Daten in der Tabelle in der Datenbank belegen.|
|Indexgrösse (KB)|Wie viel Platz die Tabellenindizes (Schlüssel) in der Datenbank belegen.|
|Komprimierung|Die Art der Komprimierung, **Zeile**, **Seite** oder **Keine**, die auf die Tabelle in der Datenbank angewendet wird. Weitere Informationen finden Sie unter [Datenkomprimierung](/sql/relational-databases/data-compression/data-compression?).|

> [!NOTE]
> Wenn Sie Daten in einer Tabelle löschen, startet [!INCLUDE[prod_short](includes/prod_short.md)] mehrere Prozesse im Hintergrund, um sicherzustellen, dass alles in Ihrer Datenbank bereinigt wird. Die Werte auf der Seite Tabelleninformationen werden erst aktualisiert, wenn diese Prozesse abgeschlossen sind, was eine Weile dauern kann. Die Wartezeit kann je nach Grösse Ihrer Datenbank variieren.

> [!IMPORTANT]  
> Auf der Seite **Tabelleninformationen** werden Daten- und Indexgrössen angezeigt. Die Summe der Tabellengrössen stimmt jedoch nicht mit der verwendeten Gesamtkapazität überein, da hier die Datengrösse und nicht die tatsächlich zugewiesene Grösse angezeigt wird. Der zugewiesene Speicherplatz ist immer grösser als der genutzte Speicherplatz, um zu vermeiden, dass bei jeder Einfügung Speicherplatz zugewiesen werden muss, was die Leistung erheblich einschränken würde


## <a name="see-also"></a>Siehe auch

[Überprüfen von Seiten](across-inspect-page.md)  
[Artikel zur Leistung für Entwickler](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
