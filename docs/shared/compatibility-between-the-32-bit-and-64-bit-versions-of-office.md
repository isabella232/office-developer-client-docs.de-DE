---
title: Kompatibilität zwischen der 32-Bit- und 64-Bit-Version von Office
ms.date: 04/27/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Erfahren Sie, wie die 32-Bit-Version von Office mit der 64-Bit-Version von Office kompatibel ist.
ms.openlocfilehash: 924f7a1aa891addc5841e6cdefc5226dcb056096
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796313"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a>Kompatibilität zwischen der 32-Bit- und 64-Bit-Version von Office

Erfahren Sie, wie die 32-Bit-Version von Office mit der 64-Bit-Version von Office kompatibel ist.
  
Office-Anwendungen sind in 32-Bit- und 64-Bit-Versionen verfügbar. 
  
Die 64-Bit-Versionen von Office können Sie weitere Daten für höhere Kapazität, beispielsweise beim Arbeiten mit einer großen Anzahl in Microsoft Excel 2010 bewegen. Wenn Sie 32-Bit-Code zu schreiben, können Sie die 64-Bit-Version von Office ohne Änderungen. Wenn Sie die 64-Bit-Code schreiben, Sie sollten jedoch sicherstellen, dass der Code enthält bestimmte Schlüsselwörter und bedingte Kompilierung-Konstanten, um sicherzustellen, dass der Code abwärtskompatibel mit früheren Versionen von Office und der richtige Code Wenn ausgeführt wird Sie Mischen von 32-Bit- und 64-Bit-Code.
  
Visual Basic für Applikationen 7.0 (VBA 7) in die 64-Bit-Versionen für Office freigegeben wird, und es funktioniert mit 32-Bit- und 64-Bit-Anwendungen. Die Änderungen, die in diesem Artikel beschriebenen gelten nur für die 64-Bit-Versionen von Office. Mithilfe der 32-Bit-Versionen von Microsoft Office aktivieren Sie zum Verwenden von Lösungen in früheren Versionen von Office ohne weitere Änderungen erstellt.
  
> [!NOTE]
> In der Standardeinstellung bei der Installation einer 64-Bit-Version von Office, auch Installation von 32-Bit-Version, die zusammen mit der 64-Bit-System installiert ist. Sie müssen die Installationsoption für Microsoft Office 64-Bit-Version explizit auswählen. 
  
In VBA 7 müssen Sie die vorhandene Windows-API-Anweisungen (**Declare** -Anweisungen) entwickelt, die 64-Bit-Version aktualisieren. Darüber hinaus müssen Sie Adresszeiger aktualisieren und Anzeigen von Fensterhandles in benutzerdefinierten Typen, die von diesen Anweisungen verwendet werden. Dies wird ausführlich in diesem Artikel ebenfalls wie Kompatibilität zwischen der 32-Bit- und 64-Bit-Versionen und Lösungsvorschläge Probleme erläutert. 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a>32-Bit- und 64-Bit-Systeme im Vergleich
<a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a>

Anwendungen, die mit der 64-Bit-Versionen von Office können größere Adressräume als 32-Bit-Versionen verweisen. Dies bedeutet, zusätzlichem physikalischen Arbeitsspeicher für Daten als vor verwendet werden können, Verschieben von Daten innerhalb und außerhalb der physischen Speicher aufgewendeten potenziell Reduzierung den Aufwand
  
Zusätzlich zu verweisen (bekannt als Zeiger) bestimmte Orte im physischen Arbeitsspeicher, auch können Adressen Sie Anzeige Fenster Bezeichner (bekannt als Handles) verweisen. Die Größe (in Bytes) der Zeiger oder Handle hängt davon ab, ob Sie eine 32-Bit oder 64-Bit-System verwendet werden. 
  
Wenn Sie Ihrer vorhandenen Lösungen mit den 64-Bit-Versionen von Office ausführen möchten, beachten Sie die folgenden:
  
- Systemeigene 64-Bit-Prozessen in Office können nicht 32-Bit-Binärdateien geladen werden. Dies wird erwartet, dass ein häufiges Problem sein, wenn Sie vorhandene Microsoft ActiveX-Steuerelemente und vorhandenen-add-ins.
    
- VBA haben nicht bereits einen Zeiger Datentyp, damit mussten Sie 32-Bit-Variablen zum Speichern von Zeigern und Handles verwenden. Diese Variablen jetzt kürzen 64-Bit-Werte, die beim Verwenden von **Declare** -Anweisungen durch API-Aufrufe zurückgegeben. 
    
## <a name="vba-7-code-base"></a>VBA 7-Codebasis
<a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a>

VBA 7 ersetzt den VBA-Code in Office 2007 und früheren Versionen Basiskalender. VBA 7 ist in der 32-Bit- und 64-Bit-Version von Office verfügbar. Es bietet zwei Konstanten für die bedingte Kompilierung: 
  
