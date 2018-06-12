---
title: Excel-Neuberechnung
manager: kelbow
ms.date: 03/09/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
localization_priority: Normal
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790467"
---
# <a name="excel-recalculation"></a>Excel-Neuberechnung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Eine Neuberechnung kann in Microsoft Excel auf verschiedene Weisen ausgel�st werden, beispielsweise durch folgende Aktionen:
  
- Eingeben neuer Daten (wenn Excel sich im automatischen Neuberechnungsmodus befindet, siehe Beschreibung weiter unten in diesem Thema)
    
- Ausgeben der expliziten Anweisung, dass Excel eine Arbeitsmappe ganz oder teilweise neu berechnen soll
    
- L�schen oder Einf�gen einer Zeile oder Spalte
    
- Speichern einer Arbeitsmappe bei aktivierter Option **Vor dem Speichern neu berechnen** 
    
- Durchf�hren bestimmter Autofilter-Aktionen
    
- Doppelklicken auf eine Zeilen- oder Spaltentrennlinie (im automatischen Berechnungsmodus)
    
- Hinzuf�gen, Bearbeiten oder L�schen eines definierten Namens
    
- Umbenennen eines Arbeitsblatts
    
- �ndern der Position eines Arbeitsblatts in Bezug auf andere Arbeitsbl�tter
    
- Ausblenden oder Einblenden von Zeilen, nicht aber Spalten
    
> [!NOTE]
> [!HINWEIS] In diesem Thema wird kein Unterschied dazwischen gemacht, ob der Benutzer direkt eine Taste dr�ckt oder mit der Maus klickt und ob die entsprechenden Aufgaben von einem Befehl oder einem Makro ausgef�hrt werden. Der Benutzer f�hrt den Befehl aus oder veranlasst die Ausf�hrung des Befehls durch eine Aktion, sodass dies als Benutzeraktion angesehen wird. Daher bedeutet bedeutet der Ausdruck "der Benutzer": "der Benutzer oder ein vom Benutzer gestarteter Befehl oder Prozess". 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>Abh�ngigkeit, ge�nderte Zellen und neu berechnete Zellen

Die Berechnung von Arbeitsbl�ttern in Excel kann als dreistufiger Prozess betrachtet werden:
  
1. Erstellen einer Abh�ngigkeitsstruktur
    
2. Erstellen einer Berechnungskette
    
3. Neuberechnen von Zellen
    
Die Abh�ngigkeitsstruktur informiert Excel dar�ber, welche Zellen von anderen abh�ngen, bzw. welche Zellen Vorg�nger von anderen sind. Aus dieser Struktur erstellt Excel eine Berechnungskette. Die Berechnungskette listet alle Zellen mit Formeln in der Reihenfolge auf, in der sie berechnet werden sollen. W�hrend der Neuberechnung �berarbeitet Excel diese Kette, wenn eine Formel gefunden wird, die von einer noch nicht berechneten Zelle abh�ngt. In diesem Fall werden die Zelle, die gerade berechnet wird, und die davon abh�ngigen Zellen in der Kette nach unten verschoben. Aus diesem Grund k�nnen Berechnungszeiten in einem Arbeitsblatt, das gerade erst ge�ffnet wurde, h�ufig in den ersten paar Berechnungszyklen verbessert werden.
  
Wenn eine �nderung an der Struktur einer Arbeitsmappe vorgenommen wird (z. B. durch Eingabe einer neuen Formel), erstellt Excel die Abh�ngigkeitsstruktur und die Berechnungskette neu. Wenn neue Daten oder neue Formeln eingegeben werden, markiert Excel alle Zellen, die von den neuen Daten abh�ngen, als Zellen, f�r die eine Neuberechnung erforderlich ist. Auf diese Weise markierte Zellen werden als  *ge�ndert*  bezeichnet. Alle direkt und indirekt abh�ngigen Zellen werden als ge�ndert markiert; dies bedeutet Folgendes: Wenn B1 von A1 und C1 von B1 abh�ngt, werden bei einer �nderung von A1 sowohl B1 als auch C1 als ge�ndert markiert. 
  
