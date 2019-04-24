---
title: Zugreifen auf DLLs in Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Zugreifen auf DLLs [excel 2007],DLLs [Excel 2007], Zugreifen in Excel
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: fac4ad30048aa1bf3879009bc97ea46a112a9ce5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304011"
---
# <a name="access-dlls-in-excel"></a>Zugreifen auf DLLs in Excel

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Sie können auf eine DLL-Funktion oder einen Befehl in Microsoft Excel auf verschiedene Arten zugreifen:
  
- Über ein Microsoft VBA-Codemodul (Visual Basic for Applications), in dem die Funktion oder der Befehl mithilfe einer **Declare**-Anweisung verfügbar gemacht wurde 
    
- Über eine XLM-Makrovorlage mithilfe der Funktion **CALL** oder **REGISTER** 
    
- Direkt aus dem Arbeitsblatt oder von einem angepassten Element in der Benutzeroberfläche
    
XLM-Funktionen werden in dieser Dokumentation nicht behandelt. Verwenden Sie nach Möglichkeit eine der beiden anderen Methoden.
  
Für den direkten Zugriff aus dem Arbeitsblatt oder von einem angepassten Element der Benutzeroberfläche muss die Funktion oder der Befehl zunächst bei Excel registriert werden. Informationen über das Registrieren von Befehlen und Funktionen finden Sie unter [Zugriff auf XLL-Code in Excel](accessing-xll-code-in-excel.md).
  
## <a name="calling-dll-functions-and-commands-from-vba"></a>Aufrufen von DLL-Funktionen und -Befehlen in VBA

In VBA können Sie mit der **Declare**-Anweisung auf DLL-Funktionen und -Befehle zugreifen. Diese Anweisung verfügt über eine Syntax für Befehle und eine für Funktionen. 
  
- **Syntax 1 - Befehle**
    
  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- **Syntax 2 - Funktionen**
    
  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

Die optionalen Schlüsselwörter **Public** und **Private** geben den Geltungsbereich der importierten Funktion an: das gesamte Visual Basic-Projekt bzw. nur das Visual Basic-Modul. Der Name ist der Name, den Sie im VBA-Code verwenden möchten. Wenn sich dieser vom Namen in der DLL unterscheidet, müssen Sie den Aliasspezifizierer "aliasname" verwenden und sollten den Namen der Funktion so angeben, wie er von der DLL exportiert wird. Wenn Sie durch Verweis auf eine DLL-Ordnungszahl auf eine DLL-Funktion zugreifen möchten, müssen Sie einen Aliasnamen angeben, der aus der Ordnungszahl mit dem Präfix **#** besteht.
  
Befehle müssen **void** zurückgeben. Funktionen müssen Typen zurückgeben, die VBA **ByVal** erkennen kann. Dies bedeutet, dass einige Typen einfacher zurückgegeben werden, wenn Argumente direkt geändert werden: Zeichenfolgen, Arrays, benutzerdefinierte Typen und Objekte.
  
> [!NOTE]
> VBA kann nicht überprüfen, ob die im Visual Basic-Modul angegebene Argumentliste und Rückgabe identisch mit den in der DLL-Datei codierten Werten sind. Sie sollten dies selbst sehr sorgfältig prüfen, da ein Fehler zum Absturz von Excel führen kann. 
  
Wenn die Argumente der Funktion oder des Befehls nicht durch Verweis oder Zeiger übergeben werden, muss ihnen das **ByVal**-Schlüsselwort in der **arglist**-Deklaration vorangestellt werden. Wenn eine C/C++-Funktion Zeigerargumente oder eine C++-Funktion Verweisargumente verwendet, müssen diese Funktionen **ByRef** übergeben werden. Das **ByRef**-Schlüsselwort kann in Argumentlisten ausgelassen werden, da es der VBA-Standardwert ist. 
  
### <a name="argument-types-in-cc-and-vba"></a>Argumenttypen in C/C++ und VBA

Beachten Sie beim Vergleichen der Deklarationen von Argumenttypen in C/C++ und VBA die folgenden Punkte.
  
