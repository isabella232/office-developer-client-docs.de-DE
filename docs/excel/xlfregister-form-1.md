---
title: XlfRegister (Formular 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- XlfRegister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4fb4e8656b4f27105a30764cdda020849a07645e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790603"
---
# <a name="xlfregister-form-1"></a>XlfRegister (Formular 1)

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann aus einem Befehl DLL oder XLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde. Dies ist gleich aus einer Excel-XLM-Makrovorlage Aufrufen **Registrieren** . 
  
**XlfRegister** kann in zwei Formen aufgerufen werden: 
  
- XlfRegister (Formular 1): registriert einen einzelnen Befehl oder eine Funktion.
    
- [XlfRegister (Form 2)](xlfregister-form-2.md): Lasten und aktiviert eine XLL.
    
In Form 1 aufgerufen, diese Funktion stellt eine DLL-Funktion oder einen Befehl nach Excel zur Verfügung, dessen Verwendungszähler auf 1 festgelegt, und gibt seine Registrierung-ID, die an die Funktion später erneut anzurufen, mithilfe der [XlUDF](xludf.md) oder die **XlfCall** -Funktion verwendet werden kann. Die ID der Registrierung wird auch zum Aufheben der Registrierung der Funktion mit [XlfUnregister (Formular 1)](xlfunregister-form-1.md)verwendet. Wenn die Funktion registriert wurde, inkrementiert **XlfRegister** erneut aufrufen seiner Verwendung. 
  
Diese Form der Funktion definiert ausgeblendeten Name das Argument Funktion Text _PxFunctionText_, also und der Ausdruck ergibt auch auf die Registrierung-ID der Funktion oder Befehl. Wenn Sie die Funktion aufgehoben, löschen Sie dieser Name mit dem [XlfSetName](xlfsetname.md). Weitere Informationen finden Sie unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).
  
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

_pxModuleText_ (**XltypeStr**)
  
Der Name der DLL, die die Funktion enthält. Dies kann durch Aufrufen von nur XLL-Funktion, [XlGetName](xlgetname.md) , wenn die Funktion registriert auch innerhalb der derzeit ausgeführten DLL abgerufen werden. 
  
_pxProcedure_ (**XltypeStr** oder **XltypeNum**)
  
Wenn eine Zeichenfolge wird der Name der Funktion aufrufen, wie er in der DLL-Code angezeigt. Wenn eine Zahl, die Ordinal-Eigenschaft Anzahl der aufzurufenden Funktion exportieren. Aus Gründen der Übersichtlichkeit immer verwenden Sie in Form einer Zeichenfolge.
  
_pxTypeText_ (**XltypeStr**)
  
Ein optionaler String, der die Typen der Argumente an die Funktion und den Typ des Rückgabewerts der Funktion angibt. Weitere Informationen finden Sie unter "Anmerkungen". Dieses Argument kann für eine eigenständige DLL (XLL) ausgelassen werden, die ein [XlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) oder **xlAutoRegister12**enthält. 
  
> [!NOTE]
> **xlAutoRegister12** wird nur in Excel 2007 unterstützt. 
  
Wenn dieses Argument fehlt **XlfRegister** aufgerufen wird, Excel ruft **XlAutoRegister** oder **xlAutoRegister12**, wenn einer der beiden vorhanden ist, in der angegebenen DLL, die dann ordnungsgemäß die Funktion registrieren sollte durch diese Informationen bereitstellen.
  
_pxFunctionText_ (**XltypeStr**)
  
Funktionsname, wie er erscheint im Funktions-Assistenten. Dieses Argument ist optional. Wenn es ausgelassen wird, wird die Funktion ist nicht verfügbar in den Funktions-Assistenten, und kann nur mithilfe der **rufen Sie** mithilfe der Funktionen Registration-ID aus einer XLM-Makrovorlage-Funktion aufgerufen werden. Aus diesem Grund sollten Sie für die Verwendung des normalen Arbeitsblatt, dieses Argument nach Bedarf behandelt. 
  
_pxArgumentText_ (**XltypeStr**)
  
Ein optionaler Text-Zeichenfolge, die Argumente an die Funktion beschreibt. Der Benutzer sieht dies im Funktions-Assistenten. Wenn es nicht angegeben ist, erstellt Excel grundlegende Beschreibungen von _PxTypeText_.
  
