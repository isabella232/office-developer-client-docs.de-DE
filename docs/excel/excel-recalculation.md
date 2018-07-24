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
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790467"
---
# <a name="excel-recalculation"></a>Excel-Neuberechnung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Eine Neuberechnung kann in Microsoft Excel auf verschiedene Weisen ausgelöst werden, beispielsweise durch folgende Aktionen:
  
- Eingeben neuer Daten (wenn Excel sich im automatischen Neuberechnungsmodus befindet, siehe Beschreibung weiter unten in diesem Thema)
    
- Ausgeben der expliziten Anweisung, dass Excel eine Arbeitsmappe ganz oder teilweise neu berechnen soll
    
- Löschen oder Einfügen einer Zeile oder Spalte
    
- Speichern einer Arbeitsmappe bei aktivierter Option **Vor dem Speichern neu berechnen** 
    
- Durchführen bestimmter Autofilter-Aktionen
    
- Doppelklicken auf eine Zeilen- oder Spaltentrennlinie (im automatischen Berechnungsmodus)
    
- Hinzufügen, Bearbeiten oder Löschen eines definierten Namens
    
- Umbenennen eines Arbeitsblatts
    
- Ändern der Position eines Arbeitsblatts in Bezug auf andere Arbeitsblätter
    
- Ausblenden oder Einblenden von Zeilen, nicht aber Spalten
    
> [!NOTE]
> In diesem Thema wird kein Unterschied dazwischen gemacht, ob der Benutzer direkt eine Taste drückt oder mit der Maus klickt und ob die entsprechenden Aufgaben von einem Befehl oder einem Makro ausgeführt werden. Der Benutzer führt den Befehl aus oder veranlasst die Ausführung des Befehls durch eine Aktion, sodass dies als Benutzeraktion angesehen wird. Daher bedeutet bedeutet der Ausdruck "der Benutzer": "der Benutzer oder ein vom Benutzer gestarteter Befehl oder Prozess". 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>Abhängigkeit, geänderte Zellen und neu berechnete Zellen

Die Berechnung von Arbeitsblättern in Excel kann als dreistufiger Prozess betrachtet werden:
  
1. Erstellen einer Abhängigkeitsstruktur
    
2. Erstellen einer Berechnungskette
    
3. Neuberechnen von Zellen
    
Die Abhängigkeitsstruktur informiert Excel darüber, welche Zellen von anderen abhängen, bzw. welche Zellen Vorgänger von anderen sind. Aus dieser Struktur erstellt Excel eine Berechnungskette. Die Berechnungskette listet alle Zellen mit Formeln in der Reihenfolge auf, in der sie berechnet werden sollen. Während der Neuberechnung überarbeitet Excel diese Kette, wenn eine Formel gefunden wird, die von einer noch nicht berechneten Zelle abhängt. In diesem Fall werden die Zelle, die gerade berechnet wird, und die davon abhängigen Zellen in der Kette nach unten verschoben. Aus diesem Grund können Berechnungszeiten in einem Arbeitsblatt, das gerade erst geöffnet wurde, häufig in den ersten paar Berechnungszyklen verbessert werden.
  
Wenn eine �nderung an der Struktur einer Arbeitsmappe vorgenommen wird (z. B. durch Eingabe einer neuen Formel), erstellt Excel die Abh�ngigkeitsstruktur und die Berechnungskette neu. Wenn neue Daten oder neue Formeln eingegeben werden, markiert Excel alle Zellen, die von den neuen Daten abh�ngen, als Zellen, für die eine Neuberechnung erforderlich ist. Auf diese Weise markierte Zellen werden als  *ge�ndert*  bezeichnet. Alle direkt und indirekt abh�ngigen Zellen werden als ge�ndert markiert; dies bedeutet Folgendes: Wenn B1 von A1 und C1 von B1 abh�ngt, werden bei einer �nderung von A1 sowohl B1 als auch C1 als ge�ndert markiert. 
  
