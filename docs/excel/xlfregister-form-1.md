---
title: xlfRegister (Formular 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfregister-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 167e7be32a7904376e0e40a82965c21d3866e93d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605555"
---
# <a name="xlfregister-form-1"></a>xlfRegister (Formular 1)

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann über einen DLL- oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde. Dies entspricht dem Aufrufen von **REGISTER** aus einer Excel XLM-Makrovorlage. 
  
**xlfRegister** kann in zwei Formen aufgerufen werden: 
  
- xlfRegister (Formular 1): Registriert einen einzelnen Befehl oder eine Funktion.
    
- [xlfRegister (Formular 2):](xlfregister-form-2.md)Lädt und aktiviert eine XLL.
    
In Form 1 aufgerufen, stellt diese Funktion eine DLL-Funktion oder einen Befehl Excel zur Verfügung, legt die Anzahl der Verwendung auf 1 fest und gibt die Registrierungs-ID zurück, die verwendet werden kann, um die Funktion später mithilfe der [XlUDF-](xludf.md) oder **xlfCall-Funktion** aufzurufen. Die Registrierungs-ID wird auch verwendet, um die Registrierung der Funktion mit [xlfUnregister (Formular 1)](xlfunregister-form-1.md)aufzuheben. Wenn die Funktion registriert wurde, erhöht das erneute Aufrufen von **xlfRegister** die Verwendungsanzahl. 
  
Diese Form der Funktion definiert auch einen ausgeblendeten Namen, bei dem es sich um das Argument des Funktionstexts  _pxFunctionText_ handelt und der zur Registrierungs-ID der Funktion oder des Befehls ausgewertet wird. Wenn Sie die Registrierung der Funktion aufheben, löschen Sie diesen Namen mithilfe von [xlfSetName.](xlfsetname.md) Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, int iCount,
    LPXLOPER12 pxModuleText,   LPXLOPER12 pxProcedure,
    LPXLOPER12 pxTypeText,     LPXLOPER12 pxFunctionText,
    LPXLOPER12 pxArgumentText, LPXLOPER12 pxMacroType,
    LPXLOPER12 pxCategory,     LPXLOPER12 pxShortcutText,
    LPXLOPER12 pxHelpTopic,    LPXLOPER12 pxFunctionHelp,
    LPXLOPER12 pxArgumentHelp1, LPXLOPER12 pxArgumentHelp2,
        ...);