- Ein VBA- **String** wird bei einer ByVal-Übergabe als Zeiger auf eine Byte-String-BSTR-Struktur übergeben, bei einer **ByRef**-Übergabe als Zeiger auf einen Zeiger.
    
- Eine VBA- **Variant**, die eine Zeichenfolge enthält, wird bei einer **ByVal**-Übergabe als Zeiger auf eine Unicode-Breitzeichen-String-BSTR-Struktur übergeben, bei einer **ByRef**-Übergabe als Zeiger auf einen Zeiger.
    
- Der VBA-Datentyp **Integer** ist eine 16-Bit-Typentsprechung des Datentyps "signed short" in C/C++. 
    
- Der VBA-Datentyp **Long** ist eine 32-Bit-Typentsprechung für den Datentyp "signed int" in C/C++. 
    
- Sowohl VBA als auch C/C++ unterstützen die Definition benutzerdefinierter Datentypen mit der Anweisung **Type** bzw. **struct**. 
    
- Der Datentyp **Variant** wird in VBA und C/C++ unterstützt; für C/C++ ist er in den Windows-OLE/COM-Headerdateien als VARIANT definiert. 
    
- VBA-Arrays sind OLE- **SafeArrays**, die für C/C++ in den Windows-OLE/COM-Headerdateien als **SAFEARRAY** sind.
    
- Der VBA-Datentyp **Currency** wird bei einer **ByVal**-Übergabe als Struktur des Typs **CY** übergeben (definiert in der Windows-Headerdatei "wtypes.h") und bei einer **ByRef**-Übergabe als Zeiger darauf.
    
In VBA werden Datenelemente in benutzerdefinierten Datentypen für 4-Byte-Grenzen gepackt, in Visual Studio werden sie hingegen standardmäßig für 8-Byte-Grenzen gepackt. Daher müssen Sie die C/C++-Strukturdefinition in einen `#pragma pack(4) … #pragma pack()`-Block einschließen, um eine Fehlausrichtung der Elemente zu vermeiden. 
  
Nachfolgend finden Sie ein Beispiel für entsprechende Benutzertypdefinitionen.
  
```vb
Type VB_User_Type
    i As Integer
    d As Double
    s As String
End Type

```

```cpp
#pragma pack(4)
struct C_user_type
{
    short iVal;
    double dVal;
    BSTR bstr; // VBA String type is a byte string
}
#pragma pack() // restore default

```

VBA unterstützt in einigen Fällen einen größeren Wertebereich als Excel. Der VBA-Datentyp "double" ist IEEE-konform und unterstützt subnormale Zahlen, die derzeit im Arbeitsblatt auf null abgerundet werden. Der VBA-Datentyp **Date** kann Datumsangaben ab dem 1. Januar 0100 mithilfe negativer serialisierter Datumsangaben darstellen. Excel unterstützt nur serialisierte Datumsangaben größer oder gleich null. Der VBA-Datentyp **Currency** ist eine skalierte 64-Bit-Ganzzahl und erreicht Genauigkeiten, die in 8-Byte-Double-Werten nicht unterstützt werden, daher hat er keine Entsprechung im Arbeitsblatt. 
  
Excel übergibt nur Variant-Werte der folgenden Typen an eine benutzerdefinierte VBA-Funktion.
  
|**VBA-Datentyp**|**Bit-Flags für C/C++-Variant-Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|Gleitkommawert mit doppelter Genauigkeit  <br/> |**VT_R8** <br/> ||
|Boolean  <br/> |**VT_BOOL** <br/> ||
|Datum  <br/> |**VT_DATE** <br/> ||
|Zeichenfolge  <br/> |**VT_BSTR** <br/> |OLE-Bstr-Byte-String  <br/> |
|Range  <br/> |**VT_DISPATCH** <br/> |Bereichs- und Zellbezüge  <br/> |
|Variant-Wert mit einem Array  <br/> |**VT_ARRAY** | **VT_VARIANT** <br/> |Literale Arrays  <br/> |
|Ccy  <br/> |**VT_CY** <br/> |64-Bit-Ganzzahl, skaliert für eine Genauigkeit von 4 Dezimalstellen  <br/> |
|Variant-Wert mit einem Fehler  <br/> |**VT_ERROR** <br/> ||
||**VT_EMPTY** <br/> |Leere Zellen oder ausgelassenen Argumente  <br/> |
   
