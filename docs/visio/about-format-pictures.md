---
title: Informationen zu Formatierungsangaben
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251831
localization_priority: Normal
ms.assetid: df4c1c70-8b41-c046-7415-643188af0e06
description: Eine Formatierungsangabe ist ein Formatcode, der bestimmt, wie ein Wert angezeigt wird. Sie können beispielsweise die Anzahl von Stellen bestimmen, die rechts oder links von einem Dezimaltrennzeichen angezeigt werden, oder Sie legen fest, ob eine Zeichenfolge in Klein- oder Großschreibung angezeigt wird.
ms.openlocfilehash: 7043c9819f41ec2c08345c84010328be75677918
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344555"
---
# <a name="about-format-pictures"></a>Informationen zu Formatierungsangaben

Eine Formatierungsangabe ist ein Formatcode, der bestimmt, wie ein Wert angezeigt wird. Sie können beispielsweise die Anzahl von Stellen bestimmen, die rechts oder links von einem Dezimaltrennzeichen angezeigt werden, oder Sie legen fest, ob eine Zeichenfolge in Klein- oder Großschreibung angezeigt wird.
  
> [!NOTE]
> Um Formatierungsangaben für Datum und Uhrzeit mit den Funktionen von Microsoft Office System zu definieren, schließen Sie die Formatierungsangaben in doppelte geschweifte Klammern ein, z. B. "{{m/t/jj}}". Wenn Sie ein vordefiniertes Format verwenden, beispielsweise 201, legen Sie es in geschweifte Klammern und Spitze Klammern wie folgt ein: "{\<201\>}". 
  
In den folgenden Abschnitten werden Symbole angezeigt, mit denen Sie verschiedene Typen von Werten für die Anzeige formatieren können.
  
## <a name="string-and-numeric-values"></a>Zeichenfolgen und numerische Werte

