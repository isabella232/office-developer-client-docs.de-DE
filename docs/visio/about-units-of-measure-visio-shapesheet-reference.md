---
title: Informationen zu Maßeinheiten (Visio-ShapeSheet-Referenz)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251828
localization_priority: Normal
ms.assetid: 48f765a8-7485-03c0-3484-d4ec07822600
description: Wenn Sie Felder in Text einfügen oder Formeln erstellen, geben Sie häufig Maßeinheiten für die eingegebenen Werte an.
ms.openlocfilehash: d23c3f30841c81d07c09e57c0802e09edb0fe3c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360452"
---
# <a name="about-units-of-measure-visio-shapesheet-reference"></a>Informationen zu Maßeinheiten (Visio-ShapeSheet-Referenz)

Wenn Sie Felder in Text einfügen oder Formeln erstellen, geben Sie häufig Maßeinheiten für die eingegebenen Werte an.
  
Microsoft Visio wertet das Ergebnis einer Formel je nach der Zelle, in der Sie die Formel eingeben, unterschiedlich aus. In general, cells that represent shape position, a dimension, or an angle require a number-unit pair that consists of a number and the qualifying units needed to interpret the number. Many other cells don't require units and evaluate to a string, to TRUE or FALSE, or to an index. Beispiel: die gleiche Formel, die in der **Zelle FillForegnd** -Zelle die Farbe 5 aus der Farbpalette der Zeichnung angibt, ist true (und sperrt die Breite der Form) in der Zelle LockWidth-Zelle. 
  
Geben Sie immer eine Maßeinheit an, wenn Sie eine Formel in eine Zelle eingeben, für die ein Bemaßungswert erforderlich ist. Wenn Sie keine Maßeinheit angeben, verwendet Visio die Standardeinheit für diese Zelle. Hierbei kann es sich um Seiteneinheiten, Zeichnungseinheiten, Einheitenoptionen, Einheiten für die Dauer und Winkeleinheiten handeln.
  
## <a name="units-of-measure"></a>Maßeinheiten

Verwenden Sie bei der Angabe von Maßeinheiten in ShapeSheet-Formularen die in der folgenden Liste angegebenen Abkürzungen.
  
|**So geben Sie diese Maßeinheiten an**|**Verwenden Sie**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| Zentimeter  <br/> | cm  <br/> |**visCentimeters (69)** <br/> |
| Cicero  <br/> | c  <br/> |**visCiceros (54)** <br/> |
| Datum oder Uhrzeit  <br/> | date  <br/> |**visDate (40)** <br/> |
| Grad  <br/> | deg  <br/> |**visDegrees (81)** <br/> |
| Didot  <br/> | d  <br/> |**visDidots (53)** <br/> |
| Vergangene Wochen  <br/> | ew  <br/> |**visElapsedWeek (43)** <br/> |
| Vergangene Tage  <br/> | ed  <br/> |**visElapsedDay (44)** <br/> |
| Vergangene Stunden  <br/> | eh  <br/> |**visElapsedHour (45)** <br/> |
| Vergangene Minuten  <br/> | em  <br/> |**visElapsedMin (46)** <br/> |
| Vergangene Sekunden  <br/> | es  <br/> |**visElapsedSec (47)** <br/> |
| Fuß  <br/> | ft  <br/> |**visFeet (66)** <br/> |
| Zoll  <br/> | in  <br/> |**visInches (65)** <br/> |
| Kilometer  <br/> | km  <br/> |**visKilometers (72)** <br/> |
| Meter  <br/> | m  <br/> |**visMeters (71)** <br/> |
| Meilen  <br/> | mi  <br/> |**visMiles (68)** <br/> |
| Millimeter  <br/> | mm  <br/> |**visMillimeters (70)** <br/> |
| Minuten  <br/> | '  <br/> |**visMin (84)** <br/> |
| Nautische Meilen  <br/> | nm  <br/> |**visNautMiles (76)** <br/> |
| Prozent  <br/> | %  <br/> |**visPercent (33)** <br/> |
| Pica  <br/> | p  <br/> |**visPicas (51)** <br/> |
| Punkte  <br/> | pt  <br/> |**visPoints (50)** <br/> |
| Bogenmaß  <br/> | rad  <br/> |**visRadians (83)** <br/> |
| Sekunden  <br/> | "  <br/> |**visSec (85)** <br/> |
| Yard  <br/> | yd  <br/> |**visYards (75)** <br/> |
   