Sie können den Typ eines übergebenen Variant-Werts in VBA mithilfe von **VarType** überprüfen, allerdings gibt die Funktion den Typ der Bereichswerte zurück, wenn sie mit Verweisen aufgerufen wird. Um zu ermitteln, ob ein **Variant**-Wert ein **Range**-Verweisobjekt ist, können Sie die **IsObject**-Funktion verwenden. 
  
Sie können **Variants** mit Variantenarrays in VBA aus einem **Range** erstellen, indem Sie die zugehörige **Value**-Eigenschaft einem **Variant**-Wert zuweisen. Alle Zellen im Quellbereich, die mit dem Standardwährungsformat aus den zu diesem Zeitpunkt gültigen Landes-/Regionaleinstellungen formatiert sind, werden in Arrayelemente des Typ **Currency** konvertiert. Alle als Datumsangaben formatierten Zellen werden in Arrayelemente des Typs **Date** konvertiert. Zellen mit Zeichenfolgen werden in Breitzeichen- **BSTR**-Variant-Werte konvertiert. Zellen mit Fehlern werden in **Variants** des Typs **VT_ERROR** konvertiert. Zellen mit **Boolean** **True** oder **False** werden in **Variants** des Typs **VT_BOOL** konvertiert. 
  
> [!NOTE]
> Der **Variant**-Wert speichert **True** als -1 und **False** als 0. Zahlen, die nicht als Datumsangaben oder Währungsbeträge formatiert sind, werden in Variant-Werte des Typs **VT_R8** konvertiert. 
  
### <a name="variant-and-string-arguments"></a>Variant- und String-Argumente

Excel arbeitet intern mit Breitzeichen-Unicode-Strings. Wenn die Deklaration einer benutzerdefinierten VBA-Funktion die Verwendung eines **String**-Arguments angibt, konvertiert Excel die angegebene Zeichenfolge mit einer für das jeweilige Gebietsschema spezifischen Methode in einen Byte-String-Wert. Wenn die Funktion als Unicode-String übergeben werden soll, muss die benutzerdefinierte VBA-Funktion ein **Variant**- anstelle eines **String**-Arguments verwenden. Die DLL-Funktion kann dann diesen **Variant**-BSTR-Breitzeichen-String von VBA akzeptieren. 
  
Um Unicode-Strings als einer DLL an VBA zurückzugeben, müssen Sie ein **Variant**-String-Argument direkt bearbeiten. Damit dies möglich ist, müssen Sie die DLL-Funktion so deklarieren, dass ein Zeiger auf die **Variant** und im C/C++-Code verwendet wird, und müssen das Argument im VBA-Code als "  `ByRef varg As Variant`" deklarieren. Der alte Zeichenfolgenspeicher muss gelöscht werden, und der neue Zeichenfolgenwert muss unter Verwendung de OLE-Bstr-String-Funktionen nur in der DLL erstellt werden.
  
Um einen Byte-String aus einer DLL an VBA zurückzugeben, müssen Sie ein Byte-String-BSTR-Argument direkt bearbeiten. Damit dies möglich ist, müssen Sie die DLL-Funktion so deklarieren, dass sie einen Zeiger auf einen Zeiger zu BSTR und im C/C++-Code verwendet, und müssen das Argument im VBA-Code als " **ByRef varg As String**" deklarieren.
  
Sie sollten nur Zeichenfolgen, die mit diesen Methoden von VBA übergeben werden, mit den OLE-BSTR-String-Funktionen bearbeiten, um Speicherprobleme zu vermeiden. Sie müssen beispielsweise **SysFreeString** aufrufen, um den Speicher freizugeben, bevor Sie die übergebene Zeichenfolge überschreiben, und **SysAllocStringByteLen** oder **SysAllocStringLen**, um Speicher für eine neue Zeichenfolge zuzuordnen. 
  
