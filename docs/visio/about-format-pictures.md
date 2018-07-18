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
ms.openlocfilehash: 94e406d1584d721cadb48205773e28b98bc871a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796368"
---
# <a name="about-format-pictures"></a>Informationen zum Formatieren von Bildern

Eine Formatierungsangabe ist ein Formatcode, der bestimmt, wie ein Wert angezeigt wird. Sie können beispielsweise die Anzahl von Stellen bestimmen, die rechts oder links von einem Dezimaltrennzeichen angezeigt werden, oder Sie legen fest, ob eine Zeichenfolge in Klein- oder Großschreibung angezeigt wird.
  
> [!NOTE]
> Wenn eine Formatierungsangabe Datums- oder Zeitwerte mithilfe von Microsoft Office System Formatierung definieren möchten, schließen Sie die Formatierungsangaben in doppelte geschweifte Klammern ein, beispielsweise "{{m/JJ}}". Wenn Sie ein vordefiniertes Format verwenden, beispielsweise 201, schließen Sie dieses in geschweifte und spitzen Klammern wie folgt: "{\<201\>}" 
  
Die folgenden Abschnitte zeigen Symbole, mit denen Sie unterschiedliche Typen von Werten für die Anzeige formatieren können.
  
## <a name="string-and-numeric-values"></a>Zeichenfolgen und numerische Werte

