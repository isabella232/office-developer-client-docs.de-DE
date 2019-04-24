---
title: xlfRegister (Formular 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfRegister-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3cd2e5072c8602fe301028e69592220a8345c211
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303864"
---
# <a name="xlfregister-form-1"></a>xlfRegister (Formular 1)

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann von einem DLL-oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde. Dies entspricht dem Aufrufen von **Register** aus einer Excel-XML-Makrovorlage. 
  
**xlfRegister** kann in zwei Formen aufgerufen werden: 
  
- xlfRegister (Formular 1): registriert einen einzelnen Befehl oder eine Funktion.
    
- [xlfRegister (Formular 2)](xlfregister-form-2.md): lädt und aktiviert eine XLL.
    
In Form 1 aufgerufen, stellt diese Funktion eine DLL-Funktion oder einen Befehl für Excel zur Verfügung, legt die Verwendungsanzahl auf 1 fest und gibt Ihre Registrierungs-ID zurück, die verwendet werden kann, um die Funktion später mithilfe der [xlUDF](xludf.md) -oder der **xlfCall** -Funktion aufzurufen. Die Registrierungs-ID wird auch verwendet, um die Registrierung der Funktion mithilfe von [xlfUnregister (Formular 1)](xlfunregister-form-1.md)aufzuheben. Wenn die Funktion registriert wurde, wird durch Aufrufen von **xlfRegister** erneut die Verwendungsanzahl erhöht. 
  
Diese Form der Funktion definiert auch einen ausgeblendeten Namen, der das Funktionstext Argument _pxFunctionText_ist und das zur Registrierungs-ID der Funktion oder des Befehls ausgewertet wird. Wenn Sie die Registrierung der Funktion aufheben, löschen Sie diesen Namen mit dem [xlfSetName](xlfsetname.md). Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
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
  
Der Name der DLL, die die Funktion enthält. Dies kann durch Aufrufen der XLL-only-Funktion [xlGetName](xlgetname.md) abgerufen werden, wenn sich die registrierte Funktion auch innerhalb der aktuell ausgeführten dll befindet. 
  
_pxProcedure_ (**xltypeStr** oder **xltypeNum**)
  
Wenn eine Zeichenfolge, der Name der Funktion aufrufen, wie es im DLL-Code angezeigt wird. Wenn eine Zahl, die ordinale Export Nummer der Funktion, die aufgerufen werden soll. Aus Gründen der Übersichtlichkeit verwenden Sie immer das Zeichenfolgen Formular.
  
_pxTypeText_ (**xltypeStr**)
  
Eine optionale Zeichenfolge, die die Typen von Argumenten für die Funktion und den Typ des Rückgabewerts der Funktion angibt. Weitere Informationen finden Sie im Abschnitt "Hinweise". Dieses Argument kann für eine eigenständige DLL (XLL) ausgelassen werden, die eine [xlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) oder **xlAutoRegister12**enthält. 
  
> [!NOTE]
> **xlAutoRegister12** wird nur in Excel 2007 unterstützt. 
  
Wenn **xlfRegister** aufgerufen wird, wenn dieses Argument fehlt, ruft Excel **xlAutoRegister** oder **xlAutoRegister12**auf, wenn es in der angegebenen DLL vorhanden ist, die dann die Funktion ordnungsgemäß registrieren soll, indem Sie diese Informationen bereitstellen.
  
_pxFunctionText_ (**xltypeStr**)
  
Der Funktionsname, wie er im Funktions-Assistenten angezeigt wird. Dieses Argument ist optional; Wenn Sie nicht angegeben wird, ist die Funktion im Funktions-Assistenten nicht verfügbar und kann nur mithilfe der **Call** -Funktion mithilfe der Registrierungs-ID der Funktionen aus einem XML-Makroblatt aufgerufen werden. Daher sollten Sie bei normaler Arbeitsblatt Verwendung dieses Argument bei Bedarf behandeln. 
  
_pxArgumentText_ (**xltypeStr**)
  
Eine optionale Textzeichenfolge, die die Argumente für die Funktion beschreibt. Der Benutzer sieht dies im Funktions-Assistenten. Wenn dies nicht der Fall ist, erstellt Excel grundlegende Beschreibungen aus _pxTypeText_.
  
_pxMacroType_ (**xltypeNum** oder **xltypeInt**)
  
Ein optionales Argument, das den Typ des XLL-Einstiegspunkts angibt. Der Standardwert ist 1, wenn er ausgelassen wird.
  
|||||
|:-----|:-----|:-----|:-----|
| _pxMacroType-Wert_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Kann aus einem Arbeitsblatt aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Kann aus einem Makroblatt aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|Kann aus einer definierten Namensdefinition aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|Kann aus einem bedingten Formatausdruck aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Im Funktions-Assistenten für Arbeitsblattfunktionen aufgelistet  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Im Funktions-Assistenten für Makroblatt Funktionen aufgeführt  <br/> |Nein  <br/> |Ja  <br/> |Ja  <br/> |
   
In der Praxis sollten Sie 1 für Arbeitsblattfunktionen, 1 für die äquivalenten Funktionen des Makros (als **#** Typ registriert) verwenden, die Sie im Arbeitsblatt aufrufen möchten, und 2 für Befehle. 
  
> [!NOTE]
> XLL-Befehle werden ausgeblendet und nicht in Dialogfeldern zum Ausführen von Makros angezeigt, obwohl ihre Namen überall dort eingegeben werden können, wo ein gültiger Befehlsname erforderlich ist. 
  
_pxCategory_ (**xltypeStr** oder **xltypeNum**)
  
Ein optionales Argument, mit dem Sie angeben können, zu welcher Kategorie die neue Funktion oder der Befehl gehören soll. Der Funktions-Assistent unterteilt Funktionen nach Typ (Category). Sie können einen Kategorienamen oder eine fortlaufende Nummer angeben, wobei die Nummer die Position ist, an der die Kategorie im Funktions-Assistenten angezeigt wird. Weitere Informationen finden Sie im Abschnitt "Category Names". Wenn Sie nicht angegeben wird, wird die benutzerdefinierte Kategorie angenommen.
  
_pxShortcutText_ (**xltypeStr**)
  
Eine Zeichenfolge mit einem Zeichen, die die Groß-/Kleinschreibung berücksichtigt, die den Steuerelement Schlüssel angibt, der diesem Befehl zugewiesen ist. "A" weist beispielsweise diesen Befehl zur Steuerung von + UMSCHALT + A zu. Dieses Argument ist optional und wird nur für Befehle verwendet.
  
_pxHelpTopic_ (**xltypeStr**)
  
Ein optionaler Verweis auf die Hilfedatei (. chm oder. hlp), die angezeigt werden soll, wenn der Benutzer auf die Schaltfläche Hilfe klickt (wenn die benutzerdefinierte Funktion angezeigt wird). Kann im Formular `filepath!HelpContextID` oder `https://address/path_to_file_in_site!0`sein. Beide Teile vor und nach dem "!" sind erforderlich.  *HelpContextID* darf keine einfachen Anführungszeichen enthalten und wird von Excel in eine unsignierte Ganzzahl mit einer Länge von 4 Bytes in Dezimalform konvertiert. Wenn Sie das URL-Formular verwenden, öffnet Excel nur die referenzierte Hilfedatei. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Eine optionale Zeichenfolge zur Beschreibung der benutzerdefinierten Funktion, wenn Sie im Funktions-Assistenten ausgewählt wird.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Optional. Die erste der Zeichenfolgen, die die benutzerdefinierten Argumente der Funktion beschreiben, wenn die Funktion im Funktions-Assistenten ausgewählt ist. In Excel 2003 und früher kann **xlfRegister** maximal 30 Argumente annehmen, sodass Sie diese Hilfe nur für die ersten 20 ihrer Funktionsargumente bereitstellen können. Ab Excel 2007 kann **xlfRegister** bis zu 255 Argumente verwenden, sodass Sie diese Hilfe für bis zu 245 Funktionsparameter bereitstellen können. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn die Registrierung erfolgreich war, gibt diese Funktion die Register-ID der Funktion (**xltypeNum**) zurück, die in Aufrufen von **xlUDF** und **xlfUnregister** in einer DLL oder beim **aufrufen** und Aufheben der **Registrierung** in einem XML-Makroblatt verwendet werden kann. Andernfalls wird ein #VALUE! zurück. 
  
## <a name="remarks"></a>Bemerkungen

### <a name="data-types"></a>Datentypen

Das Argument _pxTypeText_ gibt den Datentyp des Rückgabewerts und die Datentypen aller Argumente für die DLL-Funktion oder Coderessource an. Das erste Zeichen von _pxTypeText_ gibt den Datentyp des Rückgabewerts an. Die restlichen Zeichen geben die Datentypen aller Argumente an. Eine DLL-Funktion, die eine Gleitkommazahl zurückgibt und eine ganze Zahl und eine Gleitkommazahl als Argumente akzeptiert, erfordert beispielsweise "BIB" für das _pxTypeText_ -Argument. 
  
Die Datentypen und Strukturen, die von Excel zum Austauschen von Daten mit XLLs verwendet werden, werden in den folgenden beiden Tabellen zusammengefasst.
  
In der ersten Tabelle sind die Typen aufgeführt, die in allen Versionen von Excel unterstützt werden.
  
|**Datentyp**|**Übergabe nach Wert**|**Übergabe nach Verweis (Zeiger)**|**Comments**|
|:-----|:-----|:-----|:-----|
|Boolesch  <br/> |A  <br/> |L  <br/> |Short [int] (0 = false oder 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |ASCII-Bytezeichenfolge mit Null-Terminierung  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |GeZählte ASCII-Byte-Zeichenfolge  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||16-Bit-WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16-Bit-Ganzzahl mit Vorzeichen  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32-Bit-Ganzzahl mit Vorzeichen  <br/> |
|FP  <br/> ||K  <br/> |Gleitkomma-Arraystruktur  <br/> |
|Array  <br/> ||O  <br/> |Es werden drei Argumente übergeben:<br/>-unsigned short int\*<br/>-unsigned short int\*<br/>-Double []  <br/> |
|XLOPER  <br/> ||P  <br/> |Variablen-Arbeitsblattwerte und Arrays  <br/> |
|||R  <br/> |Werte, Arrays und Bereichsbezüge  <br/> |
   
In Excel 2007 wurden die folgenden Datentypen eingeführt, um die größeren Raster und langen Unicode-Zeichenfolgen zu unterstützen.
  
|**Datentyp**|**Übergabe nach Wert**|**Übergabe nach Verweis (Zeiger)**|**Comments**|
|:-----|:-----|:-----|:-----|
|unsigned Short\*  <br/> ||C%, F%  <br/> |Zeichenfolge mit null-terminierter Unicode-Breitzeichen  <br/> |
|unsigned Short\*  <br/> ||D%, G%  <br/> |GeZählte Unicode-Breitzeichen-Zeichenfolge  <br/> |
|FP12  <br/> ||K%  <br/> |Größere Grid-Gleitkomma-Array Struktur  <br/> |
|Array  <br/> ||O%  <br/> |Es werden drei Argumente übergeben:<br/>-signed int \* /RW\*<br/>-signed int \* /Col\*<br/>-Double []  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Variablen-Arbeitsblattwerte und Arrays  <br/> |
|||U  <br/> |Werte, Arrays und Bereichsbezüge  <br/> |
   
Ab Excel 2010 wurden die folgenden Datentypen eingeführt:
  
|**Datentyp**|**Übergabe nach Wert**|**Übergabe nach Verweis (Zeiger)**|**Comments**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |Das asynchrone Handle wird verwendet, um einen ausstehenden asynchronen Funktionsaufruf von Excel und der XLL nachzuverfolgen. Das vorhanden sein des Parametertyps in der Typzeichenfolge kennzeichnet die Funktion auch als asynchron. Weitere Informationen zu asynchronen Funktionen finden Sie unter [asynchrone benutzerdefinierte Funktionen](asynchronous-user-defined-functions.md).  <br/> |
   
Die Zeichenfolgentypen **F**, **F%**, **G** und **G%** werden für Argumente verwendet, die direkt geändert werden. 
  
Beachten Sie beim Arbeiten mit den in der vorherigen Tabelle angezeigten Datentypen Folgendes:
  
- Die C-Language-Deklarationen gehen davon aus, dass der Compiler standardmäßig 8-Byte-Doubles, 2-Byte-Ganzzahlen und 4-Byte-lange ganze Zahlen verwendet.
    
- Alle Funktionen in DLLs und Code Ressourcen werden mithilfe der **__stdcall** -Aufrufkonvention aufgerufen. 
    
- Jede Funktion, die einen Datentyp als Verweis zurückgibt, also einen Zeiger auf etwas zurückgibt, kann einen NULL-Zeiger sicher zurückgeben. Excel interpretiert einen NULL-Zeiger als #NUM! zurück.
    
## <a name="additional-data-type-information"></a>Zusätzliche Datentypinformationen

Dieser Abschnitt enthält detaillierte Informationen zu den Datentypen **E**, **f**, **f**, **g**, **g**, h, **K**, **O**, **P**, **Q**, **R**und **U** sowie weitere Informationen zur _pxTypeText _-Argument. 
  
### <a name="e-data-type"></a>E-Datentyp

Excel erwartet, dass eine DLL den E-Datentyp verwendet, um Zeiger auf Gleitkommazahlen im Stapel zu übertragen. Dies kann Probleme mit einigen Sprachen verursachen (beispielsweise Borland C++), die davon ausgehen, dass die Nummer auf dem Emulator-Stapel des Prozessors übergeben wird. Die Problemumgehung besteht darin, einen Zeiger auf die Nummer im Prozessor Stapel zu übertragen. Das folgende Beispiel zeigt, wie Sie einen Double-Wert von Borland C++ zurückgeben.
  
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

### <a name="f-f-g-and-g-data-types"></a>F-, F%-, G-und G%-Datentypen

Mit den Datentypen **f**, **f%**, **g**und **g%** kann eine Funktion einen Zeichenfolgenpuffer ändern, der von Excel zugewiesen wird. Wenn der Rückgabewerttyp Code einer dieser Typen ist, ignoriert Excel den von der Funktion zurückgegebenen Wert. Stattdessen sucht Excel die Liste der Funktionsargumente für den ersten entsprechenden Datentyp (**f**, **f%**, **g**oder **g%**) und übernimmt dann den aktuellen Inhalt des zugewiesenen Zeichenfolgenpuffers als Rückgabewert. Alle Versionen von Excel weisen 256 Byte für **f** -und **g** -ASCII-Zeichenfolgen zu, und beginnend mit Excel 2007 65.536 byte werden genug für 32.768 Unicode-Zeichen für **f%** und **g%** Unicode-Strings reserviert. Beachten Sie, dass die Puffer ein count-Zeichen (Typen **g** und **g%**) oder ein null-Terminierungszeichen (Typen **f** und **f%**) aufweisen müssen, sodass die tatsächlichen maximalen Zeichenfolgenlängen 255 und 32.767 sind. Unicode-Zeichenfolgen und daher **F%** -und **G%** -Argumente sind nur über die C-API in Excel verfügbar. 
  
### <a name="k-and-k-data-types"></a>K-und K%-Datentypen

Die Datentypen **k** und **k%** verwenden Zeiger auf die Strukturen der FP-und FP12-Struktur mit variabler Größe. Diese Strukturen sind in XLLCALL definiert. H. FP12-Strukturen und daher **K%** -Argumente werden nur ab Excel 2007 unterstützt. 
  
### <a name="o-and-o-data-types"></a>O-und O%-Datentypen

Die **o** -und **o%** -Datentypen können nur für Argumente und nicht für Rückgabewerte verwendet werden, obwohl Werte zurückGegeben werden können, die ein **o** -oder **o%** -Typ-Argument ändern. Jeder übergibt drei Elemente: ein Zeiger auf die Anzahl der Zeilen in einem Array, ein Zeiger auf die Anzahl der Spalten in einem Array und einen Zeiger auf ein zweidimensionales Array von Gleitkommazahlen. 
  
Wenn Sie ein Array ändern möchten, das vom Datentyp O oder O% übergeben wurde, können Sie ">O" oder ">O%" als _pxTypeText_ -Argument verwenden. Weitere Informationen zum Ändern eines Arrays finden Sie im Abschnitt "Ändern von Funktionen, die als void deklariert wurden" in diesem Thema. 
  
Der **O** -Datentyp wurde für die direkte Kompatibilität mit Fortran-DLLs erstellt, die Argumente als Verweis übergeben. 
  
Die **O%** wird ab Excel 2007 unterstützt und entspricht der größeren Anzahl von Zeilen, die Excel unterstützt. 
  
### <a name="p-and-q-data-types"></a>P-und Q-Datentypen

Wenn DLL-Funktionsargumente unter dem Typ **P** XLOPERs oder Typ **Q** XLOPER12s registriert werden, konvertiert Excel einzelne zellenverweise auf einfache Werte und mehr zellenverweise auf Arrays, wenn Sie diese Argumente vorbereiten. Anders ausgedrückt werden **P** -und **Q** -Typen in ihrer Funktion immer als einer der folgenden Typen eingehen: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**oder **xltypeNil **, aber nicht **externen xltypeRef** oder **xltypeSRef** , da diese immer dereferenziert werden. **XLOPER12**s und daher Typ **Q** -argumente werden ab Excel 2007 nur unterstützt. 
  
Wenn die Typen **xltypeMissing** oder **xltypeNil** für Rückgabewerte verwendet werden, werden Sie von Excel als numerische NULL interpretiert. **xltypeMissing** wird übergeben, wenn der Aufrufer ein Argument auslässt. **xltypeNil** wird übergeben, wenn der Aufrufer einen Verweis auf eine leere Zelle übergibt. Wenn ein Zellbereich in ein **xltypeMulti** konvertiert wird, das als Typ **P** oder **Q**übergeben werden soll, werden alle leeren Zellen innerhalb des Bereiches in **xltypeNil** -Arrayelemente konvertiert. Fehlende Elemente in einem Literal-Array werden entsprechend als **xltypeNil** -Elemente übergeben. 
  
### <a name="volatile-functions-and-recalculation"></a>Flüchtige Funktionen und Neuberechnung

In einem Arbeitsblatt können Sie eine DLL-Funktion oder eine Coderessource als flüchtig festlegen, sodass Sie bei jeder Neuberechnung des Arbeitsblatts neu berechnet wird. Fügen Sie dazu ein Ausrufezeichen (!) nach dem letzten Argument Code im _pxTypeText_ -Argument hinzu. 
  
> [!NOTE]
> Standardmäßig werden Funktionen, die vom Typ **R** XLOPERs oder **** XLOPER12s und als Makroblatt äquivalente registriert sind (Typ **#**; siehe nächster Abschnitt), in Excel als flüchtig behandelt. 
  
### <a name="functions-declared-as-void"></a>Als void deklarierte Funktionen

Es gibt zwei Fälle, in denen eine Funktion als void zurückgegeben wird. In beiden Fällen gibt die Funktion das Ergebnis auf andere Weise zurück.
  
#### <a name="modifying-in-place"></a>Direktes Ändern

Sie können eine einzelne Ziffer _n_ für den Rückgabewert Code in _pxTypeText_verwenden, wobei _n_ eine Zahl zwischen 1 und 9 ist. Dadurch wird Excel angewiesen, den Wert der Variablen an der Stelle zu übernehmen, auf die durch das _n_th-Argument in _pxTypeText_ als Rückgabewert verwiesen wird. Dies wird auch als Änderung an Stelle bezeichnet. Bei dem _n_th-Argument muss es sich um einen Datentyp für die Weitergabe von verweisen handeln (C, D, E, F, F%, G, G, K, K,%, L, M, N, O,%, P, Q, R oder U). Die DLL-Funktion oder die Coderessource muss auch mit dem Schlüsselwort **void** in den Sprachen C/C++ (oder dem Schlüsselwort **Procedure** in der Sprache Pascal) deklariert werden. 
  
Beispielsweise kann eine DLL-Funktion, die eine NULL-terminierte Zeichenfolge akzeptiert, und zwei Zeiger auf ganze Zahlen als Argumente die Zeichenfolge ändern. Verwenden Sie "1FMM" als _pxTypeText_ -Argument, und deklarieren Sie die Funktion als void. 
  
Frühere Versionen von Excel, **\>** die am Anfang von _pxTypeText_ verwendet werden, um anzugeben, dass die Funktion als void deklariert wurde und dass das erste Argument direkt geändert werden sollte, gab es keine Möglichkeit, ein anderes Argument als das erste zu ändern. Die **\>** entspricht _n_ = 1 in aktuellen Excel-Versionen, und diese Verwendung von **\>** synchronen Funktionen wird nur aus Gründen der Abwärtskompatibilität unterstützt. 
  
#### <a name="asynchronous-functions"></a>Asynchrone Funktionen

Eine asynchrone Funktion, die mit einem Parameter vom Typ X in **pxTypeText**bezeichnet wird, gibt ihr Ergebnis nicht aus dem anfänglichen Funktionsaufruf zurück. Stattdessen müssen Sie eine asynchrone Funktion als void deklarieren, und später gibt das Add-in das Ergebnis über einen Rückruf zurück. Die asynchrone Funktion muss **\>** am Anfang von **pxTypeText**registriert werden. In asynchronen Funktionen **\>** weist darauf hin, dass die Funktion als void deklariert wird, aber nicht darauf hindeutet, dass das erste Argument direkt geändert wird. Weitere Informationen zu asynchronen Funktionen finden Sie unter [asynchrone benutzerdefinierte Funktionen](asynchronous-user-defined-functions.md). 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Registrieren von Arbeitsblattfunktionen als entsprechendes Makroblatt (Behandlung nicht berechneter Zellen)

Wenn Sie **#** ein Zeichen nach dem letzten Parametercode in _pxTypeText_ platzieren, erhält die Funktion die gleichen Aufrufberechtigungen wie Funktionen in einem Makroblatt. Hierbei handelt es sich um folgende Schritte vor dem Upgrade: 
  
- Die Funktion kann die Werte von Zellen abrufen, die noch nicht in diesem neuberechnungs Zyklus berechnet wurden.
    
- Die Funktion kann beliebige der XML-Informationsfunktionen (Klasse 2) aufrufen, beispielsweise **xlfGetCell**.
    
- Wenn das Nummernzeichen (#) nicht vorhanden ist: Auswerten einer nicht berechneten Zelle führt zu einem **xlretUncalced** -Fehler, und die aktuelle Funktion wird erneut aufgerufen, nachdem die Zelle berechnet wurde. das Aufrufen einer anderen XML-Informationsfunktion als **xlfCaller** führt zu einem **xlretInvXlfn** -Fehler. 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Registrieren von Arbeitsblattfunktionen als threadsicher

Ab Excel 2007 kann Excel die Neuberechnung von Multithread-Arbeitsmappen ausführen. Dies führt dazu, dass Sie unterschiedliche Instanzen einer threadsicheren Funktion gleichzeitigen Threads für die erneute Auswertung zuweisen können. Ab Excel 2007 sind die meisten integrierten Arbeitsblattfunktionen threadsicher. Ab Excel 2007 ermöglicht Excel auch XLLs das Registrieren von Arbeitsblattfunktionen als threadsicher. Fügen Sie dazu ein Zeichen nach **$** dem letzten Parametercode in _pxTypeText_ein. 
  
> [!NOTE]
> Nur Arbeitsblattfunktionen können als threadsicher deklariert werden. Excel betrachtet eine entsprechende Makroblatt Funktion nicht als threadsicher, sodass Sie nicht beide **#** und **$** Zeichen an das _pxTypeText_ -Argument anfügen können. 
  
Wenn Sie eine Funktion als threadsicher registriert haben, müssen Sie sicherstellen, dass Sie sich auf threadsicher verhält, obwohl Excel Thread unsichere Aufrufe über die C-API ablehnt. Wenn beispielsweise eine threadsichere Funktion versucht, **xlfGetCell**aufzurufen, schlägt der Aufruf mit dem **xlretNotThreadSafe** -Fehler fehl. 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Registrieren von Arbeitsblattfunktionen als Cluster sicher

Ab Excel 2010 kann Excel Funktionsaufrufe an einen festgelegten Compute-Cluster Anbieter Abladen. Weitere Informationen finden Sie unter [Cluster Safe Functions](cluster-safe-functions.md). Alle XLL-Arbeitsblattfunktionen, die als Cluster sicher registriert sind, nehmen an der Entlastung bei, wenn ein Cluster verfügbar ist. Cluster sichere Funktionen werden registriert, indem das **&amp;** Zeichen nach dem letzten Parametercode im _pxTypeText_ -Argument eingeschlossen wird. 
  
Wenn Sie eine Funktion als Cluster sicher registriert haben, müssen Sie sicherstellen, dass Sie sich auf eine Cluster sichere Weise verhält. Weitere Informationen finden Sie unter [Cluster Safe Functions](cluster-safe-functions.md).
  
> [!NOTE]
> Nur Arbeitsblattfunktionen können als Cluster sicher deklariert werden. In Excel wird die äquivalente Funktion eines Makro Blatts nicht als Cluster sicher betrachtet, sodass Sie sowohl **#** als auch **&amp;** Zeichen nicht an das _pxTypeText_ -Argument anfügen können. Arbeitsblattfunktionen können sowohl als Cluster sicher als auch als threadsicher deklariert werden. In diesem Fall ermöglicht Excel, dass diese Funktionen bei deaktivierter Cluster Verschiebung an Multithread-Neuberechnungen beteiligt werden. 
  
### <a name="category-names"></a>Kategorienamen

Verwenden Sie die folgenden Richtlinien, um zu bestimmen, in welcher Kategorie ihre XLL-Funktionen platziert werden sollen.
  
- Wenn die Funktion etwas bewirkt, das vom Benutzer als Teil ihrer Add-in-Benutzeroberfläche ausgeführt werden kann, sollten Sie die Funktion in die Kategorie **Commands** einfügen. 
    
- Wenn die Funktion Informationen über den Zustand des Add-Ins oder andere nützliche Informationen zurückgibt, sollten Sie die-Funktion in der Kategorie **Information** platzieren. 
    
- Ein Add-in sollte nie Funktionen oder Befehle zur **benutzerdefinierten** Kategorie hinzufügen. Diese Kategorie ist ausschließlich für Endbenutzer bestimmt. 
    
Die Kategorie wird mithilfe des _pxCategory_ -Parameters für **xlfRegister**angegeben. Dabei kann es sich um eine Zahl oder einen Text handeln, der einer der hartcodierten Standardkategorien entspricht, oder dem Text einer neuen Kategorie, die von der DLL angegeben wird. Wenn der angegebene Text noch nicht vorhanden ist, erstellt Excel eine neue Kategorie mit diesem Namen.
  
In der folgenden Tabelle sind die Standardkategorien aufgeführt, die angezeigt werden, wenn Sie das Dialogfeld **Funktion einfügen** aus einem Arbeitsblatt anzeigen. 
  
|**Number**|**Text**|
|:-----|:-----|
|1  <br/> |Finanzen  <br/> |
|2  <br/> |Datum &amp; und Uhrzeit  <br/> |
|3  <br/> |Math. &amp; Trigonom.  <br/> |
|4  <br/> |Text  <br/> |
|5  <br/> |Logik  <br/> |
|6  <br/> |Lookup &amp; Reference  <br/> |
|7  <br/> |Datenbank  <br/> |
|8  <br/> |Statistik  <br/> |
|9  <br/> |Informationen  <br/> |
|14  <br/> |Benutzerdefiniert  <br/> |
||Engineering (ab Excel 2007)  <br/> |
||Cube (ab Excel 2007)  <br/> |
   
Darüber hinaus werden diese Kategorien auch angezeigt, wenn Sie das Dialogfeld **Funktion einfügen** aus einer Makrovorlage anzeigen. 
  
|**Number**|**Text**|
|:-----|:-----|
|10  <br/> |Befehle  <br/> |
|11  <br/> |DDE/Extern  <br/> |
|12  <br/> |Benutzerorientiert  <br/> |
|13  <br/> |Makrosteuerung  <br/> |
   
### <a name="example"></a>Beispiel

Weitere Informationen finden Sie im **** Code für die `\SAMPLES\GENERIC\GENERIC.C`xlAutoOpen-Funktion in.
  
## <a name="see-also"></a>Siehe auch

- [REGISTER.ID](xlfregisterid.md)
- [Registrierung](xlfunregister-form-1.md)
- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