Wenn eine Zelle direkt oder indirekt von sich selbst abh�ngt, erkennt Excel den Zirkelbezug und gibt eine Warnung aus. Dies ist normalerweise eine Fehlerbedingung, die der Benutzer beheben muss, und Excel zeigt sehr hilfreiche grafische und Navigationstools an, die den Benutzer bei der Suche nach dem Ursprung des Zirkelbezugs unterst�tzen. In einigen F�llen ist diese Bedingung sogar w�nschenswert, z.�B. wenn Sie eine iterative Berechnung durchf�hren m�chten, bei der der Startpunkt der jeweils n�chsten Iteration das Ergebnis der vorherigen Iteration ist. Excel unterst�tzt die Steuerung von iterativen Berechnungen �ber das Dialogfeld mit Berechnungsoptionen.
  
Nachdem Zellen als ge�ndert markiert wurden, wird bei der n�chsten Neuberechnung der Inhalt jeder ge�nderten Zelle von Excel erneut ausgewertet, und zwar in der von der Berechnungskette vorgegebenen Reihenfolge. F�r das vorherige Beispiel bedeutet dies, dass zuerst B1 und dann C1 ausgewertet wird. Diese Neuberechnung findet im automatischen Neuberechnungsmodus unmittelbar nach dem Markieren der Zellen als ge�ndert statt, andernfalls erst sp�ter.
  
Ab Microsoft Excel 2002 unterst�tzt das **Range**-Objekt in Microsoft Visual Basic for Applications (VBA) die **Range.Dirty**-Methode, die Zellen mit der Markierung versieht, dass eine Berechung erforderlich ist. Wenn diese Methode zusammen mit der **Range.Calculate**-Methode verwendet wird (siehe n�chster Abschnitt), wird die erzwungene Neuberechnung von Zellen in einem angegebenen Bereich aktiviert. Dies ist bei der Durchf�hrung einer eingeschr�nkten Berechnung im manuellen Berechnungsmodus w�hrend eines Makros hilfreich, um zu vermeiden, dass unn�tigerweise Zellen berechnet werden, die nicht mit der Makrofunktion in Zusammenhang stehen. Berechnungsmethoden f�r Bereiche stehen in der C-API nicht zur Verf�gung. 
  
In Excel 2002 und fr�heren Versionen wurde von Excel f�r jedes Arbeitsblatt in jeder ge�ffneten Arbeitsmappe eine Berechnungskette erstellt. Dies f�hrte dazu, dass die Verarbeitung von Verkn�pfungen zwischen Arbeitsbl�ttern ziemlich kompliziert war, und erforderte einige Sorgfalt, um eine effiziente Neuberechnung sicherzustellen. Insbesondere sollten Sie in Excel 2000 arbeitsblatt�bergreifende Abh�ngigkeiten m�glichst vermeiden und Arbeitsbl�tter in alphabetischer Reihenfolge benennen, sodass Arbeitsbl�tter, die von anderen Arbeitsbl�ttern abh�ngig sind, alphabetisch nach den Arbeitsbl�ttern kommen, von denen sie abh�ngen.
  
In Excel 2007 wurde die Logik verbessert und erm�glicht die Neuberechnung in mehreren Threads, sodass Abschnitte der Berechnungskette nicht voneinander abh�ngig sind und gleichzeitig berechnet werden k�nnen. Sie k�nnen Excel so konfigurieren, dass mehrere Threads auf einem Computer mit einem einzelnen Prozessor verwendet werden, oder dass ein einzelner Thread auf einem Computer mit mehreren Prozessoren oder Prozessorkernen verwendet wird. 
  
## <a name="asynchronous-user-defined-functions-udfs"></a>Asynchrone benutzerdefinierte Funktionen (User-Defined Functions, UDFs)

