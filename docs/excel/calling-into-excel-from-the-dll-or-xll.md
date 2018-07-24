---
title: Aufrufen von Excel von der DLL oder XLL aus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- dialog boxes [excel 2007], invoking excel commands,DLLs [Excel 2007], calling into Excel,passing arguments to C API functions [Excel 2007],commands [Excel 2007], invoking with dialog boxes,commands [Excel 2007], accessible from DLL/XLL,Excel4 function [Excel 2007],Excel12 function [Excel 2007],XLCallVer function [Excel 2007],operRes argument [Excel 2007],functions [Excel 2007], accessible from DLL/XLL,Excel12v function [Excel 2007],DLL-only functions [Excel 2007],C API [Excel 2007], passing arguments,count argument [Excel 2007],commands [Excel 2007], calling in international versions,DLL-only commands [Excel 2007],international versions [Excel 2007], calling functions and commands,XLLs [Excel 2007], calling into Excel,Excel 4v function [Excel 2007],xlfn argument [Excel 2007],functions [Excel 2007], calling in international versions
localization_priority: Normal
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f36d2f59b7f5bef9f9ffdca4d13e95c788bf113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790443"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a>Aufrufen von Excel von der DLL oder XLL aus

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Mit Microsoft Excel können DLL-Dateien auf integrierte Excel-Befehle, Arbeitsblattfunktionen und Makrovorlagenfunktionen zugreifen. Diese sind �ber in Visual Basic for Applications (VBA) aufgerufene DLL-Befehle und -Funktionen und �ber direkt in Excel aufgerufene registrierte XLL-Befehle und Funktionen verf�gbar.
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a>Excel4-, Excel4v-, Excel12- und Excel12v-Funktionen

Mit Excel können DLL_Dateien �ber die [Excel4](excel4-excel12.md)-, [Excel4v](excel4v-excel12v.md)-, [Excel12](excel4-excel12.md)- und [Excel12v](excel4v-excel12v.md)-R�ckruffunktionen auf Befehle und Funktionen zugreifen.
  
Die **Excel4**- und **Excel4v**-Funktionen wurden in Excel, Version 4 eingef�hrt. Sie arbeiten mit der **XLOPER**-Datenstruktur. In Excel 2007 wurden zwei neue R�ckruffunktionen eingef�hrt, **Excel12** und **Excel12v**, die mit der **XLOPER12**-Datenstruktur arbeiten. Die **Excel4**- und **Excel4v**-Funktionen werden von der Bibliothek �Xlcall32.lib" in Ihrem DLL- oder XLL-Projekt exportiert. **Excel12** und **Excel12v** sind in der SDK C++-Quelldatei �Xlcall.cpp" enthalten, die in Ihrem Projekt enthalten sein muss, wenn Sie mit **XLOPER12**-Strukturen auf Excel-Funktionen zugreifen m�chten . 
  
Der folgende Code zeigt die Funktionsprototypen für diese vier Funktionen. Die ersten drei Argumente sind bis auf die Ausnahme,dass das zweite Argument auf ein **XLOPER**-Objekt im ersten Paar und auf ein **XLOPER12**-Objekt im zweiten Paar zeigt, identisch. Die Aufrufkonvention ist **_cdecl** in **Excel4** und **Excel12**, um Variablenargumentlisten zuzulassen. Die drei Punkte geben die Zeiger auf **XLOPER**-Werte für **Excel4** und **XLOPER12**-Werte für **Excel12** an. Die Anzahl der Zeiger entspricht dem Wert des  _count_-Parameters. 
  
**Alle Excel-Versionen**
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
**Ab Excel 2007**
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
Damit die DLL **Excel4**, **Excel4v**, **Excel12** oder **Excel12v** aufrufen kann, muss Excel das Steuerelement an die DLL �bergeben. Dies bedeutet, dass diese C-API-Rückrufe nur in den folgenden Szenarien aufgerufen werden können:
  
- Von einem XLL-Befehl aus, der Excel direkt oder über VBA aufgerufen hat.
    
- Von einer XLL-Arbeitsblatt- oder Makrovorlagenfunktion aus, die Excel direkt oder über VBA aufgerufen hat.
    
Sie können die Excel-C-API in den folgenden Szenarien nicht aufrufen:
  