- **VBA7** - kann sichergestellt werden die Abwärtskompatibilität des Codes Sie testen, ob der Anwendung VBA 7 oder der vorherigen Version von VBA verwendet wird. 
    
- **Win64** Überprüft, ob Code als 32-Bit oder 64-Bit-Version ausgeführt wird. 
    
Mit bestimmten Ausnahmen können die Makros in einem Dokument, der in der 32-Bit-Version der Anwendung funktioniert auch in der 64-Bit-Version.
  
## <a name="activex-control-and-com-add-in-compatibility"></a>ActiveX-Steuerelementen und COM-add-in-Kompatibilität
<a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a>

Vorhandene 32-Bit-ActiveX-Steuerelemente, sind nicht kompatibel mit den 64-Bit-Versionen von Office. Für ActiveX-Steuerelemente und COM-Objekte:
  
- Wenn Sie den Quellcode, 64-Bit-Version selbst generiert haben.
- Wenn Sie nicht über den Quellcode verfügen, wenden Sie sich an den Hersteller für eine aktualisierte Version.
    
Systemeigene 64-Bit-Prozessen in Office können nicht 32-Bit-Binärdateien geladen werden. Dazu gehören die Standardsteuerelemente des **MSComCtl** (TabStrip, Symbolleiste, StatusBar, Fortschrittsleiste, TreeView, ListViews, ImageList, Schieberegler, ImageCombo) und die Steuerelemente des **MSComCt2** (Animation, UpDown, Monatsansicht, DateTimePicker, FlatScrollBar). Diese Steuerelemente wurden von 32-Bit-Versionen von Office vor Office 2010 installiert. Sie müssen eine Alternative zu Ihrer vorhandenen VBA-Lösungen zu finden, die diese Steuerelemente verwenden, wenn Sie den Code für die 64-Bit-Versionen von Office migrieren. 
  
## <a name="api-compatibility"></a>API-Kompatibilität
<a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a>

Die Kombination von VBA und Typ Bibliotheken stellt Ihnen eine Vielzahl von Funktionalität zum Erstellen von Office-Anwendungen. Allerdings müssen manchmal Sie kommunizieren direkt mit Betriebssystem des Computers und anderen Komponenten, beispielsweise wenn Sie Arbeitsspeicher oder Prozesse, beim Arbeiten mit UI-Elemente Linke Fenster und Steuerelemente oder beim Ändern der Windows-Registrierungs zu verwalten. In diesen Szenarien ist die beste Option, eine der externen Funktionen verwenden, die in DLL-Dateien eingebettet sind. Zu diesem Zweck in VBA-API-Aufrufe **Declare** -Anweisungen verwenden. 
  