Wenn eine Zelle direkt oder indirekt von sich selbst abhängt, erkennt Excel den Zirkelbezug und gibt eine Warnung aus. Dies ist normalerweise eine Fehlerbedingung, die der Benutzer beheben muss, und Excel zeigt sehr hilfreiche grafische und Navigationstools an, die den Benutzer bei der Suche nach dem Ursprung des Zirkelbezugs unterstützen. In einigen Fällen ist diese Bedingung sogar wünschenswert, z. B. wenn Sie eine iterative Berechnung durchführen möchten, bei der der Startpunkt der jeweils nächsten Iteration das Ergebnis der vorherigen Iteration ist. Excel unterstützt die Steuerung von iterativen Berechnungen über das Dialogfeld mit Berechnungsoptionen.
  
Nachdem Zellen als geändert markiert wurden, wird bei der nächsten Neuberechnung der Inhalt jeder geänderten Zelle von Excel erneut ausgewertet, und zwar in der von der Berechnungskette vorgegebenen Reihenfolge. Für das vorherige Beispiel bedeutet dies, dass zuerst B1 und dann C1 ausgewertet wird. Diese Neuberechnung findet im automatischen Neuberechnungsmodus unmittelbar nach dem Markieren der Zellen als geändert statt, andernfalls erst später.
  
Ab Microsoft Excel 2002 unterst�tzt das **Range**-Objekt in Microsoft Visual Basic for Applications (VBA) die **Range.Dirty**-Methode, die Zellen mit der Markierung versieht, dass eine Berechung erforderlich ist. Wenn diese Methode zusammen mit der **Range.Calculate**-Methode verwendet wird (siehe n�chster Abschnitt), wird die erzwungene Neuberechnung von Zellen in einem angegebenen Bereich aktiviert. Dies ist bei der Durchf�hrung einer eingeschr�nkten Berechnung im manuellen Berechnungsmodus w�hrend eines Makros hilfreich, um zu vermeiden, dass unn�tigerweise Zellen berechnet werden, die nicht mit der Makrofunktion in Zusammenhang stehen. Berechnungsmethoden für Bereiche stehen in der C-API nicht zur Verf�gung. 
  
In Excel 2002 und früheren Versionen wurde von Excel für jedes Arbeitsblatt in jeder geöffneten Arbeitsmappe eine Berechnungskette erstellt. Dies führte dazu, dass die Verarbeitung von Verknüpfungen zwischen Arbeitsblättern ziemlich kompliziert war, und erforderte einige Sorgfalt, um eine effiziente Neuberechnung sicherzustellen. Insbesondere sollten Sie in Excel 2000 arbeitsblattübergreifende Abhängigkeiten möglichst vermeiden und Arbeitsblätter in alphabetischer Reihenfolge benennen, sodass Arbeitsblätter, die von anderen Arbeitsblättern abhängig sind, alphabetisch nach den Arbeitsblättern kommen, von denen sie abhängen.
  
In Excel 2007 wurde die Logik verbessert und erm�glicht die Neuberechnung in mehreren Threads, sodass Abschnitte der Berechnungskette nicht voneinander abh�ngig sind und gleichzeitig berechnet werden können. Sie können Excel so konfigurieren, dass mehrere Threads auf einem Computer mit einem einzelnen Prozessor verwendet werden, oder dass ein einzelner Thread auf einem Computer mit mehreren Prozessoren oder Prozessorkernen verwendet wird. 
  
## <a name="asynchronous-user-defined-functions-udfs"></a>Asynchrone benutzerdefinierte Funktionen (User-Defined Functions, UDFs)

Wenn eine Berechnung eine asynchrone UDF erkennt, wird der Status der aktuellen Formel gespeichert, die UDF-Datei gestartet und die Auswertung der restlichen Zellen fortgesetzt. Nach Abschluss der Zellenauswertung wartet Excel auf den Abschluss der asynchronen Funktionen, sofern noch asynchrone Funktionen ausgeführt werden. Nachdem die einzelnen asynchronen Funktionen Ergebnisse gemeldet haben, beendet Excel die Formel und führt dann einen neuen Berechnungslauf durch, um Zellen neu zu berechnen, die die Zelle mit dem Verweis auf die asynchrone Funktion verwenden.
  
## <a name="volatile-and-non-volatile-functions"></a>Veränderliche und nicht veränderliche Funktionen