- Von einem Betriebssystemereignis aus (z.�B. von der [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx)-Funktion aus). 
    
- Von einem Hintergrundthread aus, den die DLL erstellt hat.
    
### <a name="return-values"></a>Rückgabewerte

Alle diese vier Funktionen geben eine ganze Zahl zur�ck, mit der dem Aufrufer mitgeteilt wird, ob die Funktion oder der Befehl erfolgreich aufgerufen wurden. Die zur�ckgegebenen Werte können die folgenden sein:
  
|**R�ckgabewert**|**Definiert in Xlcall.h als**|**Beschreibung**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |Die Funktion oder der Befehl wurde erfolgreich ausgef�hrt. Dies bedeutet jedoch nicht, dass die Ausf�hrung ohne Fehler erfolgte. **Excel4** k�nnte z.�B. **xlretSuccess** beim Aufrufen der **FIND**-Funktion zur�ckgeben, obwohl **#VALUE!** als Wert ermittelt wurde, da der Suchtext nicht gefunden werden konnte. Sie sollten den Typ und den Wert des zur�ckgegebenen **XLOPER/XLOPER12**-Objekts pr�fen, bei dem dies m�glich ist.  <br/> |
|1  <br/> |**xlretAbort** <br/> |Ein Makrobefehl wurde durch Klicken des Benutzers auf die Schaltfl�che **Abbrechen** oder durch Dr�cken der ESC-Taste beendet.  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |Die angegebene Funktion oder der angegebene Befehlscode ist ung�ltig. Dieser Fehler kann auftreten, wenn die aufgerufene Funktion nicht �ber die Berechtigung zum Aufrufen der Funktion oder des Befehls verf�gt. Eine Arbeitsblattfunktion z.�B. kann eine Makrovorlagenfunktion oder eine Befehlsfunktion nicht aufrufen.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Die Anzahl der im Aufruf angegebenen Argumente ist falsch.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Mindestens eines der **XLOPER**- oder **XLOPER12**-Argumentwerte ist falsch formatiert oder aufgef�llt.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Excel hat ein festgestellt, dass der Vorgang möglicherweise zum Stapelüberlauf führt und hat die Funktion deshalb nicht aufgerufen.  <br/> |
|32  <br/> |**xlretFailed** <br/> |Beim Ausf�hren des Befehls oder der Funktion ist ein Fehler aufgetreten, dessen Ursache nicht von einem der anderen R�ckgabewerte beschrieben wird. Ein Vorgang, der zu viel Speicher erfordert, w�rde z.�B. diesen Fehler zur�ckgeben. Dies kann bei dem Versuch auftreten, einen sehr gro�en Verweis in ein **xltypeMulti**-Array mithilfe der [xlCoerce](http://msdn.microsoft.com/library/guid_9d47c16c-a7e7-4998-b594-9cf001827b7b%28Office.15%29.aspx)-Funktion zu konvertieren.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Bei dem Vorgang wurde versucht, den Wert einer nicht berechneten Zelle abzurufen. Um Integrit�t der Neuberechnung in Excel zu erhalten, ist dies für Excel-Arbeitsblattfunktionen nicht zul�ssig. Als Makrovorlagenfunktionen registrierte XLL-Befehle und Funktionen d�rfen jedoch auf nicht berechnete Zellwerte zugreifen.  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |(Ab Excel 2007) Eine als threadsicher registrierte XLL-Arbeitsblattfunktion hat versucht, eine C-API-Funktion aufzurufen, die nicht threadsicher ist. Eine threadsichere Funktion darf z.�B. die XLM-Funktion **xlfGetCell** nicht aufrufen.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |(AbExcel 2010) Das asynchrone Behandeln von Funktionen ist ung�ltig.  <br/> |
|512  <br/> |**xlretNotClusterSafe** <br/> |(Ab Excel 2010) Der Aufruf wird auf Clustern nicht unterst�tzt.  <br/> |
   
Gibt die Funktion einen der Fehlerwerte in der Tabelle zur�ck(d.�h. sie gibt nicht **xlretSuccess** zur�ck), wird der zur�ckgegebene **XLOPER**- oder **XLOPER12**-Wert auch auf **#VALUE!** festgelegt. Unter bestimmten Umst�nden reicht es m�glicherweise aus, dies zu pr�fen. Beachten Sie jedoch, dass ein Aufruf sowohl **xlretSuccess** als auch **#VALUE!** zur�ckgeben kann.
  
Wenn ein Aufruf der C-API zu **xlretUncalced** oder **xlretAbort** f�hrt, sollte der DLL- oder XLL-Code ein Steuerelement an Excel zur�ckgeben, bevor weitere C-API-Aufrufe durchgef�hrt werden (andere als Aufrufe der [xlfree](http://msdn.microsoft.com/library/guid_8ce2eef2-0138-495d-b6cb-bbb727a3cda4%28Office.15%29.aspx)-Funktion zum Freigeben der an Excel zugewiesenen Arbeitsspeicherressourcen in **XLOPER**- und **XLOPER12**-Werten). 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a>Befehls- oder Funktionsenumerationsargument: xlfn

Das  _xlfn_-Argument ist das erste Argument der R�ckruffunktionen und ist eine ganze 32-Bit-Zahl mit Vorzeichen. Der Wert des Arguments sollte eine der in der SDK-Headerdatei �Xlcall.h" definierten Funktions- oder Befehlsenumerationen sein, wie im folgenden Beispiel dargestellt. 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

Alle Arbeitsblatt- und Makrovorlagenfunktionen stellen Hexadezimalwerte zwischen 0 (**xlfCount**) und 0x0fff dar, wobei die höchste zugewiesen Zahl in Excel 2013 die Dezimalzahl 547 ist, Hexadezimalwert 0x0223 (**xlfFloor_precise**).
  
Alle Befehlsfunktionen stellen Hexadezimalwerte zwischen 0x8000 (**xlcBeep**) und 0x8fff dar, wobei die höchste zugewiesen Zahl in Excel 2013 die Hexadezimalzahl 0x8328 ist (**xlcHideallInkannots**). Sie werden in der Headerdatei als  `(n | xlCommand)` definiert, wobei  `n` als eine Dezimalzahl gr��er als oder gleich 0 und **xlCommand** als Hexadezimalzahl 0x8000 definiert ist. 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a>Aufrufen von Excel-Befehlen, die Dialogfelder verwenden

Einige der Befehlcodes entsprechen Aktionen in Excel, die Dialogfelder verwenden. **xlcFileDelete** verwendet z. B. ein einzelnes Argument: einen Dateinamen oder eine Dateimaske. Dieser Befehl kann mit dem Dialogfeld aufgerufen werden, sodass der Benutzer den Löschvorgang abbrechen oder ändern kann. Er kann auch ohne das Dialogfeld aufgerufen werden. In diesem Fall werden die Dateien ohne jegliche weitere Interaktion gelöscht, wobei vorausgesetzt wird, dass sie vorhanden sind und der Aufrufer über die entsprechende Berechtigung verfügt. Um solche Befehle im Dialogfeldformat aufrufen zu können, muss die Befehlsenumeration durch den bitweisen OR-Operator mit 0x1000 (**xlPrompt**) verknüpft sein.
  
Im folgenden Codebeispiel werden die Dateien im aktuellen Verzeichnis gel�scht, die der Maske �my_data\*.bak" entsprechen, wobei ein Dialogfeld nur angezeigt wird, wenn das Argument wahr ist.
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a>Aufrufen von Funktionen und Befehlen in internationalen Versionen

Sie können Excel zum Anzeigen von Funktionen und der XLM-Befehlsnamen in einer Vielzahl von Sprachen konfigurieren. Einige C-API-Befehle und -Funktionen verwenden Zeichenfolgen, die als Funktions- oder Befehlsnamen interpretiert werden. **xlcFormula** verwendet z. B. ein Zeichenfolgenargument, das in einer angegebenen Zelle eingefügt werden soll. Damit Ihr Add-In mit allen Spracheinstellungen funktioniert, können Sie die Zeichenfolgennamen in Englisch angeben und das Bit 0x2000 (**xlIntl**) in der Funktions- oder Befehlsenumeration festlegen.
  
Im folgenden Code wird das �quivalent von  `=SUM(X1:X100)` in Zelle A2 des aktiven Arbeitsblatts platziert. Beachten Sie, dass die Framework-Funktion **TempActiveRef** zum Erstellen des tempor�ren Verweises **XLOPER** verwendet wird. Die Formel wird in Zelle A2 in der vom Gebietsschema vorgegebenen Sprache angezeigt (z.�B.  `=SOMME(X1:X100)`, wenn Franz�sisch festgelegt ist). 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> Da das Ergebnis des Aufrufs von **Excel12** nicht erforderlich ist, kann 0 (NULL) als zweites Argument anstelle der Adresse des **xResult**-Objekts �bergeben werden. Dies wird im n�chsten Abschnitt genauer erl�utert. 
  
### <a name="dll-only-functions-and-commands"></a>Nur DLL-Funktionen und -Befehle

Excel unterst�tzt eine kleine Anzahl von Funktionen, auf die nur von einer DLL oder XLL aus zugegriffen werden kann. Sie werden in der Headerdatei als  `(n | xlSpecial)` definiert, wobei  `n` als eine Dezimalzahl gr��er als oder gleich 0 und  `xlSpecial` als Hexadezimalzahl 0x4000 definiert ist. Diese Funktionen sind in der folgenden Tabelle und unter [Referenz zur API-Funktion](excel-xll-sdk-api-function-reference.md) aufgef�hrt.
  
||||
|:-----|:-----|:-----|
|[xlFree](xlfree.md) <br/> |0 | xlSpecial  <br/> |Gibt die für Excel zugewiesenen Arbeitsspeicherressourcen frei.  <br/> |
|[xlStack](xlstack.md) <br/> |1 | xlSpecial  <br/> |Gibt den freien Speicherplatz im Excel-Stapel zurück.  <br/> |
|[xlCoerce](xlcoerce.md) <br/> |2 | xlSpecial  <br/> |Konvertiert zwischen **XLOPER**- und **XLOPER12**-Typen.  <br/> |
|[xlSet](xlset.md) <br/> |3 | xlSpecial  <br/> |Bietet eine schnelle Methode zum Festlegen von Zellwerten.  <br/> |
|[xlSheetId](xlsheetid.md) <br/> |4 | xlSpecial  <br/> |Ruft einen Arbeitsblattnamen aus seiner internen ID ab.  <br/> |
|[xlSheetNm](xlsheetnm.md) <br/> |5 | xlSpecial  <br/> |Ruft eine interne Arbeitsblatt-ID aus dem zugehörigen Namen ab.  <br/> |
|[xlAbort](xlabort.md) <br/> |6 | xlSpecial  <br/> |�berpr�ft, ob der Benutzer auf die Schaltfl�che **Abbrechen** geklickt oder die ESC-Taste gedr�ckt hat.  <br/> |
|[xlGetInst](xlgetinst.md) <br/> |7 | xlSpecial  <br/> |Ruft das Excel-Instanzhandle ab.  <br/> |
|[xlGetHwnd](xlgethwnd.md) <br/> |8 | xlSpecial  <br/> |Ruft die Zugriffsnummer des Excel-Hauptfensters ab.  <br/> |
|[xlGetName](xlgetname.md) <br/> |9 | xlSpecial  <br/> |Ruft den Pfad und den Dateinamen der DLL-Datei ab.  <br/> |
|[xlEnableXLMsgs](xlenablexlmsgs.md) <br/> |10 | xlSpecial  <br/> |Diese Funktion ist veraltet und wird nicht mehr aufgerufen.  <br/> |
|[xlDisableXLMsgs](xldisablexlmsgs.md) <br/> |11 | xlSpecial  <br/> |Diese Funktion ist veraltet und wird nicht mehr aufgerufen.  <br/> |
|[xlDefineBinaryName](xldefinebinaryname.md) <br/> |12 | xlSpecial  <br/> |Definiert den Namen eines dauerhaften binären Speichers.  <br/> |
|[xlGetBinaryName](xlgetbinaryname.md) <br/> |13 | xlSpecial  <br/> |Ruft die Namensdaten eines dauerhaften binären Speichers ab.  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a>Rückgabewert XLOPER/XLOPER12: operRes

Das _operRes_-Argument ist das zweite Argument für die Rückrufe und ist ein Zeiger auf ein **XLOPER**- (**Excel4** und **Excel4v**) oder **XLOPER12**-Objekt (**Excel12** und **Excel12v**). Nach einem erfolgreichen Aufruf enthält es den Rückgabewert der Funktion oder des Befehls. **operRes** kann auf 0 (null) (NULL-Zeiger) festgelegt werden, wenn kein R�ckgabewert erforderlich ist. Die vorherigen Inhalte von **operRes** werden �berschrieben, sodass der vollst�ndige Arbeitsspeicher, auf den gezeigt wurde, vor dem Aufruf freigegeben werden muss, um Arbeitsspeicherverluste zu vermeiden. 
  
Wenn die Funktion oder der Befehl nicht aufgerufen werden kann (z.�B. wenn die Argumente falsch sind), wird für **operRes** der Fehler **#VALUE!** festgelegt. Ein Befehl gibt immer **Boolean** **TRUE** zur�ck, wenn dieser erfolgreich war, oder **FALSE**, wenn dabei ein Fehler aufgetreten ist oder dieser vom Benutzer abgebrochen wurde. 
  
## <a name="number-of-subsequent-arguments-count"></a>Anzahl nachfolgender Argumente: count

Das  _count_-Argument ist das dritte Argument für die Rückrufe und ist eine ganze 32-Bit-Zahl mit Vorzeichen. Es sollte auf die Anzahl der nachfolgenden Argumente, beginnend bei 1, festgelegt werden. Wenn eine Funktion oder ein Befehl keine Argumente verwendet, sollte sie bzw. es auf 0 (null) festgelegt werden. In Microsoft Office Excel 2003 betr�gt die maximale Anzahl an Argumenten, die jede Funktion verwenden kann, 30, wobei die meisten weniger verwenden. Ab Excel 2007, wurde die maximale Anzahl von Argumenten, die jede Funktion verwenden kann, auf 255 erh�ht. 
  
In **Excel4** und **Excel12** ist  _count_ die Anzahl der Zeiger auf **XLOPER**- oder **XLOPER12**-Werte, die �bergeben werden. Achten Sie darauf, nicht weniger Argumente zu �bergeben, als der Wert, auf den  _count_ festgelegt ist. Dies w�rde dazu f�hren, dass Excel im Stapel liest und versucht, ung�ltige **XLOPER**- oder **XLOPER12**-Werte zu verarbeiten, was zum Absturz der Anwendung f�hren kann. 
  
In **Excel4v** und **Excel12v** ist  _count_ die Gr��e des Arrays der Zeiger auf **XLOPER**- oder **XLOPER12**-Werte, die als n�chstes und letztes Argument �bergeben werden. Auch hier sollten Sie darauf achten, dass das �bergebene Array nicht kleiner ist als die  _count_-Elemente, da dies zu Grenz�berschreitungen des Arrays f�hren kann. 
  
## <a name="passing-arguments-to-c-api-functions"></a>Übergeben von Argumenten an C-API-Funktionen

**Excel4** und **Excel12** verwenden nach  _count_ jeweils Variablenl�ngen-Argumentlisten, die als Zeiger auf **XLOPER**- und **XLOPER12**-Werte interpretiert werden. **Excel4v** und **Excel12v** verwenden nach  _count_ ein einzelnes Argument, das bei **Excel4v** einen Zeiger auf ein Array von Zeigern auf **XLOPER**-Werte und bei **Excel12v** auf **XLOPER12**-Werte darstellt.
  
Die Arrayformen **Excel4v** und **Excel12v** erm�glichen es Ihnen, einen Aufruf an die C-API ordnungsgem�� zu codieren, wenn die Anzahl der Argumente variabel ist. Das folgende Beispiel zeigt eine Funktion, die ein Array mit Zahlen von variabler Gr��e verwendet und �ber die C-API Excel-Arbeitsblattfunktionen nutzt, um Summe, Mittelwert, Minimum und Maximum zu berechnen. 
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

Beim Ersetzen von Verweisen auf **XLOPER12**-Werte durch **XLOPER**, und von **Excel12v** durch **Excel4v**, w�re im vorangehenden Code eine Funktion das Ergebnis, die mit allen Versionen von Excel funktioniert. Dieser Vorgang der Excel-Funktionen **SUM**, **AVERAGE**, **MIN** und **MAX** ist so einfach, dass es effizienter w�re, diese in C zu codieren, statt Vorbereitung der Argumente und des Aufrufs in Excel. Viele der Excel-Funktionen sind jedoch komplexer, sodass dieser Ansatz in bestimmten Szenarien hilfreich ist. 
  
Im Thema [xlfRegister](http://msdn.microsoft.com/library/guid_c730124c-1886-4a0f-8f06-79763025537d%28Office.15%29.aspx) ist ein weiteres Beispiel für die Verwendung mit **Excel4v** und **Excel12v** enthalten. Beim Registrieren einer XLL-Arbeitsblattfunktion können Sie eine beschreibende Zeichenfolge für jedes Argument angeben, das im Dialogfeld **Funktion einf�gen** verwendet wird. Die Gesamtanzahl der für **xlfRegister** angegebenen Argumente h�ngt daher von der Anzahl der Argumente ab, die Ihre XLL-Funktion verwendet, und variiert je nach Funktion. 
  
Beim Aufrufen einer C-API-Funktion oder eines -Befehls mit der gleichen Anzahl von Argumenten, m�chten Sie den zus�tzlichen Schritt vermeiden und kein Array von Zeigern für diese Argumente erstellen. In diesen F�llen ist es einfacher, **Excel4** und **Excel12** zu verwenden. Beim Registrieren von XLL-Funktionen und -Befehlen z.�B. m�ssen Sie den vollst�ndigen Pfad und Dateinamen der DLL oder XLL angeben. Sie können den Dateinamen in einem Aufruf von **xlfGetName** abrufen und diesen anschlie�end mit einem Aufruf von **xlFree** freigeben, wie im folgenden Beispiel für **Excel4** und **Excel12** dargestellt.
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

In der Praxis kann die **Excel12v_example**-Funktion effizienter codiert werden, indem ein einziges **xltypeMulti** **XLOPER12**-Argument erstellt und die C-API mithilfe von **Excel12** aufgerufen wird, wie im folgenden Beispiel gezeigt.
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> In diesem Fall wird der R�ckgabewert von **Excel12** ignoriert. Stattdessen �berpr�ft der Code, ob das zur�ckgegebene **XLOPER12**-Objekt **xltypeNum** aufweist, um zu ermitteln, ob der Aufruf erfolgreich war. 
  
## <a name="xlcallver"></a>XLCallVer

Neben den Rückrufen **Excel4**, **Excel4v**, **Excel12** und **Excel12v** exportiert Excel eine **XLCallVer**-Funktion, die die Version der aktuell ausgeführten C-API zurückgibt.
  
Der Funktionsprototyp lautet wie folgt:
  
 `int pascal XLCallVer(void);`
  
Sie können diese threadsichere Funktion von einem beliebigen XLL-Befehl oder einer -Funktion aus aufrufen.
  
In Excel 97 bis Excel 2003 gibt **XLCallVer**den Wert 1280 = 0x0500 hex = 5 x 256 zur�ck, was auf Excel Version�5 hinweist. Ab Excel 2007 wird 3072 = 0x0c00 hex = 12 x 256 zur�ckgegeben, was auf Version 12 hinweist.
  
Obwohl Sie auf diese Weise feststellen können, ob die neue C-API zur Laufzeit verf�gbar ist, m�chten Sie m�glicherweise unter Verwendung von `Excel4(xlfGetWorkspace, &version, 1, &arg)` die ausgef�hrte Excel-Version ermitteln, wobei  `arg` ist ein numerischer Wert **XLOPER**, der auf 2 festgelegt ist. Die Funktion gibt eine Zeichenfolge **XLOPER** zur�ck, d.�h. die Version, die dann in eine ganze Zahl umgewandelt werden kann. Der Grund für die Verwendung der Excel-Version statt der C-API-Version stellen Unterschiede zwischen Excel 2000, Excel 2002 und Excel 2003 dar, die das Add-In ggf. auch erkennen muss. Es wurden beispielsweise �nderungen an der Genauigkeit einiger Statistikfunktionen vorgenommen.
  
## <a name="see-also"></a>Siehe auch



[Erstellen von XLLs](creating-xlls.md)
  
[Zugreifen auf XLL-Code in Excel](accessing-xll-code-in-excel.md)
  
[Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)
  
[C-API-Rückruffunktionen Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)
  
[Entwickeln von XLLs für Excel](developing-excel-xlls.md)

