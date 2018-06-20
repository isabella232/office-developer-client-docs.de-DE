---
title: Datentypen von Excel verwendet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- Registrierung Datentypen [excel 2007], Excel-Datentypen, Zeichenfolgen [Excel 2007], Zahlen [Excel 2007], Datenstrukturen [Excel 2007], Datentypen [Excel 2007]
localization_priority: Normal
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b32a9beb2f77c12e6b6f2c445672c717a2546386
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790402"
---
# <a name="data-types-used-by-excel"></a>Datentypen von Excel verwendet

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel tauscht mehrere ANSI-C/C++-Typen und auch einige Excel-spezifische Datenstrukturen. Diese sind hier erwähnten, um einen Kontext für anderen Abschnitten bereitzustellen, und sie werden ausführlich im Thema [XlfRegister (Formular 1)](xlfregister-form-1.md) . 
  
## <a name="ansi-cc-types"></a>ANSI C/C++-Typen

### <a name="numbers"></a>Zahlen

Alle Versionen von Excel:
  
- 8-Byte-Gleitkommazahl
    
- [signed] Short [Int] &ndash; für **boolesche** Werte und auch Ganzzahlen verwendet 
    
- nicht signierte Short [Int]
    
- [lange signiert] Int
    
### <a name="strings"></a>Zeichenfolgen

Alle Versionen von Excel:
  
- [signed] Char \* &ndash; Null terminierte Byte-Zeichenfolgen mit bis zu 255 Zeichen
    
- nicht signierte Char \* &ndash; Zeichenfolgen mit bis zu 255 Zeichen Länge gezählt Byte
    
Starten in Excel 2007:
  
- nicht signierte kurzfristige \* &ndash; Unicode-Zeichenfolgen von bis zu 32.767 Zeichen, die Null endende oder Länge gezählt werden können
    
Alle Arbeitsblatt Zahlen in Excel werden als Double-Werte gespeichert, sodass es nicht erforderlich ist (und sogar eine kleine Konvertierung Aufwand führt) zum Deklarieren von Add-in-Funktionen als Integer-Typen mit Excel austauschen.
  
Bei Verwendung von Integer-Typen Excel überprüft, ob die Eingaben sind innerhalb der Grenzen des Typs, und sie nicht mit **#NUM!** Falls außerhalb der diese. Die Ausnahme ist, wenn Sie eine Funktion, die ein **Boolean** -Argument mit short int implementiert registrieren In diesem Fall keine Eingaben ungleich NULL ist auf 1 konvertiert, und 0 (null) direkt übergeben wird. 
  
## <a name="excel-specific-data-structures"></a>Excel-spezifische Datenstrukturen

Alle Versionen von Excel:
  
- **FZ** &ndash; ein zweidimensionales Array Gleitkomma-Struktur unterstützt bis zu 65.356 Zeilen durch die maximalen Anzahl Spalten in der angegebenen Version von Excel unterstützt. 
    
- **XLOPER** &ndash; eine mit mehreren Typ Datenstruktur, die alle Arbeitsblatt Datentypen (einschließlich Fehler), ganze Zahlen, Bereich Referenzen, XLM-Fluss Steuerelement Makrovorlage und eine binäre Zentralspeicher-Datentyp darstellen kann. 
    
   > [!NOTE]
   > Zeichenfolgen werden als Zeichenfolgen von bis zu 255 Zeichen Länge gezählt Byte dargestellt. 
  
Starten in Excel 2007:
  
- **FP12** &ndash; ein zweidimensionales Array Gleitkomma-Struktur unterstützen alle Zeilen und Spalten in Excel 2007 starten. 
    
- **XLOPER12** &ndash; eine mit mehreren Typ Datenstruktur, die alle Arbeitsblatt Datentypen (einschließlich Fehler), ganze Zahlen, Bereich Referenzen, XLM-Fluss Steuerelement Makrovorlage und eine binäre Zentralspeicher-Datentyp darstellen kann. 
    
   > [!NOTE]
   > Zeichenfolgen werden als Unicode-Zeichenfolgen von bis zu 32.767 Zeichen Länge gezählt dargestellt. 
  
## <a name="registration-data-type-codes"></a>Typcodes, die Registrierungsdaten

XLL-Funktionen werden mit der C-API-Funktion **XlfRegister**, die als dritte Argument akzeptiert eine Zeichenfolge bestehend aus, die die Typen zurück und Argument codieren registriert. Diese Zeichenfolge enthält auch Informationen, die weist Excel, ob die Funktion veränderliche ist, ist threadsicheren (beginnend in Excel 2007), Makroblatt entspricht, und, ob sie das Ergebnis zurückgibt durch ein Argument direkten ändern.
  