_pxMacroType_ (**XltypeNum** oder **vom Typ XltypeInt**)
  
Zeigen Sie ein optionales Argument, das den Typ des XLL-Eintrags angibt. Der Standardwert, ist wenn es ausgelassen wird, 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _PxMacroType Wert_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Kann aus einem Arbeitsblatt aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Kann von einem Makroblatt aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|Kann aus einer Definition definierten Namen aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|Kann aus einem Ausdruck für bedingte Formatierung aufgerufen werden  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|In den Funktions-Assistenten für Microsoft Excel-Arbeitsblattfunktionen aufgeführten  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|In den Funktions-Assistenten für Makro Blatt Funktionen aufgelistet  <br/> |Nein  <br/> |Ja  <br/> |Ja  <br/> |
   
Sie sollten 1 für Microsoft Excel-Arbeitsblattfunktionen, 1 für Makro Blatt entsprechenden Funktionen verwenden, in der Praxis (als Typ registriert **#**), die Sie aus dem Arbeitsblatt und 2 für Befehle aufrufen möchten. 
  
> [!NOTE]
> XLL-Befehle ausgeblendet und nicht in den Dialogfeldern für die Ausführung von Makros angezeigt werden, ein gültigen Befehlsnamen ist erforderlich, auch wenn ihre Namen an einer beliebigen Stelle eingegeben werden können. 
  
_pxCategory_ (**XltypeStr** oder **XltypeNum**)
  
Ein optionales Argument, mit dem Sie die Kategorie an, die die neue Funktion oder den Befehl gehören soll. Funktions-Assistenten dividiert Funktionen durch Type (Kategorie). Sie können angeben, einen Kategorienamen oder eine fortlaufende Zahl, wobei die Anzahl der Position ist in der die Kategorie im Funktions-Assistenten angezeigt wird. Weitere Informationen finden Sie im Abschnitt "Kategorienamen". Wenn es ausgelassen wird, wird davon ausgegangen, dass die benutzerdefinierte Kategorie.
  
_pxShortcutText_ (**XltypeStr**)
  
Eine Zeichenfolge einem Zeichen, Groß-/Kleinschreibung beachtet, die angibt, die dem Befehl zugewiesene STRG-Taste. "A" wird beispielsweise mit diesem Befehl STRG + UMSCHALT + A. Dieses Argument ist optional und wird für die Befehle nur.
  
_pxHelpTopic_ (**XltypeStr**)
  
Einen optionalen Verweis auf die Hilfedatei (chm oder hlp) angezeigt wird, wenn der Benutzer die Schaltfläche Hilfe klickt (wenn die benutzerdefinierte Funktion angezeigt wird). Kann im Format `filepath!HelpContextID` oder `http://address/path_to_file_in_site!0`. Beide Webparts vor und nach der "!" sind erforderlich.  *HelpContextID* darf keine Apostrophe enthalten und wird von Excel in eine Ganzzahl ohne Vorzeichen 4 Bytes lang, im Dezimalformat konvertiert werden. Wenn Sie das URL-Formular zu verwenden, wird Excel nur die referenzierten Hilfedatei geöffnet. 
  
_pxFunctionHelp_ (**XltypeStr**)
  
Ein optionaler String, der die benutzerdefinierte Funktion beschreibt, wenn er im Funktions-Assistenten ausgewählt ist.
  
_pxArgumentHelp1_ (**XltypeStr**)
  
Optional. Die erste der Zeichenfolgen, die die benutzerdefinierten Argumente der Funktion beschreiben, wenn die Funktion im Funktions-Assistenten ausgewählt wird. In Excel 2003 und früheren Versionen können **XlfRegister** , maximal 30 Argumente, damit Sie diese Hilfe für die ersten 20 nur Ihre Funktionsargumente bereitstellen können. Ab Excel 2007 können **XlfRegister** bis zu 255 Argumente, damit Sie diese Hilfe für bis zu 245 Funktionsparameter bereitstellen können. 
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Wenn die Registrierung erfolgreich war, gibt diese Funktion die Register-ID der Funktion (**XltypeNum**), die in Aufrufen von **XlUDF** und **XlfUnregister** in einer DLL oder mit **ANRUFEN** und **Registrierung** in einer XLM-Makrovorlage verwendet werden kann. Andernfalls gibt es eine #VALUE! Fehler. 
  
## <a name="remarks"></a>Hinweise

### <a name="data-types"></a>Datentypen

Das Argument _PxTypeText_ gibt den Datentyp des Rückgabewerts und die Datentypen der Argumente der DLL-Funktion oder Code-Ressource. Das erste Zeichen des _PxTypeText_ gibt den Datentyp des Rückgabewerts. Das erste Zeichen gibt die Datentypen aller Argumente. Beispielsweise würde eine DLL-Funktion, die gibt eine Gleitkommazahl zurück und akzeptiert eine ganze Zahl und eine Gleitkommazahl als Argumente "LITERATURVERZEICHNIS" für das Argument _PxTypeText_ erfordern. 
  
Die Datentypen und Strukturen, die von Excel zum Austauschen von Daten mit XLLs verwendet werden in den folgenden zwei Tabellen zusammengefasst.
  
Die erste Tabelle enthält die in allen Versionen von Excel unterstützten Typen.
  
|**Datentyp**|**Übergebener Wert**|**Übergebener Verweis (Zeiger)**|**Comments**|
|:-----|:-----|:-----|:-----|
|Boolean  <br/> |A  <br/> |L  <br/> |Short [Int] (0 = False oder 1 = True)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|Char\*  <br/> ||C, F  <br/> |NULL endende ASCII-Byte-Zeichenfolge  <br/> |
|ohne Vorzeichen\*  <br/> ||D, G  <br/> |Gezählte ASCII-Byte-Zeichenfolge  <br/> |
|nicht signierte Short [Int]  <br/> |H  <br/> ||16-Bit-Version von WORD  <br/> |
|[signed] Short [Int]  <br/> |I  <br/> |M  <br/> |16-Bit-Ganzzahl mit Vorzeichen  <br/> |
|[lange signiert] Int  <br/> |J  <br/> |N  <br/> |32-Bit-Ganzzahl mit Vorzeichen  <br/> |
|FZ  <br/> ||K  <br/> |Gleitkommazahl Arraystruktur  <br/> |
|Array  <br/> ||O  <br/> |Es werden drei Argumente übergeben:<br/>-nicht signierte kurze Int\*<br/>-nicht signierte kurze Int\*<br/>-double]  <br/> |
|XLOPER  <br/> ||P  <br/> |Variable vom Typ Arbeitsblattwerte und arrays  <br/> |
|||R  <br/> |Werte, Arrays und Bereich Referenzen  <br/> |
   