Wenn eine Berechnung eine asynchrone UDF erkennt, wird der Status der aktuellen Formel gespeichert, die UDF-Datei gestartet und die Auswertung der restlichen Zellen fortgesetzt. Nach Abschluss der Zellenauswertung wartet Excel auf den Abschluss der asynchronen Funktionen, sofern noch asynchrone Funktionen ausgef�hrt werden. Nachdem die einzelnen asynchronen Funktionen Ergebnisse gemeldet haben, beendet Excel die Formel und f�hrt dann einen neuen Berechnungslauf durch, um Zellen neu zu berechnen, die die Zelle mit dem Verweis auf die asynchrone Funktion verwenden.
  
## <a name="volatile-and-non-volatile-functions"></a>Ver�nderliche und nicht ver�nderliche Funktionen

Excel unterst�tzt das Konzept einer ver�nderlichen Funktion; dies ist eine Funktion, deren Wert sich auch dann von einem Moment zum n�chsten �ndern kann, wenn keines ihrer Argumente (sofern vorhanden) ge�ndert wurde. Excel wertet Zellen mit ver�nderliche Funktionen und alle untergeordneten Zellen bei jeder Neuberechnung neu aus. Aus diesem Grund kann die Verwendung einer gro�en Anzahl von ver�nderlichen Funktionen die Neuberechnung verlangsamen. Verwenden Sie diese Funktionen m�glichst selten.
  
Die folgenden Excel-Funktionen sind ver�nderlich:
  
- **NOW**
    
- **TODAY**
    
- **RANDBETWEEN**
    
- **OFFSET**
    
- **INDIRECT**
    
- **INFO** (abh�ngig von den Argumenten) 
    
- **CELL** (abh�ngig von den Argumenten) 
    
- **SUMMEWENN** (in Abhängigkeit vom Argumente) 
    
Sowohl VBA als auch die C-API bieten M�glichkeiten, Excel dar�ber zu informieren, dass eine benutzerdefinierte Funktion (UDF) als ver�nderlich behandelt werden soll. Bei Verwendung von VBA wird die UDF wie folgt als ver�nderlich deklariert.
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

Standardm��ig geht Excel davon aus, dass VBA-UDFs nicht ver�nderlich sind. Excel erf�hrt erst beim ersten Aufruf einer UDF, dass diese ver�nderlich ist. Eine ver�nderliche UDF kann wie in diesem Beispiel gezeigt wieder als nicht ver�nderlich festgelegt werden.
  
Mit der C-API k�nnen Sie eine XLL-Funktion schon vor dem ersten Aufruf als ver�nderlich registrieren. Au�erdem k�nnen Sie den ver�nderlichen Status einer Arbeitsblattfunktion damit ein- und ausschalten.
  
Standardm��ig werden XLL-UDFs, die Bereichsargumente akzeptieren und als Makrovorlagenentsprechungen deklariert sind, von Excel als unver�nderlich behandelt. Sie k�nnen diesen Standardstatus beim ersten Aufruf der UDF mit der **xlfVolatile**-Funktion deaktivieren. 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>Berechnungsmodi, Befehle, selektive Neuberechnung und Datentabellen

Excel verf�gt �ber drei Berechnungsmodi:
  
- Automatisch
    
- Automatisch au�er bei Datentabellen
    
- Manuell
    
Im automatischen Berechnungsmodus erfolgt die Neuberechnung nach jeder Dateneingabe und nach bestimmten Ereignissen, wie z.�B. den im vorherigen Abschnitt genannten Beispielen. F�r sehr gro�e Arbeitsmappen ist die Neuberechnungszeit m�glicherweise so lang, dass Benutzer Neuberechnungen auf absolut erforderliche F�lle beschr�nken m�ssen. Hierzu unterst�tzt Excel den manuellen Modus. Der Benutzer kann den Modus �ber das Excel-Men�system oder programmgesteuert mithilfe von VBA, COM oder der C-API ausw�hlen.
  
