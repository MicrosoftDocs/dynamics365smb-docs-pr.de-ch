---
title: Buchungsdatum bei der Eingabe von Anpassungswerten im Vergleich zur Quelleingabe
description: 'Informieren Sie sich über das Szenario „Buchungsdatum der Korrekturwerteingabe im Vergleich zum Buchungsdatum der Eingabe, die die Korrektur verursacht, wie z.B. Neubewertung oder Artikelzu-/abschläge“, wenn Sie den Batchauftrag Lagerreg. fakt. ein-/abschlagen ausführen.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---

# <a name="posting-date-on-adjustment-value-entry-compared-to-the-source-entry"></a><a name="posting-date-on-adjustment-value-entry-compared-to-the-source-entry"></a>Buchungsdatum bei der Eingabe von Anpassungswerten im Vergleich zur Quelleingabe

Dieser Artikel vergleicht das Buchungsdatum auf dem Anpassungswert-Eintrag mit dem Buchungsdatum auf dem Eintrag, der die Ausführung des Batchauftrags Lagerreg. fakt. fakt. Artikel Zu-/Abschläge verursacht, insbesondere ein Szenario mit Aufwertung und ein Szenario mit Artikelzu-/abschlägen.

Der Batchauftrag **Kostenreg. fakt. Einst. Preise anpassen** verarbeitet Ihre Daten je nach Szenario und Konfiguration von [!INCLUDE[prod_short](includes/prod_short.md)]. In diesem Abschnitt beschreiben wir zwei separate Prozesse und zeigen für jeden die Art der Auswirkung, die der Batchauftrag Lagerreg. fakt. Einst. Preise auf die Daten hat.

## <a name="revaluation-scenario"></a><a name="revaluation-scenario"></a>Szenario Neubewertung

### <a name="prerequisites"></a><a name="prerequisites"></a>Voraussetzungen

Bitte geben Sie die folgenden Werte ein:

**Lagerbestandseinrichtung**:  

- Automatische Lagerbuchung = Ja  

- Automatische Lagerregulierung = Immer  

- Durchschnittliche Kalkulation kalkuliert. Typ = Element  

- Durchschnittskostenperiode= Tag  

**Fibuposten Einrichtung**:  

- Zulassen Buchung von = am 1. Januar 2021  

- Buchungen zugel. bis = Leer  

**Benutzer Einrichtung**:  

- Zulassen Buchung von = 1. Dezember 2020  

- Buchungen zugel. bis = Leer  

### <a name="to-test-the-scenario"></a><a name="to-test-the-scenario"></a>So führen Sie ein Testszenario aus

Testen Sie dieses Szenario, indem Sie die folgenden Schritte ausführen.

1. Erstellen Sie ein **Element** namens TEST mit den folgenden Werten:  

     - Basiseinheit = PCS  

     - Kostenberechnungsmethode = Durchschnitt  

     - Wählen Sie Buchungsgruppen optional aus.  

2. Öffnen Sie ein **Element Journal**, erstellen Sie dann eine neue Erfassung und buchen Sie eine Zeile wie folgt:  

     - Buchungsdatum = 15. Dezember 2020  

     - Artikel = TEST  

     - Eink.-Posten ausgleichen = Einkauf  

     - Menge = 100  

     - Stückpreis = 10  

3. Öffnen Sie ein **Element Journal**, erstellen Sie dann eine neue Erfassung und buchen Sie eine Zeile wie folgt:  

     - Datum = 20. Dezember 2020  

     - Artikel = TEST  

     - Eingangsart = Negative Anpassung  

     - Menge = 2  

4. Öffnen Sie ein **Element Journal**, erstellen Sie dann eine neue Erfassung und buchen Sie eine Zeile wie folgt:  

     - Datum = 15. Januar 2021  

     - Artikel = TEST  

     - Eingangsart = Negative Anpassung  

     - Menge = 3  

5. Öffnen Sie ein **Element Neubewertungs Erf.-Journal**, erstellen Sie eine neue Buchung und buchen Sie eine Zeile wie folgt:  

     - Artikel = TEST  

     - Auf Eintrag anwenden = Einkaufsposten auswählen, der unter Schritt 2 gebucht wurde. Das Buchungsdatum der Neubewertung ist derselbe, wie der Posten, der angepasst wird.  

     - Einheitskosten (aufgewertet) = 40  