> [!NOTE]
> Microsoft bietet eine Win32API.txt-Datei, die enthält 1.500 Declare-Anweisungen und ein Tool zum Kopieren von der **Declare** -Anweisung, die Sie in Ihrem Code verwenden möchten. Diese Anweisungen sind allerdings für 32-Bit-Systeme und müssen in konvertiert werden 64-Bit-mithilfe der weiter unten in diesem Artikel erläuterten Informationen. Bis sie als sicher für die markiert haben, nicht vorhandene **Declare** -Anweisungen in 64-Bit-VBA kompiliert 64-Bit-Version mit dem **PtrSafe** -Attribut. Beispiele für diese Art der Konvertierung finden Sie unter Excel MVP Jan Karel Pieterse Website unter [http://www.jkp-ads.com/articles/apideclarations.asp](http://www.jkp-ads.com/articles/apideclarations.asp). Die [Office Code Compatibility Inspector user's Guide](http://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) ist hilfreich, die Syntax der API **Declare** -Anweisungen für das **PtrSafe** -Attribut zu überprüfen, falls erforderlich, und die entsprechenden Typ zurück. 
  
**Declare** -Anweisungen ähneln eine der folgenden, je nachdem, ob Sie eine Unterroutine (kein Rückgabewert) oder eine Funktion (die verfügt einen Rückgabewert) aufrufen werden. 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

Die **SubName** oder **Funktionsname** -Funktion wird durch den tatsächlichen Namen der Prozedur in der DLL-Datei ersetzt und stellt den Namen dar, der verwendet wird, wenn die Prozedur aus VBA-Code aufgerufen wird. Sie können auch ein **AliasName** -Argument für den Namen der Prozedur angeben. Der Name der DLL-Datei, die die aufgerufenen Prozedur enthält folgt das Schlüsselwort **Lib** . Und schließlich enthält die Liste der Argumente, die Parameter und die Datentypen, die an die Prozedur übergeben werden müssen. 
  
Die folgenden **Declare** -Anweisung wird ein *Unterschlüssel* in der Windows-Registrierung geöffnet und der Wert ersetzt. 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

Der Eintrag Windows.h (Fensterhandle) für die **RegOpenKeyA** -Funktion lautet wie folgt: 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

In Visual C# und Microsoft Visual C++ kompiliert das vorherige Beispiel ordnungsgemäß für 32-Bit- und 64-Bit. Dies ist, da HKEY als einen Zeiger definiert ist, dessen Größe die Größe des Speichers der Plattform wiedergibt, die in der Code kompiliert wird.
  
In früheren Versionen von VBA wurde kein Datentyp bestimmter Zeiger so der Datentyp **Long** verwendet wurde. Und da der Datentyp **Long** immer 32-Bit, diese Umbrüche bei der Verwendung auf einem System mit 64-Bit-Speicher ist, da die oberen 32 Bits möglicherweise abgeschnitten oder möglicherweise andere Arbeitsspeicheradressen überschreiben. Eine der folgenden Situationen kann unvorhersehbares Verhalten oder System Abstürze führen. 
  
Um dieses Problem zu beheben, VBA enthält einen Datentyp true *Zeiger* : **LongPtr**. Diese neuen Datentyp können Sie die ursprüngliche **Declare** -Anweisung schreiben ordnungsgemäß als: 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

Dieser Datentyp und das neue **PtrSafe** -Attribut können Sie mithilfe dieser **Declare** -Anweisung auf 32-Bit oder 64-Bit-Systemen. Das **PtrSafe** -Attribut zeigt der VBA-Compiler, dass die **Declare** -Anweisung für die 64-Bit-Version von Office vorgesehen ist. Ohne dieses Attribut führt die mithilfe der **Declare** -Anweisung in einem 64-Bit-System zu einem Kompilierungsfehler. Das **PtrSafe** -Attribut ist optional auf der 32-Bit-Version von Office. Auf diese Weise können vorhandene **Declare** -Anweisungen genauso wie bisher. 
  
Die folgende Tabelle enthält weitere Informationen zu den neuen Qualifizierer und Daten Typeas sowie einen anderen Datentyp, zwei Konvertierungsoperatoren und drei Funktionen.
  
|Typ|Element|Beschreibung|
|:-----|:-----|:-----|
|Qualifizierer  <br/> |**PtrSafe** <br/> |Gibt an, dass die **Declare** -Anweisung mit 64-Bit kompatibel ist. Dieses Attribut ist auf 64-Bit-Systemen erforderlich.  <br/> |
|Datentyp  <br/> |**LongPtr** <br/> |Ein variabler Datentyp ist ein 4-Byte-Datentyp auf 32-Bit-Versionen und einer 8-Byte-Datentyp auf 64-Bit-Versionen von Microsoft Office. Dies ist die empfohlene Option Zeiger oder ein Handle für neuen Code, sondern auch für legacy-Code zu deklarieren, wenn sie in der 64-Bit-Version von Office ausgeführt hat. Es ist nur unterstützte in die VBA 7-Laufzeit auf 32-Bit- und 64-Bit. Beachten Sie, dass Sie es aber nicht numerische Typen numerische Werte zuweisen können.  <br/> |
|Datentyp  <br/> |**LongLong** <br/> |Dies ist ein 8-Byte-Datentyp, der nur in 64-Bit-Versionen von Microsoft Office zur Verfügung steht. Sie können numerische Werte, aber nicht numerische Typen (so abgeschnitten) zuweisen.  <br/> |
|Konvertierungsoperator  <br/> |**CLngPtr** <br/> |Konvertiert einen einfachen Ausdruck in einen **LongPtr** -Datentyp.  <br/> |
|Konvertierungsoperator  <br/> |**CLngLng** <br/> |Konvertiert einen einfachen Ausdruck in einen **LongLong** -Datentyp.  <br/> |
|Funktion  <br/> |**VarPtr** <br/> |Variant Konverter. Gibt einen **LongPtr** auf 64-Bit-Versionen, und ein **Long** auf 32-Bit-Versionen (4 Bytes) zurück.  <br/> |
|Funktion  <br/> |**ObjPtr** <br/> |Objekt-Konverter. Gibt einen **LongPtr** auf 64-Bit-Versionen, und ein **Long** auf 32-Bit-Versionen (4 Bytes) zurück.  <br/> |
|Funktion  <br/> |**StrPtr** <br/> |Zeichenfolgenkonverter. Gibt einen **LongPtr** auf 64-Bit-Versionen, und ein **Long** auf 32-Bit-Versionen (4 Bytes) zurück.  <br/> |
   
Im folgenden Beispiel wird veranschaulicht, wie einige dieser Elemente in einer **Declare** -Anweisung verwenden. 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

Beachten Sie, dass **Declare** -Anweisungen ohne das **PtrSafe** -Attribut als nicht kompatibel mit der 64-Bit-Version von Office werden. 
  
Es gibt zwei Konstanten für die bedingte Kompilierung: **VBA7** und **Win64**. Zum Sicherstellen der Abwärtskompatibilität mit früheren Versionen von Microsoft Office, verwenden Sie die **VBA7** -Konstante (Dies ist der normalen Groß-/Kleinschreibung) zu verhindern, dass 64-Bit-Code in der früheren Version von Office verwendet wird. Code, für die unterscheidet sich zwischen der 32-Bit-Version und der 64-Bit-Version, wie das Aufrufen von ein Math-API, **LongLong** für die 64-Bit-Version verwendet, und **lange** für ihre 32-Bit-Version verwenden Sie die **Win64** -Konstante. Der folgende Code zeigt die Verwendung der folgenden zwei-Konstanten. 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

Zusammengefasst, wenn Sie die 64-Bit-Code schreiben und in früheren Versionen von Office verwenden möchten, sollten Sie die Konstante **VBA7** bedingte Kompilierung verwenden. Wenn Sie in Office 32-Bit-Code schreiben, funktioniert jedoch, dass Code in früheren Versionen von Office ohne die Notwendigkeit für die Kompilierungskonstante ist. Wenn Sie sicherstellen möchten, dass Sie 32-Bit-Anweisungen für die 32-Bit-Versionen und 64-Bit-Anweisungen für 64-Bit-Versionen verwenden, ist die beste Option, verwenden Sie die bedingte Kompilierung **Win64** -Konstante. 
  
## <a name="using-conditional-compilation-attributes"></a>Verwenden von bedingten kompilierungsattributen
<a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a>

Das folgende Beispiel zeigt die VBA-Code geschrieben für 32-Bit, die aktualisiert werden muss. Beachten Sie die Datentypen in der Vorversion Code, die aktualisiert werden, um **LongPtr** zu verwenden, da sie auf Handles oder Zeiger verweisen. 
  
### <a name="vba-code-written-for-32-bit-versions"></a>VBA-Code geschrieben für 32-Bit-Versionen
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a>VBA-Code umgeschrieben für 64-Bit-Versionen
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a>

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a>Wann sollte ich die 64-Bit-Version von Office verwenden?
  
Dies ist mehr, die darum, welche hostanwendung (Excel, Word, usw.), die Sie verwenden. Excel ist beispielsweise viel größerer Arbeitsblätter mit der 64-Bit-Version von Microsoft Office zu verarbeiten.
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a>Kann ich die 64-Bit- und 32-Bit-Versionen von Office-Side-by-Side installieren?
  
Nein.
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a>Wann sollte ich lange Parameter in LongPtr konvertieren?
  
Sie müssen die Windows-API-Dokumentation auf der Microsoft Developers Network für die Funktion zu überprüfen, den Sie anrufen möchten. Handles und Zeiger müssen in **LongPtr**konvertiert werden soll. Als Beispiel enthält die Dokumentation zu [RegOpenKeyA](http://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) die folgende Signatur: 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

Der Parameter sind wie folgt definiert:
  
|Parameter|Beschreibung|
|:-----|:-----|
|hKey [in]  <br/> |Ein *behandeln* einen Registrierungsschlüssel.  <br/> |
|LpSubKey [in, optional]  <br/> |Der Name der dem Registrierungsunterschlüssel geöffnet werden soll.  <br/> |
|ulOptions  <br/> |Dieser Parameter ist reserviert und muss NULL sein.  <br/> |
|SamDesired [in]  <br/> |Eine Maske, die die gewünschten Zugriffsrechte für den Schlüssel angibt.  <br/> |
|PhkResult [Out]  <br/> |Ein *Zeiger* auf eine Variable, die ein Handle für das geöffnete Schlüssel erhält.  <br/> |
   
In [Win32API_PtrSafe.txt](http://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b)ist die **Declare** -Anweisung folgendermaßen definiert: 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a>Werden Zeigern und Handles in Strukturen konvertiert?
  
Ja. Finden Sie in des **MSG** -Typs in Win32API_PtrSafe.txt: 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a>Wann sollte ich Strptr, Varpt und Objptr verwenden?
  
Sie sollten diese Funktionen verwenden, Zeiger auf Zeichenfolgen, Variablen und Objekte abrufen. Auf der 64-Bit-Version von Office zurückgegebenen diese Funktionen einer 64-Bit- **LongPtr**an **Declare** -Anweisungen übergeben werden kann. Die Verwendung dieser Funktionen wurde aus früheren Versionen von VBA nicht geändert. Der einzige Unterschied ist, dass sie jetzt eine **LongPtr**zurückgeben.
  
## <a name="see-also"></a>Siehe auch
<a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a>

- [Anatomie einer Declare-Anweisung](https://msdn.microsoft.com/en-us/library/office/aa671659.aspx)
    