Datentabellen sind spezielle Strukturen in einem Arbeitsblatt. Der Benutzer richtet zuerst die Berechnung des Ergebnisses auf einem Arbeitsblatt ein. Diese h�ngt von einer oder zwei ver�nderbaren Schl�sseleingaben und anderen Parametern ab. Der Benutzer kann dann eine Tabelle mit Ergebnissen f�r einen Satz von Werten f�r eine oder beide Schl�sseleingaben erstellen. Die Tabelle wird mit dem **Assistenten f�r Datentabellen** erstellt. Nachdem die Tabelle eingerichtet wurde, f�gt Excel die Eingaben einzeln nacheinander in die Berechnung ein und kopiert den resultierenden Wert in die Tabelle. Da eine oder zwei Eingaben verwendet werden k�nnen, k�nnen Datentabellen ein- oder zweidimensional sein. 
  
Die Neuberechnung von Datentabellen wird etwas anders gehandhabt:
  
- Die Neuberechnung erfolgt asynchron zur normalen Neuberechnung der Arbeitsmappe, sodass die Neuberechnung gro�er Tabellen l�nger dauern kann der Vorgang f�r den Rest der Arbeitsmappe.
    
- Zirkelbez�ge sind zul�ssig. Wenn die zur Ermittlung des Ergebnisses verwendete Berechnung von einem oder mehreren Werten aus der Datentabelle abh�ngt, gibt Excel keinen Fehler f�r den Zirkelbezug zur�ck. 
    
Da Excel die Neuberechnung von Datentabellen anders handhabt und die Berechnung gro�er Tabellen, die komplexe oder langwierige Berechnungen erfordern, sehr lange dauern kann, haben Sie in Excel die M�glichkeit, die automatische Berechnung von Datentabellen zu deaktivieren. Legen Sie hierzu den Berechnungsmodus auf "Automatisch au�er bei Datentabellen" fest. Wenn dieser Berechnungsmodus aktiv ist, dr�ckt der Benutzer F9 oder f�hrt einen entsprechenden Programmiervorgang aus, um die Datentabellen neu zu berechnen.
  
Excel stellt Methoden zur Verf�gung, mit denen Sie den Neuberechnungsmodus �ndern und die Neuberechnung steuern k�nnen. Diese Methoden wurden von Version zu Version verbessert, um eine pr�zisere Steuerung zu erm�glichen. Die betreffenden Funktionen der C-API entsprechen denen in Excel, Version 5, und bieten daher nicht das Ma� an Steuerung, von dem Sie bei Verwendung von VBA in neueren Versionen profitieren. 
  
Diese Methoden werden am h�ufigsten verwendet, wenn sich Excel im manuellen Berechnungsmodus befindet, und erlauben die selektive Berechnung von Arbeitsmappen, Arbeitsbl�ttern und Bereichen, die vollst�ndige Neuberechnung aller ge�ffneten Arbeitsmappen und sogar die vollst�ndige Neuerstellung der Abh�ngigkeitsstruktur und der Berechnungskette.
  
### <a name="range-calculation"></a>Bereichsberechnung

Tastenkombination: keine
  
VBA: **Range.Calculate** (eingef�hrt in Excel 2000, ge�ndert in Excel 2007) und **Range.CalculateRowMajorOrder** (eingef�hrt in Excel 2007) 
  
C-API: nicht unterst�tzt
  
- **Manueller Modus**
    
    Berechnet nur die Zellen im angegebenen Bereich neu, unabh�ngig davon, ob sie ge�ndert wurden oder nicht. Das Verhalten der **Range.Calculate**-Methode wurde in Excel 2007 ge�ndert; das alte Verhalten wird jedoch noch von der **Range.CalculateRowMajorOrder** -Methode unterst�tzt. 
    
