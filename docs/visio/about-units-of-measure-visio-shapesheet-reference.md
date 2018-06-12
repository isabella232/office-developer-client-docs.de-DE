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
ms.openlocfilehash: ce8ad1cdcbdaba713edeb06f4cd949e49f82a311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796379"
---
# <a name="about-units-of-measure-visio-shapesheet-reference"></a>Informationen zu Maßeinheiten (Visio-ShapeSheet-Referenz)

Wenn Sie Felder in Text einfügen oder Formeln erstellen, geben Sie häufig Maßeinheiten für die eingegebenen Werte an.
  
Microsoft Visio wertet das Ergebnis einer Formel unterschiedlich, je nachdem die Zelle, in der Sie die Formel eingeben. Im Allgemeinen erfordern Zellen, die Position der Form, eine Dimension oder eines Winkels darstellen Zahl-Einheit-Paar, der eine Zahl und der qualifizierenden zur Interpretation der Zahl erforderlichen Einheiten besteht. Viele andere Zellen nicht erfordern Einheiten und Auswerten von in eine Zeichenfolge, TRUE oder FALSE oder auf einen Index. Beispielsweise die gleiche Formel, die in die Zelle **FillForegnd** Farbe 5 aus der Zeichnung Farbpalette bedeutet entspricht "TRUE" (und sperrt die Breite des Shapes) in die Zelle LockWidth. 
  
Geben Sie immer eine Maßeinheit an, wenn Sie eine Formel in eine Zelle eingeben, für die ein Bemaßungswert erforderlich ist. Wenn Sie keine Maßeinheit angeben, verwendet Visio die Standardeinheit für diese Zelle. Hierbei kann es sich um Seiteneinheiten, Zeichnungseinheiten, Einheitenoptionen, Einheiten für die Dauer und Winkeleinheiten handeln.
  
## <a name="units-of-measure"></a>Maßeinheiten

Verwenden Sie bei der Angabe von Maßeinheiten in ShapeSheet-Formularen die in der folgenden Liste angegebenen Abkürzungen.
  
|**So geben Sie diese Maßeinheiten an**|**Verwenden Sie**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| Zentimeter  <br/> | cm  <br/> |**VisCentimeters (69)** <br/> |
| Cicero  <br/> | c  <br/> |**VisCiceros (54)** <br/> |
| Datum oder Uhrzeit  <br/> | date  <br/> |**VisDate (40)** <br/> |
| Grad  <br/> | deg  <br/> |**visDegrees lautet (81)** <br/> |
| Didot  <br/> | d  <br/> |**VisDidots (53)** <br/> |
| Vergangene Wochen  <br/> | ew  <br/> |**VisElapsedWeek (43)** <br/> |
| Vergangene Tage  <br/> | ed  <br/> |**VisElapsedDay (44)** <br/> |
| Vergangene Stunden  <br/> | eh  <br/> |**VisElapsedHour (45)** <br/> |
| Vergangene Minuten  <br/> | em  <br/> |**visElapsedMin lautet (46)** <br/> |
| Vergangene Sekunden  <br/> | es  <br/> |**VisElapsedSec (47)** <br/> |
| Fuß  <br/> | ft  <br/> |**VisFeet (66)** <br/> |
| Zoll  <br/> | in  <br/> |**VisInches (65)** <br/> |
| Kilometer  <br/> | km  <br/> |**VisKilometers (72)** <br/> |
| Meter  <br/> | m  <br/> |**VisMeters (71)** <br/> |
| Meilen  <br/> | mi  <br/> |**VisMiles (68)** <br/> |
| Millimeter  <br/> | mm  <br/> |**VisMillimeters (70)** <br/> |
| Minuten  <br/> | '  <br/> |**VisMin (84)** <br/> |
| Nautische Meilen  <br/> | nm  <br/> |**VisNautMiles (76)** <br/> |
| Prozent  <br/> | %  <br/> |**VisPercent (33)** <br/> |
| Pica  <br/> | p  <br/> |**VisPicas (51)** <br/> |
| Punkte  <br/> | pt  <br/> |**visPoints lautet (50)** <br/> |
| Bogenmaß  <br/> | rad  <br/> |**VisRadians (83)** <br/> |
| Sekunden  <br/> | "  <br/> |**VisSec (85)** <br/> |
| Yard  <br/> | yd  <br/> |**VisYards (75)** <br/> |
   
## <a name="compound-units-of-measure"></a>Zusammengesetzte Maßeinheiten

In Formeln können Sie Maßeinheiten für zusammengesetzte Zahlen mit den Abkürzungen aus der folgenden Tabelle angeben. Visio vereinfacht die Ergebnisse und zeigt sie in den zusammengesetzten Einheiten an.
  
Wenn Sie 45,635 ° eingeben, zeigt Visio den äquivalenten Wert beispielsweise als 45° 38' 6".
  
|**So geben Sie Einheiten an**|**Verwenden Sie diese Abkürzung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| Cicero und Didot  <br/> | CICERO/DIDOT  <br/> |**VisCicerosAndDidots (52)** <br/> |
| Grad, Minuten und Sekunden  <br/> | °  <br/> |**VisDegreeMinSec (82)** <br/> |
| Fuß und Zoll  <br/> | FEET/INCH  <br/> |**VisFeetAndInches (67)** <br/> |
| Pica und Punkte  <br/> | PICAPOINTS  <br/> |**VisPicasAndPoints (49)** <br/> |
   
