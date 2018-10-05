---
title: Kompatibilität zwischen der 32-Bit- und der 64-Bit-Version von Office
ms.date: 04/27/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Erfahren Sie, wie die 32-Bit-Version von Office mit der 64-Bit-Version von Office kompatibel ist.
ms.openlocfilehash: eeff11f11d4f2595b7111c0233703d09b1c46651
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390940"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a><span data-ttu-id="a29b1-103">Kompatibilität zwischen der 32-Bit- und der 64-Bit-Version von Office</span><span class="sxs-lookup"><span data-stu-id="a29b1-103">Compatibility between the 32-bit and 64-bit versions of Office</span></span>

<span data-ttu-id="a29b1-104">Erfahren Sie, wie die 32-Bit-Version von Office mit der 64-Bit-Version von Office kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="a29b1-104">Find out how the 32-bit version of Office is compatible with the 64-bit version of Office.</span></span>
  
<span data-ttu-id="a29b1-105">Office-Anwendungen sind in 32-Bit- und 64-Bit-Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a29b1-105">Office applications are available in 32-bit and 64-bit versions.</span></span> 
  
<span data-ttu-id="a29b1-106">Die 64-Bit-Versionen von Office können Sie weitere Daten für höhere Kapazität, beispielsweise beim Arbeiten mit einer großen Anzahl in Microsoft Excel 2010 bewegen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-106">The 64-bit versions of Office enable you to move more data around for increased capability, for example when you work with large numbers in Microsoft Excel 2010.</span></span> <span data-ttu-id="a29b1-107">Wenn Sie 32-Bit-Code zu schreiben, können Sie die 64-Bit-Version von Office ohne Änderungen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-107">When writing 32-bit code, you can use the 64-bit version of Office without any changes.</span></span> <span data-ttu-id="a29b1-108">Wenn Sie die 64-Bit-Code schreiben, Sie sollten jedoch sicherstellen, dass der Code enthält bestimmte Schlüsselwörter und bedingte Kompilierung-Konstanten, um sicherzustellen, dass der Code abwärtskompatibel mit früheren Versionen von Office und der richtige Code Wenn ausgeführt wird Sie Mischen von 32-Bit- und 64-Bit-Code.</span><span class="sxs-lookup"><span data-stu-id="a29b1-108">However, when you write 64-bit code, you should ensure that your code contains specific keywords and conditional compilation constants to ensure that the code is backward compatible with earlier version of Office, and that the correct code is being executed if you mix 32-bit and 64-bit code.</span></span>
  
<span data-ttu-id="a29b1-109">Visual Basic für Applikationen 7.0 (VBA 7) in die 64-Bit-Versionen für Office freigegeben wird, und es funktioniert mit 32-Bit- und 64-Bit-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-109">Visual Basic for Applications 7.0 (VBA 7) is released in the 64-bit versions for Office, and it works with both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="a29b1-110">Die Änderungen, die in diesem Artikel beschriebenen gelten nur für die 64-Bit-Versionen von Office.</span><span class="sxs-lookup"><span data-stu-id="a29b1-110">The changes described in this article apply only to the 64-bit versions of Office.</span></span> <span data-ttu-id="a29b1-111">Mithilfe der 32-Bit-Versionen von Microsoft Office aktivieren Sie zum Verwenden von Lösungen in früheren Versionen von Office ohne weitere Änderungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="a29b1-111">Using the 32-bit versions of Microsoft Office enable you to use solutions built in previous versions of Office without further modifications.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a29b1-112">In der Standardeinstellung bei der Installation einer 64-Bit-Version von Office, auch Installation von 32-Bit-Version, die zusammen mit der 64-Bit-System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a29b1-112">By default, when you install a 64-bit version of Office, you also install the 32-bit version is installed along with the 64-bit system.</span></span> <span data-ttu-id="a29b1-113">Sie müssen die Installationsoption für Microsoft Office 64-Bit-Version explizit auswählen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-113">You must explicitly select the Microsoft Office 64-bit version installation option.</span></span> 
  
<span data-ttu-id="a29b1-114">In VBA 7 müssen Sie die vorhandene Windows-API-Anweisungen (**Declare** -Anweisungen) entwickelt, die 64-Bit-Version aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a29b1-114">In VBA 7, you must update existing Windows API statements (**Declare** statements) to work with the 64-bit version.</span></span> <span data-ttu-id="a29b1-115">Darüber hinaus müssen Sie Adresszeiger aktualisieren und Anzeigen von Fensterhandles in benutzerdefinierten Typen, die von diesen Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a29b1-115">Additionally, you must update address pointers and display window handles in user-defined types that are used by these statements.</span></span> <span data-ttu-id="a29b1-116">Dies wird ausführlich in diesem Artikel ebenfalls wie Kompatibilität zwischen der 32-Bit- und 64-Bit-Versionen und Lösungsvorschläge Probleme erläutert.</span><span class="sxs-lookup"><span data-stu-id="a29b1-116">This is discussed in more detail in this article as well as compatibility issues between the 32-bit and 64-bit versions and suggested solutions.</span></span> 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a><span data-ttu-id="a29b1-117">32-Bit- und 64-Bit-Systeme im Vergleich</span><span class="sxs-lookup"><span data-stu-id="a29b1-117">Comparing 32-bit and 64-bit systems</span></span>
<span data-ttu-id="a29b1-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span><span class="sxs-lookup"><span data-stu-id="a29b1-118"></span></span>