Die folgenden **Artikelposten** und **Wertposten** wurden gebucht:  

**Lagerposten – Einkauf**:  

|Postennummer  |Artikelnr.  |Buch. Datum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |2020-12-15         |Einkauf         |T00001         |100         |4000         |95        |

**Wertposten**  

|Postennummer  |Artikelnr.  |Buch. Datum  |Lagerposten Laufnr.  |Lagerpostenart  |Postenart   |Belegnummer  |Postenmenge der Artikelnummer  |Einstandsbetrag (tatsächl.)  |Gebuchte Lagerregulierung an G/L  |Ausgleich  |Ausgleich mit Lfd. Nr.  |Buchungsspurcode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   2020-12-15    |317         |Einkauf         |EK-Preis         |T00001         |100         |1 000,00          |1 000,00    |Nein         |0         |ITEMNL         |
|379     |TEST   |**2020-12-15**    |317         |Einkauf         |Neubewertung         |T04002         |0         |3 000,00         |3 000,00         |Nein         |0         |REVALINL         |

**Lagerposten – Abgang, Schritt 3**  

|Laufnr.  |Artikelnr.  |Buch. Datum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |2020-12-20   |Abgang  |T00002         |-2         |-80         | 0        |

**Wertposten**  

|Postennummer  |Artikelnr.  |Buch. Datum  |Lagerposten Laufnr.  |Lagerpostenart  |Postenart   |Belegnummer  |Postenmenge der Artikelnummer  |Einstandsbetrag (tatsächl.)  |Gebuchte Lagerregulierung an G/L  |Ausgleich  |Ausgleich mit Lfd. Nr.  |Buchungsspurcode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   2020-12-20    |318         |Abgang         |EK-Preis         |T00002         |-2         |-20          |-20    |Nein         |0         |ITEMNL         |
|380     |TEST   |**2021-01-01**    |318         |Abgang         |EK-Preis         |T04002         |0         |-60         |-60         |Ja         |377         |INVTADAMT         |

**Lagerposten – Abgang, Schritt 4**  

|Laufnr.  |Artikelnr.  |Buch. Datum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |2021-01-15   |Abgang  |T00003         |-3         |-120         | 0        |

**Wertposten**  

|Postennummer  |Artikelnr.  |Buch. Datum  |Lagerposten Laufnr.  |Lagerpostenart  |Postenart   |Belegnummer  |Postenmenge der Artikelnummer  |Einstandsbetrag (tatsächl.)  |Gebuchte Lagerregulierung an G/L  |Ausgleich  |Ausgleich mit Lfd. Nr.  |Buchungsspurcode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   2021-01-15    |319         |Abgang         |EK-Preis         |T00003         |-3         |-30          |-30    |Nein         |0         |ITEMNL         |
|381     |TEST   |**2021-01-15**    |319         |Abgang         |EK-Preis         |T04003         |0         |-90         |-90         |Ja         |378         |INVTADAMT         |

Der Batchauftrag **Kostenreg. fakt. Einst. Preise anpassen** hat eine Kostenänderung erkannt und die Negativen Anpassungen angepasst.  

**Überprüfung Buchungsdatum des erstellten Ausgleichs-Wertposten:** Der früheste zugelassene Buchungszeitraum, den die Stapelverarbeitung Lagerreg verknüpft, ist am 1. Januar 2021, wie in der Fibuposten Einrichtung festgelegt.  

**Negative Anpassung in Schritt 3:** zugewiesenes Buchungsdatum ist am 1. Januar, wie von in der Fibuposten-Einrichtung festgelegt. Das Buchungsdatum des Werteintrags im Anpassungsumfang ist der 20. Dezember 2020. Gemäss der Finanzbuchhaltungs-Einrichtung liegt das Datum nicht im zulässigen Buchungsdatumsbereich. Daher werden die Buchungsdaten, die im Feld Buchungen zulassen in der Fibuposteneinrichtung festgelegt sind, den Ausgleichs-Wertposten zugeordnet.  

**Abgang in Schritt 4:** weist Buchungsdatum 15. Januar auf. Der Wertposten im Bereich des Ausgleichs hat Buchungsdatum am 15. Januar, das innerhalb des Bereichs des zugelassenen Buchungszeitraums entsprechend der Fibuposten-Einrichtung ist.  