Sie können Excel-Arbeitsblattfehler als **Variants** in VBA erstellen, indem Sie die **CVerr**-Funktion mit den in der folgenden Tabelle aufgeführten Argumenten verwenden. Arbeitsblattfehler können auch mit **Variants** vom Typ **VT_ERROR** und mit den folgenden Werten im **ulVal**-Feld von einer DLL an VBA zurückgegeben werden. 
  
|**Fehler**|**UlVal-Wert der Variante**|**CVerr-Argument**|
|:-----|:-----|:-----|
|#NULL!  <br/> |2148141008  <br/> |2000  <br/> |
|#DIV/0!  <br/> |2148141015  <br/> |2007  <br/> |
|#VALUE!  <br/> |2148141023  <br/> |2015  <br/> |
|#REF!  <br/> |2148141031  <br/> |2023  <br/> |
|#NAME?  <br/> |2148141037  <br/> |2029  <br/> |
|#NUM!  <br/> |2148141044  <br/> |2036  <br/> |
|#N/A  <br/> |2148141050  <br/> |2042  <br/> |
   
Beachten Sie, dass der angegebene Variantwert **ulVal** dem Wert des **CVerr**-Arguments plus dem Hexadezimalwert x800A0000 entspricht. 
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a>Direktes Aufrufen von DLL-Funktionen aus dem Arbeitsblatt

Sie können aus dem Arbeitsblatt nicht auf Win32-DLL-Funktionen zugreifen, ohne beispielsweise VBA oder XLM als Schnittstelle zu verwenden oder ohne Excel vorab Angaben zur Funktion, zu deren Argumenten und zum Rückgabetyp zu machen. Der erforderliche Prozess wird als Registrierung bezeichnet.
  
Der Zugriff auf die Funktionen einer DLL kann in einem Arbeitsblatt mit den folgenden Methoden erfolgen:
  
- Deklarieren der Funktion in VBA wie zuvor beschrieben und Zugreifen auf die Funktion über eine benutzerdefinierte VBA-Funktion
    
- Aufrufen der DLL-Funktion durch Ausführen von CALL für eine XLM-Makrovorlage und Zugreifen auf die Funktion über eine benutzerdefinierte XLM-Funktion
    
- Verwenden eines XLM- oder VBA-Befehls zum Aufrufen der XLM-Funktion **REGISTER**, die die Informationen bereitstellt, die Excel zum Erkennen der Funktion benötigt, wenn diese in eine Arbeitsblattzelle eingegeben wird 
    
- Umwandeln der DLL in eine XLL und Registrieren der Funktion mithilfe der C-API-Funktion **xlfRegister** beim Aktivieren der XLL 
    
Die vierte Methode ist eigenständig: Der Code, der die Funktionen registriert, und der Funktionscode sind beide im gleichen Codeprojekt enthalten. Am Add-In vorgenommene Änderungen erfordern keine Änderungen an einem XLM-Blatt oder einem VBA-Codemodul. Um dies auf gut verwaltete Weise durchzuführen, ohne den Funktionsumfang der C-API zu verlassen, müssen Sie die DLL in eine XLL umwandeln und das resultierende Add-In mithilfe des Add-In-Managers laden. Dies ermöglicht es Excel, eine Funktion aufzurufen, die die DLL verfügbar macht, wenn das Add-In geladen oder aktiviert wird; von dort aus können Sie alle Funktionen der XLL registrieren und andere DLL-Initialisierungen ausführen.
  
## <a name="calling-dll-commands-directly-from-excel"></a>Direktes Aufrufen von DLL-Befehlen aus Excel

Auf Win32-DLL-Befehle kann nicht direkt aus Excel-Dialogfeldern und -Menüs zugegriffen werden, ohne dass eine Schnittstelle wie z. B. VBA vorhanden ist oder die Befehle vorab registriert werden.
  