<span data-ttu-id="a29b1-119">Anwendungen, die mit der 64-Bit-Versionen von Office können größere Adressräume als 32-Bit-Versionen verweisen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-119">Applications built with the 64-bit versions of Office can reference larger address spaces than 32-bit versions.</span></span> <span data-ttu-id="a29b1-120">Dies bedeutet, zusätzlichem physikalischen Arbeitsspeicher für Daten als vor verwendet werden können, Verschieben von Daten innerhalb und außerhalb der physischen Speicher aufgewendeten potenziell Reduzierung den Aufwand</span><span class="sxs-lookup"><span data-stu-id="a29b1-120">This means you can use more physical memory for data than before, potentially reducing the overhead spent moving data in and out of physical memory</span></span>
  
<span data-ttu-id="a29b1-121">Zusätzlich zu verweisen (bekannt als Zeiger) bestimmte Orte im physischen Arbeitsspeicher, auch können Adressen Sie Anzeige Fenster Bezeichner (bekannt als Handles) verweisen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-121">In addition to referring specific locations (known as pointers) in physical memory, you can also use addresses to reference display window identifiers (known as handles).</span></span> <span data-ttu-id="a29b1-122">Die Größe (in Bytes) der Zeiger oder Handle hängt davon ab, ob Sie eine 32-Bit oder 64-Bit-System verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a29b1-122">The size (in bytes) of the pointer or handle depends on whether you're using a 32-bit or 64-bit system.</span></span> 
  
<span data-ttu-id="a29b1-123">Wenn Sie Ihrer vorhandenen Lösungen mit den 64-Bit-Versionen von Office ausführen möchten, beachten Sie die folgenden:</span><span class="sxs-lookup"><span data-stu-id="a29b1-123">If you want to run your existing solutions with the 64-bit versions of Office, be aware of the following:</span></span>
  
- <span data-ttu-id="a29b1-124">Systemeigene 64-Bit-Prozessen in Office können nicht 32-Bit-Binärdateien geladen werden.</span><span class="sxs-lookup"><span data-stu-id="a29b1-124">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="a29b1-125">Dies wird erwartet, dass ein häufiges Problem sein, wenn Sie vorhandene Microsoft ActiveX-Steuerelemente und vorhandenen-add-ins.</span><span class="sxs-lookup"><span data-stu-id="a29b1-125">This is expected to be a common issue when you have existing Microsoft ActiveX controls and existing add-ins.</span></span>
    
- <span data-ttu-id="a29b1-126">VBA haben nicht bereits einen Zeiger Datentyp, damit mussten Sie 32-Bit-Variablen zum Speichern von Zeigern und Handles verwenden.</span><span class="sxs-lookup"><span data-stu-id="a29b1-126">VBA previously didn't have a pointer data type, so you had to use 32-bit variables to store pointers and handles.</span></span> <span data-ttu-id="a29b1-127">Diese Variablen jetzt kürzen 64-Bit-Werte, die beim Verwenden von **Declare** -Anweisungen durch API-Aufrufe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a29b1-127">These variables now truncate 64-bit values returned by API calls when using **Declare** statements.</span></span> 
    
## <a name="vba-7-code-base"></a><span data-ttu-id="a29b1-128">VBA 7-Codebasis</span><span class="sxs-lookup"><span data-stu-id="a29b1-128">VBA 7 code base</span></span>
<span data-ttu-id="a29b1-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span><span class="sxs-lookup"><span data-stu-id="a29b1-129"></span></span>

<span data-ttu-id="a29b1-130">VBA 7 ersetzt den VBA-Code in Office 2007 und früheren Versionen Basiskalender.</span><span class="sxs-lookup"><span data-stu-id="a29b1-130">VBA 7 replaces the VBA code base in Office 2007 and earlier versions.</span></span> <span data-ttu-id="a29b1-131">VBA 7 ist in der 32-Bit- und 64-Bit-Version von Office verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a29b1-131">VBA 7 is available in both the 32-bit and 64-bit versions of Office.</span></span> <span data-ttu-id="a29b1-132">Es bietet zwei Konstanten für die bedingte Kompilierung:</span><span class="sxs-lookup"><span data-stu-id="a29b1-132">It provides two conditional compilation constants:</span></span> 
  
- <span data-ttu-id="a29b1-133">**VBA7** - kann sichergestellt werden die Abwärtskompatibilität des Codes Sie testen, ob der Anwendung VBA 7 oder der vorherigen Version von VBA verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a29b1-133">**VBA7** - Helps ensure the backward compatibility of your code by testing whether your application is using VBA 7 or the previous version of VBA.</span></span> 
    
- <span data-ttu-id="a29b1-134">**Win64** Überprüft, ob Code als 32-Bit oder 64-Bit-Version ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a29b1-134">**Win64** Tests whether code is running as 32-bit or 64-bit.</span></span> 
    
<span data-ttu-id="a29b1-135">Mit bestimmten Ausnahmen können die Makros in einem Dokument, der in der 32-Bit-Version der Anwendung funktioniert auch in der 64-Bit-Version.</span><span class="sxs-lookup"><span data-stu-id="a29b1-135">With certain exceptions, the macros in a document that work in the 32-bit version of the application also work in the 64-bit version.</span></span>
  