```

## <a name="parameters"></a>Parameter

_pxModuleText_ (**xltypeStr**)
  
Der Name der DLL, die die Funktion enthält. Dies kann durch Aufrufen der XLL-only-Funktion [xlGetName](xlgetname.md) abgerufen werden, wenn sich die registrierte Funktion auch innerhalb der derzeit ausgeführten DLL befindet. 
  
_pxProcedure_ (**xltypeStr** oder **xltypeNum**)
  
Wenn es sich um eine Zeichenfolge handelt, wird der Name der funktion aufgerufen, wie sie im DLL-Code angezeigt wird. Wenn es sich um eine Zahl handelt, die Ordnungsexportnummer der aufzurufenden Funktion. Verwenden Sie aus Gründen der Übersichtlichkeit immer das Zeichenfolgenformular.
  
_pxTypeText_ (**xltypeStr**)
  
Eine optionale Zeichenfolge, die die Typen von Argumenten für die Funktion und den Typ des Rückgabewerts der Funktion angibt. Weitere Informationen finden Sie unter "Anmerkungen". Dieses Argument kann für eine eigenständige DLL (XLL) ausgelassen werden, die eine [XlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) oder **xlAutoRegister12** enthält. 
  
> [!NOTE]
> **xlAutoRegister12** wird nur in Excel 2007 unterstützt. 
  
Wenn **xlfRegister** mit diesem Argument nicht aufgerufen wird, ruft Excel **xlAutoRegister** oder **xlAutoRegister12** auf, falls in der angegebenen DLL vorhanden, die dann die Funktion ordnungsgemäß registrieren sollte, indem sie diese Informationen bereitstellt.
  
_pxFunctionText_ (**xltypeStr**)
  
Der Funktionsname, wie er im Funktions-Assistenten angezeigt wird. Dieses Argument ist optional. wenn sie ausgelassen wird, ist die Funktion nicht im Funktions-Assistenten verfügbar und kann nur mithilfe der **CALL-Funktion** mithilfe der Funktionsregistrierungs-ID aus einem XLM-Makroblatt aufgerufen werden. Daher sollten Sie dieses Argument bei der normalen Verwendung von Arbeitsblättern nach Bedarf behandeln. 
  
_pxArgumentText_ (**xltypeStr**)
  
Eine optionale Textzeichenfolge, die die Argumente für die Funktion beschreibt. Dies wird dem Benutzer im Funktions-Assistenten angezeigt. Wenn sie ausgelassen wird, erstellt Excel grundlegende Beschreibungen aus _pxTypeText_.
  
_pxMacroType_ (**xltypeNum** oder **xltypeInt**)
  
Ein optionales Argument, das den Typ des XLL-Einstiegspunkts angibt. Der Standardwert ist 1, wenn er nicht angegeben wird.
  
|||||
|:-----|:-----|:-----|:-----|
| _pxMacroType-Wert_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Kann aus einem Arbeitsblatt aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Kann aus einem Makroblatt aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|Kann aus einer definierten Namensdefinition aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|Kann aus einem bedingten Formatausdruck aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Aufgelistet im Funktions-Assistenten für Arbeitsblattfunktionen  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Aufgelistet im Funktions-Assistenten für Makrovorlagenfunktionen  <br/> |Nein  <br/> |Ja  <br/> |Ja  <br/> |
   
In der Praxis sollten Sie 1 für Arbeitsblattfunktionen verwenden, 1 für äquivalente Makrovorlagenfunktionen (registriert als **#** Typ), die Sie aus dem Arbeitsblatt aufrufen möchten, und 2 für Befehle. 
  
> [!NOTE]
> XLL-Befehle werden ausgeblendet und nicht in Dialogfeldern zum Ausführen von Makros angezeigt, obwohl ihre Namen überall eingegeben werden können, wo ein gültiger Befehlsname erforderlich ist. 
  
_pxCategory_ (**xltypeStr** oder **xltypeNum**)
  
Ein optionales Argument, mit dem Sie angeben können, zu welcher Kategorie die neue Funktion oder der neue Befehl gehören soll. Der Funktions-Assistent teilt Funktionen nach Typ (Kategorie). Sie können einen Kategorienamen oder eine sequenzielle Zahl angeben, wobei die Zahl die Position ist, an der die Kategorie im Funktions-Assistenten angezeigt wird. Weitere Informationen finden Sie im Abschnitt "Kategorienamen". Wenn sie ausgelassen wird, wird die Benutzerdefinierte Kategorie angenommen.
  
_pxShortcutText_ (**xltypeStr**)
  
Eine Zeichenfolge mit einem Zeichen, bei der die Groß-/Kleinschreibung beachtet wird und die den diesem Befehl zugewiesenen Steuerelementschlüssel angibt. Beispielsweise weist "A" diesen Befehl CONTROL+UMSCHALT+A zu. Dieses Argument ist optional und wird nur für Befehle verwendet.
  
_pxHelpTopic_ (**xltypeStr**)
  
Ein optionaler Verweis auf die Hilfedatei (CHM oder HLP), die angezeigt werden soll, wenn der Benutzer auf die Hilfeschaltfläche klickt (wenn Ihre benutzerdefinierte Funktion angezeigt wird). Kann im Formular  `filepath!HelpContextID` oder  `https://address/path_to_file_in_site!0` . Beide Teile vor und nach dem "!" sind erforderlich.  *HelpContextID* darf keine einfachen Anführungszeichen enthalten und wird durch Excel in eine ganze Zahl ohne Vorzeichen mit einer Länge von 4 Byte in Dezimalform konvertiert. Wenn Sie das URL-Formular verwenden, öffnet Excel nur die referenzierte Hilfedatei. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Eine optionale Zeichenfolge, die Ihre benutzerdefinierte Funktion beschreibt, wenn sie im Funktions-Assistenten ausgewählt wird.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Optional. Die erste Zeichenfolge, die die benutzerdefinierten Argumente der Funktion beschreibt, wenn die Funktion im Funktions-Assistenten ausgewählt wird. In Excel 2003 und früheren Versionen kann **xlfRegister** maximal 30 Argumente verwenden, sodass Sie diese Hilfe nur für die ersten 20 Ihrer Funktionsargumente bereitstellen können. Ab Excel 2007 kann **xlfRegister** bis zu 255 Argumente verwenden, sodass Sie diese Hilfe für bis zu 245 Funktionsparameter bereitstellen können. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn die Registrierung erfolgreich war, gibt diese Funktion die Register-ID der Funktion (**xltypeNum**) zurück, die in Aufrufen von **xlUDF** und **xlfUnregister** in einer DLL oder mit **CALL** und **UNREGISTER** in einem XLM-Makroblatt verwendet werden kann. Andernfalls wird ein #VALUE zurückgegeben. zurück. 
  