|**Zeichen**|**Beschreibung**|
|:-----|:-----|
|#  <br/> |Platzhalter für Ziffer. Zeigt entweder eine Ziffer oder keinen Wert an. Vorangestellte und nachfolgende Nullen werden nicht angezeigt. Befinden sich links vom Dezimaltrennzeichen mehr Ziffern als Platzhalter, werden alle Ziffern angezeigt. Befinden sich rechts vom Dezimaltrennzeichen mehr Ziffern als Platzhalter, wird der Bruchteil auf die Anzahl der Platzhalter gerundet. Bei Abmessungen werden Untereinheiten mit dem Wert 0 nicht angezeigt, wenn der Platzhalter die äußerste linke Ziffer ist.  <br/> Beispielsweise wird FORMAT(0Fuß 11.25Zoll,"#.##u") als 11,25 Zoll angezeigt.  <br/> |
|0  <br/> |Platzhalter für eine Ziffer (Null). Zeigt entweder eine Ziffer oder keinen Wert an. Vorangestellte und nachfolgende Nullen werden angezeigt. Befinden sich links vom Dezimaltrennzeichen mehr Ziffern als Platzhalter, werden alle Ziffern angezeigt. Befinden sich rechts vom Dezimaltrennzeichen mehr Ziffern als Platzhalter, wird der Bruchteil auf die Anzahl der Platzhalter gerundet. Bei Abmessungen werden Untereinheiten mit dem Wert 0 angezeigt.  <br/> Beispielsweise wird FORMAT(2Fuß 11.33Zoll,"0.## u") als 2 Fuß 11,33 Zoll angezeigt.  <br/> |
|.  <br/> |Platzhalter für Dezimalstellen. Legt die Anzahl von Ziffern fest, die links und rechts vom Dezimaltrennzeichen angezeigt werden. Bei einer mehrteiligen Einheit wird das Dezimaltrennzeichen in der kleinsten (äußersten rechten) Untereinheit verwendet. Zeigt das Dezimaltrennzeichen an, das in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das betreffende System definiert ist.<br/> Beispielsweise wird FORMAT(250 cm,"0.000 u") als 250,000 cm angezeigt.  <br/> |
|,  <br/> |Tausendertrennzeichen. Wenn das Trennzeichen von Platzhaltern für Ziffern umgeben (# oder 0) wird, trennt dieses Tausender von Hunderten innerhalb eines numerischen Werts, der aus vier oder mehr Ziffern links vom Dezimaltrennzeichen besteht. Zeigt das Tausendertrennzeichen an, das in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das betreffende System definiert ist.<br/> |
|E- E+ e- e+  <br/> |Wissenschaftliches Format. Wenn das Format wenigstens einen Platzhalter für Ziffern rechts von diesem Symbol enthält, wird die Zahl im wissenschaftlichen Format angezeigt. Fügen Sie das E oder e zwischen der Zahl und ihrem Exponenten ein. Bei E+ oder e+ wird das Zeichen + vor einem positiven Exponenten und das Zeichen - vor einem negativen Exponenten angezeigt. Bei E- oder e- wird das Minuszeichen (-) nur bei einem negativen Exponenten angezeigt.  <br/> Beispielsweise wird FORMAT(12345.67,"###.#e+#") als 123,5e+2 angezeigt.  <br/> |
|u oder U  <br/> |Platzhalter für kurzen Bezeichnung. Fügt abgekürzt einheitenbeschriftungen nach jedem Untereinheit. Beispiel: Zoll, Fuß, Grad. Der Platzhalter U Fügt gemischten Groß-/Kleinschreibung Etiketten, während der Platzhalter u Kleinbuchstabe Etiketten eingefügt. Fügt die gleiche Anzahl von Leerzeichen vor der Bezeichnung wie vor dem Platzhalter ein.  <br/> Beispielsweise wird FORMAT(12 c 13 d,"#u") als 13c1 angezeigt.  <br/> |
|uu oder UU  <br/> |Platzhalter für lange Beschriftung. Einheitenbeschriftungen nach jedem Untereinheit eingefügt. Beispiel: Zoll, Fuß, Grad der U Platzhalter fügt Groß-Etiketten, während der Platzhalter u Kleinbuchstabe Etiketten eingefügt. Fügt die gleiche Anzahl von Leerzeichen vor der Bezeichnung wie vor dem Platzhalter ein.  <br/> Beispielsweise wird FORMAT(12.43Zoll,"# #/4 UU") als 12 2/4 ZOLL angezeigt.  <br/> |
|uuu oder UUU  <br/> |Platzhalter für universelle Beschriftung. Das Formular Universal (in Visio intern) der einheitenbeschriftungen nach jedem Untereinheit eingefügt. Der Platzhalter U Fügt gemischten Groß-/Kleinschreibung Etiketten, während der Platzhalter u Kleinbuchstabe Etiketten eingefügt. Fügt die gleiche Anzahl von Leerzeichen vor der Bezeichnung wie vor dem Platzhalter ein.  <br/> |
|/  <br/> |Platzhalter für einen Bruch. Zeigt den Ausdruck als ganze Zahl mit einem Bruchteil an, wenn ein vorangestellter Platzhalter für Ziffern vorhanden ist. Sonst wird nur die ganze Zahl im Dividend angezeigt. Wenn im Divisor dem Ziffernplatzhalter eine Zahl folgt, wird der Bruchteil auf den nächsten Bruchteil abgerundet, dessen Dividend 1 ist, und vereinfacht. Wird im Divisor eine Zahl ohne den Ziffernplatzhalter angegeben, wird auf den nächsten Bruchteil gerundet, aber nicht vereinfacht.  <br/> Beispielsweise wird FORMAT(12,43,"# #/4") als 12 2/4 angezeigt.  <br/> |
|Leerzeichen  <br/> |Zeigt ein Leerzeichen in der formatierten Ausgabe. Um ein anderes Zeichen anzuzeigen, verwenden Sie den umgekehrten Schrägstrich (\) Zeichen.  <br/> |
   
## <a name="currency-values"></a>Währungswerte

|**Zeichen**|**Beschreibung**|
|:-----|:-----|
|$  <br/> |Währungssymbol. Zeigt das Währungssymbol an, das für die Einstellungen unter **Region und Sprache** (Systemsteuerung) für das betreffende System definiert wurde.<br/> |
|u oder U  <br/> |Platzhalter für kurzen Bezeichnung. Fügt das Standardsymbol für lokale Währung oder den dreistelligen Währung Abkürzungen für nicht lokalen Währungen. Beispielsweise $99,00, 42,70 FRF. Der Platzhalter u fügt Kleinbuchstaben und U Groß-Etiketten eingefügt.  <br/> |
|uu oder UU  <br/> |Platzhalter für lange Beschriftung. Fügt lange Währung Etiketten nach jedem Untereinheit. Beispiel: US-Dollar, französische Franc. Der Platzhalter u fügt Kleinbuchstaben und U Groß-Etiketten eingefügt.  <br/> |
|uuu oder UUU  <br/> |Platzhalter für universelle Beschriftung. Die universelle, zwei-Währung Abkürzungen für alle Währungen nach jedem Untereinheit eingefügt. Beispielsweise 99.00 USD, 42,70 FRF. Der Platzhalter u fügt Kleinbuchstaben und U Groß-Etiketten eingefügt. Fügt die gleiche Anzahl von Leerzeichen vor der Bezeichnung wie vor dem Platzhalter ein.  <br/> |
   
## <a name="text-values"></a>Textwerte

|**Zeichen**|**Beschreibung**|
|:-----|:-----|
|\  <br/> |Zeigt das nächste Zeichen ist. Um einen umgekehrten Schrägstrich anzuzeigen, geben Sie \\. Siehe auch "Text".  <br/> |
|"text" bzw. 'text'  <br/> |Zeigt den Text in Anführungszeichen unverändert an. Siehe auch \ (Umgekehrter Schrägstrich).  <br/> |
|@  <br/> |Textplatzhalter. Ersetzt eine Zeichenfolge, wenn der Wert eines Ausdrucks eine Zeichenfolge ist.  <br/> Beispielsweise ergibt FORMAT("Hallo", "'Sie haben Folgendes eingegeben ('@')'") die Ausgabe "Sie haben Folgendes eingegeben (Hallo)".  <br/> |
|@+  <br/> |Platzhalter für Text in Großbuchstaben. Bei Zeichenfolgen wird die Eingabe durch Großbuchstaben ersetzt.  <br/> Beispielsweise ergibt FORMAT("Hallo", "@ @+ @-") die Ausgabe "Hallo HALLO hallo".  <br/> |
|@-  <br/> |Platzhalter für Text. Für String-Werten ersetzt die Eingabe durch Kleinbuchstaben.  <br/> Beispielsweise ergibt FORMAT("Hallo", "@ @+ @-") die Ausgabe "Hallo HALLO hallo".  <br/> |
   
## <a name="date-values"></a>Datumswerte

|**Zeichen**|**Beschreibung**|
|:-----|:-----|
|c oder C  <br/> |Datums- oder Zeitplatzhalter. Zeigt Datums- und Zeitwerte in einem kurzen (c) oder langem (C) Datumsformat und einem allgemeinen Zeitformat an. Bis einschließlich Version 4.0 von Visio wird dieser Platzhalter ignoriert.  <br/> Beispiel: FORMAT(DATETIME("6/25/07 12:05"),"C") wird als Montag, 25. Juni 2007, 12:05:00 Uhr angezeigt. FORMAT(DATETIME("Jun. 25, 2007"),"c") wird als 25.6.2007 wiedergegeben.  <br/> |
|/  <br/> |Datumstrennzeichen. Wenn der Ausdruck ein Datum ist, trennt dieses Zeichen die einzelnen Datumskomponenten. Zeigt das Datumstrennzeichen an, das für das System in den Einstellungen unter **Region und Sprache** (Systemsteuerung) definiert ist.<br/> |
| [ ]  <br/> |Platzhalter für vergangenes Datum. Wird zusammen mit den Platzhaltern d, dd, w und ww benutzt, um Dauereinheiten anzuzeigen.  <br/> Beispielsweise bedeutet [d] oder [dd] vergangene Tage und [w] oder [ww] vergangene Wochen.  <br/> |
|d  <br/> |Tagplatzhalter. Zeigt den Tag als Zahl (von 1 bis 31) ohne vorangestellte 0 an.  <br/> |
|dd  <br/> | Tagplatzhalter. Zeigt den Tag als Zahl (von 01 bis 31) mit vorangestellter 0 an.  <br/> |
|ddd oder w  <br/> |Platzhalter für kurzen Tag der Woche. Zeigt den Tag in abgekürzter Form an (Son-Sam).  <br/> |
|Dddd oder w  <br/> |Platzhalter für langen Tag der Woche. Zeigt den Tag in vollständiger Schreibweise (Sonntag-Samstag) an.  <br/> |
|ddddd  <br/> |Platzhalter für kurzes Datum. Zeigt das Datum im kurzen Format an, das in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das jeweilige System definiert ist.<br/> |
|dddd  <br/> |Platzhalter für langes Datum. Zeigt das Datum im langen Format an, das in den Einstellungen unter **Region und Sprache** (Systemsteuerung) für das jeweilige System definiert ist.<br/> |
|D  <br/> |Tagplatzhalter für traditionelles Chinesisch. Zeigt den Monatstag als ausgeschriebene Ordnungszahl an. Gebietsschemaspezifisch.  <br/> |
|D_c  <br/> |Tagplatzhalter für traditionelles Chinesisch. Zeigt den Monatstag als ausgeschriebene Ordnungszahl an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|W_c oder w_c  <br/> |Tagplatzhalter für traditionelles Chinesisch. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|w_e  <br/> |Platzhalter für kurzen Tag der Woche für Englisch. Zeigt den Tag in abgekürzter Form an (Sun-Sat). Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|w_j  <br/> |Platzhalter für kurzen Tag der Woche für Japanisch. Zeigt den Tag in abgekürzter Form an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|w_k  <br/> |Platzhalter für kurzen Tag der Woche für Koreanisch. Zeigt den Tag in abgekürzter Form an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|W_s oder w_s  <br/> |Tagplatzhalter für vereinfachtes Chinesisch. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|ww_e  <br/> |Platzhalter für langen Tag der Woche für Englisch. Zeigt den Tag in vollständiger Schreibweise (Sunday-Saturday) an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|ww_j  <br/> |Platzhalter für langen Tag der Woche für Japanisch. Zeigt den Tag in voller Schreibung an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|w_k  <br/> |Platzhalter für langen Tag der Woche für Koreanisch. Zeigt den Tag in voller Schreibung an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|M  <br/> |Monatsplatzhalter. Zeigt den Monat als Zahl (von 1 bis 12) ohne vorangestellte 0 an. Siehe auch m (Platzhalter für Minute).  <br/> |
|MM  <br/> |Monatsplatzhalter. Zeigt den Monat als Zahl (von 01 bis 12) mit vorangestellter 0 an. Siehe auch mm (Platzhalter für Minute).  <br/> |
|MMM  <br/> |Monatsplatzhalter. Zeigt den Monat in abgekürzter Form an (Jan-Dez).  <br/> |
|MMMM  <br/> |Monatsplatzhalter. Zeigt den vollständigen Monatsnamen an (Januar-Dezember).  <br/> |
|MMMM_c  <br/> |Monatsplatzhalter für traditionelles Chinesisch. Zeigt den vollständigen Monatsnamen an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|MMMM_e  <br/> |Monatsplatzhalter für Englisch. Zeigt den vollständigen Monatsnamen an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|jj  <br/> |Jahresplatzhalter. Zeigt die Jahreszahl als zweistellige Zahl an (00-99).  <br/> |
|jjjj  <br/> |Jahresplatzhalter. Zeigt die Jahreszahl als vierstellige Zahl an (1900-2078).  <br/> |
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
|e_j  <br/> |Jahresplatzhalter. Zeigt für Japanisch das Gengo-Jahr als ein- oder zweistellige arabische Zahl an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|e_k  <br/> |Jahresplatzhalter. Zeigt für Koreanisch das koreanische Jahr als vierstellige arabische Zahl an. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|E  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für traditionelles Chinesisch eine Zeichenfolge an, die das republikanische Jahr darstellt. Zeigt für Japanisch das Gengo-Jahr als ein- oder zweistellige Zahl ohne vorangestellte Null an. Zeigt für Koreanisch das koreanische Jahr als vierstellige arabische Zahl an.  <br/> |
|E_c  <br/> |Jahresplatzhalter. Zeigt für traditionelles Chinesisch eine Zeichenfolge an, die das republikanische Jahr darstellt. Unabhängig vom Gebietsschema des Benutzers.  <br/> |
|ee  <br/> |Jahresplatzhalter. Gebietsschemaspezifisch. Zeigt für traditionelles Chinesisch eine Zeichenfolge an, die das julianische Jahr darstellt. Zeigt für Japanisch das Gengo-Jahr als zweistellige arabische Zahl an, die erforderlichenfalls eine vorangestellte Null enthält. Zeigt für Koreanisch das koreanische Jahr als vierstellige arabische Zahl an.  <br/> |
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
   