## <a name="activex-control-and-com-add-in-compatibility"></a><span data-ttu-id="a29b1-136">ActiveX-Steuerelementen und COM-add-in-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="a29b1-136">ActiveX control and COM add-in compatibility</span></span>
<span data-ttu-id="a29b1-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="a29b1-137"></span></span>

<span data-ttu-id="a29b1-138">Vorhandene 32-Bit-ActiveX-Steuerelemente, sind nicht kompatibel mit den 64-Bit-Versionen von Office.</span><span class="sxs-lookup"><span data-stu-id="a29b1-138">Existing 32-bit ActiveX controls, are not compatible with the 64-bit versions of Office.</span></span> <span data-ttu-id="a29b1-139">Für ActiveX-Steuerelemente und COM-Objekte:</span><span class="sxs-lookup"><span data-stu-id="a29b1-139">For ActiveX controls and COM objects:</span></span>
  
- <span data-ttu-id="a29b1-140">Wenn Sie den Quellcode, 64-Bit-Version selbst generiert haben.</span><span class="sxs-lookup"><span data-stu-id="a29b1-140">If you have the source code, generate a 64-bit version yourself.</span></span>
- <span data-ttu-id="a29b1-141">Wenn Sie nicht über den Quellcode verfügen, wenden Sie sich an den Hersteller für eine aktualisierte Version.</span><span class="sxs-lookup"><span data-stu-id="a29b1-141">If you don't have the source code, contact the vendor for an updated version.</span></span>
    
<span data-ttu-id="a29b1-142">Systemeigene 64-Bit-Prozessen in Office können nicht 32-Bit-Binärdateien geladen werden.</span><span class="sxs-lookup"><span data-stu-id="a29b1-142">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="a29b1-143">Dazu gehören die Standardsteuerelemente des **MSComCtl** (TabStrip, Symbolleiste, StatusBar, Fortschrittsleiste, TreeView, ListViews, ImageList, Schieberegler, ImageCombo) und die Steuerelemente des **MSComCt2** (Animation, UpDown, Monatsansicht, DateTimePicker, FlatScrollBar).</span><span class="sxs-lookup"><span data-stu-id="a29b1-143">This includes the common controls of **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) and the controls of **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span></span> <span data-ttu-id="a29b1-144">Diese Steuerelemente wurden von 32-Bit-Versionen von Office vor Office 2010 installiert.</span><span class="sxs-lookup"><span data-stu-id="a29b1-144">These controls were installed by 32-bit versions of Office earlier than Office 2010.</span></span> <span data-ttu-id="a29b1-145">Sie müssen eine Alternative zu Ihrer vorhandenen VBA-Lösungen zu finden, die diese Steuerelemente verwenden, wenn Sie den Code für die 64-Bit-Versionen von Office migrieren.</span><span class="sxs-lookup"><span data-stu-id="a29b1-145">You'll need to find an alternative for your existing VBA solutions that use these controls when you migrate the code to the 64-bit versions of Office.</span></span> 
  
## <a name="api-compatibility"></a><span data-ttu-id="a29b1-146">API-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="a29b1-146">API compatibility</span></span>
<span data-ttu-id="a29b1-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="a29b1-147"></span></span>

