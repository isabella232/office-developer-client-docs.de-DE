---
title: xlfRegister (Formular 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfregister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3cd2e5072c8602fe301028e69592220a8345c211
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303864"
---
# <a name="xlfregister-form-1"></a>xlfRegister (Formular 1)

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann über einen DLL- oder XLL-Befehl aufgerufen werden, der selbst von einem Microsoft Excel. Dies entspricht dem Aufruf **von REGISTER** aus Excel XLM-Makroblatts. 
  
**xlfRegister** kann in zwei Formen aufgerufen werden: 
  
- xlfRegister (Form 1): Registriert einen einzelnen Befehl oder eine einzelne Funktion.
    
- [xlfRegister (Form 2):](xlfregister-form-2.md)Lädt und aktiviert eine XLL.
    
In Form 1 aufgerufen, stellt diese Funktion eine DLL-Funktion oder einen Befehl für Excel zur Verfügung, legt die Verwendungsanzahl auf 1 fest und gibt die Registrierungs-ID zurück, mit der die Funktion später mithilfe der [xlUDF-](xludf.md) oder **xlfCall-Funktion** aufgerufen werden kann. Die Registrierungs-ID wird auch zum Aufheben der Registrierung der Funktion mithilfe von [xlfUnregister (Formular 1) verwendet.](xlfunregister-form-1.md) Wenn die Funktion registriert wurde, erhöht der Aufruf **von xlfRegister** erneut die Verwendungsanzahl. 
  
Diese Form der Funktion definiert auch einen ausgeblendeten Namen, bei dem es sich um das Funktionstextargument  _pxFunctionText_ handelt und der zur Registrierungs-ID der Funktion oder des Befehls ausgewertet wird. Wenn Sie die Registrierung der Funktion aufheben, löschen Sie diesen Namen mithilfe von [xlfSetName](xlfsetname.md). Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
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
  
Der Name der DLL, die die Funktion enthält. Dies kann durch Aufrufen der nur XLL-Funktion [xlGetName](xlgetname.md) erhalten werden, wenn sich die registrierte Funktion auch innerhalb der aktuell ausgeführten DLL befindet. 
  
_pxProcedure_ (**xltypeStr** oder **xltypeNum**)
  
Wenn eine Zeichenfolge, der Name der Funktion, die wie im DLL-Code angezeigt wird. Wenn eine Zahl, die Ordnungsexportnummer der zu aufrufende Funktion. Verwenden Sie aus Gründen der Übersichtlichkeit immer das Zeichenfolgenformular.
  
_pxTypeText_ (**xltypeStr**)
  
Eine optionale Zeichenfolge, die die Typen von Argumenten für die Funktion und den Typ des Rückgabewerts der Funktion angibt. Weitere Informationen finden Sie unter "Anmerkungen". Dieses Argument kann für eine eigenständige DLL (XLL) ausgelassen werden, die eine [xlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) oder **xlAutoRegister12 enthält.** 
  
> [!NOTE]
> **xlAutoRegister12** wird nur in Excel 2007 unterstützt. 
  
Wenn **xlfRegister** aufgerufen wird, wenn dieses Argument fehlt, ruft Excel **xlAutoRegister** oder **xlAutoRegister12** auf, wenn eine der beiden in der angegebenen DLL vorhanden ist, die dann die Funktion ordnungsgemäß registrieren sollte, indem sie diese Informationen an die Angegebene Dll ankn stellt.
  
_pxFunctionText_ (**xltypeStr**)
  
Der Funktionsname, wie er im Funktions-Assistenten angezeigt wird. Dieses Argument ist optional. Wenn sie nicht angegeben wird, ist die Funktion im Funktions-Assistenten nicht verfügbar und kann nur mithilfe der **CALL-Funktion** mithilfe der Registrierungs-ID der Funktionen aus einem XLM-Makroblatt aufgerufen werden. Daher sollten Sie dieses Argument bei normaler Arbeitsblattnutzung bei Bedarf behandeln. 
  
_pxArgumentText_ (**xltypeStr**)
  
Eine optionale Textzeichenfolge, die die Argumente für die Funktion beschreibt. Dies wird dem Benutzer im Assistenten für Funktionen angezeigt. Wenn sie nicht angegeben wird, erstellt Excel grundlegende Beschreibungen aus _pxTypeText_.
  
_pxMacroType_ (**xltypeNum** oder **xltypeInt**)
  
Ein optionales Argument, das den Typ des XLL-Einstiegspunkts angibt. Wenn er nicht angegeben wird, ist der Standardwert 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _pxMacroType-Wert_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Kann von einem Arbeitsblatt aus aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Kann aus einem Makroblatt aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|Kann über eine definierte Namensdefinition aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|Kann von einem Ausdruck für ein bedingtes Format aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Im Funktions-Assistenten für Arbeitsblattfunktionen aufgeführt  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Im Funktions-Assistenten für Makroblattfunktionen aufgeführt  <br/> |Nein  <br/> |Ja  <br/> |Ja  <br/> |
   
In der Praxis sollten Sie 1 für Arbeitsblattfunktionen, 1 für makroblattäquivalente Funktionen (als Typ registriert) verwenden, die Sie vom Arbeitsblatt aufrufen möchten, und 2 für **#** Befehle. 
  
> [!NOTE]
> XLL-Befehle werden ausgeblendet und nicht in Dialogfeldern zum Ausführen von Makros angezeigt, obwohl deren Namen überall eingegeben werden können, wo ein gültiger Befehlsname erforderlich ist. 
  
_pxCategory_ (**xltypeStr** oder **xltypeNum**)
  
Ein optionales Argument, mit dem Sie angeben können, zu welcher Kategorie die neue Funktion oder der neue Befehl gehören soll. Der Funktions-Assistent teilt Funktionen nach Typ (Kategorie) auf. Sie können einen Kategorienamen oder eine sequenzielle Zahl angeben, wobei die Zahl die Position ist, an der die Kategorie im Funktions-Assistenten angezeigt wird. Weitere Informationen finden Sie im Abschnitt "Kategorienamen". Wenn sie nicht angegeben wird, wird die benutzerdefinierte Kategorie angenommen.
  
_pxShortcutText_ (**xltypeStr**)
  
Eine zeichenfolge mit einem Zeichen, bei der die Zwischenschreibung beachtet wird, die die diesem Befehl zugewiesene Steuerelementtaste angibt. Beispielsweise weist "A" diesen Befehl CONTROL+SHIFT+A zu. Dieses Argument ist optional und wird nur für Befehle verwendet.
  
_pxHelpTopic_ (**xltypeStr**)
  
Optionaler Verweis auf die Hilfedatei (.chm oder hlp), die angezeigt werden soll, wenn der Benutzer auf die Schaltfläche Hilfe klickt (wenn Ihre benutzerdefinierte Funktion angezeigt wird). Kann im Format oder  `filepath!HelpContextID`  `https://address/path_to_file_in_site!0` sein. Beide Teile vor und nach dem "!" sind erforderlich.  *HelpContextID* darf keine einzelnen Anführungszeichen enthalten und wird von Excel in eine nicht signierte ganze Zahl von 4 Byte in Dezimalform konvertiert. Wenn Sie das URL-Formular verwenden, Excel nur die Hilfedatei geöffnet, auf die verwiesen wird. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Eine optionale Zeichenfolge, die Ihre benutzerdefinierte Funktion beschreibt, wenn sie im Funktions-Assistenten ausgewählt ist.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Optional. Die erste der Zeichenfolgen, die die benutzerdefinierten Argumente der Funktion beschreiben, wenn die Funktion im Funktions-Assistenten ausgewählt ist. In Excel 2003 und früheren Versionen kann **xlfRegister** mindestens 30 Argumente verwenden, damit Sie diese Hilfe nur für die ersten 20 Funktionsargumente bereitstellen können. Ab Excel 2007 kann **xlfRegister** bis zu 255 Argumente verwenden, sodass Sie diese Hilfe für bis zu 245 Funktionsparameter bereitstellen können. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn die Registrierung erfolgreich war, gibt diese Funktion die Register-ID der Funktion (**xltypeNum**) zurück, die in Aufrufen von **xlUDF** und **xlfUnregister** in einer DLL oder mit **CALL** und **UNREGISTER** in einem XLM-Makroblatt verwendet werden kann. Andernfalls wird ein #VALUE! zurück. 
  
## <a name="remarks"></a>Hinweise

### <a name="data-types"></a>Datentypen

Das  _Argument pxTypeText_ gibt den Datentyp des Rückgabewerts und die Datentypen aller Argumente für die DLL-Funktion oder Coderessource an. Das erste Zeichen von  _pxTypeText_ gibt den Datentyp des Rückgabewerts an. Die verbleibenden Zeichen geben die Datentypen aller Argumente an. Beispielsweise erfordert eine DLL-Funktion, die eine Gleitkommazahl zurückgibt und eine ganze Zahl und eine Gleitkommazahl als Argumente verwendet, "BIB" für das _Argument pxTypeText._ 
  
Die Datentypen und Strukturen, die von Excel zum Austausch von Daten mit XLLs verwendet werden, sind in den folgenden beiden Tabellen zusammengefasst.
  
In der ersten Tabelle sind die Typen aufgeführt, die in allen Versionen von Excel.
  
|**Datentyp**|**Übergabe nach Wert**|**Übergabe nach Verweis (Zeiger)**|**Kommentare**|
|:-----|:-----|:-----|:-----|
|Boolesch  <br/> |A  <br/> |L  <br/> |short [int] (0=false oder 1=true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |ASCII-Bytezeichenfolge mit Null-Terminierung  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Gezählte ASCII-Bytezeichenfolge  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||16-Bit-WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16-Bit-signierte ganze Zahl  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32-Bit-signierte ganze Zahl  <br/> |
|FP  <br/> ||K  <br/> |Gleitkomma-Arraystruktur  <br/> |
|Array  <br/> ||O  <br/> |Es werden drei Argumente übergeben:<br/>- unsigned short int \*<br/>- unsigned short int \*<br/>- double []  <br/> |
|XLOPER  <br/> ||P  <br/> |Variablen-Arbeitsblattwerte und Arrays  <br/> |
|||R  <br/> |Werte, Arrays und Bereichsbezüge  <br/> |
   
In Excel 2007 wurden die folgenden Datentypen eingeführt, um die größeren Raster und langen Unicode-Zeichenfolgen zu unterstützen.
  
|**Datentyp**|**Übergabe nach Wert**|**Übergabe nach Verweis (Zeiger)**|**Kommentare**|
|:-----|:-----|:-----|:-----|
|unsigned short \*  <br/> ||C%, F%  <br/> |Mit Null beendete Unicode-Breitzeichenzeichenfolge  <br/> |
|unsigned short \*  <br/> ||D%, G%  <br/> |Gezählte Unicode-Breitzeichenzeichenfolge  <br/> |
|FP12  <br/> ||K%  <br/> |Größere Raster-Gleitkommaarraystruktur  <br/> |
|Array  <br/> ||O%  <br/> |Es werden drei Argumente übergeben:<br/>- signiert int \* / RW \*<br/>- signiert int \* /COL \*<br/>- double []  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Variablen-Arbeitsblattwerte und Arrays  <br/> |
|||U  <br/> |Werte, Arrays und Bereichsbezüge  <br/> |
   
Ab Excel 2010 wurden die folgenden Datentypen eingeführt:
  
|**Datentyp**|**Übergabe nach Wert**|**Übergabe nach Verweis (Zeiger)**|**Kommentare**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |Das asynchrone Handle wird verwendet, um einen ausstehenden asynchronen Funktionsaufruf von Excel und der XLL nachzuverfolgen.Das Vorhandensein des Parametertyps in der Typzeichenfolge bestimmt die Funktion auch als asynchron. Weitere Informationen zu asynchronen Funktionen finden Sie unter [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).  <br/> |
   
Die Zeichenfolgentypen **F**, **F%**, **G** und **G%** werden für Argumente verwendet, die direkt geändert werden. 
  
Beachten Sie folgendes, wenn Sie mit den in der vorherigen Tabelle angezeigten Datentypen arbeiten:
  
- Bei den C-Language-Deklarationen wird davon ausgegangen, dass ihr Compiler standardmäßig 8-Byte-Doubles, 2-Byte-Short-Ganzzahlen und 4-Byte-Ganzzahlen verwendet.
    
- Alle Funktionen in DLLs und Coderessourcen werden mithilfe der __stdcall **aufgerufen.** 
    
- Jede Funktion, die einen Datentyp per Verweis zurückgibt, d. h. einen Zeiger auf etwas zurückgibt, kann einen Nullzeiger sicher zurückgeben. Excel interpretiert einen Nullzeiger als #NUM! zurück.
    
## <a name="additional-data-type-information"></a>Zusätzliche Datentypinformationen

Dieser Abschnitt enthält detaillierte Informationen zu den Datentypen **E,** **F,** **F%**, **G**, **G%**, **K**, **O**, **P**, **Q**, **R** und **U** sowie weitere Informationen zum _Argument pxTypeText._ 
  
### <a name="e-data-type"></a>E-Datentyp

Excel erwartet eine DLL, die den Datentyp E verwendet, um Zeiger an Gleitkommazahlen auf dem Stapel zu übergeben. Dies kann probleme mit einigen Sprachen (z. B. Borland C++) verursachen, die erwarten, dass die Nummer im #A0 übergeben wird. Die Problemumgehung besteht im Übergeben eines Zeigers auf die Nummer im Coprozessorstapel. Im folgenden Beispiel wird gezeigt, wie ein Double aus Borland C++ zurückgeben wird.
  
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

Mit den **Datentypen F,** **F%**, **G** und **G%** kann eine Funktion einen Zeichenfolgenpuffer ändern, der von der Excel. Wenn der Rückgabewerttypcode einer dieser Typen ist, ignoriert Excel den von der Funktion zurückgegebenen Wert. Stattdessen durchsucht Excel die Liste der Funktionsargumente nach dem ersten entsprechenden Datentyp (**F**, **F%**, **G** oder **G%**) und nimmt dann den aktuellen Inhalt des zugeordneten Zeichenfolgenpuffers als Rückgabewert an. Alle Versionen von Excel weisen 256 Byte für **F-** und G-ASCII-Zeichenfolgen zu, und ab Excel 2007 werden 65.536 Bytes zugewiesen, genug für 32.768 Unicode-Zeichen, für **F%** und  **G%** Unicode-Zeichenfolgen. Denken Sie daran, dass die Puffer ein Anzahlzeichen (Typen **G** und **G%**) oder ein Nullendzeichen (Typen **F** und **F%**) enthalten müssen, damit die tatsächlichen maximalen Zeichenfolgenlängen 255 und 32.767 sind. #A0 und daher **die Argumente F%** und **G%** sind nur über die C-API in Excel. 
  
### <a name="k-and-k-data-types"></a>K- und K%-Datentypen

Die **Datentypen K** **und K%** verwenden Zeiger auf die FP- und FP12-Strukturen mit variabler Größe. Diese Strukturen sind in XLLCALL.H definiert. FP12-Strukturen und daher **K%-Argumente** werden nur ab Excel 2007 unterstützt. 
  
### <a name="o-and-o-data-types"></a>O- und O%-Datentypen

Die **O-** und **O%-Datentypen** können nur für Argumente verwendet werden, nicht für Rückgabewerte, obwohl Werte zurückgegeben werden können, wenn ein **O-** oder O%-Typargument geändert wird.  Jedes übergibt drei Elemente: einen Zeiger auf die Anzahl der Zeilen in einem Array, einen Zeiger auf die Anzahl der Spalten in einem Array und einen Zeiger auf ein zweidimensionales Array von Gleitkommazahlen. 
  
Zum Ändern eines Arrays, das vom O- oder O%-Datentyp übergeben wird, können Sie ">O" oder ">O%" als  _Argument pxTypeText_ verwenden. Weitere Informationen zum Ändern eines Arrays finden Sie im Abschnitt "Modifying in Place: Functions Declared as Void" in diesem Thema. 
  
Der **O-Datentyp** wurde für die direkte Kompatibilität mit Fortran-DLLs erstellt, die Argumente per Verweis übergeben. 
  
Das **O%** wird ab Excel 2007 unterstützt und bietet Platz für die größere Anzahl von Zeilen, die Excel unterstützt. 
  
### <a name="p-and-q-data-types"></a>P- und Q-Datentypen

Wenn DLL-Funktionsargumente als Typ **P** XLOPERs oder **Q** XLOPER12s registriert werden, konvertiert Excel bei der Vorbereitung dieser Argumente Verweise aus einzelnen Zellen in einfache Werte und Verweise mit mehreren Zellen in Arrays. Mit anderen Worten, **P-** und **Q-Typen** werden immer in Ihrer Funktion als einer der folgenden Typen eintreffen: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing** oder **xltypeNil**, aber nicht **xltypeRef** oder **xltypeSRef,** da diese immer dereferenced sind. **XLOPER12** s und  daher Q-Argumente eingeben, werden nur ab Excel 2007 unterstützt. 
  
Wenn die **Typen xltypeMissing** oder **xltypeNil** für Rückgabewerte verwendet werden, werden sie von Excel numerischen Null interpretiert. **xltypeMissing** wird übergeben, wenn der Aufrufer ein Argument ausbiert. **xltypeNil** wird übergeben, wenn der Aufrufer einen Verweis auf eine leere Zelle übergibt. Wenn ein Zellbereich in einen **xltypeMulti** konvertiert wird, der als Typ **P** oder **Q** übergeben wird, werden alle leeren Zellen innerhalb des Bereichs in **xltypeNil-Arrayelemente** konvertiert. Fehlende Elemente in einem Literalarray werden ähnlich wie **xltypeNil-Elemente** übergeben. 
  
### <a name="volatile-functions-and-recalculation"></a>Volatile Funktionen und Neuberechnung

In einem Arbeitsblatt können Sie eine DLL-Funktion oder Coderessource flüchtig machen, sodass sie jedes Mal neu berechnet wird, wenn das Arbeitsblatt neu berechnet wird. Fügen Sie dazu ein Ausrufezeichen (!) nach dem letzten Argumentcode im  _Argument pxTypeText_ hinzu. 
  
> [!NOTE]
> Standardmäßig werden Funktionen, die den Typ **R** XLOPERs oder **U** XLOPER12s verwenden und als Makroblattäquivalente registriert sind (Typ ; siehe nächster Abschnitt), in der #A0 **#** als Excel. 
  
### <a name="functions-declared-as-void"></a>Als ungültig deklarierte Funktionen

Es gibt zwei Fälle, in denen die Deklarieren einer Funktion als void zurückruft werden muss. In beiden Fällen gibt die Funktion ihr Ergebnis mit anderen Mitteln zurück.
  
#### <a name="modifying-in-place"></a>Ändern an Ort und Stelle

Sie können eine einzelne Ziffer  _n_ für den Rückgabetypcode in  _pxTypeText_ verwenden, wobei  _n_ eine Zahl zwischen 1 und 9 ist. Dadurch wird Excel angewiesen, den Wert der Variablen an der Position zu übernehmen, auf die das argument _n_th in _pxTypeText_ als Rückgabewert verweist. Dies wird auch als "Ändern" bezeichnet. Das _n_th-Argument muss ein Pass-by-Reference-Datentyp sein (C, D, E, F, F%, G, G%, K, K%, L, M, N, O, O%, P, Q, R oder U). Die DLL-Funktion oder Coderessource muss auch mit dem **Schlüsselwort void** in den C/C++-Sprachen (oder dem **Prozedurschlüsselwort** in der Sprache "Pascal" ) deklariert werden. 
  
Beispielsweise kann eine DLL-Funktion, die eine mit Null beendete Zeichenfolge und zwei Zeiger auf ganze Zahlen als Argumente verwendet, die Zeichenfolge an Ort und Stelle ändern. Verwenden Sie "1FMM" als  _Argument pxTypeText,_ und deklarieren Sie die Funktion als void. 
  
Frühere Versionen von Excel zu Beginn von **\>** _pxTypeText_ verwendet, um zu signalisieren, dass die Funktion als void deklariert wurde und dass das erste Argument an Ort und Stelle geändert werden sollte. Es gab keine Möglichkeit, ein anderes Argument als das erste zu ändern. Die **\>** entspricht _n_ = 1 in aktuellen Excel, und diese Verwendung in synchronen Funktionen wird nur zur Abwärtskompatibilität **\>** unterstützt. 
  
#### <a name="asynchronous-functions"></a>Asynchrone Funktionen

Eine asynchrone Funktion, die mit einem Parameter vom Typ X in **pxTypeText** bezeichnet wird, gibt das Ergebnis aus dem anfänglichen Funktionsaufruf nicht zurück. Stattdessen müssen Sie eine asynchrone Funktion als void deklarieren, und später gibt das Add-In das Ergebnis über einen Rückruf zurück. Die asynchrone Funktion muss am Anfang von **\>** **pxTypeText registriert werden.** Gibt in asynchronen Funktionen an, dass die Funktion als void deklariert wird, aber nicht angibt, dass das erste Argument an Ort und **\>** Stelle geändert wird. Weitere Informationen zu asynchronen Funktionen finden Sie unter [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md). 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Registrieren von Arbeitsblattfunktionen als Makroblattäquivalente (Behandlung nicht berechneter Zellen)

Durch das Platzieren eines Zeichens nach dem letzten **#** Parametercode in  _pxTypeText_ erhält die Funktion dieselben aufrufenden Berechtigungen wie Funktionen in einem Makroblatt. Hierbei handelt es sich um folgende Schritte vor dem Upgrade: 
  
- Die Funktion kann die Werte von Zellen abrufen, die in diesem Neuberechnungszyklus noch nicht berechnet wurden.
    
- Die Funktion kann beliebige XLM-Informationsfunktionen (Klasse 2) aufrufen, z. B. **xlfGetCell**.
    
- Wenn das Nummernzeichen (#) nicht vorhanden ist: Das Auswerten einer nicht berechneten Zelle führt zu einem **xlretUncalced-Fehler,** und die aktuelle Funktion wird erneut aufgerufen, nachdem die Zelle berechnet wurde. Das Aufrufen einer anderen XLM-Informationsfunktion **als xlfCaller** führt zu einem **xlretInvXlfn-Fehler.** 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Registrieren von Arbeitsblattfunktionen als threadsicher

Ab Excel 2007 kann Excel neu berechnete Arbeitsmappen mit mehrerenReads ausführen. Dies bedeutet, dass gleichzeitigen Threads zur Neubewertung verschiedene Instanzen einer threadsicheren Funktion zugewiesen werden können. Ab Excel 2007 sind die meisten integrierten Arbeitsblattfunktionen threadsicher. Ab Excel 2007 ermöglicht Excel XLLs auch die Registrierung von Arbeitsblattfunktionen als threadsicher. Fügen Sie dazu ein Zeichen **$** nach dem letzten Parametercode in _pxTypeText ein._ 
  
> [!NOTE]
> Nur Arbeitsblattfunktionen können als threadsicher deklariert werden. Excel wird eine Makroblattäquivalentfunktion nicht als threadsicher eingestuft, sodass Sie nicht sowohl als auch Zeichen an das **#** **$** Argument _pxTypeText anfügen_ können. 
  
Wenn Sie eine Funktion als threadsicher registriert haben, müssen Sie sicherstellen, dass sie sich threadsicher verhält, auch wenn Excel threadunsichere Aufrufe über die C-API ablehnt. Wenn beispielsweise eine threadsichere Funktion versucht, **xlfGetCell** auf aufruft, schlägt der Aufruf mit dem **xlretNotThreadSafe-Fehler** fehl. 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Registrieren von Arbeitsblattfunktionen als clustersicher

Ab Excel 2010 können Excel Funktionsaufrufe an einen bestimmten Computeclusteranbieter ausladen. Weitere Informationen finden Sie unter [Cluster Safe Functions](cluster-safe-functions.md). Alle als clustersicher registrierten XLL-Arbeitsblattfunktionen nehmen am Offloading teil, wenn ein Cluster verfügbar ist. Clustersichere Funktionen werden registriert, indem das Zeichen nach dem letzten **&amp;** Parametercode im  _Argument pxTypeText hinzugefügt_ wird. 
  
Wenn Sie eine Funktion als clustersicher registriert haben, müssen Sie sicherstellen, dass sie sich clustersicher verhält. Weitere Informationen finden Sie unter [Cluster Safe Functions](cluster-safe-functions.md).
  
> [!NOTE]
> Nur Arbeitsblattfunktionen können als clustersicher deklariert werden. Excel wird eine Makroblattäquivalentfunktion nicht als clustersicher eingestuft, sodass Sie nicht sowohl als auch Zeichen an das **#** **&amp;** Argument _pxTypeText anfügen_ können. Arbeitsblattfunktionen können sowohl als clustersicher als auch als threadsicher deklariert werden. In diesem Fall Excel diese Funktionen an der Multithreadneuberechnung teilnehmen, wenn das Clusterabladen deaktiviert ist. 
  
### <a name="category-names"></a>Kategorienamen

Verwenden Sie die folgenden Richtlinien, um zu bestimmen, in welche Kategorie Ihre XLL-Funktionen einzuordnen sind.
  
- Wenn die Funktion etwas tut, was vom Benutzer als Teil der Add-In-Benutzeroberfläche ausgeführt werden kann, sollten Sie die Funktion in die Kategorie **Befehle** setzen. 
    
- Wenn die Funktion Informationen über den Status des Add-Ins oder andere nützliche Informationen zurückgibt, sollten Sie die Funktion in die Kategorie **Information** setzen. 
    
- Ein Add-In sollte der benutzerdefinierten Kategorie nieMals Funktionen oder **Befehle** hinzufügen. Diese Kategorie ist für die ausschließliche Verwendung von Endbenutzern. 
    
Die Kategorie wird mit dem _Parameter pxCategory_ an **xlfRegister angegeben.** Dies kann eine Zahl oder ein Text sein, der einer der hart codierten Standardkategorien oder dem Text einer neuen Kategorie entspricht, die von der DLL angegeben wird. Wenn der angegebene Text noch nicht vorhanden ist, Excel eine neue Kategorie mit diesem Namen erstellt.
  
In der folgenden Tabelle sind die Standardkategorien aufgeführt, die angezeigt werden, wenn Sie das Dialogfeld **Funktion** einfügen in einem Arbeitsblatt anzeigen. 
  
|**Number**|**Text**|
|:-----|:-----|
|1  <br/> |Finanzwesen  <br/> |
|2  <br/> |&amp;Datumszeit  <br/> |
|3  <br/> |Math. &amp; Trigonom.  <br/> |
|4   <br/> |Text  <br/> |
|5   <br/> |Logik  <br/> |
|6   <br/> |Lookup &amp; Reference  <br/> |
|7   <br/> |Datenbank  <br/> |
|8   <br/> |Statistik  <br/> |
|9   <br/> |Informationen  <br/> |
|14   <br/> |Benutzerdefiniert  <br/> |
||Engineering (ab Excel 2007)  <br/> |
||Cube (ab Excel 2007)  <br/> |
   
Darüber hinaus sind diese Kategorien auch sichtbar, wenn Sie das Dialogfeld **Funktion** einfügen in einem Makroblatt anzeigen. 
  
|**Number**|**Text**|
|:-----|:-----|
|10  <br/> |Befehle  <br/> |
|11  <br/> |DDE/Extern  <br/> |
|12   <br/> |Benutzerorientiert  <br/> |
|13  <br/> |Makrosteuerung  <br/> |
   
### <a name="example"></a>Beispiel

Weitere Informationen finden Sie im Code für die **xlAutoOpen-Funktion** in  `\SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>Siehe auch

- [REGISTER.ID](xlfregisterid.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