- **Modi "Automatisch" und "Automatisch au�er bei Datentabellen"**
    
    Berechnet die Arbeitsmappe neu, erzwingt jedoch keine Neuberechnung des Bereichs oder einer Zelle im Bereich.
    
### <a name="active-worksheet-calculation"></a>Berechnung des aktiven Arbeitsblatts

Tastenkombination: UMSCHALT + F9
  
VBA: **ActiveSheet.Calculate**
  
C-API: **xlcCalculateDocument**
  
- **Alle Modi**
    
    Berechnet nur die Zellen neu, die im aktiven Arbeitsblatt als zu berechnen markiert sind.
    
### <a name="specified-worksheet-calculation"></a>Berechnung des angegebenen Arbeitsblatts

Tastenkombination: keine
  
VBA: **Worksheets(** Reference **).Calculate**
  
C-API: nicht unterst�tzt
  
- **Alle Modi**
    
    Berechnet nur die ge�nderten Zellen und ihre abh�ngigen Zellen innerhalb des angegebenen Arbeitsblatts neu. "Reference" ist der Name des Arbeitsblatts als Zeichenfolge oder die Indexnummer in der entsprechenden Arbeitsmappe.
    
    In Excel 2000 und sp�teren Versionen steht eine **Boolean**-Arbeitsblatteigenschaft zur Verf�gung, die **EnableCalculation**-Eigenschaft. Durch Festlegen dieser Eigenschaft auf **True** von **False** werden alle Zellen im angegebenen Arbeitsblatt als ge�ndert definiert. In automatischen Modi l�st dies au�erdem eine Neuberechnung der gesamten Arbeitsmappe aus. 
    
    Im manuellen Modus bewirkt der folgende Code, dass nur das aktive Blatt neu berechnet wird.
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a>Neuerstellung der Arbeitsmappenstruktur und erzwungene Neuberechnung

Tastenkombination: STRG + ALT + UMSCHALT + F9 (eingef�hrt in Excel 2002)
  
VBA: **Workbooks(** Reference **).ForceFullCalculation** (eingef�hrt in Excel 2007) 
  
C-API: nicht unterst�tzt
  
- **Alle Modi**
    
    Bewirkt, dass Excel die Abh�ngigkeitsstruktur und die Berechnungskette f�r eine bestimmte Arbeitsmappe neu berechnet, und erzwingt eine Neuberechnung aller Zellen, die Formeln enthalten.
    
### <a name="all-open-workbooks"></a>Alle ge�ffneten Arbeitsmappen

Tastenkombination: F9
  
VBA: **Application.Calculate**
  
C-API: **xlcCalculateNow**
  
- **Alle Modi**
    
    Berechnet alle Zellen neu, die Excel als ge�ndert markiert hat, d.�h. abh�ngige Elemente von ver�nderlichen oder ge�nderten Daten sowie programmgesteuert als ge�ndert markierte Zellen. Im Berechnungsmodus "Automatisch au�er bei Datentabellen" werden die Tabellen berechnet, die aktualisiert werden m�ssen, sowie alle ver�nderlichen Funktionen und ihre abh�ngigen Elemente.
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>Neuerstellung der Struktur und erzwungene Berechnung f�r alle ge�ffneten Arbeitsmappen

Tastenkombination: STRG + ALT + F9.
  
VBA: **Application.CalculateFull**
  
C-API: nicht unterst�tzt
  
- **Alle Modi**
    
    Berechnet alle Zellen in allen ge�ffneten Arbeitsmappen neu. Im Berechnungsmodus "Automatisch au�er bei Datentabellen" wird die Neuberechnung der Tabellen erzwungen.
    
## <a name="see-also"></a>Siehe auch



[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Datentypen von Excel verwendet](data-types-used-by-excel.md)
  
[Speicherverwaltung in Excel](memory-management-in-excel.md)
  
[Excel-Programmierkonzepte](excel-programming-concepts.md)