<span data-ttu-id="a29b1-148">Die Kombination von VBA und Typ Bibliotheken stellt Ihnen eine Vielzahl von Funktionalität zum Erstellen von Office-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-148">The combination of VBA and type libraries gives you lots of functionality to create Office applications.</span></span> <span data-ttu-id="a29b1-149">Allerdings müssen manchmal Sie kommunizieren direkt mit Betriebssystem des Computers und anderen Komponenten, beispielsweise wenn Sie Arbeitsspeicher oder Prozesse, beim Arbeiten mit UI-Elemente Linke Fenster und Steuerelemente oder beim Ändern der Windows-Registrierungs zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a29b1-149">However, sometimes you must communicate directly with the computer's operating system and other components, such as when you manage memory or processes, when working with UI elements linke windows and controls, or when modifying the Windows registry.</span></span> <span data-ttu-id="a29b1-150">In diesen Szenarien ist die beste Option, eine der externen Funktionen verwenden, die in DLL-Dateien eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="a29b1-150">In these scenarios, your best option is to use one of the external functions that are embedded in DLL files.</span></span> <span data-ttu-id="a29b1-151">Zu diesem Zweck in VBA-API-Aufrufe **Declare** -Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a29b1-151">You do this in VBA by making API calls using **Declare** statements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a29b1-152">Microsoft bietet eine Win32API.txt-Datei, die enthält 1.500 Declare-Anweisungen und ein Tool zum Kopieren von der **Declare** -Anweisung, die Sie in Ihrem Code verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="a29b1-152">Microsoft provides a Win32API.txt file that contains 1,500 Declare statements and a tool to copy the **Declare** statement that you want into your code.</span></span> <span data-ttu-id="a29b1-153">Diese Anweisungen sind allerdings für 32-Bit-Systeme und müssen in konvertiert werden 64-Bit-mithilfe der weiter unten in diesem Artikel erläuterten Informationen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-153">However, these statements are for 32-bit systems and must be converted to 64-bit by using the information discussed later in this article.</span></span> <span data-ttu-id="a29b1-154">Bis sie als sicher für die markiert haben, nicht vorhandene **Declare** -Anweisungen in 64-Bit-VBA kompiliert 64-Bit-Version mit dem **PtrSafe** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="a29b1-154">Existing **Declare** statements won't compile in 64-bit VBA until they've been marked as safe for 64-bit by using the **PtrSafe** attribute.</span></span> <span data-ttu-id="a29b1-155">Beispiele für diese Art der Konvertierung finden Sie unter Excel MVP Jan Karel Pieterse Website unter [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span><span class="sxs-lookup"><span data-stu-id="a29b1-155">You can find examples of this type of conversion at Excel MVP Jan Karel Pieterse's website at [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span></span> <span data-ttu-id="a29b1-156">Die [Office Code Compatibility Inspector user's Guide](https://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) ist hilfreich, die Syntax der API **Declare** -Anweisungen für das **PtrSafe** -Attribut zu überprüfen, falls erforderlich, und die entsprechenden Typ zurück.</span><span class="sxs-lookup"><span data-stu-id="a29b1-156">The [Office Code Compatibility Inspector user's guide](https://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) is a useful tool to inspect the syntax of API **Declare** statements for the **PtrSafe** attribute, if needed, and the appropriate return type.</span></span> 
  
<span data-ttu-id="a29b1-157">**Declare** -Anweisungen ähneln eine der folgenden, je nachdem, ob Sie eine Unterroutine (kein Rückgabewert) oder eine Funktion (die verfügt einen Rückgabewert) aufrufen werden.</span><span class="sxs-lookup"><span data-stu-id="a29b1-157">**Declare** statements resemble one of the following, depending on whether you are calling a subroutine (which has no return value) or a function (which does have a return value).</span></span> 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

<span data-ttu-id="a29b1-158">Die **SubName** oder **Funktionsname** -Funktion wird durch den tatsächlichen Namen der Prozedur in der DLL-Datei ersetzt und stellt den Namen dar, der verwendet wird, wenn die Prozedur aus VBA-Code aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a29b1-158">The **SubName** function or **FunctionName** function is replaced by the actual name of the procedure in the DLL file and represents the name that is used when the procedure is called from VBA code.</span></span> <span data-ttu-id="a29b1-159">Sie können auch ein **AliasName** -Argument für den Namen der Prozedur angeben.</span><span class="sxs-lookup"><span data-stu-id="a29b1-159">You can also specify an **AliasName** argument for the name of the procedure.</span></span> <span data-ttu-id="a29b1-160">Der Name der DLL-Datei, die die aufgerufenen Prozedur enthält folgt das Schlüsselwort **Lib** .</span><span class="sxs-lookup"><span data-stu-id="a29b1-160">The name of the DLL file that contains the procedure being called follows the **Lib** keyword.</span></span> <span data-ttu-id="a29b1-161">Und schließlich enthält die Liste der Argumente, die Parameter und die Datentypen, die an die Prozedur übergeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-161">And finally, the argument list contains the parameters and the data types that must be passed to the procedure.</span></span> 
  
<span data-ttu-id="a29b1-162">Die folgenden **Declare** -Anweisung wird ein *Unterschlüssel* in der Windows-Registrierung geöffnet und der Wert ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a29b1-162">The following **Declare** statement opens a  *subkey*  in the Windows registry and replaces its value.</span></span> 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

<span data-ttu-id="a29b1-163">Der Eintrag Windows.h (Fensterhandle) für die RegOpenKeyA-Funktion lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a29b1-163">The Windows.h (window handle) entry for the **RegOpenKeyA** function is as follows:</span></span> 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

<span data-ttu-id="a29b1-164">In Visual C# und Microsoft Visual C++ kompiliert das vorherige Beispiel ordnungsgemäß für 32-Bit- und 64-Bit.</span><span class="sxs-lookup"><span data-stu-id="a29b1-164">In Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit.</span></span> <span data-ttu-id="a29b1-165">Dies ist, da HKEY als einen Zeiger definiert ist, dessen Größe die Größe des Speichers der Plattform wiedergibt, die in der Code kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="a29b1-165">This is because HKEY is defined as a pointer, whose size reflects the memory size of the platform that the code is compiled in.</span></span>
  
<span data-ttu-id="a29b1-166">In früheren Versionen von VBA wurde kein Datentyp bestimmter Zeiger so der Datentyp **Long** verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a29b1-166">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used.</span></span> <span data-ttu-id="a29b1-167">Und da der Datentyp **Long** immer 32-Bit, diese Umbrüche bei der Verwendung auf einem System mit 64-Bit-Speicher ist, da die oberen 32 Bits möglicherweise abgeschnitten oder möglicherweise andere Arbeitsspeicheradressen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="a29b1-167">And because the **Long** data type is always 32-bits, this breaks when used on a system with 64-bit memory because the upper 32-bits might be truncated or might overwrite other memory addresses.</span></span> <span data-ttu-id="a29b1-168">Eine der folgenden Situationen kann unvorhersehbares Verhalten oder System Abstürze führen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-168">Either of these situations can result in unpredictable behavior or system crashes.</span></span> 
  
<span data-ttu-id="a29b1-169">Um dieses Problem zu beheben, VBA enthält einen Datentyp true *Zeiger* : **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="a29b1-169">To resolve this, VBA includes a true  *pointer*  data type: **LongPtr**.</span></span> <span data-ttu-id="a29b1-170">Diese neuen Datentyp können Sie die ursprüngliche **Declare** -Anweisung schreiben ordnungsgemäß als:</span><span class="sxs-lookup"><span data-stu-id="a29b1-170">This new data type enables you to write the original **Declare** statement correctly as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

<span data-ttu-id="a29b1-171">Dieser Datentyp und das neue **PtrSafe** -Attribut können Sie mithilfe dieser **Declare** -Anweisung auf 32-Bit oder 64-Bit-Systemen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-171">This data type and the new **PtrSafe** attribute enable you to use this **Declare** statement on either 32-bit or 64-bit systems.</span></span> <span data-ttu-id="a29b1-172">Das **PtrSafe** -Attribut zeigt der VBA-Compiler, dass die **Declare** -Anweisung für die 64-Bit-Version von Office vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="a29b1-172">The **PtrSafe** attribute indicates to the VBA compiler that the **Declare** statement is targeted for the 64-bit version of Office.</span></span> <span data-ttu-id="a29b1-173">Ohne dieses Attribut führt die mithilfe der **Declare** -Anweisung in einem 64-Bit-System zu einem Kompilierungsfehler.</span><span class="sxs-lookup"><span data-stu-id="a29b1-173">Without this attribute, using the **Declare** statement in a 64-bit system will result in a compile-time error.</span></span> <span data-ttu-id="a29b1-174">Das **PtrSafe** -Attribut ist optional auf der 32-Bit-Version von Office.</span><span class="sxs-lookup"><span data-stu-id="a29b1-174">The **PtrSafe** attribute is optional on the 32-bit version of Office.</span></span> <span data-ttu-id="a29b1-175">Auf diese Weise können vorhandene **Declare** -Anweisungen genauso wie bisher.</span><span class="sxs-lookup"><span data-stu-id="a29b1-175">This enables existing **Declare** statements to work as they always have.</span></span> 
  
<span data-ttu-id="a29b1-176">Die folgende Tabelle enthält weitere Informationen zu den neuen Qualifizierer und Daten Typeas sowie einen anderen Datentyp, zwei Konvertierungsoperatoren und drei Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-176">The following table provides more information about the new qualifier and data typeas well as another data type, two conversion operators, and three functions.</span></span>
  
|<span data-ttu-id="a29b1-177">Typ</span><span class="sxs-lookup"><span data-stu-id="a29b1-177">Type</span></span>|<span data-ttu-id="a29b1-178">Element</span><span class="sxs-lookup"><span data-stu-id="a29b1-178">Item</span></span>|<span data-ttu-id="a29b1-179">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a29b1-179">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a29b1-180">Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="a29b1-180">Qualifier</span></span>  <br/> |<span data-ttu-id="a29b1-181">**PtrSafe**</span><span class="sxs-lookup"><span data-stu-id="a29b1-181">**PtrSafe**</span></span> <br/> |<span data-ttu-id="a29b1-p119">Gibt an, dass die **Declare**-Anweisung mit 64-Bit-Systemen kompatibel ist. Dieses Attribut ist auf 64-Bit-Systemen obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="a29b1-p119">Indicates that the **Declare** statement is compatible with 64-bits. This attribute is mandatory on 64-bit systems.  </span></span><br/> |
|<span data-ttu-id="a29b1-184">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a29b1-184">Data Type</span></span>  <br/> |<span data-ttu-id="a29b1-185">**LongPtr**</span><span class="sxs-lookup"><span data-stu-id="a29b1-185">**LongPtr**</span></span> <br/> |<span data-ttu-id="a29b1-186">Ein variabler Datentyp ist ein 4-Byte-Datentyp auf 32-Bit-Versionen und einer 8-Byte-Datentyp auf 64-Bit-Versionen von Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="a29b1-186">A variable data type which is a 4-bytes data type on 32-bit versions and an 8-byte data type on 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="a29b1-187">Dies ist die empfohlene Option Zeiger oder ein Handle für neuen Code, sondern auch für legacy-Code zu deklarieren, wenn sie in der 64-Bit-Version von Office ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="a29b1-187">This is the recommended way of declaring a pointer or a handle for new code but also for legacy code if it has to run in the 64-bit version of Office.</span></span> <span data-ttu-id="a29b1-188">Es ist nur unterstützte in die VBA 7-Laufzeit auf 32-Bit- und 64-Bit.</span><span class="sxs-lookup"><span data-stu-id="a29b1-188">It is only supported in the VBA 7 runtime on 32-bit and 64-bit.</span></span> <span data-ttu-id="a29b1-189">Beachten Sie, dass Sie es aber nicht numerische Typen numerische Werte zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="a29b1-189">Note that you can assign numeric values to it but not numeric types.</span></span>  <br/> |
|<span data-ttu-id="a29b1-190">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a29b1-190">Data Type</span></span>  <br/> |<span data-ttu-id="a29b1-191">**LongLong**</span><span class="sxs-lookup"><span data-stu-id="a29b1-191">**LongLong**</span></span> <br/> |<span data-ttu-id="a29b1-192">Dies ist ein 8-Byte-Datentyp, der nur in 64-Bit-Versionen von Microsoft Office zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a29b1-192">This is an 8-byte data type which is available only in 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="a29b1-193">Sie können numerische Werte, aber nicht numerische Typen (so abgeschnitten) zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-193">You can assign numeric values but not numeric types (to avoid truncation).</span></span>  <br/> |
|<span data-ttu-id="a29b1-194">Konvertierungsoperator</span><span class="sxs-lookup"><span data-stu-id="a29b1-194">Conversion Operator</span></span>  <br/> |<span data-ttu-id="a29b1-195">**CLngPtr**</span><span class="sxs-lookup"><span data-stu-id="a29b1-195">**CLngPtr**</span></span> <br/> |<span data-ttu-id="a29b1-196">Konvertiert einen einfachen Ausdruck in einen **LongPtr**-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="a29b1-196">Converts a simple expression to a **LongPtr** data type.</span></span>  <br/> |
|<span data-ttu-id="a29b1-197">Konvertierungsoperator</span><span class="sxs-lookup"><span data-stu-id="a29b1-197">Conversion Operator</span></span>  <br/> |<span data-ttu-id="a29b1-198">**CLngLng**</span><span class="sxs-lookup"><span data-stu-id="a29b1-198">**CLngLng**</span></span> <br/> |<span data-ttu-id="a29b1-199">Konvertiert einen einfachen Ausdruck in einen **LongLong**-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="a29b1-199">Converts a simple expression to a **LongLong** data type.</span></span>  <br/> |
|<span data-ttu-id="a29b1-200">Funktion</span><span class="sxs-lookup"><span data-stu-id="a29b1-200">Function</span></span>  <br/> |<span data-ttu-id="a29b1-201">**VarPtr**</span><span class="sxs-lookup"><span data-stu-id="a29b1-201">**VarPtr**</span></span> <br/> |<span data-ttu-id="a29b1-p122">Variantenkonverter. Gibt auf 64-Bit-Versionen **LongPtr** und auf 32-Bit-Versionen **Long** (4 Bytes) zurück.</span><span class="sxs-lookup"><span data-stu-id="a29b1-p122">Variant converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="a29b1-204">Funktion</span><span class="sxs-lookup"><span data-stu-id="a29b1-204">Function</span></span>  <br/> |<span data-ttu-id="a29b1-205">**ObjPtr**</span><span class="sxs-lookup"><span data-stu-id="a29b1-205">**ObjPtr**</span></span> <br/> |<span data-ttu-id="a29b1-p123">Objektkonverter. Gibt auf 64-Bit-Versionen **LongPtr** und auf 32-Bit-Versionen **Long** (4 Bytes) zurück.</span><span class="sxs-lookup"><span data-stu-id="a29b1-p123">Object converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="a29b1-208">Funktion</span><span class="sxs-lookup"><span data-stu-id="a29b1-208">Function</span></span>  <br/> |<span data-ttu-id="a29b1-209">**StrPtr**</span><span class="sxs-lookup"><span data-stu-id="a29b1-209">**StrPtr**</span></span> <br/> |<span data-ttu-id="a29b1-p124">Zeichenfolgenkonverter. Gibt auf 64-Bit-Versionen **LongPtr** und auf 32-Bit-Versionen **Long** (4 Bytes) zurück.</span><span class="sxs-lookup"><span data-stu-id="a29b1-p124">String converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
   
<span data-ttu-id="a29b1-212">Im folgenden Beispiel ist die Verwendung einiger dieser Elemente in einer **Declare**-Anweisung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a29b1-212">The follow example shows how to use some of these items in a **Declare** statement.</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

<span data-ttu-id="a29b1-213">Beachten Sie, dass **Declare** -Anweisungen ohne das **PtrSafe** -Attribut als nicht kompatibel mit der 64-Bit-Version von Office werden.</span><span class="sxs-lookup"><span data-stu-id="a29b1-213">Note that **Declare** statements without the **PtrSafe** attribute are assumed not to be compatible with the 64-bit version of Office.</span></span> 
  
<span data-ttu-id="a29b1-214">Es gibt zwei Konstanten für die bedingte Kompilierung: **VBA7** und **Win64**.</span><span class="sxs-lookup"><span data-stu-id="a29b1-214">There are two conditional compilation constants: **VBA7** and **Win64**.</span></span> <span data-ttu-id="a29b1-215">Zum Sicherstellen der Abwärtskompatibilität mit früheren Versionen von Microsoft Office, verwenden Sie die **VBA7** -Konstante (Dies ist der normalen Groß-/Kleinschreibung) zu verhindern, dass 64-Bit-Code in der früheren Version von Office verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a29b1-215">To ensure backward compatibility with previous versions of Microsoft Office, you use the **VBA7** constant (this is the more typical case) to prevent 64-bit code from being used in the earlier version of Office.</span></span> <span data-ttu-id="a29b1-216">Code, für die unterscheidet sich zwischen der 32-Bit-Version und der 64-Bit-Version, wie das Aufrufen von ein Math-API, **LongLong** für die 64-Bit-Version verwendet, und **lange** für ihre 32-Bit-Version verwenden Sie die **Win64** -Konstante.</span><span class="sxs-lookup"><span data-stu-id="a29b1-216">For code that is different between the 32-bit version and the 64-bit version, such as calling a math API that uses **LongLong** for its 64-bit version and **Long** for its 32-bit version, you use the **Win64** constant.</span></span> <span data-ttu-id="a29b1-217">Der folgende Code zeigt die Verwendung der folgenden zwei-Konstanten.</span><span class="sxs-lookup"><span data-stu-id="a29b1-217">The following code shows the use of these two constants.</span></span> 
  
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

<span data-ttu-id="a29b1-218">Zusammengefasst, wenn Sie die 64-Bit-Code schreiben und in früheren Versionen von Office verwenden möchten, sollten Sie die Konstante **VBA7** bedingte Kompilierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="a29b1-218">To summarize, if you write 64-bit code and intend to use it in previous versions of Office, you will want to use the **VBA7** conditional compilation constant.</span></span> <span data-ttu-id="a29b1-219">Wenn Sie in Office 32-Bit-Code schreiben, funktioniert jedoch, dass Code in früheren Versionen von Office ohne die Notwendigkeit für die Kompilierungskonstante ist.</span><span class="sxs-lookup"><span data-stu-id="a29b1-219">However, if you write 32-bit code in Office, that code works as is in previous versions of Office without the need for the compilation constant.</span></span> <span data-ttu-id="a29b1-220">Wenn Sie sicherstellen möchten, dass Sie 32-Bit-Anweisungen für die 32-Bit-Versionen und 64-Bit-Anweisungen für 64-Bit-Versionen verwenden, ist die beste Option, verwenden Sie die bedingte Kompilierung **Win64** -Konstante.</span><span class="sxs-lookup"><span data-stu-id="a29b1-220">If you want to ensure that you are using 32-bit statements for 32-bit versions and 64-bit statements for 64-bit versions, your best option is to use the **Win64** conditional compilation constant.</span></span> 
  
## <a name="using-conditional-compilation-attributes"></a><span data-ttu-id="a29b1-221">Verwenden von bedingten kompilierungsattributen</span><span class="sxs-lookup"><span data-stu-id="a29b1-221">Using conditional compilation attributes</span></span>
<span data-ttu-id="a29b1-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span><span class="sxs-lookup"><span data-stu-id="a29b1-222"></span></span>

<span data-ttu-id="a29b1-223">Das folgende Beispiel zeigt die VBA-Code geschrieben für 32-Bit, die aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a29b1-223">The following example shows VBA code written for 32-bit that needs to be updated.</span></span> <span data-ttu-id="a29b1-224">Beachten Sie die Datentypen in der Vorversion Code, die aktualisiert werden, um **LongPtr** zu verwenden, da sie auf Handles oder Zeiger verweisen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-224">Notice the data types in the legacy code that are updated to use **LongPtr** because they refer to handles or pointers.</span></span> 
  
### <a name="vba-code-written-for-32-bit-versions"></a><span data-ttu-id="a29b1-225">VBA-Code geschrieben für 32-Bit-Versionen</span><span class="sxs-lookup"><span data-stu-id="a29b1-225">VBA code written for 32-bit versions</span></span>
  
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

### <a name="vba-code-rewritten-for-64-bit-versions"></a><span data-ttu-id="a29b1-226">VBA-Code umgeschrieben für 64-Bit-Versionen</span><span class="sxs-lookup"><span data-stu-id="a29b1-226">VBA code rewritten for 64-bit versions</span></span>
  
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

<span data-ttu-id="a29b1-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span><span class="sxs-lookup"><span data-stu-id="a29b1-227"></span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="a29b1-228">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="a29b1-228">Frequently asked questions</span></span>

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a><span data-ttu-id="a29b1-229">Wann sollte ich die 64-Bit-Version von Office verwenden?</span><span class="sxs-lookup"><span data-stu-id="a29b1-229">When should I use the 64-bit version of Office?</span></span>
  
<span data-ttu-id="a29b1-230">Dies ist mehr, die darum, welche hostanwendung (Excel, Word, usw.), die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="a29b1-230">This is more a matter of which host application (Excel, Word, and so forth) you are using.</span></span> <span data-ttu-id="a29b1-231">Excel ist beispielsweise viel größerer Arbeitsblätter mit der 64-Bit-Version von Microsoft Office zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a29b1-231">For example, Excel is able to handle much larger worksheets with the 64-bit version of Microsoft Office.</span></span>
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a><span data-ttu-id="a29b1-232">Kann ich die 64-Bit- und 32-Bit-Versionen von Office-Side-by-Side installieren?</span><span class="sxs-lookup"><span data-stu-id="a29b1-232">Can I install 64-bit and 32-bit versions of Office side-by-side?</span></span>
  
<span data-ttu-id="a29b1-233">Nein.</span><span class="sxs-lookup"><span data-stu-id="a29b1-233">No.</span></span>
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a><span data-ttu-id="a29b1-234">Wann sollte ich lange Parameter in LongPtr konvertieren?</span><span class="sxs-lookup"><span data-stu-id="a29b1-234">When should I convert Long parameters to LongPtr?</span></span>
  
<span data-ttu-id="a29b1-235">Sie müssen die Windows-API-Dokumentation auf der Microsoft Developers Network für die Funktion zu überprüfen, den Sie anrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="a29b1-235">You need to check the Windows API documentation on the Microsoft Developers Network for the function you want to call.</span></span> <span data-ttu-id="a29b1-236">Handles und Zeiger müssen in **LongPtr**konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a29b1-236">Handles and pointers need to be converted to **LongPtr**.</span></span> <span data-ttu-id="a29b1-237">Als Beispiel enthält die Dokumentation zu [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) die folgende Signatur:</span><span class="sxs-lookup"><span data-stu-id="a29b1-237">As an example, the documentation for [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) provides the following signature:</span></span> 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

<span data-ttu-id="a29b1-238">Der Parameter sind wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="a29b1-238">The parameters are defined as:</span></span>
  
|<span data-ttu-id="a29b1-239">Parameter</span><span class="sxs-lookup"><span data-stu-id="a29b1-239">Parameter</span></span>|<span data-ttu-id="a29b1-240">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a29b1-240">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="a29b1-241">hKey [in]</span><span class="sxs-lookup"><span data-stu-id="a29b1-241">hKey [in]</span></span>  <br/> |<span data-ttu-id="a29b1-242">Ein *behandeln* einen Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="a29b1-242">A  *handle*  to an open registry key.</span></span>  <br/> |
|<span data-ttu-id="a29b1-243">LpSubKey [in, optional]</span><span class="sxs-lookup"><span data-stu-id="a29b1-243">lpSubKey [in, optional]</span></span>  <br/> |<span data-ttu-id="a29b1-244">Der Name der dem Registrierungsunterschlüssel geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a29b1-244">The name of the registry subkey to be opened.</span></span>  <br/> |
|<span data-ttu-id="a29b1-245">ulOptions</span><span class="sxs-lookup"><span data-stu-id="a29b1-245">ulOptions</span></span>  <br/> |<span data-ttu-id="a29b1-246">Dieser Parameter ist reserviert und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a29b1-246">This parameter is reserved and must be zero.</span></span>  <br/> |
|<span data-ttu-id="a29b1-247">SamDesired [in]</span><span class="sxs-lookup"><span data-stu-id="a29b1-247">samDesired [in]</span></span>  <br/> |<span data-ttu-id="a29b1-248">Eine Maske, die die gewünschten Zugriffsrechte für den Schlüssel angibt.</span><span class="sxs-lookup"><span data-stu-id="a29b1-248">A mask that specifies the desired access rights to the key.</span></span>  <br/> |
|<span data-ttu-id="a29b1-249">PhkResult [Out]</span><span class="sxs-lookup"><span data-stu-id="a29b1-249">phkResult [out]</span></span>  <br/> |<span data-ttu-id="a29b1-250">Ein *Zeiger* auf eine Variable, die ein Handle für das geöffnete Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="a29b1-250">A  *pointer*  to a variable that receives a handle to the opened key.</span></span>  <br/> |
   
<span data-ttu-id="a29b1-251">In [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b)ist die **Declare** -Anweisung folgendermaßen definiert:</span><span class="sxs-lookup"><span data-stu-id="a29b1-251">In [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), the **Declare** statement is defined as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a><span data-ttu-id="a29b1-252">Werden Zeigern und Handles in Strukturen konvertiert?</span><span class="sxs-lookup"><span data-stu-id="a29b1-252">Should I convert pointers and handles in structures?</span></span>
  
<span data-ttu-id="a29b1-253">Ja.</span><span class="sxs-lookup"><span data-stu-id="a29b1-253">Yes.</span></span> <span data-ttu-id="a29b1-254">Finden Sie in des **MSG** -Typs in Win32API_PtrSafe.txt:</span><span class="sxs-lookup"><span data-stu-id="a29b1-254">See the **MSG** type in Win32API_PtrSafe.txt:</span></span> 
  
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

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a><span data-ttu-id="a29b1-255">Wann sollte ich Strptr, Varpt und Objptr verwenden?</span><span class="sxs-lookup"><span data-stu-id="a29b1-255">When should I use strptr, varpt, and objptr?</span></span>
  
<span data-ttu-id="a29b1-256">Sie sollten diese Funktionen verwenden, Zeiger auf Zeichenfolgen, Variablen und Objekte abrufen.</span><span class="sxs-lookup"><span data-stu-id="a29b1-256">You should use these functions to retrieve pointers to strings, variables and objects, respectively.</span></span> <span data-ttu-id="a29b1-257">Auf der 64-Bit-Version von Office zurückgegebenen diese Funktionen einer 64-Bit- **LongPtr**an **Declare** -Anweisungen übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a29b1-257">On the 64-bit version of Office, these functions will return a 64-bit **LongPtr**, which can be passed to **Declare** statements.</span></span> <span data-ttu-id="a29b1-258">Die Verwendung dieser Funktionen wurde aus früheren Versionen von VBA nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="a29b1-258">The use of these functions has not changed from previous versions of VBA.</span></span> <span data-ttu-id="a29b1-259">Der einzige Unterschied ist, dass sie jetzt eine **LongPtr**zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a29b1-259">The only difference is that they now return a **LongPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a29b1-260">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a29b1-260">See also</span></span>
<span data-ttu-id="a29b1-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="a29b1-261"></span></span>

- [<span data-ttu-id="a29b1-262">Anatomie einer Declare-Anweisung</span><span class="sxs-lookup"><span data-stu-id="a29b1-262">Anatomy of a Declare Statement</span></span>](https://msdn.microsoft.com/library/office/aa671659.aspx)
    