Der Ausgleich, der für den Abgang in Schritt 3 geändert wird, verursacht Diskussionen. Das bevorzugte Buchungsdatum für den Ausgleichs-Wertposten wäre am 20. Dezember oder mindestens im Dezember während die Neubewertung eine Änderung im Lagerverbrauch verursacht, der im Dezember gebucht wurde.  

Um die Anpassung der Negativen Anpassung in Schritt 3 im Dezember zu erreichen, muss in der Finanzbuchhaltungs-Einrichtung im Feld Buchungen zugel. ab ein Datum im Dezember angegeben werden.  

### <a name="conclusion"></a><a name="conclusion"></a>Fazit

Mit den in diesem Szenario gewonnenen Erfahrungen sollten Sie bei der Überlegung, welche Einrichtung für einen zulässigen Buchungsdatumsbereich für eine Firma am besten geeignet ist, Folgendes in Betracht ziehen. Solange Sie zulassen, dass Änderungen des Bestandswertes in einer Periode gebucht werden, wie in diesem Fall im Dezember, sollte die Einrichtung, die die Firma für zulässige Buchungsdatumsbereiche verwendet, mit dieser Entscheidung übereinstimmen. Buchung von zulassen in der Fibuposten-Einrichtung, in diesem Fall der 1. Dezember, würde die Neubewertung ermöglichen, die im Dezember erfolgte und an betroffene ausgehenden Posten in derselben Periode weitergeleitet werden.  

Die Benutzergruppen, die nicht erlaubt sind, um im Dezember gebucht zu werden, sondern im Januar, sind wahrscheinlich durch die Fibuposteneinrichtung in diesem Szenario beschränkt und sollten stattdessen über die Benutzereinrichtung adressiert werden.  

## <a name="item-charge-scenario"></a><a name="item-charge-scenario"></a>Szenario Artikel Zu-/Abschläge

### <a name="prerequisites-1"></a><a name="prerequisites-1"></a>Voraussetzungen

Bitte geben Sie die folgenden Werte ein:

**Lagerbestandseinrichtung**:  

- Automatische Lagerbuchung = Ja  

- Automatische Lagerregulierung = Immer  

- Durchschnittliche Kalkulation kalkuliert. Typ = Element  

- Durchschnittskostenperiode= Tag  

**Fibuposten Einrichtung**:  

- Zulassen Buchung von = 1. Dezember 2020.  

- Buchungen zugel. bis = Leer  

**Benutzer Einrichtung**:  

- Zulassen Buchung von = 1. Dezember 2020.  

- Anlagenbuchungen zugel. bis = Leer  

### <a name="to-test-the-scenario-1"></a><a name="to-test-the-scenario-1"></a>So führen Sie ein Testszenario aus

Testen Sie dieses Szenario, indem Sie die folgenden Schritte ausführen:

1.  Erstellen Sie einen **Element** Belastung mit den folgenden Werten:  

     - Basiseinheit = PCS  

     - Kostenberechnungsmethode = Durchschnitt  

     - Wählen Sie Buchungsgruppen optional aus.  

2.  Erstellen Sie eine neue **Bestellung** mit den folgenden Werten:  

     - Kreditorennr.: 10000  

     - Buchungsdatum = 15. Dezember 2020

     - Kred.-Rechnungsnr.: 1234  

     Wählen Sie in der Zeile Bestellung die folgenden Werte aus:  

     - Artikel = ABSCHLAG  

     - Menge = 1  

     - Direkte Einheitskosten = 100  

     Um den Schritt abzuschliessen, buchen Sie den Beleg als eingegangen und in Rechnung gestellt.  

3.  Erstellen Sie einen neuen **Verkaufsauftrag** mit den folgenden Werten:  

     - Auftraggeber Nr.: 10000  

     - Buchungsdatum = 16. Dezember 2020  

     In der Zeile Verkaufsauftrag:  

     - Artikel = ABSCHLAG  

     - Menge = 1  

     - VK-Preis = 135  

     Um den Schritt abzuschliessen, buchen Sie den Beleg als eingegangen und in Rechnung gestellt.  

4.  Geben Sie Werte für die Seite **Fibuposten Einrichtung** ein:  

     - Zulassen Buchung von = am 1. Januar 2021  

    -  Anlagenbuchungen zugel. bis = leer  

