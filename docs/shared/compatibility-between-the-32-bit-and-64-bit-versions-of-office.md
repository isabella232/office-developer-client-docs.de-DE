---
title: Kompatibilität zwischen der 32-Bit- und der 64-Bit-Version von Office
ms.date: 07/04/2021
ms.audience: ITPro
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Hier finden Sie Informationen zur Kompatibilität zwischen der 32-Bit- und der 64-Bit-Version von Office.
localization_priority: Priority
ms.openlocfilehash: e1beaf4217091c1218653df33bd7d99883fb0862
ms.sourcegitcommit: 8dcb4dc4aa066e3d79bcccd9a9aa6cd3f192b3e1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2021
ms.locfileid: "53535892"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a>Kompatibilität zwischen der 32-Bit- und der 64-Bit-Version von Office

Hier finden Sie Informationen zur Kompatibilität zwischen der 32-Bit- und der 64-Bit-Version von Office.
  
Office-Anwendungen stehen als 32-Bit- und 64-Bit-Version zur Verfügung. 
  
Mit den 64-Bit-Versionen von Office können Sie mehr Daten verschieben, um die Funktionalität zu erhöhen, z. B. wenn Sie mit großen Zahlen in Microsoft Excel 2010 arbeiten. Beim Schreiben von 32-Bit-Code können Sie die 64-Bit-Version von Office ohne Änderungen verwenden. Wenn Sie jedoch 64-Bit-Code schreiben, sollten Sie sicherstellen, dass Ihr Code bestimmte Schlüsselwörter und bedingte Kompilierungskonstanten enthält, um sicherzustellen, dass der Code abwärtskompatibel mit einer früheren Version von Office ist und dass der richtige Code ausgeführt wird, wenn Sie 32-Bit- und 64-Bit-Code kombinieren.
  
Visual Basic for Applications 7.0 (VBA-7) ist in 64-Bit-Versionen für Office veröffentlicht und kann sowohl mit 32-Bit- als auch 64-Bit-Anwendungen verwendet werden. Die in diesem Artikel beschriebenen Änderungen gelten nur für 64-Bit-Versionen von Office. Mit 32-Bit-Versionen von Microsoft Office können Sie die in früheren Versionen von Office integrierten Lösungen verwenden, ohne weitere Änderungen vorzunehmen.
  
> [!NOTE]
> Standardmäßig installieren Sie bei der Installation einer 64-Bit-Version von Office auch die 32-Bit-Version, wenn das 64-Bit-System verwendet wird. Sie müssen explizit die Installationsoption für die 64-Bit-Version von Microsoft Office auswählen. 
  
In VBA 7 müssen Sie die vorhandenen Windows-API-Anweisungen (**Declare**-Anweisungen) aktualisieren, damit Sie mit der 64-Bit-Version verwendet werden können. Darüber hinaus müssen Sie die Adresszeiger und Anzeigefensterhandles in benutzerdefinierten Typen aktualisieren, die von diesen Anweisungen verwendet werden. Dies sowie Kompatibilitätsprobleme zwischen den 32-Bit- und 64-Bit-Versionen und die zugehörigen Lösungen werden genau in diesem Artikel erläutert. 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a>Vergleich von 32-Bit- und 64-Bit-Systemen
<a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a>

Anwendungen, die mit 64-Bit-Versionen von Office erstellt wurden, können auf größere Adressräume als 32-Bit-Versionen verweisen. Dies bedeutet, dass Sie mehr physischen Speicher für Daten als vorher verwenden können und so den potenziellen Mehraufwand für das Verschieben von Daten in und aus dem physischen Speicher reduzieren können.
  
Zusätzlich zum Verweisen auf bestimmte Speicherorte (als Zeiger bezeichnet) im physischen Speicher können Sie auch Adressen verwenden, um auf Anzeigefensterbezeichner (als Handles bezeichnet) zu verweisen. Die Größe (in Bytes) des Zeigers oder Handles hängt davon ab, ob Sie ein 32-Bit- oder 64-Bit-System verwenden. 
  