In Excel 2007, die die folgenden Datentypen eingeführt wurden zur Unterstützung der größerer Raster und lange Unicode-Zeichenfolgen.
  
|**Datentyp**|**Übergebener Wert**|**Übergebener Verweis (Zeiger)**|**Comments**|
|:-----|:-----|:-----|:-----|
|nicht signierte short\*  <br/> ||C %, F %  <br/> |Zeichenfolge mit NULL terminierte Unicode-Breitzeichen  <br/> |
|nicht signierte short\*  <br/> ||D %, G %  <br/> |Gezählte Unicode-Zeichenfolge mit Breitzeichen  <br/> |
|FP12  <br/> ||K %  <br/> |Größere Rasterstruktur Gleitkomma-array  <br/> |
|Array  <br/> ||O %  <br/> |Es werden drei Argumente übergeben:<br/>-signiert Int \* / Lese\*<br/>-signiert Int \* / SP\*<br/>-double]  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Variable vom Typ Arbeitsblattwerte und arrays  <br/> |
|||U  <br/> |Werte, Arrays und Bereich Referenzen  <br/> |
   
Die folgenden Daten in Excel 2010 beginnende wurden Typen eingeführt:
  
|**Datentyp**|**Übergebener Wert**|**Übergebener Verweis (Zeiger)**|**Comments**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |Von Excel und die XLL wird asynchrone Handle zum Nachverfolgen eines ausstehenden asynchronen Funktionsaufrufs verwendet. Das Vorhandensein der den Parametertyp in der Zeichenfolge weist die Funktion auch als asynchrone. Weitere Informationen zu asynchronen Funktionen finden Sie unter [Asynchronous User-Defined-Funktionen](asynchronous-user-defined-functions.md).  <br/> |
   