Excel unterstützt das Konzept einer veränderlichen Funktion; dies ist eine Funktion, deren Wert sich auch dann von einem Moment zum nächsten ändern kann, wenn keines ihrer Argumente (sofern vorhanden) geändert wurde. Excel wertet Zellen mit veränderliche Funktionen und alle untergeordneten Zellen bei jeder Neuberechnung neu aus. Aus diesem Grund kann die Verwendung einer großen Anzahl von veränderlichen Funktionen die Neuberechnung verlangsamen. Verwenden Sie diese Funktionen möglichst selten.
  
Die folgenden Excel-Funktionen sind veränderlich:
  
- **NOW**
    
- **TODAY**
    
- **RANDBETWEEN**
    
- **OFFSET**
    
- **INDIRECT**
    
- **INFO** (abhängig von den Argumenten) 
    
- **CELL** (abhängig von den Argumenten) 
    
- **SUMIF** (abhängig von den Argumenten) 
    
Sowohl VBA als auch die C-API bieten Möglichkeiten, Excel darüber zu informieren, dass eine benutzerdefinierte Funktion (UDF) als veränderlich behandelt werden soll. Bei Verwendung von VBA wird die UDF wie folgt als veränderlich deklariert.
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

Standardmäßig geht Excel davon aus, dass VBA-UDFs nicht veränderlich sind. Excel erfährt erst beim ersten Aufruf einer UDF, dass diese veränderlich ist. Eine veränderliche UDF kann wie in diesem Beispiel gezeigt wieder als nicht veränderlich festgelegt werden.
  
Mit der C-API können Sie eine XLL-Funktion schon vor dem ersten Aufruf als veränderlich registrieren. Außerdem können Sie den veränderlichen Status einer Arbeitsblattfunktion damit ein- und ausschalten.
  
Standardm��ig werden XLL-UDFs, die Bereichsargumente akzeptieren und als Makrovorlagenentsprechungen deklariert sind, von Excel als unver�nderlich behandelt. Sie können diesen Standardstatus beim ersten Aufruf der UDF mit der **xlfVolatile**-Funktion deaktivieren. 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>Berechnungsmodi, Befehle, selektive Neuberechnung und Datentabellen

Excel verfügt über drei Berechnungsmodi:
  
- Automatic
    
- Automatisch außer bei Datentabellen
    
- Manual
    
Im automatischen Berechnungsmodus erfolgt die Neuberechnung nach jeder Dateneingabe und nach bestimmten Ereignissen, wie z. B. den im vorherigen Abschnitt genannten Beispielen. Für sehr große Arbeitsmappen ist die Neuberechnungszeit möglicherweise so lang, dass Benutzer Neuberechnungen auf absolut erforderliche Fälle beschränken müssen. Hierzu unterstützt Excel den manuellen Modus. Der Benutzer kann den Modus über das Excel-Menüsystem oder programmgesteuert mithilfe von VBA, COM oder der C-API auswählen.
  
Datentabellen sind spezielle Strukturen in einem Arbeitsblatt. Der Benutzer richtet zuerst die Berechnung des Ergebnisses auf einem Arbeitsblatt ein. Diese h�ngt von einer oder zwei ver�nderbaren Schl�sseleingaben und anderen Parametern ab. Der Benutzer kann dann eine Tabelle mit Ergebnissen für einen Satz von Werten für eine oder beide Schl�sseleingaben erstellen. Die Tabelle wird mit dem **Assistenten für Datentabellen** erstellt. Nachdem die Tabelle eingerichtet wurde, f�gt Excel die Eingaben einzeln nacheinander in die Berechnung ein und kopiert den resultierenden Wert in die Tabelle. Da eine oder zwei Eingaben verwendet werden können, können Datentabellen ein- oder zweidimensional sein. 
  
Die Neuberechnung von Datentabellen wird etwas anders gehandhabt:
  
- Die Neuberechnung erfolgt asynchron zur normalen Neuberechnung der Arbeitsmappe, sodass die Neuberechnung großer Tabellen länger dauern kann der Vorgang für den Rest der Arbeitsmappe.
    
- Zirkelbezüge sind zulässig. Wenn die zur Ermittlung des Ergebnisses verwendete Berechnung von einem oder mehreren Werten aus der Datentabelle abhängt, gibt Excel keinen Fehler für den Zirkelbezug zurück. 
    