5.  Erstellen Sie eine neue **Bestellung** mit den folgenden Werten:  

     - Kreditorennr.: 10000  

     - Buchungsdatum = 2. Januar 2021  

     - Kred.-Rechnungsnr.: 2345  

     In der Zeile Bestellung:  

     - Artikelkosten = FRACHT  

     - Menge = 1  

     - Direkte Einheitskosten = 3  

     - Weisen Sie die Artikel Zu-/Abschläge dem Kauf-Eingang aus Schritt 2 zu.  

     Um den Schritt abzuschliessen, buchen Sie den Beleg als eingegangen und in Rechnung gestellt.  


**Status Lagerposten des Einkaufsschritts 2**:  
  
|Postennummer  |Artikelnr.  |Buch. Datum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |ABSCHLAG         |2020-12-15         |Einkauf         |107030         |1         |105         |0        |

**Wertposten**  

|Postennummer |Artikelnr.  |Buch. Datum  |Lagerposten Laufnr.  |Lagerpostenart  |Postenart   |Belegnummer  | Artikel Zu-/Abschlagsnr.    |  Lagerpostenmenge   |Einstandsbetrag (tatsächl.)     |Gebuchte Lagerregulierung an G/L |Ausgleich |Ausgleich mit Laufnr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |ABSCHLAG|   2020-12-15    |324         |Einkauf         |EK-Preis         |108029         |         |1          |100    |100         |NEIN         |0         |
|399      |ABSCHLAG   |2021-01-02    |324         |Einkauf         |EK-Preis         |108009         |FRACHT         |0         |3         |3         |NEIN         |0         |

**Status Lagerposten Verkauf**:  
  
|Laufnr.  |Artikelnr.  |Buch. Datum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |ABSCHLAG         |2020-12-16         |Verkauf         |102035         |-1         |-105         |0        |

**Wertposten**  

|Postennummer |Artikelnr.  |Buch. Datum  |Lagerposten Laufnr.  |Lagerpostenart  |Postenart   |Belegnummer  | Artikel Zu-/Abschlagsnr.    |  Lagerpostenmenge   |Einstandsbetrag (tatsächl.)     |Gebuchte Lagerregulierung an G/L |Ausgleich |Ausgleich mit Laufnr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |ABSCHLAG|   2020-12-16    |325         |Verkauf         |EK-Preis         |109024         |         |-1          |-100    |-100         |NEIN         |0         |
|400      |ABSCHLAG   |2021-01-01    |325         |Verkauf         |EK-Preis         |109024         |         |0         |-3         |-3         |Ja         |398         |

6.  Am Arbeitstag, dem 3. Januar, trifft eine Einkaufsrechnung ein, die einen zusätzlichen Artikel Zu-/Abschlag zu dem in Schritt 2 getätigten Kauf enthält. Diese Rechnung hat das Belegdatum 30. Dezember und wird daher mit dem Buchungsdatum 30. Dezember 2020 gebucht.  

     Erstellen Sie eine neue **Bestellung** mit den folgenden Werten:  

     - Kreditorennr.: 10000  

     - Buchungsdatum = 30. Dezember 2020  

     - Kred.-Rechnungsnr.: 3456  

     Wählen Sie in der Zeile Bestellung die folgenden Werte aus:  

     - Artikelkosten = FRACHT  

     - Menge = 1  

     - Direkte Einheitskosten = 2  

     Artikel Zu-/Abschläge dem Kaufbeleg aus Schritt 2 zuordnen  

     Um den Schritt abzuschliessen, buchen Sie den Beleg als eingegangen und in Rechnung gestellt.  


**Status Lagerposten des Einkaufs**:  

|Postennummer  |Artikelnr.  |Buch. Datum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |ABSCHLAG         |2020-12-15         |Einkauf         |107030         |1         |105         |0        |

**Wertposten**  

|Laufnr. |Artikelnr.  |Buch. Datum  |Lagerposten Laufnr.  |Lagerpostenart  |Postenart   |Belegnummer  | Artikel Zu-/Abschlagsnr.    |  Lagerpostenmenge   |Einstandsbetrag (tatsächl.)     |Gebuchte Lagerregulierung an G/L |Ausgleich |Ausgleich mit Laufnr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |ABSCHLAG   |2020-12-15    |324         |Einkauf         |EK-Preis         |108029         |            |1         |100    |100         |Nein         |0         |
|399      |ABSCHLAG   |2021-01-02    |324         |Einkauf         |EK-Preis         |108030         |FRACHT   |0         |3         |3         |Nein         |0         |
|401      |ABSCHLAG   |**2020-12-30**    |324         |Einkauf         |EK-Preis         |108031         |FRACHT   |0         |2         |2         |Nein         |0         |