|**Zeichen**|**Beschreibung**|
|:-----|:-----|
|#  <br/> |Platzhalter für Ziffer. Zeigt entweder eine Ziffer oder keinen Wert an. Vorangestellte und nachfolgende Nullen werden nicht angezeigt. Befinden sich links vom Dezimaltrennzeichen mehr Ziffern als Platzhalter, werden alle Ziffern angezeigt. Befinden sich rechts vom Dezimaltrennzeichen mehr Ziffern als Platzhalter, wird der Bruchteil auf die Anzahl der Platzhalter gerundet. Bei Abmessungen werden Untereinheiten mit dem Wert 0 nicht angezeigt, wenn der Platzhalter die äußerste linke Ziffer ist.  <br/> Beispielsweise wird FORMAT(0Fuß 11.25Zoll,"#.##u") als 11,25 Zoll angezeigt.  <br/> |
|0  <br/> |Platzhalter für eine Ziffer (Null). Zeigt entweder eine Ziffer oder keinen Wert an. Vorangestellte und nachfolgende Nullen werden angezeigt. Befinden sich links vom Dezimaltrennzeichen mehr Ziffern als Platzhalter, werden alle Ziffern angezeigt. Befinden sich rechts vom Dezimaltrennzeichen mehr Ziffern als Platzhalter, wird der Bruchteil auf die Anzahl der Platzhalter gerundet. Bei Abmessungen werden Untereinheiten mit dem Wert 0 angezeigt.  <br/> Beispielsweise wird FORMAT(2Fuß 11.33Zoll,"0.## u") als 2 Fuß 11,33 Zoll angezeigt.  <br/> |
|.  <br/> |Platzhalter für Dezimalstellen. Legt die Anzahl von Ziffern fest, die links und rechts vom Dezimaltrennzeichen angezeigt werden. Bei einer mehrteiligen Einheit wird das Dezimaltrennzeichen in der kleinsten (äußersten rechten) Untereinheit verwendet. Zeigt das Dezimaltrennzeichen an, das in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das betreffende System definiert ist.<br/> Beispielsweise wird FORMAT(250 cm,"0.000 u") als 250,000 cm angezeigt.  <br/> |
|,  <br/> |Tausendertrennzeichen. Wenn das Trennzeichen von Platzhaltern für Ziffern umgeben (# oder 0) wird, trennt dieses Tausender von Hunderten innerhalb eines numerischen Werts, der aus vier oder mehr Ziffern links vom Dezimaltrennzeichen besteht. Zeigt das Tausendertrennzeichen an, das in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das betreffende System definiert ist.<br/> |
|E- E+ e- e+  <br/> |Wissenschaftliches Format. Wenn das Format wenigstens einen Platzhalter für Ziffern rechts von diesem Symbol enthält, wird die Zahl im wissenschaftlichen Format angezeigt. Fügen Sie das E oder e zwischen der Zahl und ihrem Exponenten ein. Bei E+ oder e+ wird das Zeichen + vor einem positiven Exponenten und das Zeichen - vor einem negativen Exponenten angezeigt. Bei E- oder e- wird das Minuszeichen (-) nur bei einem negativen Exponenten angezeigt.  <br/> Beispielsweise wird FORMAT(12345.67,"###.#e+#") als 123,5e+2 angezeigt.  <br/> |
|u oder U  <br/> |Platzhalter für Kurzbezeichnung. Fügt eine abgekürzte Einheitenbezeichnung nach jeder Untereinheit ein. Beispiel: Zoll, Fuß, Grad. Der Platzhalter U fügt groß Schreibungs Beschriftungen ein, während der u-Platzhalter Kleinbuchstaben einfügt. Fügt die gleiche Anzahl von Leerzeichen vor der Bezeichnung wie vor dem Platzhalter ein.  <br/> Beispielsweise wird FORMAT(12 c 13 d,"#u") als 13c1 angezeigt.  <br/> |
|uu oder UU  <br/> |Platzhalter für Langbezeichnungen. Fügt nach jeder Untereinheit Einheitenbezeichnungen ein. Beispiel: inch, feet, Grad der U-Platzhalter fügt gemischte Groß-/Kleinschreibung-Beschriftungen ein, während der u-Platzhalter kleine Beschriftungen einfügt. Fügt die gleiche Anzahl von Leerzeichen vor der Bezeichnung wie vor dem Platzhalter ein.  <br/> Beispielsweise wird FORMAT(12.43Zoll,"# #/4 UU") als 12 2/4 ZOLL angezeigt.  <br/> |
|uuu oder UUU  <br/> |Universeller Platzhalter für Bezeichnungen. Fügt nach jeder Untereinheit die universelle Form (die interne Form von Visio) der Einheitenbezeichnung ein. Der Platzhalter U fügt groß Schreibungs Beschriftungen ein, während der u-Platzhalter Kleinbuchstaben einfügt. Fügt die gleiche Anzahl von Leerzeichen vor der Bezeichnung wie vor dem Platzhalter ein.  <br/> |
|/  <br/> |Platzhalter für einen Bruch. Zeigt den Ausdruck als ganze Zahl mit einem Bruchteil an, wenn ein vorangestellter Platzhalter für Ziffern vorhanden ist. Sonst wird nur die ganze Zahl im Dividend angezeigt. Wenn im Divisor dem Ziffernplatzhalter eine Zahl folgt, wird der Bruchteil auf den nächsten Bruchteil abgerundet, dessen Dividend 1 ist, und vereinfacht. Wird im Divisor eine Zahl ohne den Ziffernplatzhalter angegeben, wird auf den nächsten Bruchteil gerundet, aber nicht vereinfacht.  <br/> Beispielsweise wird FORMAT(12,43,"# #/4") als 12 2/4 angezeigt.  <br/> |
|Leerzeichen  <br/> |Zeigt ein Leerzeichen in der formatierten Ausgabe an. Um ein anderes Zeichen anzuzeigen, verwenden Sie den\) umgekehrten Schrägstrich (Character.  <br/> |
   
## <a name="currency-values"></a>Währungswerte

|**Zeichen**|**Beschreibung**|
|:-----|:-----|
|$  <br/> |Währungssymbol. Zeigt das Währungssymbol an, das für die Einstellungen unter **Region und Sprache** (Systemsteuerung) für das betreffende System definiert wurde.  <br/> |
|u oder U  <br/> |Platzhalter für Kurzbezeichnung. Fügt das Standardsymbol für die lokale Währung oder eine drei Zeichen lange Währungsabkürzung für nicht lokale Währungen ein. Beispiele: €99,00, 42,70 FRF. Der Platzhalter u fügt Kleinbuchstaben ein, und U fügt gemischte Groß-/Kleinschreibung-Beschriftungen ein.  <br/> |
|uu oder UU  <br/> |Platzhalter für Langbezeichnungen. Fügt lange Währungsbezeichnungen nach jeder Untereinheit ein. Beispiele: US-Dollar, Französischer Franc. Der Platzhalter u fügt Kleinbuchstaben ein, und U fügt gemischte Groß-/Kleinschreibung-Beschriftungen ein.  <br/> |
|uuu oder UUU  <br/> |Universeller Platzhalter für Bezeichnungen. Fügt die universelle, 3 Zeichen lange Währungsabkürzung für alle Währungen nach jeder Untereinheit ein. Beispiele: 99,00 USD, 42,70 FRF. Der Platzhalter u fügt Kleinbuchstaben ein, und U fügt gemischte Groß-/Kleinschreibung-Beschriftungen ein. Fügt die gleiche Anzahl von Leerzeichen vor der Bezeichnung wie vor dem Platzhalter ein.  <br/> |
   
## <a name="text-values"></a>Textwerte

|**Zeichen**|**Beschreibung**|
|:-----|:-----|
|\  <br/> |Zeigt das nächste Zeichen wie eingegeben an. Geben \\Sie zum Anzeigen des umgekehrten Schrägstrichs ein. Siehe auch "text".  <br/> |
|"text" bzw. 'text'  <br/> |Zeigt den Text in Anführungszeichen unverändert an. Siehe auch \ (Umgekehrter Schrägstrich).  <br/> |
|@  <br/> |Textplatzhalter. Ersetzt eine Zeichenfolge, wenn der Wert eines Ausdrucks eine Zeichenfolge ist.  <br/> Beispielsweise ergibt FORMAT("Hallo", "'Sie haben Folgendes eingegeben ('@')'") die Ausgabe "Sie haben Folgendes eingegeben (Hallo)".  <br/> |
|@+  <br/> |Platzhalter für Text in Großbuchstaben. Bei Zeichenfolgen wird die Eingabe durch Großbuchstaben ersetzt.  <br/> Beispielsweise ergibt FORMAT("Hallo", "@ @+ @-") die Ausgabe "Hallo HALLO hallo".  <br/> |
|@-  <br/> |Textplatzhalter. Bei Zeichenfolgen wird die Eingabe durch Kleinbuchstaben ersetzt.  <br/> Beispielsweise ergibt FORMAT("Hallo", "@ @+ @-") die Ausgabe "Hallo HALLO hallo".  <br/> |
   
## <a name="date-values"></a>Datumswerte

|**Zeichen**|**Beschreibung**|
|:-----|:-----|
|c oder C  <br/> |Datums- oder Zeitplatzhalter. Zeigt Datums- und Zeitwerte in einem kurzen (c) oder langem (C) Datumsformat und einem allgemeinen Zeitformat an. Bis einschließlich Version 4.0 von Visio wird dieser Platzhalter ignoriert.  <br/> Beispiel: FORMAT (DATETIME ("6/25/07 12:05"), "C") wird am Montag, 2007 12:05:00 Uhr angezeigt. FORMAT (DATETIME ("Jun. 25, 2007"), "c") zeigt 6/25/2007 an.  <br/> |
|/  <br/> |Datumstrennzeichen. Wenn der Ausdruck ein Datum ist, trennt dieses Zeichen die einzelnen Datumskomponenten. Zeigt das Datumstrennzeichen an, das für das System in den Einstellungen unter **Region und Sprache** (Systemsteuerung) definiert ist.<br/> |
| [ ]  <br/> |Platzhalter für vergangenes Datum. Wird zusammen mit den Platzhaltern d, dd, w und ww benutzt, um Dauereinheiten anzuzeigen.  <br/> Beispielsweise bedeutet [d] oder [dd] vergangene Tage und [w] oder [ww] vergangene Wochen.  <br/> |
|d  <br/> |Tagplatzhalter. Zeigt den Tag als Zahl (von 1 bis 31) ohne vorangestellte 0 an.  <br/> |
|dd  <br/> | Tagplatzhalter. Zeigt den Tag als Zahl (von 01 bis 31) mit vorangestellter 0 an.  <br/> |
|ddd oder w  <br/> |Platzhalter für kurzen Tag der Woche. Zeigt den Tag in abgekürzter Form an (Son-Sam).  <br/> |
|dddd oder w  <br/> |Platzhalter für langen Tag der Woche. Zeigt den Tag in vollständiger Schreibweise (Sonntag-Samstag) an.  <br/> |
|ddddd  <br/> |Platzhalter für kurzes Datum. Zeigt das Datum im kurzen Format an, das in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das jeweilige System definiert ist.<br/> |
|dddd  <br/> |Platzhalter für langes Datum. Zeigt das Datum im langen Format an, das in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das jeweilige System definiert ist.  <br/> |
|D  <br/> |Tagplatzhalter für traditionelles Chinesisch. Zeigt den Monatstag als ausgeschriebene Ordnungszahl an. Gebietsschemaspezifisch.  <br/> |
|D_c  <br/> |Tagplatzhalter für traditionelles Chinesisch. Zeigt den Monatstag als ausgeschriebene Ordnungszahl an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|w_c oder w_c  <br/> |Tagplatzhalter für traditionelles Chinesisch. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|w_e  <br/> |Platzhalter für kurzen Tag der Woche für Englisch. Zeigt den Tag in abgekürzter Form an (Sun-Sat). Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|w_j  <br/> |Platzhalter für kurzen Tag der Woche für Japanisch. Zeigt den Tag in abgekürzter Form an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|w_k  <br/> |Platzhalter für kurzen Tag der Woche für Koreanisch. Zeigt den Tag in abgekürzter Form an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|w_s oder w_s  <br/> |Tagplatzhalter für vereinfachtes Chinesisch. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|ww_e  <br/> |Platzhalter für langen Tag der Woche für Englisch. Zeigt den Tag in vollständiger Schreibweise (Sunday-Saturday) an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|ww_j  <br/> |Platzhalter für langen Tag der Woche für Japanisch. Zeigt den Tag in voller Schreibung an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|w_k  <br/> |Platzhalter für langen Tag der Woche für Koreanisch. Zeigt den Tag in voller Schreibung an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|M  <br/> |Monatsplatzhalter. Zeigt den Monat als Zahl (von 1 bis 12) ohne vorangestellte 0 an. Siehe auch m (Platzhalter für Minute).  <br/> |
|MM  <br/> |Monatsplatzhalter. Zeigt den Monat als Zahl (von 01 bis 12) mit vorangestellter 0 an. Siehe auch mm (Platzhalter für Minute).  <br/> |
|MMM  <br/> |Monatsplatzhalter. Zeigt den Monat in abgekürzter Form an (Jan-Dez).  <br/> |
|MMMM  <br/> |Monatsplatzhalter. Zeigt den vollständigen Monatsnamen an (Januar-Dezember).  <br/> |
|MMMM_c  <br/> |Monatsplatzhalter für traditionelles Chinesisch. Zeigt den vollständigen Monatsnamen an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|MMMM_e  <br/> |Monatsplatzhalter für Englisch. Zeigt den vollständigen Monatsnamen an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|yy  <br/> |Jahresplatzhalter. Zeigt die Jahreszahl als zweistellige Zahl an (00-99).  <br/> |
|yyyy  <br/> |Jahresplatzhalter. Zeigt die Jahreszahl als vierstellige Zahl an (1900-2078).  <br/> |
|g  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für Japanisch die gekürzte Version der Gengo-Zeitrechnung an. Zeigt für Koreanisch die koreanische Jahreskennzeichnung mit nachfolgendem Leerzeichen an.  <br/> |
|g_j  <br/> |Jahresplatzhalter. Zeigt für Japanisch die gekürzte Version der Gengo-Zeitrechnung an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|gg oder G  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für traditionelles Chinesisch die kurze Version der formalen Jahreskennzeichnung an. Zeigt für Japanisch die kurze Version der Gengo-Zeitrechnung in Kanji-Zeichen an. Zeigt für Koreanisch die koreanische Jahreskennzeichnung mit nachfolgendem Leerzeichen an.  <br/> |
|gg_c  <br/> |Jahresplatzhalter. Zeigt für traditionelles Chinesisch die kurze Version der formalen Jahreskennzeichnung an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|gg_j  <br/> |Jahresplatzhalter. Zeigt für Japanisch die kurze Version der Gengo-Zeitrechnung in Kanji-Zeichen an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|gg_k  <br/> |Jahresplatzhalter. Zeigt für Koreanisch die koreanische Jahreskennzeichnung mit nachfolgendem Leerzeichen an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|ggg oder GG  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für traditionelles Chinesisch die vollständige Version der formalen Jahreskennzeichnung an. Zeigt für Japanisch die vollständige Version der Gengo-Zeitrechnung in Kanji-Zeichen an. Zeigt für Koreanisch die koreanische Jahreskennzeichnung mit nachfolgendem Leerzeichen an.  <br/> |
|ggg_c  <br/> |Jahresplatzhalter. Zeigt für traditionelles Chinesisch die vollständige Version der formalen Jahreskennzeichnung an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|ggg_j  <br/> |Jahresplatzhalter. Zeigt für Japanisch die vollständige Version der Gengo-Zeitrechnung in Kanji-Zeichen an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|e  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für traditionelles Chinesisch eine Zeichenfolge an, die das julianische Jahr darstellt. Zeigt für Japanisch das Gengo-Jahr als ein- oder zweistellige Zahl ohne vorangestellte Null an. Zeigt für Koreanisch das koreanische Jahr als vierstellige arabische Zahl an.  <br/> |
|e_c  <br/> |Jahresplatzhalter. Zeigt für traditionelles Chinesisch eine Zeichenfolge an, die das julianische Jahr darstellt. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|E_J  <br/> |Jahresplatzhalter. Zeigt für Japanisch das Gengo-Jahr als ein- oder zweistellige arabische Zahl an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|e_k  <br/> |Jahresplatzhalter. Zeigt für Koreanisch das koreanische Jahr als vierstellige arabische Zahl an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|E  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für traditionelles Chinesisch eine Zeichenfolge an, die das republikanische Jahr darstellt. Zeigt für Japanisch das Gengo-Jahr als ein- oder zweistellige Zahl ohne vorangestellte Null an. Zeigt für Koreanisch das koreanische Jahr als vierstellige arabische Zahl an.  <br/> |
|E_c  <br/> |Jahresplatzhalter. Zeigt für traditionelles Chinesisch eine Zeichenfolge an, die das republikanische Jahr darstellt. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|EE  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für traditionelles Chinesisch eine Zeichenfolge an, die das julianische Jahr darstellt. Zeigt für Japanisch das Gengo-Jahr als zweistellige arabische Zahl an, die erforderlichenfalls eine vorangestellte Null enthält. Zeigt für Koreanisch das koreanische Jahr als vierstellige arabische Zahl an.  <br/> |
|ee_j  <br/> |Jahresplatzhalter. Zeigt für Japanisch das Gengo-Jahr als zweistellige arabische Zahl an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|EE  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für traditionelles Chinesisch eine Zeichenfolge an, die das republikanische Jahr darstellt. Zeigt für Japanisch das Gengo-Jahr als zweistellige arabische Zahl an, die erforderlichenfalls eine vorangestellte Null enthält. Zeigt für Koreanisch das koreanische Jahr als vierstellige arabische Zahl an.  <br/> |
|n oder N  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für traditionelles Chinesisch das republikanische Jahr als arabische Zahl an. Zeigt für Japanisch das Gengo-Jahr als ein- oder zweistellige Zahl ohne vorangestellte Null an. Zeigt für Koreanisch das koreanische Jahr als vierstellige arabische Zahl an.  <br/> |
|n_c  <br/> |Jahresplatzhalter. Zeigt für traditionelles Chinesisch das republikanische Jahr als arabische Zahl an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|nn oder NN  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für traditionelles Chinesisch das republikanische Jahr als arabische Zahl an. Zeigt für Japanisch das Gengo-Jahr als zweistellige arabische Zahl an, die erforderlichenfalls eine vorangestellte Null enthält. Zeigt für Koreanisch das koreanische Jahr als vierstellige arabische Zahl an.  <br/> |
   
## <a name="time-values"></a>Zeitwerte

|**Zeichen**|**Beschreibung**|
|:-----|:-----|
|:  <br/> |Uhrzeittrennzeichen. Zeigt die Uhrzeit an, die in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das betreffende System definiert ist.<br/> |
|[ ]  <br/> |Platzhalter für vergangene Zeit. Wird zusammen mit den Platzhaltern h, hh, m, mm, s und ss verwendet, um Dauereinheiten anzuzeigen. Beispielsweise bedeutet [h] oder [hh] vergangene Stunden, [m] oder [mm] vergangene Minuten und [s] oder [ss] vergangene Sekunden.  <br/> |
|h  <br/> |Stundenplatzhalter. Zeigt die Stundenangabe ohne vorangestellte Null im 12-Stunden-Format an (0-12).  <br/> |
|hh  <br/> |Stundenplatzhalter. Zeigt die Stundenangabe mit vorangestellter Null im 12-Stunden-Format an (00-12).  <br/> |
|H  <br/> |Stundenplatzhalter. Zeigt die Stundenangabe ohne vorangestellte Null im 24-Stunden-Format an (0-24).  <br/> |
|HH  <br/> |Stundenplatzhalter. Zeigt die Stundenangabe mit vorangestellter Null im 24-Stunden-Format an (00-24).  <br/> |
|m  <br/> |Minutenplatzhalter. Zeigt die Minuten ohne vorangestellte Null an (0-59).  <br/> |
|mm  <br/> |Minutenplatzhalter. Zeigt die Minuten mit vorangestellter Null an (00-59).  <br/> |
|s  <br/> |Sekundenplatzhalter. Zeigt die Sekunden ohne vorangestellte Null an (0-59).  <br/> |
|ss  <br/> |Sekundenplatzhalter. Zeigt die Sekunden mit vorangestellter Null an (00-59).  <br/> |
|t  <br/> |AM/PM-Abkürzung. Zeigt die in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das jeweilige System definierte Abkürzung an.<br/> |
|tt  <br/> |AM/PM-Kennzeichner. Zeigt den vollständigen Kennzeichner an, der in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das jeweilige System definiert ist.<br/> |
|t_c oder tt_c  <br/> |AM/PM-Kennzeichner für traditionelles Chinesisch. Zeigt den Kennzeichner an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|t_k oder tt_k  <br/> |AM/PM-Kennzeichner für Koreanisch. Zeigt den Kennzeichner an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|t_j oder tt_j  <br/> |AM/PM-Kennzeichner für Japanisch. Zeigt den Kennzeichner an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|t_e  <br/> |AM/PM-Kennzeichner für Englisch. Zeigt den Kennzeichner in Kurzformat an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|tt_e  <br/> |AM/PM-Kennzeichner für Englisch. Zeigt den vollständigen Kennzeichner an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|t_s oder tt_s  <br/> |AM/PM-Kennzeichner für vereinfachtes Chinesisch. Zeigt den Kennzeichner an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|T  <br/> |Allgemeines Zeitformat.  <br/> |
   