## <a name="compound-units-of-measure"></a>Zusammengesetzte Maßeinheiten

In Formeln können Sie Maßeinheiten für zusammengesetzte Zahlen mit den Abkürzungen aus der folgenden Tabelle angeben. Visio vereinfacht die Ergebnisse und zeigt sie in den zusammengesetzten Einheiten an.
  
Wenn Sie beispielsweise 45,635° eingeben, zeigt Visio den äquivalenten Wert als 45° 38' 6" an.
  
|**So geben Sie Einheiten an**|**Verwenden Sie diese Abkürzung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| Cicero und Didot  <br/> | CICERO/DIDOT  <br/> |**visCicerosAndDidots (52)** <br/> |
| Grad, Minuten und Sekunden  <br/> | °  <br/> |**visDegreeMinSec (82)** <br/> |
| Fuß und Zoll  <br/> | FEET/INCH  <br/> |**visFeetAndInches (67)** <br/> |
| Pica und Punkte  <br/> | PICAPOINTS  <br/> |**visPicasAndPoints (49)** <br/> |
   
## <a name="fractional-units-of-measure"></a>Maßeinheiten für Bruchzahlen

Sie können Bruch Maßeinheiten in der Zelle **DrawingScale** angeben, um die Anzahl der Lineal-Unterabteilungen zu beeinflussen, die Visio im Zeichnungsfenster anzeigt. By default, Visio divides distances into tenths when drawing its rulers. Wenn Sie Fractional Maßeinheiten in der Zelle **DrawingScale** verwenden, teilt Visio den Abstand in Folgendes ein: 
  
- Achtel für *visInchFrac* und *visMileFrac* 
    
- Zwölftel für  *visFeetAndInches* 
    
Fractional units of measure have no effect in cells other than in the DrawingScale cell.
  
|**So geben Sie Maßeinheiten für Bruchzahlen an**|**Verwenden Sie diese Abkürzung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| Zoll als Bruchzahlangabe  <br/> | IN_F  <br/> |**visInchFrac (73)** <br/> |
| Meilen als Bruchzahlen  <br/> | MI_F  <br/> |**visMileFrac (74)** <br/> |
| Fuß und Zoll  <br/> | FEET/INCH  <br/> |**visFeetAndInches (67)** <br/> |
   
## <a name="multidimensional-units-of-measure"></a>Mehrdimensionale Maßeinheiten

In Formeln können Sie Maßeinheiten für mehrdimensionale Zahlen mit den Abkürzungen aus der folgenden Tabelle angeben. Visio vereinfacht die Ergebnisse und zeigt sie als mehrdimensionale Einheiten an.
  
|**So geben Sie mehrdimensionale Einheiten an**|**Verwenden Sie diese Abkürzung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| Acre  <br/> | Hektar  <br/> |**visAcre (36)** <br/> |
| Zentimeter  <br/> | SQ. CM., SQ CM, CM.^2, CM^2  <br/> |**visCentimeters (69)** <br/> |
| Fuß  <br/> | SQ. FT., SQ FT, FT.^2, FT^2  <br/> |**visFeet (66)** <br/> |
| Hektar  <br/> | HECTARES, HECTARE, HA., HA  <br/> |**visHectare (37)** <br/> |
| Zoll  <br/> | SQ. IN., SQ IN, IN.^2, IN^2  <br/> |**visInches (65)** <br/> |
| Kilometer  <br/> | SQ. KM., SQ KM, KM.^2, KM ^2  <br/> |**visKilometers (72)** <br/> |
| Meter  <br/> | SQ. M., SQ M, M.^2, M ^2  <br/> |**visMeters (71)** <br/> |
| Meilen  <br/> | SQ. MI., SQ MI, MI.^2, MI ^2  <br/> |**visMiles (68)** <br/> |
| Millimeter  <br/> | SQ. MM., SQ MM, MM.^2, MM ^2  <br/> |**visMillimeters (70)** <br/> |
| Yard  <br/> | SQ. YD., SQ YD, YD.^2, YD^2  <br/> |**visYards (75)** <br/> |
   