Die Zeichenfolgentypen **F**, **F %**, **G**und **G %** werden für Argumente verwendet, die direkte geändert werden. 
  
Bei der Arbeit mit der Datentypen, die in der vorherigen Tabelle angezeigt werden Sie sollten Sie Folgendes beachten:
  
- Die Programmiersprache C-Deklarationen wird davon ausgegangen, dass Ihre Compiler standardmäßig 8-Byte-verdoppelt, kurze 2-Byte-Ganzzahlen und 4-Byte-Ganzzahlen verwendet.
    
- Alle Funktionen in DLLs und Code-Ressourcen sind mit der Aufrufkonvention **__stdcall** aufgerufen. 
    
- Jede Funktion, die einen Datentyp per Verweis, d. h.,, der einen Zeiger auf einen anderen Wert zurückgibt zurückgibt, kann problemlos einen null-Zeiger zurück. Excel interpretiert einen null-Zeiger als ein #NUM! Fehler.
    
## <a name="additional-data-type-information"></a>Zusätzliche Datentypinformationen

Dieser Abschnitt enthält ausführliche Informationen zu den **E**, **F**, **F %**, **G**, **G %**, **K**, **O**, **P**, **Q**, **R**und **U** -Datentypen und andere Informationen zu den _pxTypeText _Argument. 
  
### <a name="e-data-type"></a>E-Datentyp

Excel erwartet eine DLL unter Verwendung des Datentyps E Zeiger an Gleitkommawerte auf dem Stapel übergeben. Dadurch können Probleme mit einigen Sprachen (beispielsweise Borland C++), die erwarten, dass die Zahl, die auf dem Coprozessor Emulator Stapel übergeben werden sollen. Die problemumgehung besteht darin, einen Zeiger auf der Anzahl der Coprozessor Stapel übergeben. Im folgenden Beispiel wird gezeigt, wie Borland C++ einen Double-Wert zurückgegeben.
  
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

### <a name="f-f-g-and-g-data-types"></a>F, F %, G und G %-Datentypen

Mit der **F**, **F %**, **G**und **G %** -Datentypen kann eine Funktion einen Zeichenfolgenpuffer bearbeiten, der von Excel zugeordnet ist. Wenn der Code für den Rückgabewert dieser Typ ist, ignoriert Excel den Wert, der von der Funktion zurückgegeben. Stattdessen Excel durchsucht die Liste der Argumente der Funktion für den ersten entsprechenden Datentyp (**F**, **F %**, **G**oder **G %**) und nimmt dann den aktuellen Inhalt des Puffers zugewiesene Zeichenfolge als Rückgabewert. Alle Versionen von Excel reservieren 256 Byte für **F** und **G** ASCII-Zeichenfolgen, und starten in Excel 2007 65.536 Byte zugeordnet werden, genügend für 32.768 Unicode-Zeichen, **F %** und **G %** Unicode-Zeichenfolgen. Denken Sie daran, dass die Puffer ein Count Zeichen (Typen **G** und **G %**) oder ein Null-abschließendes Zeichen (Typen **F** und **F %**) umfassen müssen, damit die Zeichenfolge tatsächlich maximale Länge 255 und 32.767 sind. Unicode-Zeichenfolgen und Typargumente **F** und **G %** , daher stehen nur über die C-API in Excel. 
  
### <a name="k-and-k-data-types"></a>K und K %-Datentypen

Verwenden Sie die Datentypen **K** und **K %** Zeiger auf die FZ und FP12 Strukturen variabler Größe jeweils. Diese Strukturen sind in XLLCALL definiert. H. FP12 Strukturen und daher **K %** Typargumente, werden nur unterstützt ab Excel 2007. 
  
### <a name="o-and-o-data-types"></a>O und O %-Datentypen

Die Datentypen **O** und **O %** kann nur für Argumente verwendet werden, nicht als Rückgabewerte, obwohl meine ändern direkten Typargument **O** oder **O %** Werte zurückgegeben werden können. Jede übergibt drei Elemente: einen Zeiger auf die Anzahl der Zeilen in einem Array, einen Zeiger auf die Anzahl der Spalten in einem Array und einen Zeiger auf ein zweidimensionales Array von Gleitkommawerte. 
  
