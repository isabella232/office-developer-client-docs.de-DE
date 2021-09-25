---
title: Von Excel verwendete Datentypen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- Registrierung von Datentypen [Excel 2007]; Excel-Datentypen; Zeichenfolgen [Excel 2007]; Zahlen [Excel 2007]; Datenstrukturen [Excel 2007]; Datentypen [Excel 2007]
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.localizationpriority: high
ms.openlocfilehash: 76cddf8c63c9cba46181e916194f983bcdd6c1f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576737"
---
# <a name="data-types-used-by-excel"></a>Von Excel verwendete Datentypen

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel tauscht mehrere NSI C/C++-Typen und auch einige Excel-spezifische Datenstrukturen aus. Diese werden hier genannt, um einen Kontext für andere Abschnitte zu liefern. Im Thema [xlfRegister (Formular 1)](xlfregister-form-1.md) werden sie ausführlich erläutert. 
  
## <a name="ansi-cc-types"></a>ANSI C/C++-Typen

### <a name="numbers"></a>Zahlen

Alle Versionen von Excel:
  
- 8-Byte-Gleitkommawert mit doppelter Genauigkeit
    
- [signed] short [int] &ndash; verwendet für **boolesche** Werte und auch Ganzzahlen 
    
- unsigned short [int]
    
- [signed long] int
    
### <a name="strings"></a>Zeichenfolgen

Alle Versionen von Excel:
  
- [signed] char \* &ndash;Bytezeichenfolgen mit Null-Terminierung von bis zu 255 Zeichen
    
- unsigned char \* &ndash;Bytezeichenfolgen mit Längenzählung von bis zu 255 Zeichen
    
Ab Excel 2007:
  
- unsigned short \* &ndash; Unicode-Zeichenfolgen von bis zu 32.767 Zeichen, bei denen Null-Terminierung oder Längenzählung möglich ist
    
Alle Arbeitsblattnummern in Excel werden als "Double" gespeichert. Deshalb ist es nicht erforderlich (und führt tatsächlich zu einem kleinen Konvertierungsmehraufwand), bei Excel Add-In-Funktionen als Ganzzahl-Austauschtypen zu deklarieren.
  
Dort, wo Sie Ganzzahltypen verwenden, überprüft Excel, ob die Eingaben die Grenzwerte des Typs einhalten.  Wenn das nicht zutrifft, lautet die Fehlermeldung #NUM!. Die einzige Ausnahme: Wenn Sie eine Funktion zur Verwendung eines **booleschen** Arguments registrieren, das mit "short int" implementiert wurde, wird jede Eingabe von ungleich Null in "1" konvertiert, und Null wird direkt übergeben. 
  
## <a name="excel-specific-data-structures"></a>Excel-spezifische Datenstrukturen

Alle Versionen von Excel:
  
- **FP** &ndash; ist eine zweidimensionale Gleitkomma-Arraystruktur, die bis zu 65.356 Zeilen mal der maximalen Anzahl Spalten unterstützt, die in der jeweiligen Excel-Version unterstützt werden. 
    
- **XLOPER** &ndash;, eine für mehrere Typen geeignete Datenstruktur, die alle Arbeitsblatt-Datentypen (einschließlich Fehlern), Ganzzahlen, Bereichsbezüge, Flusssteuerungstypen für XLM-Makrovorlagen und einen internen Datentyp für binären Speicher darstellen kann. 
    
   > [!NOTE]
   > Zeichenfolgen werden als Bytezeichenfolgen mit Längenzählung von bis zu 255 Zeichen Länge dargestellt. 
  
Ab Excel 2007:
  
- **FP12** &ndash;, eine zweidimensionale Gleitkomma-Arraystruktur, die ab Excel 2007 alle Zeilen und Spalten unterstützt. 
    
- **XLOPER12** &ndash;, eine für mehrere Typen geeignete Datenstruktur, die alle Arbeitsblatt-Datentypen (einschließlich Fehlern), Ganzzahlen, Bereichsbezüge, Flusssteuerungstypen für XLM-Makrovorlagen und einen internen Datentyp für binären Speicher darstellen kann. 
    
   > [!NOTE]
   > Zeichenfolgen werden als Unicode-Zeichenfolgen mit Längenzählung von bis zu 32.767 Zeichen Länge dargestellt. 
  
## <a name="registration-data-type-codes"></a>Registrierungscodes für Datentypen