Wenn Sie Ihre vorhandenen Lösungen mit 64-Bit-Versionen von Office ausführen möchten, beachten Sie die folgenden Punkte:
  
- Systemeigene 64-Bit-Prozesse in Office können keine 32-Bit-Binärdateien laden. Es wird erwartet, dass dies ein häufiges Problem ist, wenn Sie über vorhandene Microsoft ActiveX-Steuerelemente und Add-Ins verfügen.
    
- VBA hatte zuvor keinen pointer-Datentyp, sodass Sie 32-Bit-Variablen zum Speichern von Zeigern und Handles verwenden mussten. Mit diesen Variablen werden nun die von API-Aufrufen zurückgegebenen 64-Bit-Werte abgeschnitten, wenn Sie **Declare**-Anweisungen verwenden. 
    
## <a name="vba-7-code-base"></a>VBA 7-Codebasis
<a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a>

Die VBA-Codebasis in Office 2007 und früheren Versionen wird durch VBA 7 ersetzt. VBA 7 ist sowohl in 32-Bit- als auch in 64-Bit-Versionen von Office verfügbar. Dies bietet zwei Konstanten für die bedingte Kompilierung: 
  
- **VBA7** – Stellt Abwärtskompatibilität des Codes sicher, indem getestet wird, ob die Anwendung VBA 7 oder die ältere Version von VBA verwendet. 
    
- **Win64** – Überprüft, ob der Code als 32-Bit- oder 64-Bit-Version ausgeführt wird. 
    
Die Markos in einem Dokument, die in der 32-Bit-Version der Anwendung funktionieren, funktionieren, mit einigen Ausnahmen, auch in der 64-Bit-Version.
  
## <a name="activex-control-and-com-add-in-compatibility"></a>Kompatibilität mit ActiveX-Steuerelementen und COM-Add-Ins
<a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a>

Vorhandene 32-Bit-ActiveX-Steuerelemente sind nicht mit den 64-Bit-Versionen von Office kompatibel. Für ActiveX-Steuerelemente und COM-Objekte:
  
- Wenn der Quellcode verfügbar ist, generieren Sie selbst eine 64-Bit-Version.
- Wenn Sie nicht über den Quellcode verfügen, wenden Sie sich an den Anbieter, um eine aktualisierte Version zu erhalten.
    
Von systemeigenen 64-Bit-Prozessen in Office können keine 32-Bit-Binärdateien geladen werden. Dies umfasst die allgemeinen Steuerelemente von **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) und die Steuerelemente von **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar). Diese Steuerelemente wurden von 32-Bit-Office-Versionen von älteren Office-Versionen als Office 2010 installiert. Sie müssen eine Alternative für Ihre vorhandenen VBA-Lösungen finden, die diese Steuerelemente verwenden, wenn Sie den Code zu 64-Bit-Versionen von Office migrieren. 
  
## <a name="api-compatibility"></a>API-Kompatibilität
<a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a>

Die Kombination von VBA und Typbibliotheken bietet viele Funktionen zum Erstellen von Office-Anwendungen. Manchmal müssen Sie allerdings direkt mit dem Betriebssystem des Computers und andere Komponenten kommunizieren, zum Beispiel wenn Sie Arbeitsspeicher oder Prozesse verwalten, bei der Arbeit mit Benutzeroberflächenelementen wie Fenster und Steuerelemente oder beim Ändern der Windows-Registrierung. In den folgenden Szenarien wird empfohlen, eine der in DLL-Dateien eingebetteten externen Funktionen zu verwenden. Dies können Sie in VBA erledigen, indem Sie API-Aufrufe mithilfe von **Declare**-Anweisungen ausführen. 
  