Auf die Befehle einer DLL kann mit folgenden Methoden zugegriffen werden:
  
- Deklarieren des Befehls in VBA wie zuvor beschrieben und Zugreifen auf die Funktion über ein VBA-Makro
    
- Aufrufen des DLL-Befehls durch Ausführen von **CALL** für eine XLM-Makrovorlage und Zugreifen auf die Funktion über ein XLM-Makro 
    
- Verwenden eines XLM- oder VBA-Befehls zum Aufrufen der XLM-Funktion **REGISTER**, die die Informationen bereitstellt, die Excel zum Erkennen des Befehls benötigt, wenn dieser in ein Dialogfeld eingegeben wird, das den Namen eines Makrobefehls erwartet 
    
- Umwandeln der DLL in eine XLL und Registrieren des Befehls mit der C-API-Funktion **xlfRegister** 
    
Wie bereits weiter oben im Kontext von DLL-Funktionen erläutert, ist die vierte Methode die eigenständigste, und Registrierungscode und Befehlscode bleiben hier nahe beieinander. Hierzu müssen Sie die DLL in eine XLL umwandeln und das resultierende Add-In mithilfe des Add-In-Managers laden. Wenn Sie Befehle auf diese Weise registrieren, haben Sie außerdem die Möglichkeit, den Befehl an ein Element der Benutzeroberfläche anzufügen, z. B. ein benutzerdefiniertes Menü, oder ein Ereignistrap einzurichten, das den Befehl bei einem bestimmten Tastaturanschlag oder einem anderen Ereignis aufruft.
  
Für alle bei Excel registrierten XLL-Befehle wird von Excel die folgende Form vorausgesetzt.
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> Der Rückgabewert wird von Excel ignoriert, es sei denn, der Aufruf erfolgt aus einer XLM-Makrovorlage; in diesem Fall wird der Rückgabewert in **TRUE** oder **FALSE** konvertiert. Sie müssen daher 1 zurückgeben, wenn der Befehl erfolgreich ausgeführt wurde, und 0 bei einem Fehler oder Benutzerabbruch. 
  
## <a name="dll-memory-and-multiple-dll-instances"></a>DLL-Speicher und mehrere DLL-Instanzen

Wenn eine Anwendung eine DLL lädt, wird der ausführbare Code der DLL in den globalen Heap geladen, damit er ausgeführt werden kann, und für die Datenstrukturen wird Speicherplatz im globalen Heap zugewiesen. Windows verwendet Speicherzuordnung, damit diese Speicherbereiche so angezeigt werden, als wären sie im Prozess der Anwendung enthalten, sodass die Anwendung darauf zugreifen kann.
  
Wenn anschließend eine zweite Anwendung die DLL lädt, erstellt Windows keine weitere Kopie des ausführbaren DLL-Codes, da der Speicher schreibgeschützt ist. Windows ordnet den Speicher des ausführbaren DLL-Codes den Prozessen beider Anwendungen zu. Es wird jedoch auch eine zweiter Speicherbereich für eine private Kopie der DLL-Datenstrukturen zugewiesen, und diese Kopie wird nur dem zweiten Prozess zugeordnet. Dadurch wird sichergestellt, dass keine Anwendung einen Konflikt mit den DLL-Daten der anderen Anwendung verursachen kann.
  
Dies bedeutet, dass sich DLL-Entwickler keine Gedanken darüber machen müssen, dass mehrere Anwendungen oder mehrere Instanzen der gleichen Anwendung auf statische und globale Variablen und Datenstrukturen zugreifen. Jede Instanz jeder Anwendung ruft eine eigene Kopie der DLL-Daten ab.
  
DLL-Entwickler müssen sich jedoch Gedanken darüber machen, dass dieselbe Instanz einer Anwendung die DLL mehrmals aus unterschiedlichen Threads aufruft, da dies zu einem Konflikt für die Daten dieser Instanz führen kann. Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von DLLs](developing-dlls.md) 
- [Aufrufen von Excel von der DLL oder XLL aus](calling-into-excel-from-the-dll-or-xll.md)