XLL-Funktionen werden mit der C API-Funktion **xlfRegister** registriert, deren drittes Argument eine Zeichenfolge aus Buchstaben ist, die die Rückgabe- und Argumenttypen codieren. Diese Zeichenfolge enthält auch die Informationen, die Excel mitteilen, ob die Funktion veränderlich, threadsicher (ab Excel 2007) und gleichwertig mit einer Makrovorlage ist und ob sie ihr Ergebnis durch Änderung eines vorhandenen Arguments zurückgibt.
  
Die nachstehende Tabelle wird im Thema [xlfRegister (Formular 1)](xlfregister-form-1.md) reproduziert und ausführlicher erläutert. Sie wird hier wiedergegeben, um einen Kontext für den restlichen Abschnitt zu liefern. So könnte beispielsweise eine Funktion, die eine Unicode-Zeichenfolge mit Längenzählung verwendet (ab Excel 2007), so beschrieben werden: Verwendet ein Argument des Typs "C%". 
  
|Datentyp|Übergabe nach Wert|Übergabe nach Verweis (Zeiger)|Kommentare|
|:-----|:-----|:-----|:-----|
|Boolesch  <br/> |A  <br/> |L  <br/> |short (0=false oder 1=true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |ASCII-Bytezeichenfolge mit Null-Terminierung  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |ASCII-Bytezeichenfolge mit Längenzählung  <br/> |
|unsigned short \* (ab Excel 2007)  <br/> ||C%, F%  <br/> |Unicode-Zeichenfolge für Breitzeichen mit Null-Terminierung  <br/> |
|unsigned short \* (ab Excel 2007)  <br/> ||D%, G%  <br/> |Unicode-Zeichenfolge für Breitzeichen mit Längenzählung  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16-Bit  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32-Bit  <br/> |
|Array  <br/> ||O  <br/> | Als drei Argumente nach Verweis übergeben:  <br/>1. short int \*Zeilen  <br/>2. short int \*Spalten  <br/>3. double \*Array  <br/> |
|Array  <br/> (ab Excel 2007)  <br/> ||O%  <br/> | Als drei Argumente nach Verweis übergeben:  <br/>1. int \*Zeilen  <br/>2. int \*Spalten  <br/>3. double \*Array  <br/> |
|FP  <br/> ||K  <br/> |Gleitkomma-Arraystruktur  <br/> |
|FP12  <br/> (ab Excel 2007)  <br/> ||K%  <br/> |Gleitkomma-Arraystruktur (großes Raster)  <br/> |
|XLOPER  <br/> ||P  <br/> |Variablen-Arbeitsblattwerte und Arrays  <br/> |
|||R  <br/> |Werte, Arrays und Bereichsbezüge  <br/> |
|XLOPER12  <br/> (ab Excel 2007)  <br/> ||Q  <br/> |Variablen-Arbeitsblattwerte und Arrays  <br/> |
|||U  <br/> |Werte, Arrays und Bereichsbezüge  <br/> |
   
Die Typen **C%**, **F%**, **D%**, **G%**, **K%**, **O%**, **Q** und **U** waren in Microsoft Office Excel 2007 alle neu und werden in früheren Versionen nicht unterstützt. Die Zeichenfolgentypen **F**, **F%**, **G** und **G%** werden für Argumente verwendet, die direkt geändert werden. Wenn die Argumente **XLOPER** oder **XLOPER12** als die Typen **P** bzw. **Q** registriert werden, konvertiert Excel bei der Vorbereitung Bezüge auf eine Zelle in einfache Werte und Bezüge auf mehrere Zellen in Arrays. 
  
Die Typen **P** und **Q** gibt es in Ihrer Funktion immer als einen der folgenden Typen: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing** oder **xltypeNil**, aber nicht als **xltypeRef** oder **xltypeSRef** weil diese Typen immer dereferenziert werden. 
  
Typ **O**, bei dem es sich tatsächlich um drei Argumente im Stapel handelt, wurde zwecks Kompatibilität mit Fortran-DLLs eingeführt, bei denen Argumente nach Verweis übergeben werden. Er kann nicht für die Rückgabe eines Werts verwendet werden – außer indem das Argument als Rückgabewert zum direkten Ändern deklariert wird und die Ergebnisse in die referenzierten Werte eingefügt werden. Der Typ **O%** erweitert den Typ **O** in Excel 2007, sodass er auf Arrays zugreifen kann, deren Bereiche größer als das Office Excel 2003-Raster sind. 
  
## <a name="see-also"></a>Siehe auch

- [xlfRegister (Formular 1)](xlfregister-form-1.md)
- [Konzepte der Excel-Programmierung](excel-programming-concepts.md)
- [Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)