## <a name="universal-strings"></a>Universelle Zeichenfolgen

In lokalisierten Visio-Versionen hängt die Gruppe der erkannten Zeichenfolgen von der Sprache ab. Wenn das Programm mit mehreren Sprachen arbeiten soll, verwenden Sie die universellen Zeichenfolgen für Maßeinheiten.
  
|**Für**|**Verwenden Sie**|
|:-----|:-----|
| Zentimeter  <br/> | CM  <br/> |
| Cicero  <br/> | C  <br/> |
| Cicero und Didot  <br/> | CICERO/DIDOT  <br/> |
| Datum oder Uhrzeit  <br/> | DATE  <br/> |
| Grad  <br/> | DEG  <br/> |
| Grad, Minuten, Sekunden  <br/> | °  <br/> |
| Didot  <br/> | D  <br/> |
| Vergangene Wochen  <br/> | EW  <br/> |
| Vergangene Tage  <br/> | ED  <br/> |
| Vergangene Stunden  <br/> | EH  <br/> |
| Vergangene Minuten  <br/> | EM  <br/> |
| Vergangene Sekunden  <br/> | ES  <br/> |
| Fuß  <br/> | FT  <br/> |
| Fuß und Zoll  <br/> | FEET/INCH  <br/> |
| Zoll  <br/> | IN  <br/> |
| Zoll als Bruchzahlangabe  <br/> | IN_F  <br/> |
| Kilometer  <br/> | KM  <br/> |
| Meter  <br/> | M  <br/> |
| Meilen  <br/> | MI  <br/> |
| Meilen als Bruchzahlen  <br/> | MI_F  <br/> |
| Millimeter  <br/> | MM  <br/> |
| Minuten  <br/> | '  <br/> |
| Nautische Meilen  <br/> | NM  <br/> |
| Prozent  <br/> | %  <br/> |
| Pica  <br/> | P  <br/> |
| Pica und Punkte  <br/> | PICAPOINTS  <br/> |
| Punkte  <br/> | PT  <br/> |
| Bogenmaß  <br/> | RAD  <br/> |
| Sekunden  <br/> | "  <br/> |
| Yard  <br/> | YD  <br/> |
   
## <a name="implicit-units-of-measure"></a>Implizite Maßeinheiten

Wenn Visio ein Zahl-Einheit-Paar analysiert und speichert, können explizite oder implizite Einheiten verwendet werden. Eine in expliziten Einheiten angegebene Zahl wird immer in der ursprünglich eingegebenen Maßeinheit angezeigt. Eine in impliziten Einheiten angegebene Zahl wird stets in einen entsprechenden Wert in der Einheit der Zeichnung, des Zeichenblatts oder in die der Zelle entsprechenden Gradangaben konvertiert.
  
Angenommen, Sie geben 1 Zoll in Zelle "A" mit expliziten Einheiten und in Zelle "B" mit impliziten Einheiten ein und beide Zellen verwenden Zeichnungseinheiten. Im nächsten Schritt ändern Sie die Standardeinheit für das Zeichenblatt in Zentimeter. Zelle "A" zeigt weiterhin 1 Zoll an, da sie explizite Einheiten verwendet, die sich nicht mit den Standardwerten ändern. Zelle "B" zeigt nun 2,54 cm an, den entsprechenden Wert in der Standardeinheit.
  
Wenn Sie Einheiten implizit eingeben möchten, verwenden Sie folgende Syntax.
  