In der folgenden Tabelle ist reproduziert und ausführlicher im Thema [XlfRegister (Formular 1)](xlfregister-form-1.md) . Es ist hier reproduziert, um einen Kontext für den Rest dieses Abschnitts zu gewährleisten. Beispielsweise könnte eine Funktion, die eine Länge gezählt Unicode-Zeichenfolge (beginnend in Excel 2007) akzeptiert als Offlineschalten von einem Typ C % Argument beschrieben werden. 
  
|Datentyp|Übergebener Wert|Übergebener Verweis (Zeiger)|Kommentare|
|:-----|:-----|:-----|:-----|
|Boolean  <br/> |A  <br/> |L  <br/> |Short (0 = False oder 1 = True)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|Char\*  <br/> ||C, F  <br/> |NULL endende ASCII-Byte-Zeichenfolge  <br/> |
|ohne Vorzeichen\*  <br/> ||D, G  <br/> |Länge-ASCII-Byte-Zeichenfolge gezählt  <br/> |
|nicht signierte kurzfristige \* (beginnend in Excel 2007)  <br/> ||C %, F %  <br/> |Zeichenfolge mit NULL terminierte Unicode-Breitzeichen  <br/> |
|nicht signierte kurzfristige \* (beginnend in Excel 2007)  <br/> ||D %, G %  <br/> |Zeichenfolge mit Unicode Breitzeichen Länge gezählt  <br/> |
|nicht signierte Short [Int]  <br/> |H  <br/> ||WORD  <br/> |
|[signed] Short [Int]  <br/> |I  <br/> |M  <br/> |16-bit  <br/> |
|[lange signiert] Int  <br/> |J  <br/> |N  <br/> |32-Bit  <br/> |
|Array  <br/> ||O  <br/> | Als drei Argumente übergeben als Verweis:  <br/>1. short Int \*Zeilen  <br/>2. short Int \*Spalten  <br/>3. Double \*Array  <br/> |
|Array  <br/> (beginnend in Excel 2007)  <br/> ||O %  <br/> | Als drei Argumente übergeben als Verweis:  <br/>1. Int \*Zeilen  <br/>2. Int \*Spalten  <br/>3. Double \*Array  <br/> |
|FZ  <br/> ||K  <br/> |Gleitkommazahl Arraystruktur  <br/> |
|FP12  <br/> (beginnend in Excel 2007)  <br/> ||K %  <br/> |Großes Gitternetz Array Gleitkomma-Struktur  <br/> |
|XLOPER  <br/> ||P  <br/> |Variable vom Typ Arbeitsblattwerte und arrays  <br/> |
|||R  <br/> |Werte, Arrays und Bereich Referenzen  <br/> |
|XLOPER12  <br/> (beginnend in Excel 2007)  <br/> ||Q  <br/> |Variable vom Typ Arbeitsblattwerte und arrays  <br/> |
|||U  <br/> |Werte, Arrays und Bereich Referenzen  <br/> |
   
Die Typen **C %**, **F %**, **D %**, **G %**, **K %**, **O %**, **Q**und **U** alle neu in Microsoft Office Excel 2007 wurden und sind nicht in früheren Versionen unterstützt. Die Zeichenfolgentypen **F**, **F %**, **G**und **G %** werden für Argumente verwendet, die direkte geändert werden. Wenn **XLOPER** oder **XLOPER12** Argumente als Typen **P** oder **Q** registriert werden, konvertiert Excel einzelne Zelle Verweise auf einfache Werte und Verweise auf Arrays mit mehreren Zelle aus, wenn er sie vorbereitet. 
  
**P** und **Q** Typen in Ihrer Funktion, die immer als eine der folgenden Objekttypen eintreffen: **XltypeNum**, **XltypeStr**, **XltypeBool**, **XltypeErr**, **XltypeMulti**, **XltypeMissing**oder **XltypeNil**, aber nicht **XltypeRef** oder **XltypeSRef** , da diese immer aufgehoben werden. 
  
Typ **O**, die drei Argumente auf dem Stapel wirklich ist, wurde für die Kompatibilität mit Fortran DLLs eingeführt, in dem Argumente als Verweis übergeben werden. Es kann nicht verwendet werden, um einen Wert außer deklarieren das Argument als Rückgabewert ändern-in-Place und platzieren die Ergebnisse in der referenzierten Werte zurückzugeben. Geben Sie **O %** erweitert Typ **O** in Excel 2007, damit es Arrays zugreifen kann, die größer als das Raster Office Excel 2003 Bereiche abzudecken. 
  
## <a name="see-also"></a>Siehe auch

- [XlfRegister (Formular 1)](xlfregister-form-1.md)
- [Excel-Programmierkonzepte](excel-programming-concepts.md)
- [Excel XLL-SDK-API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)