Da Excel die Neuberechnung von Datentabellen anders handhabt und die Berechnung großer Tabellen, die komplexe oder langwierige Berechnungen erfordern, sehr lange dauern kann, haben Sie in Excel die Möglichkeit, die automatische Berechnung von Datentabellen zu deaktivieren. Legen Sie hierzu den Berechnungsmodus auf "Automatisch außer bei Datentabellen" fest. Wenn dieser Berechnungsmodus aktiv ist, drückt der Benutzer F9 oder führt einen entsprechenden Programmiervorgang aus, um die Datentabellen neu zu berechnen.
  
Excel stellt Methoden zur Verfügung, mit denen Sie den Neuberechnungsmodus ändern und die Neuberechnung steuern können. Diese Methoden wurden von Version zu Version verbessert, um eine präzisere Steuerung zu ermöglichen. Die betreffenden Funktionen der C-API entsprechen denen in Excel, Version 5, und bieten daher nicht das Maß an Steuerung, von dem Sie bei Verwendung von VBA in neueren Versionen profitieren. 
  
Diese Methoden werden am häufigsten verwendet, wenn sich Excel im manuellen Berechnungsmodus befindet, und erlauben die selektive Berechnung von Arbeitsmappen, Arbeitsblättern und Bereichen, die vollständige Neuberechnung aller geöffneten Arbeitsmappen und sogar die vollständige Neuerstellung der Abhängigkeitsstruktur und der Berechnungskette.
  
### <a name="range-calculation"></a>Bereichsberechnung

Tastenkombination: keine
  
VBA: **Range.Calculate** (eingef�hrt in Excel 2000, ge�ndert in Excel 2007) und **Range.CalculateRowMajorOrder** (eingef�hrt in Excel 2007) 
  
C-API: nicht unterstützt
  
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
  
C-API: nicht unterstützt
  
- **Alle Modi**
    
    Berechnet nur die geänderten Zellen und ihre abhängigen Zellen innerhalb des angegebenen Arbeitsblatts neu. "Reference" ist der Name des Arbeitsblatts als Zeichenfolge oder die Indexnummer in der entsprechenden Arbeitsmappe.
    
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

Tastenkombination: STRG + ALT + UMSCHALT + F9 (eingeführt in Excel 2002)
  
VBA: **Workbooks(** Reference **).ForceFullCalculation** (eingef�hrt in Excel 2007) 
  
C-API: nicht unterstützt
  
- **Alle Modi**
    
    Bewirkt, dass Excel die Abhängigkeitsstruktur und die Berechnungskette für eine bestimmte Arbeitsmappe neu berechnet, und erzwingt eine Neuberechnung aller Zellen, die Formeln enthalten.
    
### <a name="all-open-workbooks"></a>Alle geöffneten Arbeitsmappen

Tastenkombination: F9
  
VBA: **Application.Calculate**
  
C-API: **xlcCalculateNow**
  
- **Alle Modi**
    
    Berechnet alle Zellen neu, die Excel als geändert markiert hat, d. h. abhängige Elemente von veränderlichen oder geänderten Daten sowie programmgesteuert als geändert markierte Zellen. Im Berechnungsmodus "Automatisch außer bei Datentabellen" werden die Tabellen berechnet, die aktualisiert werden müssen, sowie alle veränderlichen Funktionen und ihre abhängigen Elemente.
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>Neuerstellung der Struktur und erzwungene Berechnung für alle geöffneten Arbeitsmappen

Tastenkombination: STRG + ALT + F9.
  
VBA: **Application.CalculateFull**
  
C-API: nicht unterstützt
  
- **Alle Modi**
    
    Berechnet alle Zellen in allen geöffneten Arbeitsmappen neu. Im Berechnungsmodus "Automatisch außer bei Datentabellen" wird die Neuberechnung der Tabellen erzwungen.
    
## <a name="see-also"></a>Siehe auch



[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Datentypen von Excel verwendet](data-types-used-by-excel.md)
  
[Speicherverwaltung in Excel](memory-management-in-excel.md)
  
[Excel-Programmierkonzepte](excel-programming-concepts.md)