So ändern Sie ein Array von O oder O übergeben % Datentyp direkt, Sie können "> O" oder "> O %" als Argument _PxTypeText_ . Weitere Informationen zum Ändern der ein Array finden Sie im Abschnitt "Ändern in Place: deklariert als Void Funktionen" in diesem Thema. 
  
Der Datentyp **O** wurde für die direkte Kompatibilität mit Fortran-DLLs erstellt, die Argumente als Verweis zu übergeben. 
  
Die **O %** wird unterstützt ab Excel 2007 und berücksichtigt die größere Anzahl von Zeilen, die von Excel unterstützt. 
  
### <a name="p-and-q-data-types"></a>P und Q-Datentypen

Wenn Argumente DLL-Funktion als Typ **P** XLOPERs weiterführen registriert sind, oder geben Sie **Q** XLOPER12s, konvertiert Excel einzelne Zelle Verweise auf einfache Werte und Verweise auf Arrays mit mehreren Zelle bei der Vorbereitung der Argumente. Anders ausgedrückt, **P** und **Q** Typen werden immer Eintreffen in Ihrer Funktion als eines der folgenden Typen: **XltypeNum**, **XltypeStr**, **XltypeBool**, **XltypeErr**, **XltypeMulti**, **XltypeMissing**oder **XltypeNil **, nicht jedoch **XltypeRef** oder **XltypeSRef** , da diese immer aufgehoben werden. **XLOPER12**s und daher **Q** Typargumente werden nur unterstützt ab Excel 2007. 
  
Wenn Typen **XltypeMissing** oder **XltypeNil** für Rückgabewerte verwendet werden, als numerische 0 (null) von Excel interpretiert. Wenn der Aufrufer ein Argument weggelassen wird, wird **XltypeMissing** übergeben. **XltypeNil** wird übergeben, wenn der Aufrufer einen Verweis auf eine leere Zelle übergibt. Wenn ein Zellbereich in einer **XltypeMulti** als Typ **P** oder **Q**übergeben werden konvertiert wird, werden alle leeren Zellen des Bereichs in Arrayelementen **XltypeNil** konvertiert. Fehlende Elemente in einem Array von literalen werden auf ähnliche Weise als **XltypeNil** Elemente übergeben. 
  
### <a name="volatile-functions-and-recalculation"></a>Veränderliche Funktionen und erneute Berechnung

In einem Arbeitsblatt können Sie eine DLL-Funktion oder Coderessource erzwingen, dass dass neu berechnet, jedes Mal, wenn das Arbeitsblatt neu berechnet. Fügen Sie dazu ein Ausrufezeichen (!) nach dem letzten Argument Code im Argument _PxTypeText_ . 
  