## <a name="fractional-units-of-measure"></a>Maßeinheiten für Bruchzahlen

Sie können die Maßeinheiten für Bruchzahlen angeben, in **der Zelle DrawingScale auf die Anzahl der Lineal Einteilung auswirken, in dem Visio im Zeichnungsfenster angezeigt** . In der Standardeinstellung unterteilt Visio Abstände Zehntelsekunde beim Zeichnen der Lineale. Wenn Sie in **der Zelle DrawingScale** Maßeinheiten für Bruchzahlen verwenden, ist Visio Abstand in der folgenden unterteilt: 
  
- Achtel für *VisInchFrac* und *visMileFrac* 
    
- Zwölftel für  *visFeetAndInches* 
    
Maßeinheiten für Bruchzahlen wirken sich ausschließlich auf die Zelle DrawingScale aus.
  
|**So geben Sie Maßeinheiten für Bruchzahlen an**|**Verwenden Sie diese Abkürzung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| Zoll als Bruchzahlangabe  <br/> | IN_F  <br/> |**VisInchFrac (73)** <br/> |
| Meilen als Bruchzahlen  <br/> | MI_F  <br/> |**VisMileFrac (74)** <br/> |
| Fuß und Zoll  <br/> | FEET/INCH  <br/> |**VisFeetAndInches (67)** <br/> |
   
## <a name="multidimensional-units-of-measure"></a>Mehrdimensionale Maßeinheiten

In Formeln können Sie Maßeinheiten für mehrdimensionale Zahlen mit den Abkürzungen aus der folgenden Tabelle angeben. Visio vereinfacht die Ergebnisse und zeigt sie als mehrdimensionale Einheiten an.
  
|**So geben Sie mehrdimensionale Einheiten an**|**Verwenden Sie diese Abkürzung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| Acre  <br/> | ACRES  <br/> |**VisAcre (36)** <br/> |
| Zentimeter  <br/> | SQ. CM., SQ CM, CM.^2, CM^2  <br/> |**VisCentimeters (69)** <br/> |
| Fuß  <br/> | SQ. FT., SQ FT, FT.^2, FT^2  <br/> |**VisFeet (66)** <br/> |
| Hektar  <br/> | HECTARES, HECTARE, HA., HA  <br/> |**VisHectare (37)** <br/> |
| Zoll  <br/> | SQ. IN., SQ IN, IN.^2, IN^2  <br/> |**VisInches (65)** <br/> |
| Kilometer  <br/> | SQ. KM., SQ KM, KM.^2, KM ^2  <br/> |**VisKilometers (72)** <br/> |
| Meter  <br/> | SQ. M., SQ M, M.^2, M ^2  <br/> |**VisMeters (71)** <br/> |
| Meilen  <br/> | SQ. MI., SQ MI, MI.^2, MI ^2  <br/> |**VisMiles (68)** <br/> |
| Millimeter  <br/> | SQ. MM., SQ MM, MM.^2, MM ^2  <br/> |**VisMillimeters (70)** <br/> |
| Yard  <br/> | SQ. YD., SQ YD, YD.^2, YD^2  <br/> |**VisYards (75)** <br/> |
   
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
| _Einheit_ <br/> |Die Einheiten, in denen _Zahl_ ursprünglich ausgedrückt wurde.  <br/> |
| _Flag_ <br/> |Das Maßsystem, das verwendet werden soll, wenn die Einheit für den impliziten Wert angezeigt wird. Entsprechende Werte finden Sie unten.  <br/> |
   
Der Parameter _Flag_ entspricht einem der folgenden Buchstaben (Groß- oder Kleinbuchstaben) gibt das Maßsystem an, die verwendet werden soll, wenn die Anzeige von impliziten Einheiten angezeigt wird. 
  
|**_Kennzeichnung_**|**Bemaßungssystem**|**Beispiel**|
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
|**visDrawingUnits** <br/> |Die Maßeinheit in der Zelle DrawingScale des Zeichenblatts oder Master-Shapes, das die Zelle enthält.  <br/> |
|**visPageUnits** <br/> |Die im Feld **Maßeinheiten** auf der Registerkarte **Zeichenblatteigenschaft** des Dialogfelds **Seite einrichten** ausgewählten Einheiten (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** ).  <br/> |
|**visTypeUnits** <br/> |Die Einheiten, in **das Textfeld unter **Anzeige** auf der Registerkarte **Erweitert** im Dialogfeld **Visio-Optionen** ** ausgewählt sind (klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf **Optionen**).  <br/> |
|**visAngleUnits** <br/> |Die Einheiten, die im Dialogfeld  **Visio-Optionen** auf der Registerkarte **Weitere Optionen** unter **Anzeige** im Feld **Winkel** ausgewählt sind.  <br/> |
|**visDurationUnits** <br/> |Die Einheiten, die im Dialogfeld  **Visio-Optionen** auf der Registerkarte **Weitere Optionen** unter **Anzeige** im Feld **Dauer** ausgewählt sind.  <br/> |
   