**Status Lagerposten Verkauf**:  
  
|Postennummer  |Artikelnr.  |Buch. Datum  |Postenart   |Belegnummer  |Menge  |Einstandsbetrag (tatsächl.)  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |ABSCHLAG         |2020-12-16         |Verkauf         |102035         |-1         |-105         |0        |

**Wertposten**  

|Laufnr. |Artikelnr.  |Buch. Datum  |Lagerposten Laufnr.  |Lagerpostenart  |Postenart   |Belegnummer  | Artikel Zu-/Abschlagsnr.    |  Lagerpostenmenge   |Einstandsbetrag (tatsächl.)     |Gebuchte Lagerregulierung an G/L |Ausgleich |Ausgleich mit Laufnr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |ABSCHLAG   |2020-12-16        |325         |Verkauf         |EK-Preis         |103024         |            |-1         |-100       |-100         |Nein         |0         |
|400      |ABSCHLAG   |2021-01-01        |325         |Verkauf         |EK-Preis         |103024         |            |0          |-3         |-3         |Ja         |398         |
|402      |ABSCHLAG   |**2021-01-01**    |325         |Verkauf         |EK-Preis         |103024         |            |0          |-2         |-2         |Ja         |398         |

Lager-Bewertungsbericht wird mit 31. Dezember 2020 gedruckt

![Inhalt des Bestandsbewertungsberichts.](media/helene/TechArticleAdjustcost13.png "Inhalt des Berichts zur Inventarbewertung")

**Zusammenfassung des Szenarios:**  

Das oben beschriebene Szenario endet mit einem Lager-Bewertungsbericht und zeigt Menge = 0 an, während der Wert = 2 beträgt. Der Artikelzuschlag, der in Schritt 6 gebucht wird, ist ein Teil des Lagerzugangswerts vom Dezember, wohingegen der Lagerabgang derselben Periode nicht berücksichtigt wird.  

Der Fibuposten-Einrichtung angeben, Buchungen ab dem 1. Januar zuzulassen, war für den ersten Artikel-Zu/Abschlag gut. Die Kosten des Lagerzugangs und des Feldes Abgang wurden in derselben Periode erfasst. Für den zweiten Artikel-Zu-/Abschlag verursachte die Fibuposteneinrichtung jedoch die Änderung im Lagerverbrauch, der in der Periode danach erkannt wurde.  

**Schlussfolgerung:**  

Es ist eine Herausforderung, den Bestandsbewertungsbericht dazu zu bringen, Menge = 0 zu zeigen, während der Wert <> 0 ist. In diesem Fall ist es auch schwieriger, die optimalen Einstellungen auszudrücken, wenn die Einkaufsrechnungen am selben Tag eintreffen, aber unterschiedliche Zeiträume oder sogar Geschäftsjahre betreffen. Der Übergang zu einem neuen Geschäftsjahr erfordert in der Regel eine gewisse Planung, und dazu gehört auch die Einsicht in den Prozess Lagerreg. fakt. Einst. Preise, der die COGS erkennt.  

In diesem Szenario könnte eine Option sein, die Fibuposten so einzurichten, dass das Feld Buchung zulassen von ein Datum im Dezember für einige Tage mehr definiert und die Buchung des Zuschlages des ersten Artikelpostens zurückgestellt wird, um die Kosten für die vorherige Periode/das vorherige Finanzjahr für die Periode zu ermöglichen, um alle Kosten dort zuzuweisen, wo sie zuerst erkannt wurden und dann die erlaubten Buchungsdaten in die neue Periode des \/ Steuerjahrs zu übertragen. Die Kosten des ersten Artikelpostens mit Buchungsdatum am 2. Januar dann gebucht werden.  

## <a name="see-also"></a><a name="see-also"></a>Weitere Informationen

[Designdetails: Buchungsdatum auf Ausgleichs-Wertposten](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)  
[Designdetails: Artikelausgleich](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