> [!NOTE]
> Funktionen, die Typ **R** XLOPERs übernehmen, oder geben Sie **U** XLOPER12s und als Makro registriert sind, standardmäßig Blatt-Entsprechungen (Typ **#**; finden Sie im nächsten Abschnitt) als veränderlich in Excel verarbeitet werden. 
  
### <a name="functions-declared-as-void"></a>Funktionen als nichtig

Es gibt zwei Fälle, die zum Deklarieren einer Funktion als Void zurückgeben aufrufen. In beiden Fällen wird das Ergebnis die Funktion mit anderen Mitteln zurückgibt.
  
#### <a name="modifying-in-place"></a>Direktes Ändern

Sie können eine einzelne Ziffer _n_ für den Rückgabetyp Code in _PxTypeText_, wobei _n_ eine Zahl von 1 bis 9 ist. Dies weist Excel an, den Wert der Variablen in der Speicherort, der durch das Argument _n_th in _PxTypeText_ als Rückgabewert auf annehmen. Dies wird auch als direkte ändern bezeichnet. Das _n_th-Argument muss eine Referenz zu übergeben Datentyp (C, D, E, F, F %, G, G %, K, K %, L, M, N, O, O %, P, Q, R, oder U) sein. Die DLL-Funktion oder Code-Ressource muss auch mit dem **void** -Schlüsselwort in der C/C++-Sprachen (oder **Prozedur** -Schlüsselwort in der Sprache Pascal) deklariert werden. 
  
Beispielsweise wird eine DLL-Funktion, die eine mit Null endende Zeichenfolge und zwei Zeiger zu ganzen Zahlen als Argumente die Zeichenfolge direkt ändern können. Verwenden Sie "die Zeichenfolge 1FMM" als Argument _PxTypeText_ , und die Funktion wird als nichtig deklariert. 
  
Frühere Versionen von Excel verwendete **\>** am Anfang des _PxTypeText_ , um anzugeben, dass die Funktion wie void deklariert wurde und dass das erste Argument wurde direkt geändert werden soll – gab es keine Möglichkeit, die ein der Argumente bis auf das erste ändern. Die **\>** entspricht dem _n_ = 1 in der aktuellen Excel-Versionen und Verwendung der **\>** in synchronen Funktionen wird nur für Abwärtskompatibilität unterstützt. 
  
#### <a name="asynchronous-functions"></a>Asynchrone Funktionen

Eine asynchrone-Funktion mit einem Parameter vom Typ X in **PxTypeText**, gekennzeichnet gibt keine Ergebnisses aus der anfänglichen Funktionsaufruf zurück. Stattdessen müssen Sie eine asynchrone Funktion als void deklarieren und später das Add-in gibt das Ergebnis über einen Rückruf. Die asynchrone-Funktion muss registriert werden, mithilfe von **\>** am Anfang des **PxTypeText**. Asynchrone Funktionen **\>** gibt an, dass die Funktion ist als void deklariert, doch bedeutet nicht, dass das erste Argument direkt geändert wird. Weitere Informationen zu asynchronen Funktionen finden Sie unter [Asynchronous User-Defined-Funktionen](asynchronous-user-defined-functions.md). 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Registrieren von Microsoft Excel-Arbeitsblattfunktionen als Makro Blatt Entsprechungen (behandeln gekennzeichnete Zellen)

Platzieren von einer **#** Zeichen, nachdem der letzte Parameter Code in _PxTypeText_ die Funktion in einer Makrovorlage aufrufenden dieselben Berechtigungen wie Funktionen gibt. Dies sind wie folgt: 
  
- Die Funktion kann der Werte von Zellen abrufen, die noch nicht in diesem Zyklus neuberechnung berechnet wurde.
    
- Die Funktion kann eine der XLM Informationen (Klasse 2) Funktionen, beispielsweise **XlfGetCell**aufrufen.
    
- Wenn die Nummernzeichen (#) nicht vorhanden ist: eine Zelle gekennzeichnete Ergebnisse in ein **XlretUncalced** Fehler und der aktuellen Funktion auswerten erneut aufgerufen wird, sobald die Zelle berechnet wurde; eine beliebige XLM-Informationen-Funktion als **XlfCaller** aufrufen erzeugt einen Fehler **XlretInvXlfn** . 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Registrieren von Microsoft Excel-Arbeitsblattfunktionen als threadsicheren

Ab Excel 2007, kann Excel multithreaded Arbeitsmappe neuberechnung ausführen. Dies bedeutet, dass es verschiedene Instanzen einer threadsicheren Funktion gleichzeitige Threads für die erneute Auswertung zuweisen kann. Ab Excel 2007 sind die meisten integrierten Arbeitsblattfunktionen threadsicheren. Ab Excel 2007, kann Excel auch zum Registrieren von Microsoft Excel-Arbeitsblattfunktionen als threadsicheren XLLs. Dazu gehören ein **$** Zeichen nach dem letzten Parameter Code in _PxTypeText_. 
  
> [!NOTE]
> Nur Microsoft Excel-Arbeitsblattfunktionen können als threadsicheren deklariert werden. Excel berücksichtigt eine entsprechende Blatt Makrofunktion threadsicheren, sein, damit Sie beide anfügen können keine **#** und **$** Zeichen an das Argument _PxTypeText_ . 
  
Wenn Sie eine Funktion als threadsicheren registriert haben, müssen Sie, dass es auf eine Weise threadsicheren verhält sicherstellen, obwohl Excel eine beliebige Thread unsichere Anrufe über den der C-API abgelehnt. Beispielsweise wenn eine Funktion threadsicheren versucht, **XlfGetCell**aufzurufen, schlägt der Aufruf der **XlretNotThreadSafe** Fehler. 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Registrieren von Microsoft Excel-Arbeitsblattfunktionen als clustersichere

Starten in Excel 2010, kann Excel Funktionsaufrufe zu einem festgelegten Compute Cluster-Anbieter abnimmt. Weitere Informationen finden Sie unter [Clustersichere Funktionen](cluster-safe-functions.md). Alle XLL Arbeitsblattfunktionen als clustersichere registriert teilnehmen in Abladung, wenn ein Cluster verfügbar ist. Clustersichere-Funktionen werden durch das Einbeziehen von registriert die **&amp;** nach dem letzten Parameter Code im Argument _PxTypeText_ Zeichen. 
  
Wenn Sie eine Funktion als clustersichere registriert haben, müssen Sie sicherstellen, dass es auf eine Weise clustersichere verhält. Weitere Informationen finden Sie unter [Clustersichere Funktionen](cluster-safe-functions.md).
  
> [!NOTE]
> Nur Microsoft Excel-Arbeitsblattfunktionen können als clustersichere deklariert werden. Excel berücksichtigt eine entsprechende Blatt Makrofunktion clustersichere, sein, damit Sie beide anfügen können keine **#** und **&amp;** Zeichen an das Argument _PxTypeText_ . Microsoft Excel-Arbeitsblattfunktionen können als clustersichere und threadsicheren deklariert werden. In diesem Fall kann Excel ansetzt, diese Funktionen zum Teilnehmen an multithreaded neuberechnung beim Cluster Abladung deaktiviert ist. 
  
### <a name="category-names"></a>Kategorienamen

Verwenden Sie die folgenden Richtlinien, um zu bestimmen, in welcher Kategorie platzieren Ihrer XLL-Funktionen.
  
- Wenn die Funktion Aktionen, die vom Benutzer als Teil der Add-in-Benutzeroberfläche durchgeführt werden kann ausführt, sollten Sie die Funktion in der Kategorie **Befehle** angeben. 
    
- Wenn die Funktion Informationen zum Status des Add-Ins oder andere nützliche Informationen zurückgegeben werden, sollten Sie die Funktion in der Kategorie **Informationen** . 
    
- Ein Add-in sollten niemals Funktionen oder Befehle die **Benutzerdefinierte** Kategorie hinzufügen. Diese Kategorie ist für die ausschließliche Verwendung von Endbenutzern. 
    
Die Kategorie ist mit dem Parameter _PxCategory_ auf **XlfRegister**angegeben. Dies kann eine Nummer oder Text, der die hartcodierte Standardkategorien entspricht oder den Text einer neuen Kategorie, die von der DLL angegeben sein. Wenn der angegebene Text nicht bereits vorhanden ist, wird in Excel eine neue Kategorie mit diesem Namen erstellt.
  
Die folgende Tabelle enthält die Standardkategorien, die angezeigt werden, wenn Sie das Dialogfeld **Funktion einfügen** von in einem Arbeitsblatt anzeigen. 
  
|**Nummer**|**Text**|
|:-----|:-----|
|1  <br/> |Finanzmathematik  <br/> |
|2  <br/> |Datum &amp; Zeit  <br/> |
|3  <br/> |Math &amp; Trig  <br/> |
|4  <br/> |Text  <br/> |
|5  <br/> |Logisch  <br/> |
|6  <br/> |Lookup &amp; Verweis  <br/> |
|7  <br/> |Datenbank  <br/> |
|8  <br/> |Statistische  <br/> |
|9  <br/> |Information  <br/> |
|14  <br/> |Benutzerdefinierte  <br/> |
||Engineering (beginnend in Excel 2007)  <br/> |
||Cube (beginnend in Excel 2007)  <br/> |
   
Darüber hinaus werden diese Kategorien auch angezeigt, wenn Sie das Dialogfeld **Funktion einfügen** aus in eine Makrovorlage anzeigen. 
  
|**Nummer**|**Text**|
|:-----|:-----|
|10  <br/> |Befehle  <br/> |
|11  <br/> |DDE/externer  <br/> |
|12  <br/> |Anpassen  <br/> |
|13  <br/> |Makrosteuerung  <br/> |
   
### <a name="example"></a>Beispiel

Finden Sie im Code die Funktion **XlAutoOpen** in `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Siehe auch

- [REGISTER.](xlfregisterid.md)
- [AUFHEBEN DER REGISTRIERUNG](xlfunregister-form-1.md)
- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