> [!NOTE]
> Microsoft bietet eine Datei „Win32API.txt“ mit 1.500 Declare-Anweisungen und ein Tool zum Kopieren von **Declare**-Anweisungen in Code. Diese Anweisungen sind jedoch für 32-Bit-Systeme vorgesehen und müssen anhand der später in diesem Artikel erläuterten Informationen in 64 Bit konvertiert werden. Vorhandene **Declare**-Anweisungen werden erst in der 64-Bit-Version von VBA kompiliert, wenn Sie mit dem **PtrSafe**-Attribut als sicher für die 64-Bit-Version gekennzeichnet sind. Beispiele für diesen Typ der Konvertierung finden Sie auf der Website des Excel-MVPs Jan Karel Pieterse unter [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp). Das [Benutzerhandbuch zum Office Code Compatibility Inspector](https://docs.microsoft.com/previous-versions/office/office-2010/ee833946(v=office.14)) ist hilfreich, wenn es darum geht, die Syntax der **Declare**-Anweisungen der API für das **PtrSafe**-Attribut und die entsprechenden Rückgabetypen zu prüfen. 
  
**Declare**-Anweisungen ähneln folgendem Code, je nachdem, ob Sie eine Unterroutine (kein Rückgabewert) oder eine Funktion (mit Rückgabewert) aufrufen. 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

Die **SubName**-Funktion oder **FunctionName**-Funktion wird durch den tatsächlichen Namen der Prozedur in der DLL-Datei ersetzt und steht für den Namen, der verwendet wird, wenn die Prozedur über VBA-Code aufgerufen wird. Sie können auch ein **AliasName**-Argument für den Namen der Prozedur angeben. Der Name der DLL-Datei, die die aufgerufene Prozedur enthält, folgt dem **Lib**-Schlüsselwort. Die Argumentlist enthält schließlich die Parameter und die Datentypen, die an die Prozedur übergeben werden müssen. 
  
Mit der folgenden **Declare**-Anweisung wird ein *Unterschlüssel* in der Windows-Registrierung geöffnet und der Wert ersetzt. 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

Der Eintrag „Windows.h (Fensterhandle)“ für die **RegOpenKeyA**-Funktion lautet wie folgt: 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

In Visual C und Microsoft Visual C++ wird das vorherige Beispiel für 32-Bit und 64-Bit ordnungsgemäß kompiliert. Dies liegt daran, dass HKEY als Zeiger definiert ist, dessen Größe die Arbeitsspeichergröße der Plattform widerspiegelt, in der der Code kompiliert wird.
  
In älteren Versionen von VBA gab es keinen bestimmten pointer-Datentyp, sodass der Datentyp **Long** verwendet wurde. Da der **Long**-Datentyp immer 32 Bit aufweist, wird dieser bei Verwendung auf einem System mit 64-Bit-Arbeitsspeicher gebrochen, weil die oberen 32 Bit möglicherweise abgeschnitten oder andere Arbeitsspeicheradressen überschrieben werden. Eine dieser Situationen können zum unvorhersehbaren Verhalten oder zu Systemabstürzen führen. 
  
Um dieses Problem zu beheben, enthält VBA einen wahren *pointer*-Datentyp: **LongPtr**. Mit diesem neuen Datentyp können Sie die ursprüngliche **Declare**-Anweisung korrekt schreiben als: 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

Mit diesem Datentyp und dem neuen **PtrSafe**-Attribut können Sie diese **Declare**-Anweisung sowohl auf 32-Bit- oder 64-Bit-Systemen verwenden. Das **PtrSafe**-Attribut gibt dem VBA-Compiler an, die die **Declare**-Anweisung auf die 64-Bit-Version von Office abzielt. Ohne dieses Attribut tritt beim Verwenden der **Declare**-Anweisung in einem 64-Bit-System ein Kompilierungszeitfehler auf. Das **PtrSafe**-Attribut ist bei der 32-Bit-Version von Office optional. Dadurch funktionieren vorhandene **Declare**-Anweisungen wie gewohnt. 
  
Die folgende Tabelle enthält weitere Informationen zum neuen Qualifizierer und Datentyp sowie zu einem weiteren Datentyp, zwei Konvertierungsoperatoren und drei Funktionen.
  
|Typ|Element|Beschreibung|
|:-----|:-----|:-----|
|Qualifizierer  <br/> |**PtrSafe** <br/> |Gibt an, dass die **Declare**-Anweisung mit der 64-Bit-Version kompatibel ist. Dieses Attribut ist auf 64-Bit-Systemen erforderlich.  <br/> |
|Datentyp  <br/> |**LongPtr** <br/> |Ein Variablendatentyp, bei dem es sich um einen 4-Byte-Datentyp in 32-Bit-Versionen und einen 8-Byte-Datentyp für 64-Bit-Versionen von Microsoft Office handelt. Dies ist die empfohlene Methode zum Deklarieren eines Zeigers oder Handles für neuen Code, aber auch für Legacycode, wenn er in der 64-Bit-Version von Office ausgeführt werden muss. Sie wird nur in der VBA 7-Runtime mit 32-Bit und 64-Bit unterstützt. Beachten Sie, dass Sie ihm numerische Werte zuweisen können, aber keine numerischen Typen.  <br/> |
|Datentyp  <br/> |**LongLong** <br/> |Dies ist ein 8-Byte-Datentyp, der nur in 64-Bit-Versionen von Microsoft Office verfügbar ist. Sie können numerische Werte zuweisen, aber keine numerischen Typen (um Abschneiden zu vermeiden).  <br/> |
|Operator für die Konvertierung  <br/> |**CLngPtr** <br/> |Konvertiert einen einfachen Ausdruck in einen **LongPtr**-Datentyp.  <br/> |
|Operator für die Konvertierung  <br/> |**CLngLng** <br/> |Konvertiert einen einfachen Ausdruck in einen **LongLong**-Datentyp.  <br/> |
|Funktion  <br/> |**VarPtr** <br/> |Variantkonverter. Gibt einen **LongPtr**-Datentyp auf 64-Bit-Versionen zurück und einen **Long**-Datentyp auf 32-Bit-Versionen (4 Byte) zurück. <br/> |
|Funktion  <br/> |**ObjPtr** <br/> |Objektkonverter. Gibt einen **LongPtr**-Datentyp auf 64-Bit-Versionen zurück und einen **Long**-Datentyp auf 32-Bit-Versionen (4 Byte) zurück. <br/> |
|Funktion  <br/> |**StrPtr** <br/> |Zeichenfolgenkonverter. Gibt einen **LongPtr**-Datentyp auf 64-Bit-Versionen zurück und einen **Long**-Datentyp auf 32-Bit-Versionen (4 Byte) zurück. <br/> |
   
Im folgenden Beispiel wird gezeigt, wie Sie einige dieser Elemente in einer **Declare**-Anweisung verwenden können. 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

Beachten Sie, dass **Declare**-Anweisungen ohne das **PtrSafe**-Attribut im Allgemeinen nicht mit der 64-Bit-Version von Office kompatibel sind. 
  
Es gibt zwei Konstanten für die bedingte Kompilierung: **VBA7** und **Win64**. Um Abwärtskompatibilität mit älteren Versionen von Microsoft Office sicherzustellen, verwenden Sie die **VBA7**-Konstante (Dies ist der häufigere Fall), damit 64-Bit-Code nicht in älteren Versionen von Office verwendet wird. Bei Code, der zwischen der 32-Bit- und der 64-Bit-Version variiert, zum Beispiel beim Aufrufen einer Mathematik-API, die einen **LongLong**-Datentyp für die 64-Bit-Version und einen **Long**-Datentyp für die 32-Bit-Version verwendet, müssen Sie die **Win64**-Konstante verwenden. Der folgende Code zeigt die Verwendung dieser beiden Konstanten. 
  
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

Zusammenfassung: Wenn Sie 64-Bit-Code schreiben und dieser in älteren Versionen von Office verwendet werden soll, sollten Sie die **VBA7**-Konstante für die bedingte Kompilierung verwenden. Wenn Sie jedoch 32-Bit-Code in Office schreiben, kann dieser Code in älteren Versionen von Office verwendet werden, ohne dass Sie Änderungen vornehmen und ohne dass die Konstante für bedingte Kompilierung erforderlich ist. Wenn Sie sicherstellen möchten, dass Sie 32-Bit-Anweisungen für 32-Bit-Versionen und 64-Bit-Anweisungen für 64-Bit-Versionen verwenden, wird empfohlen, die **Win64**-Konstante für die bedingte Kompilierung zu verwenden. 
  
## <a name="using-conditional-compilation-attributes"></a>Verwenden von bedingten Kompilierungsattributen
<a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a>

Das folgende Beispiel zeigt für 32-Bit-Versionen geschriebenen VBA-Code, der aktualisiert werden muss. Beachten Sie die Datentypen im älteren Code, die für die Verwendung von **LongPtr** aktualisiert werden, da sie auf Handles oder Zeiger verweisen. 
  
### <a name="vba-code-written-for-32-bit-versions"></a>Für 32-Bit-Versionen geschriebener VBA-Code
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As LongPtr
  
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

### <a name="vba-code-rewritten-for-64-bit-versions"></a>Für 64-Bit-Versionen neu geschriebener VBA-Code
  
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
  
Dies ist eher eine Frage der Hostanwendung (Excel, Word usw.), die Sie verwenden. Excel kann zum Beispiel viel größere Arbeitsblätter in der 64-Bit-Version von Microsoft Office verarbeiten.
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a>Kann ich sowohl die 64-Bit- als auch die 32-Bit-Version von Office gleichzeitig installieren?
  
Nein.
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a>Wann sollte ich Long-Parameter in LongPtr-Parameter konvertieren?
  
Lesen Sie hierzu die entsprechenden Informationen zu der Funktion, die Sie aufrufen möchten, in der Windows-API-Dokumentation im MSDN. Handles und Zeiger müssen in **LongPtr**-Datentypen konvertiert werden. Die Dokumentation für [RegOpenKeyA](/windows/win32/api/winreg/nf-winreg-regopenkeyexa.md) bietet zum Beispiel die folgende Signatur: 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

Die Parameter sind wie folgt definiert:
  
|Parameter|Beschreibung|
|:-----|:-----|
|hKey [in]  <br/> |Ein *Handle* zu einem geöffneten Registrierungsschlüssel.  <br/> |
|lpSubKey [in, optional]  <br/> |Der Name des Registrierungsunterschlüssels, der geöffnet werden soll.  <br/> |
|ulOptions  <br/> |Dieser Parameter ist reserviert und muss 0 lauten.  <br/> |
|samDesired [in]  <br/> |Eine Maske, die die gewünschten Zugriffsrechte für den Schlüssel angibt.  <br/> |
|phkResult [out]  <br/> |Ein *Zeiger* auf eine Variable, die ein Handle zum geöffneten Schlüssel erhält.  <br/> |
   
In der Datei [Win32API_PtrSafe.txt](/office/troubleshoot/office/win32api_ptrsafe-with-64-bit-support.md) wird die **Declare**-Anweisung wie folgt definiert: 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a>Muss ich Zeiger und Handles in Strukturen konvertieren?
  
Ja. Informationen dazu finden Sie in der Datei „Win32API_PtrSafe.txt“ unter **MSG**-Typ: 
  
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

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a>Wann sollte ich strptr, varpt und objptr verwenden?
  
Sie sollten diese Funktionen verwenden, um Zeiger auf Zeichenfolgen, Variablen und Objekte abzurufen. In der 64-Bit-Version von Office geben diese Funktionen den 64-Bit-Datentyp **LongPtr**, der an die **Declare**-Anweisungen übergeben werden kann. Die Verwendung dieser Funktionen hat sich seit den älteren Versionen von VBA nicht geändert. Der einzige Unterschied besteht darin, dass sie jetzt einen **LongPtr**-Datentyp zurückgeben.
  
## <a name="see-also"></a>Siehe auch
<a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a>

- [Aufbau einer Declare-Anweisung](https://docs.microsoft.com/previous-versions/aa671659(v=vs.71))