## <a name="remarks"></a>HinwBemerkungeneise

### <a name="data-types"></a>Datentypen

Das  _Argument pxTypeText_ gibt den Datentyp des Rückgabewerts und die Datentypen aller Argumente für die DLL-Funktion oder Coderessource an. Das erste Zeichen von  _pxTypeText_ gibt den Datentyp des Rückgabewerts an. Die verbleibenden Zeichen geben die Datentypen aller Argumente an. Beispielsweise würde eine DLL-Funktion, die eine Gleitkommazahl zurückgibt und eine ganze Zahl und eine Gleitkommazahl als Argumente verwendet, "BIB" für das  _Argument pxTypeText_ erfordern. 
  
Die Datentypen und Strukturen, die von Excel zum Austauschen von Daten mit XLLs verwendet werden, sind in den folgenden beiden Tabellen zusammengefasst.
  
In der ersten Tabelle sind die Typen aufgeführt, die in allen Versionen von Excel unterstützt werden.
  
|**Datentyp**|**Übergabe nach Wert**|**Übergabe nach Verweis (Zeiger)**|**Kommentare**|
|:-----|:-----|:-----|:-----|
|Boolesch  <br/> |A  <br/> |L  <br/> |short [int] (0=false oder 1=true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |ASCII-Bytezeichenfolge mit Null-Terminierung  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Gezählte ASCII-Bytezeichenfolge  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||16-Bit-WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16-Bit-Ganzzahl mit Vorzeichen  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32-Bit-Ganzzahl mit Vorzeichen  <br/> |
|FP  <br/> ||K  <br/> |Gleitkomma-Arraystruktur  <br/> |
|Array  <br/> ||O  <br/> |Es werden drei Argumente übergeben:<br/>- unsigned short int \*<br/>- unsigned short int \*<br/>- double []  <br/> |
|XLOPER  <br/> ||P  <br/> |Variablen-Arbeitsblattwerte und Arrays  <br/> |
|||R  <br/> |Werte, Arrays und Bereichsbezüge  <br/> |
   
In Excel 2007 wurden die folgenden Datentypen eingeführt, um die größeren Raster und langen Unicode-Zeichenfolgen zu unterstützen.
  
|**Datentyp**|**Übergabe nach Wert**|**Übergabe nach Verweis (Zeiger)**|**Kommentare**|
|:-----|:-----|:-----|:-----|
|unsigned short \*  <br/> ||C%, F%  <br/> |Mit Null endende Unicode-Zeichenfolge mit breitem Zeichen  <br/> |
|unsigned short \*  <br/> ||D%, G%  <br/> |Unicode-Zeichenfolge mit breitem Zeichen gezählt  <br/> |
|FP12  <br/> ||K%  <br/> |Größere Raster-Gleitkommaarraystruktur  <br/> |
|Array  <br/> ||O%  <br/> |Es werden drei Argumente übergeben:<br/>- signed \* int/ RW \*<br/>- signed \* int/COL \*<br/>- double []  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Variablen-Arbeitsblattwerte und Arrays  <br/> |
|||U  <br/> |Werte, Arrays und Bereichsbezüge  <br/> |
   
Ab Excel 2010 wurden die folgenden Datentypen eingeführt:
  
|**Datentyp**|**Übergabe nach Wert**|**Übergabe nach Verweis (Zeiger)**|**Kommentare**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |Das asynchrone Handle wird verwendet, um einen ausstehenden asynchronen Funktionsaufruf durch Excel und die XLL nachzuverfolgen. Das Vorhandensein des Parametertyps in der Typzeichenfolge bestimmt die Funktion auch als asynchron. Weitere Informationen zu asynchronen Funktionen finden Sie unter ["Asynchrone User-Defined Funktionen".](asynchronous-user-defined-functions.md)  <br/> |
   
Die Zeichenfolgentypen **F**, **F%**, **G** und **G%** werden für Argumente verwendet, die direkt geändert werden. 
  
Beachten Sie beim Arbeiten mit den in der vorherigen Tabelle angezeigten Datentypen Folgendes:
  
- Die C-Sprachdeklarationen gehen davon aus, dass Ihr Compiler standardmäßig 8-Byte-Doubles, 2-Byte-Ganzzahlen und 4-Byte-Ganzzahlen verwendet.
    
- Alle Funktionen in DLLs und Coderessourcen werden mithilfe der **aufrufkonvention __stdcall** aufgerufen. 
    
- Jede Funktion, die einen Datentyp nach Verweis zurückgibt, d. h. einen Zeiger auf einen Wert zurückgibt, kann sicher einen NULL-Zeiger zurückgeben. Excel interpretiert einen NULL-Zeiger als #NUM! zurück.
    
## <a name="additional-data-type-information"></a>Zusätzliche Datentypinformationen

Dieser Abschnitt enthält ausführliche Informationen zu den Datentypen **E**, **F**, **F%**, **G**, **G%**, **K**, **O**, **P**, **Q**, **R** und **U** sowie weitere Informationen zum _Argument pxTypeText._ 
  
### <a name="e-data-type"></a>E-Datentyp

Excel erwartet eine DLL mit dem Datentyp E, um Zeiger an Gleitkommazahlen im Stapel zu übergeben. Dies kann probleme mit einigen Sprachen (z. B. Borland C++) verursachen, die davon ausgehen, dass die Zahl an den Koprozessor-Emulatorstapel übergeben wird. Die Problemumgehung besteht darin, einen Zeiger auf die Nummer im Coprozessorstapel zu übergeben. Das folgende Beispiel zeigt, wie Sie einen Double aus Borland C++ zurückgeben.
  
```cpp
typedef double * lpDbl;
extern "C" lpDbl __stdcall AddDbl(double D1,
    double D2, WORD npDbl)
{
    lpDbl Result;
    Result = (lpDbl)MK_FP(_SS, npDbl);
    *Result = D1 + D2;
    return (Result);
}
```

### <a name="f-f-g-and-g-data-types"></a>F-, F%-, G- und G%-Datentypen

Mit den Datentypen **F,** **F%**, **G** und **G%** kann eine Funktion einen Zeichenfolgenpuffer ändern, der von Excel zugewiesen wird. Wenn der Rückgabewerttypcode einer dieser Typen ist, ignoriert Excel den von der Funktion zurückgegebenen Wert. Stattdessen durchsucht Excel die Liste der Funktionsargumente nach dem ersten entsprechenden Datentyp (**F**, **F%**, **G** oder **G%**) und verwendet dann den aktuellen Inhalt des zugeordneten Zeichenfolgenpuffers als Rückgabewert. Alle Versionen von Excel weisen F- **und** **G** ASCII-Zeichenfolgen 256 Bytes zu, und ab Excel 2007 werden 65.536 Bytes zugewiesen, ausreichend für 32.768 Unicode-Zeichen, für **F%** und **G%** Unicode-Zeichenfolgen. Denken Sie daran, dass die Puffer ein Zählungszeichen (Typen **G** und **G%**) oder ein Nullendpunktzeichen (Typen **F** und **F%**) enthalten müssen, damit die tatsächliche maximale Zeichenfolgenlänge 255 und 32.767 beträgt. Unicode-Zeichenfolgen und somit die Argumente **F%** und **G%** sind nur über die C-API in Excel verfügbar. 
  
### <a name="k-and-k-data-types"></a>K- und K%-Datentypen

Die Datentypen **K** **und K%** verwenden Zeiger auf die FP- bzw. FP12-Strukturen variabler Größe. Diese Strukturen sind in XLLCALL.H definiert. FP12-Strukturen und somit Die **K%-Argumente** werden erst ab Excel 2007 unterstützt. 
  
### <a name="o-and-o-data-types"></a>O- und O%-Datentypen

Die  O- und **O%-Datentypen** können nur für Argumente und nicht für Rückgabewerte verwendet werden, obwohl Werte zurückgegeben werden können, indem **ein** O- oder **O%-Typargument** direkt geändert wird. Jedes Element übergibt drei Elemente: einen Zeiger auf die Anzahl der Zeilen in einem Array, einen Zeiger auf die Anzahl der Spalten in einem Array und einen Zeiger auf ein zweidimensionales Array von Gleitkommazahlen. 
  
Um ein Array zu ändern, das vom O- oder O%-Datentyp übergeben wird, können Sie ">O" oder ">O%" als  _pxTypeText-Argument_ verwenden. Weitere Informationen zum Ändern eines Arrays finden Sie im Abschnitt "Modifying in Place: Functions Declared as Void" in diesem Thema. 
  
Der **O-Datentyp** wurde für die direkte Kompatibilität mit Fortran-DLLs erstellt, die Argumente nach Verweis übergeben. 
  
**O%** wird ab Excel 2007 unterstützt und bietet Platz für die größere Anzahl von Zeilen, die Excel unterstützt. 
  
### <a name="p-and-q-data-types"></a>P- und Q-Datentypen

Wenn DLL-Funktionsargumente als Typ **P** XLOPERs oder **Typ Q** XLOPER12s registriert werden, konvertiert Excel Einzelzellenbezüge in einfache Werte und Verweise mit mehreren Zellen in Arrays, wenn diese Argumente vorbereitet werden. Mit anderen Worten, **P-** und **Q-Typen** werden in Ihrer Funktion immer als einer der folgenden Typen angezeigt: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing** oder **xltypeNil**, aber nicht **xltypeRef** oder **xltypeSRef,** da diese immer dereferenziert werden. **XLOPER12-Elemente** und daher Argumente vom Typ **Q** werden erst ab Excel 2007 unterstützt. 
  
Wenn typen **xltypeMissing** oder **xltypeNil** für Rückgabewerte verwendet werden, werden sie von Excel als numerische Null interpretiert. **xltypeMissing** wird übergeben, wenn der Aufrufer ein Argument auslässt. **xltypeNil** wird übergeben, wenn der Aufrufer einen Verweis an eine leere Zelle übergibt. Wenn ein Zellbereich in einen **xltypeMulti** konvertiert wird, der als Typ **P** oder **Q** übergeben werden soll, werden alle leeren Zellen innerhalb des Bereichs in **xltypeNil-Arrayelemente** konvertiert. Fehlende Elemente in einem Literalarray werden in ähnlicher Weise als **xltypeNil-Elemente** übergeben. 
  
### <a name="volatile-functions-and-recalculation"></a>Verändere Funktionen und Neuberechnung

Auf einem Arbeitsblatt können Sie eine DLL-Funktion oder Coderessource veränderlich machen, sodass sie jedes Mal neu berechnet wird, wenn das Arbeitsblatt neu berechnet wird. Fügen Sie dazu ein Ausrufezeichen (!) nach dem letzten Argumentcode im  _Argument pxTypeText_ hinzu. 
  
> [!NOTE]
> Standardmäßig werden Funktionen, die den Typ **R** XLOPERs oder **U** XLOPER12s verwenden und als Makrovorlagenentsprechungen registriert sind (Typ; **#** siehe nächster Abschnitt), in Excel als veränderlichkeit behandelt. 
  
### <a name="functions-declared-as-void"></a>Als "void" deklarierte Funktionen

Es gibt zwei Fälle, in denen aufgerufen wird, eine Funktion als "void zurückgeben" zu deklarieren. In beiden Fällen gibt die Funktion ihr Ergebnis auf andere Weise zurück.
  
#### <a name="modifying-in-place"></a>Änderung an Ort und Stelle

Sie können eine einzelne Ziffer  _n_ für den Rückgabetypcode in  _pxTypeText_ verwenden, wobei  _n_ eine Zahl zwischen 1 und 9 ist. Dadurch wird Excel angewiesen, den Wert der Variablen an der Position, auf die durch das argument _n_th in _pxTypeText_ verwiesen wird, als Rückgabewert zu übernehmen. Dies wird auch als direktes Ändern bezeichnet. Das _n_th Argument muss ein Pass-by-Reference-Datentyp sein (C, D, E, F, F%, G, G%, K, K%, L, M, N, O, O%, P, Q, R oder U). Die DLL-Funktion oder Coderessource muss auch mit dem **Schlüsselwort void** in den C/C++-Sprachen (oder dem **Prozedurstichwort** in der Sprache Pascal) deklariert werden. 
  
Beispielsweise kann eine DLL-Funktion, die eine Zeichenfolge mit NULL-Terminierung und zwei Zeiger auf ganze Zahlen als Argumente verwendet, die Zeichenfolge direkt ändern. Verwenden Sie "1FMM" als  _pxTypeText-Argument,_ und deklarieren Sie die Funktion als "void". 
  
Frühere Versionen von Excel **\>** zu Beginn von _pxTypeText_ verwendet, um zu signalisieren, dass die Funktion als ungültig deklariert wurde und dass das erste Argument direkt geändert werden sollte – es gab keine Möglichkeit, ein anderes Argument als das erste zu ändern. Dies **\>** entspricht _n_ = 1 in aktuellen Excel Versionen, und diese Verwendung **\>** in synchronen Funktionen wird nur aus Gründen der Abwärtskompatibilität unterstützt. 
  
#### <a name="asynchronous-functions"></a>Asynchrone Funktionen

Eine asynchrone Funktion, die mithilfe eines Parameters vom Typ X in **pxTypeText** angegeben wird, gibt das Ergebnis nicht aus dem anfänglichen Funktionsaufruf zurück. Stattdessen müssen Sie eine asynchrone Funktion als "void" deklarieren, und später gibt das Add-In das Ergebnis über einen Rückruf zurück. Die asynchrone Funktion muss mithilfe **\>** von **pxTypeText** registriert werden. Gibt in asynchronen Funktionen **\>** an, dass die Funktion als ungültig deklariert ist, aber nicht angibt, dass das erste Argument direkt geändert wird. Weitere Informationen zu asynchronen Funktionen finden Sie unter ["Asynchrone User-Defined Funktionen".](asynchronous-user-defined-functions.md) 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Registrieren von Arbeitsblattfunktionen als Makroblattentsprechungen (Umgang mit nicht berechneten Zellen)

Durch Das Platzieren eines **#** Zeichens nach dem letzten Parametercode in  _pxTypeText_ erhält die Funktion die gleichen Aufrufberechtigungen wie Funktionen auf einem Makroblatt. Hierbei handelt es sich um folgende Schritte vor dem Upgrade: 
  
- Die Funktion kann die Werte von Zellen abrufen, die in diesem Neuberechnungszyklus noch nicht berechnet wurden.
    
- Die Funktion kann eine beliebige XLM-Informationsfunktion (Klasse 2) aufrufen, z. B. **xlfGetCell**.
    
- Wenn das Nummernzeichen (#) nicht vorhanden ist: Das Auswerten einer nicht berechneten Zelle führt zu einem **XlretUncalced-Fehler,** und die aktuelle Funktion wird erneut aufgerufen, nachdem die Zelle berechnet wurde. Das Aufrufen einer anderen XLM-Informationsfunktion als **xlfCaller** führt zu einem **XlretInvXlfn-Fehler.** 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Registrieren von Arbeitsblattfunktionen als threadsicher

Ab Excel 2007 können Excel Multithread-Arbeitsmappen neu berechnen. Dies bedeutet, dass gleichzeitigen Threads zur erneuten Überprüfung verschiedene Instanzen einer threadsicheren Funktion zugewiesen werden können. Ab Excel 2007 sind die meisten der integrierten Arbeitsblattfunktionen threadsicher. Ab Excel 2007 ermöglicht Excel auch XLLs das Registrieren von Arbeitsblattfunktionen als threadsicher. Fügen Sie dazu ein **$** Zeichen hinter dem letzten Parametercode in  _pxTypeText_ ein. 
  
> [!NOTE]
> Nur Arbeitsblattfunktionen können als threadsicher deklariert werden. Excel betrachtet eine Makroblatt-äquivalente Funktion nicht als threadsicher, sodass Sie nicht sowohl Zeichen als auch **#** Zeichen an das Argument **$** _pxTypeText_ anfügen können. 
  
Wenn Sie eine Funktion als threadsicher registriert haben, müssen Sie sicherstellen, dass sie sich threadsicher verhält, obwohl Excel threadunsichere Aufrufe über die C-API ablehnt. Wenn beispielsweise eine threadsichere Funktion versucht, **xlfGetCell** aufzurufen, schlägt der Aufruf mit dem **XlretNotThreadSafe-Fehler** fehl. 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Registrieren von Arbeitsblattfunktionen als clustersicher

Ab Excel 2010 können Excel Funktionsaufrufe an einen angegebenen Computeclusteranbieter auslagern. Weitere Informationen finden Sie unter [Cluster Tresor Funktionen.](cluster-safe-functions.md) Alle als clustersicher registrierten XLL-Arbeitsblattfunktionen nehmen an der Auslagerung teil, wenn ein Cluster verfügbar ist. Clustersichere Funktionen werden registriert, indem das **&amp;** Zeichen nach dem letzten Parametercode in das Argument  _pxTypeText_ eingeschlossen wird. 
  
Wenn Sie eine Funktion als clustersicher registriert haben, müssen Sie sicherstellen, dass sie sich clustersicher verhält. Weitere Informationen finden Sie unter [Cluster Tresor Funktionen.](cluster-safe-functions.md)
  
> [!NOTE]
> Nur Arbeitsblattfunktionen können als clustersicher deklariert werden. Excel betrachtet eine Makroblatt-äquivalente Funktion nicht als clustersicher, sodass Sie nicht sowohl Zeichen als auch **#** Zeichen an das Argument **&amp;** _pxTypeText_ anfügen können. Arbeitsblattfunktionen können als cluster- und threadsicher deklariert werden. In diesem Fall ermöglichen Excel, dass diese Funktionen an der Multithread-Neuberechnung teilnehmen, wenn das Cluster-Offloading deaktiviert ist. 
  
### <a name="category-names"></a>Kategorienamen

Verwenden Sie die folgenden Richtlinien, um zu bestimmen, in welche Kategorie Ihre XLL-Funktionen eingefügt werden sollen.
  
- Wenn die Funktion eine Aktion ausführt, die vom Benutzer als Teil der Add-In-Benutzeroberfläche ausgeführt werden kann, sollten Sie die Funktion in die Kategorie **"Befehle"** einfügen. 
    
- Wenn die Funktion Informationen über den Status des Add-Ins oder andere nützliche Informationen zurückgibt, sollten Sie die Funktion in die Kategorie **"Informationen"** einfügen. 
    
- Ein Add-In sollte niemals Funktionen oder Befehle zur Kategorie **"Benutzerdefiniert"** hinzufügen. Diese Kategorie ist für die ausschließliche Verwendung von Endbenutzern vorgesehen. 
    
Die Kategorie wird mithilfe des  _pxCategory-Parameters_ für **xlfRegister** angegeben. Dies kann eine Zahl oder ein Text sein, der einer der hartcodierten Standardkategorien entspricht, oder der Text einer neuen Kategorie, die von der DLL angegeben wird. Wenn der angegebene Text noch nicht vorhanden ist, erstellt Excel eine neue Kategorie mit diesem Namen.
  
In der folgenden Tabelle sind die Standardkategorien aufgeführt, die angezeigt werden, wenn Sie das Dialogfeld **"Funktion einfügen"** in einem Arbeitsblatt anzeigen. 
  
|**Number**|**Text**|
|:-----|:-----|
|1  <br/> |Finanzwesen  <br/> |
|2  <br/> |&amp;Datum/Uhrzeit  <br/> |
|3  <br/> |Math. &amp; Trigonom.  <br/> |
|4   <br/> |Text  <br/> |
|5  <br/> |Logik  <br/> |
|6   <br/> |Lookup &amp; Reference  <br/> |
|7   <br/> |Datenbank  <br/> |
|8   <br/> |Statistik  <br/> |
|9   <br/> |Informationen  <br/> |
|14   <br/> |Benutzerdefiniert  <br/> |
||Engineering (ab Excel 2007)  <br/> |
||Cube (ab Excel 2007)  <br/> |
   
Darüber hinaus sind diese Kategorien auch sichtbar, wenn Sie das Dialogfeld **"Funktion einfügen"** in einem Makroblatt anzeigen. 
  
|**Number**|**Text**|
|:-----|:-----|
|10  <br/> |Befehle  <br/> |
|11  <br/> |DDE/Extern  <br/> |
|12   <br/> |Benutzerorientiert  <br/> |
|13  <br/> |Makrosteuerung  <br/> |
   
### <a name="example"></a>Beispiel

Siehe den Code für die **xlAutoOpen-Funktion** in  `\SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>Siehe auch

- [REGISTER.ID](xlfregisterid.md)
- [REGISTRIERUNG](xlfunregister-form-1.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