```vb
number  [unit , flag ]
```

|||
|:-----|:-----|
| _Zahl_ <br/> |Der ursprüngliche Wert, z. B. 3,7, 1,7E-4 oder 5 1/2.  <br/> |
| _Einheit_ <br/> |Die Einheiten, in denen die _Zahl_ ursprünglich ausgedrückt wird.  <br/> |
| _Flag_ <br/> |Das Maßsystem, das verwendet werden soll, wenn die Einheit für den impliziten Wert angezeigt wird. Entsprechende Werte finden Sie unten.  <br/> |
   
Das Parameter- _Flag_ ist eines der folgenden Buchstaben (groß-oder Kleinbuchstaben), das das Messsystem angibt, das verwendet werden soll, wenn die implizite Wert Einheit angezeigt wird. 
  
|**_Flagge_**|**Bemaßungssystem**|**Beispiel**|
|:-----|:-----|:-----|
| a, A  <br/> | Winkel  <br/> | =5[deg,A]  <br/> |
| d, D  <br/> | Zeichnung  <br/> | =5[in,D]  <br/> |
| e, E  <br/> | Dauer  <br/> | =5[eh,E]  <br/> |
| p, P  <br/> | Seite  <br/> | =5[in,P]  <br/> |
| t, T  <br/> | Typ  <br/> | =5[pt,T]  <br/> |
   
Zusätzlich können Sie die impliziten Einheiten DL, DP, DT, DA, DE für implizite Zeichnungseinheiten, Seiteneinheiten, Texteinheiten, Gradangaben bzw. Zeiteinheiten verwenden. Bei diesen Einheiten wird davon ausgegangen, dass es sich bei dem zugeordneten Wert um interne Einheiten handelt. Wenn das aktuelle Maßsystem beispielsweise Zentimeter ist, wird  *=2 DL*  als 2 interne Einheiten (Zoll) interpretiert und als 5,08 cm angezeigt. 
  
Wenn Sie die oben beschriebene implizite Syntax verwenden, entspricht der Ausdruck (=2 DL) dem Ausdruck 2[in,d]. Mithilfe der impliziten Syntax können Sie bestimmen, wie der Wert interpretiert werden soll. Daher könnten Sie auch 2[in,d] angeben, was als 2 Fuß interpretiert und als 60,96 cm angezeigt wird. Die impliziten Einheiten DL, DP, DT, DA und DE sind universell und verfügen über keine lokalisierten Entsprechungen.
  
## <a name="default-units-of-measure"></a>Standardmaßeinheiten

Im Folgenden werden die Standardmaßeinheiten zusammen mit den entsprechenden Einstellungen auf der Benutzeroberfläche aufgelistet.
  
|**Standardmaßeinheit**|**Entsprechung auf der Benutzeroberfläche**|
|:-----|:-----|
|**visDrawingUnits** <br/> |The units in the DrawingScale cell of the page or master containing the cell.  <br/> |
|**visPageUnits** <br/> |Die im Feld **Maßeinheiten** auf der Registerkarte **Zeichenblatteigenschaft** des Dialogfelds **Seite einrichten** ausgewählten Einheiten (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil für **Seite einrichten**).  <br/> |
|**visTypeUnits** <br/> |Die Einheiten, die im Dialogfeld **Visio-Optionen** auf der Registerkarte **erweitert** in das **Textfeld** **angezeigt** werden (Klicken Sie auf die Registerkarte **Datei** und dann auf **Optionen**).  <br/> |
|**visAngleUnits** <br/> |Die Einheiten, die im Dialogfeld  **Visio-Optionen** auf der Registerkarte **Weitere Optionen** unter **Anzeige** im Feld **Winkel** ausgewählt sind.  <br/> |
|**visDurationUnits** <br/> |Die Einheiten, die im Dialogfeld  **Visio-Optionen** auf der Registerkarte **Weitere Optionen** unter **Anzeige** im Feld **Dauer** ausgewählt sind.  <br/> |
   

