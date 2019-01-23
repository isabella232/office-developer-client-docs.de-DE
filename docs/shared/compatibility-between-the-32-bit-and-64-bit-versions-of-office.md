---
title: Kompatibilität zwischen der 32-Bit- und der 64-Bit-Version von Office
ms.date: 04/27/2016
ms.audience: ITPro
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Hier finden Sie Informationen zur Kompatibilität zwischen der 32-Bit- und der 64-Bit-Version von Office.
localization_priority: Priority
ms.openlocfilehash: b03323b37b242c9992c47cd737ae54f3f9bbf2ca
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712015"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a><span data-ttu-id="fe64c-103">Kompatibilität zwischen der 32-Bit- und der 64-Bit-Version von Office</span><span class="sxs-lookup"><span data-stu-id="fe64c-103">Compatibility between the 32-bit and 64-bit versions of Office</span></span>

<span data-ttu-id="fe64c-104">Hier finden Sie Informationen zur Kompatibilität zwischen der 32-Bit- und der 64-Bit-Version von Office.</span><span class="sxs-lookup"><span data-stu-id="fe64c-104">Find out how the 32-bit version of Office is compatible with the 64-bit version of Office.</span></span>
  
<span data-ttu-id="fe64c-105">Office-Anwendungen stehen als 32-Bit- und 64-Bit-Version zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="fe64c-105">Office applications are available in 32-bit and 64-bit versions.</span></span> 
  
<span data-ttu-id="fe64c-106">Mit der 64-Bit-Version von Office können Sie mehr Daten für erweiterte Funktionen verschieben, zum Beispiel beim Arbeiten mit großen Zahlen in Microsoft Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="fe64c-106">The 64-bit versions of Office enable you to move more data around for increased capability, for example when you work with large numbers in Microsoft Excel 2010.</span></span> <span data-ttu-id="fe64c-107">Wenn Sie 32-Bit-Code schreiben, können Sie die 64-Bit-Version von Office verwenden, ohne daran Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-107">When writing 32-bit code, you can use the 64-bit version of Office without any changes.</span></span> <span data-ttu-id="fe64c-108">Wenn Sie 64-Bit-Code schreiben, sollten Sie jedoch sicherstellen, dass der Code bestimmte Schlüsselwörter und Konstanten für bedingte Kompilierung enthält, um sicherzustellen, dass der Code mit früheren Versionen von Office abwärtskompatibel ist, und, dass der richtige Code ausgeführt wird, wenn Sie 32-Bit- und 64-Bit-Code kombinieren.</span><span class="sxs-lookup"><span data-stu-id="fe64c-108">The addition of a 64-bit version of off14short lets you move more data around for increased capability. When writing 32-bit code, you can use the 64-bit version of officenv without any changes. However, when you write 64-bit code, you should ensure that your code contains specific keywords and conditional compilation constants to ensure that the code is backward compatible with earlier version of officenv, and that the correct code is being executed if you mix 32-bit and 64-bit code.</span></span>
  
<span data-ttu-id="fe64c-109">Visual Basic for Applications 7.0 (VBA-7) ist in 64-Bit-Versionen für Office veröffentlicht und kann sowohl mit 32-Bit- als auch 64-Bit-Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-109">Visual Basic for Applications 7.0 (VBA 7) is released in the 64-bit versions for Office, and it works with both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="fe64c-110">Die in diesem Artikel beschriebenen Änderungen gelten nur für 64-Bit-Versionen von Office.</span><span class="sxs-lookup"><span data-stu-id="fe64c-110">The changes described in this article apply only to the 64-bit versions of Office.</span></span> <span data-ttu-id="fe64c-111">Mit 32-Bit-Versionen von Microsoft Office können Sie die in früheren Versionen von Office integrierten Lösungen verwenden, ohne weitere Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-111">Using the 32-bit versions of Microsoft Office enable you to use solutions built in previous versions of Office without further modifications.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fe64c-112">Standardmäßig installieren Sie bei der Installation einer 64-Bit-Version von Office auch die 32-Bit-Version, wenn das 64-Bit-System verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe64c-112">By default, when you install a 64-bit version of Office, you also install the 32-bit version is installed along with the 64-bit system.</span></span> <span data-ttu-id="fe64c-113">Sie müssen explizit die Installationsoption für die 64-Bit-Version von Microsoft Office auswählen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-113">You must explicitly select the Microsoft Office 64-bit version installation option.</span></span> 
  
<span data-ttu-id="fe64c-114">In VBA 7 müssen Sie die vorhandenen Windows-API-Anweisungen (**Declare**-Anweisungen) aktualisieren, damit Sie mit der 64-Bit-Version verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fe64c-114">In VBA 7, you must update existing Windows API statements (**Declare** statements) to work with the 64-bit version.</span></span> <span data-ttu-id="fe64c-115">Darüber hinaus müssen Sie die Adresszeiger und Anzeigefensterhandles in benutzerdefinierten Typen aktualisieren, die von diesen Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-115">Additionally, you must update address pointers and display window handles in user-defined types that are used by these statements.</span></span> <span data-ttu-id="fe64c-116">Dies sowie Kompatibilitätsprobleme zwischen den 32-Bit- und 64-Bit-Versionen und die zugehörigen Lösungen werden genau in diesem Artikel erläutert.</span><span class="sxs-lookup"><span data-stu-id="fe64c-116">This is discussed in more detail in this article as well as compatibility issues between the 32-bit and 64-bit versions and suggested solutions.</span></span> 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a><span data-ttu-id="fe64c-117">Vergleich von 32-Bit- und 64-Bit-Systemen</span><span class="sxs-lookup"><span data-stu-id="fe64c-117">Comparing 32-bit and 64-bit systems</span></span>
<span data-ttu-id="fe64c-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span><span class="sxs-lookup"><span data-stu-id="fe64c-118"></span></span>

<span data-ttu-id="fe64c-119">Anwendungen, die mit 64-Bit-Versionen von Office erstellt wurden, können auf größere Adressräume als 32-Bit-Versionen verweisen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-119">Applications built with the 64-bit versions of Office can reference larger address spaces than 32-bit versions.</span></span> <span data-ttu-id="fe64c-120">Dies bedeutet, dass Sie mehr physischen Speicher für Daten als vorher verwenden können und so den potenziellen Mehraufwand für das Verschieben von Daten in und aus dem physischen Speicher reduzieren können.</span><span class="sxs-lookup"><span data-stu-id="fe64c-120">This means you can use more physical memory for data than before, potentially reducing the overhead spent moving data in and out of physical memory</span></span>
  
<span data-ttu-id="fe64c-121">Zusätzlich zu Verweisen auf bestimmte Stellen (als Zeiger bezeichnet) im physischen Speicher können Sie auch Adressen verwenden, um auf Anzeigefensterbezeichner (als Handles bezeichnet) zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-121">In addition to referring specific locations (known as pointers) in physical memory, you can also use addresses to reference display window identifiers (known as handles).</span></span> <span data-ttu-id="fe64c-122">Die Größe (in Byte) des Zeigers oder Handles hängt davon ab, ob Sie ein 32-Bit- oder 64-Bit-System verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-122">The size (in bytes) of the pointer or handle depends on whether you're using a 32-bit or 64-bit system.</span></span> 
  
<span data-ttu-id="fe64c-123">Wenn Sie Ihre vorhandenen Lösungen mit 64-Bit-Versionen von Office ausführen möchten, beachten Sie die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="fe64c-123">If you want to run your existing solutions with the 64-bit versions of Office, be aware of the following:</span></span>
  
- <span data-ttu-id="fe64c-124">Von systemeigenen 64-Bit-Prozessen in Office können keine 32-Bit-Binärdateien geladen werden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-124">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="fe64c-125">Dieses Problem tritt häufig auf, wenn bereits Microsoft ActiveX-Steuerelemente und Add-Ins vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fe64c-125">Native 64-bit processes in off14short cannot load 32-bit binaries. This is expected to be a common issue when you have existing Microsoft ActiveX controls and existing add-ins,</span></span>
    
- <span data-ttu-id="fe64c-126">VBA hatte zuvor keinen pointer-Datentyp, sodass Sie 32-Bit-Variablen zum Speichern von Zeigern und Handles verwenden mussten.</span><span class="sxs-lookup"><span data-stu-id="fe64c-126">VBA previously didn't have a pointer data type, so you had to use 32-bit variables to store pointers and handles.</span></span> <span data-ttu-id="fe64c-127">Mit diesen Variablen werden nun die von API-Aufrufen zurückgegebenen 64-Bit-Werte abgeschnitten, wenn Sie **Declare**-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-127">These variables now truncate 64-bit values returned by API calls when using **Declare** statements.</span></span> 
    
## <a name="vba-7-code-base"></a><span data-ttu-id="fe64c-128">VBA 7-Codebasis</span><span class="sxs-lookup"><span data-stu-id="fe64c-128">VBA 7 code base</span></span>
<span data-ttu-id="fe64c-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span><span class="sxs-lookup"><span data-stu-id="fe64c-129"></span></span>

<span data-ttu-id="fe64c-130">Die VBA-Codebasis in Office 2007 und früheren Versionen wird durch VBA 7 ersetzt.</span><span class="sxs-lookup"><span data-stu-id="fe64c-130">VBA 7 replaces the VBA code base in Office 2007 and earlier versions.</span></span> <span data-ttu-id="fe64c-131">VBA 7 ist sowohl in 32-Bit- als auch in 64-Bit-Versionen von Office verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe64c-131">VBA 7 is available in both the 32-bit and 64-bit versions of Office.</span></span> <span data-ttu-id="fe64c-132">Dies bietet zwei Konstanten für die bedingte Kompilierung:</span><span class="sxs-lookup"><span data-stu-id="fe64c-132">It provides two conditional compilation constants:</span></span> 
  
- <span data-ttu-id="fe64c-133">**VBA7** – Stellt Abwärtskompatibilität des Codes sicher, indem getestet wird, ob die Anwendung VBA 7 oder die ältere Version von VBA verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe64c-133">**VBA7** - Helps ensure the backward compatibility of your code by testing whether your application is using VBA 7 or the previous version of VBA.</span></span> 
    
- <span data-ttu-id="fe64c-134">**Win64** – Überprüft, ob der Code als 32-Bit- oder 64-Bit-Version ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe64c-134">**Win64** Tests whether code is running as 32-bit or 64-bit.</span></span> 
    
<span data-ttu-id="fe64c-135">Die Markos in einem Dokument, die in der 32-Bit-Version der Anwendung funktionieren, funktionieren, mit einigen Ausnahmen, auch in der 64-Bit-Version.</span><span class="sxs-lookup"><span data-stu-id="fe64c-135">With certain exceptions, the macros in a document that work in the 32-bit version of the application also work in the 64-bit version.</span></span>
  
## <a name="activex-control-and-com-add-in-compatibility"></a><span data-ttu-id="fe64c-136">Kompatibilität mit ActiveX-Steuerelementen und COM-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="fe64c-136">ActiveX Control and COM Add-in Compatibility</span></span>
<span data-ttu-id="fe64c-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="fe64c-137"></span></span>

<span data-ttu-id="fe64c-138">Vorhandene 32-Bit-ActiveX-Steuerelemente sind nicht mit 64-Bit-Versionen von Office kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fe64c-138">Existing 32-bit ActiveX controls, are not compatible with the 64-bit versions of Office.</span></span> <span data-ttu-id="fe64c-139">Für ActiveX-Steuerelemente und COM-Objekte:</span><span class="sxs-lookup"><span data-stu-id="fe64c-139">For ActiveX controls and COM objects:</span></span>
  
- <span data-ttu-id="fe64c-140">Wenn der Quellcode verfügbar ist, generieren Sie selbst eine 64-Bit-Version.</span><span class="sxs-lookup"><span data-stu-id="fe64c-140">If you have the source code, you can generate a 64-bit version yourself,</span></span>
- <span data-ttu-id="fe64c-141">Wenn Sie nicht über den Quellcode verfügen, wenden Sie sich an den Anbieter, um eine aktualisierte Version zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fe64c-141">If you don't have the source code, contact the vendor for an updated version.</span></span>
    
<span data-ttu-id="fe64c-142">Von systemeigenen 64-Bit-Prozessen in Office können keine 32-Bit-Binärdateien geladen werden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-142">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="fe64c-143">Dies umfasst die allgemeinen Steuerelemente von **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) und die Steuerelemente von **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span><span class="sxs-lookup"><span data-stu-id="fe64c-143">This includes the common controls of **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) and the controls of **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span></span> <span data-ttu-id="fe64c-144">Diese Steuerelemente wurden von 32-Bit-Office-Versionen von älteren Office-Versionen als Office 2010 installiert.</span><span class="sxs-lookup"><span data-stu-id="fe64c-144">These controls were installed by 32-bit versions of Office earlier than Office 2010.</span></span> <span data-ttu-id="fe64c-145">Sie müssen eine Alternative für Ihre vorhandenen VBA-Lösungen finden, die diese Steuerelemente verwenden, wenn Sie den Code zu 64-Bit-Versionen von Office migrieren.</span><span class="sxs-lookup"><span data-stu-id="fe64c-145">You'll need to find an alternative for your existing VBA solutions that use these controls when you migrate the code to the 64-bit versions of Office.</span></span> 
  
## <a name="api-compatibility"></a><span data-ttu-id="fe64c-146">API-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="fe64c-146">API Compatibility</span></span>
<span data-ttu-id="fe64c-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="fe64c-147"></span></span>

<span data-ttu-id="fe64c-148">Die Kombination von VBA und Typbibliotheken bietet viele Funktionen zum Erstellen von Office-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-148">The combination of VBA and type libraries gives you lots of functionality to create Office applications.</span></span> <span data-ttu-id="fe64c-149">Manchmal müssen Sie allerdings direkt mit dem Betriebssystem des Computers und andere Komponenten kommunizieren, zum Beispiel wenn Sie Arbeitsspeicher oder Prozesse verwalten, bei der Arbeit mit Benutzeroberflächenelementen wie Fenster und Steuerelemente oder beim Ändern der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fe64c-149">However, sometimes you must communicate directly with the computer's operating system and other components, such as when you manage memory or processes, when working with UI elements linke windows and controls, or when modifying the Windows registry.</span></span> <span data-ttu-id="fe64c-150">In den folgenden Szenarien wird empfohlen, eine der in DLL-Dateien eingebetteten externen Funktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-150">In these scenarios, your best option is to use one of the external functions that are embedded in DLL files.</span></span> <span data-ttu-id="fe64c-151">Dies können Sie in VBA erledigen, indem Sie API-Aufrufe mithilfe von **Declare**-Anweisungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-151">You do this in VBA by making API calls using **Declare** statements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fe64c-152">Microsoft bietet eine Datei „Win32API.txt“ mit 1.500 Declare-Anweisungen und ein Tool zum Kopieren von **Declare**-Anweisungen in Code.</span><span class="sxs-lookup"><span data-stu-id="fe64c-152">Microsoft provides a Win32API.txt file that contains 1,500 Declare statements and a tool to copy the **Declare** statement that you want into your code.</span></span> <span data-ttu-id="fe64c-153">Diese Anweisungen sind jedoch für 32-Bit-Systeme vorgesehen und müssen anhand der später in diesem Artikel erläuterten Informationen in 64 Bit konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-153">However, these statements are for 32-bit systems and must be converted to 64-bit by using the information discussed later in this article.</span></span> <span data-ttu-id="fe64c-154">Vorhandene **Declare**-Anweisungen werden erst in der 64-Bit-Version von VBA kompiliert, wenn Sie mit dem **PtrSafe**-Attribut als sicher für die 64-Bit-Version gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="fe64c-154">Existing **Declare** statements won't compile in 64-bit VBA until they've been marked as safe for 64-bit by using the **PtrSafe** attribute.</span></span> <span data-ttu-id="fe64c-155">Beispiele für diesen Typ der Konvertierung finden Sie auf der Website des Excel-MVPs Jan Karel Pieterse unter [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span><span class="sxs-lookup"><span data-stu-id="fe64c-155">You can find examples of this type of conversion at Excel MVP Jan Karel Pieterse's website at [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span></span> <span data-ttu-id="fe64c-156">Das [Benutzerhandbuch zum Office Code Compatibility Inspector](https://technet.microsoft.com/de-DE/library/ee833946%28office.14%29.aspx) ist hilfreich, wenn es darum geht, die Syntax der **Declare**-Anweisungen der API für das **PtrSafe**-Attribut und die entsprechenden Rückgabetypen zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-156">The [Office Code Compatibility Inspector user's guide](https://technet.microsoft.com/de-DE/library/ee833946%28office.14%29.aspx) is a useful tool to inspect the syntax of API **Declare** statements for the **PtrSafe** attribute, if needed, and the appropriate return type.</span></span> 
  
<span data-ttu-id="fe64c-157">**Declare**-Anweisungen ähneln folgendem Code, je nachdem, ob Sie eine Unterroutine (kein Rückgabewert) oder eine Funktion (mit Rückgabewert) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-157">**Declare** statements resemble one of the following, depending whether you are calling a subroutine (which has no return value) or a function (which does have a return value).</span></span> 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

<span data-ttu-id="fe64c-158">Die **SubName**-Funktion oder **FunctionName**-Funktion wird durch den tatsächlichen Namen der Prozedur in der DLL-Datei ersetzt und steht für den Namen, der verwendet wird, wenn die Prozedur über VBA-Code aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fe64c-158">The **SubName** function or **FunctionName** function is replaced by the actual name of the procedure in the DLL file and represents the name that is used when the procedure is called from VBA code.</span></span> <span data-ttu-id="fe64c-159">Sie können auch ein **AliasName**-Argument für den Namen der Prozedur angeben.</span><span class="sxs-lookup"><span data-stu-id="fe64c-159">You can also specify an **AliasName** argument for the name of the procedure.</span></span> <span data-ttu-id="fe64c-160">Der Name der DLL-Datei, die die aufgerufene Prozedur enthält, folgt dem **Lib**-Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="fe64c-160">The name of the DLL file that contains the procedure being called follows the **Lib** keyword.</span></span> <span data-ttu-id="fe64c-161">Die Argumentlist enthält schließlich die Parameter und die Datentypen, die an die Prozedur übergeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-161">And finally, the argument list contains the parameters and the data types that must be passed to the procedure.</span></span> 
  
<span data-ttu-id="fe64c-162">Mit der folgenden **Declare**-Anweisung wird ein *Unterschlüssel* in der Windows-Registrierung geöffnet und der Wert ersetzt.</span><span class="sxs-lookup"><span data-stu-id="fe64c-162">The following **Declare** statement opens a *subkey* in the Windows registry and replaces its value.</span></span> 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

<span data-ttu-id="fe64c-163">Der Eintrag „Windows.h (Fensterhandle)“ für die **RegOpenKeyA**-Funktion lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fe64c-163">The Windows.h (window handle) entry for the **RegOpenKeyA** function is as follows:</span></span> 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

<span data-ttu-id="fe64c-164">In Visual C und Microsoft Visual C++ wird das vorherige Beispiel korrekt für 32-Bit- und 64-Bit-Versionen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="fe64c-164">In Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit.</span></span> <span data-ttu-id="fe64c-165">Dies liegt daran, dass HKEY als Zeiger definiert ist, dessen Größe der Speichergröße der Plattform entspricht, in der der Code kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="fe64c-165">In Microsoft Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit. This is because HKEY is defined as a pointer, whose size reflects the memory size of the platform that the code is compiled in.</span></span>
  
<span data-ttu-id="fe64c-166">In älteren Versionen von VBA gab es keinen bestimmten pointer-Datentyp, sodass der Datentyp **Long** verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fe64c-166">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used.</span></span> <span data-ttu-id="fe64c-167">Da der **Long**-Datentyp immer 32 Bit aufweist, wird dieser bei Verwendung auf einem System mit 64-Bit-Arbeitsspeicher gebrochen, weil die oberen 32 Bit möglicherweise abgeschnitten oder andere Arbeitsspeicheradressen überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-167">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used. And because the Long data type is always 32-bits, this breaks when used on a system with 64-bit memory because the upper 32-bits may be truncated or may overwrite other memory addresses.  Either of these situations can result in unpredictable behavior or system crashes.</span></span> <span data-ttu-id="fe64c-168">Eine dieser Situationen können zum unvorhersehbaren Verhalten oder zu Systemabstürzen führen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-168">Either of these situations can result in unpredictable behavior or system crashes.</span></span> 
  
<span data-ttu-id="fe64c-169">Um dieses Problem zu beheben, enthält VBA einen wahren *pointer*-Datentyp: **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="fe64c-169">To resolve this, VBA includes a true  *pointer*  data type: **LongPtr**.</span></span> <span data-ttu-id="fe64c-170">Mit diesem neuen Datentyp können Sie die ursprüngliche **Declare**-Anweisung korrekt schreiben als:</span><span class="sxs-lookup"><span data-stu-id="fe64c-170">To resolve this, VBA now contains a true pointer data type: **LongPtr**. This new data type enables you to write the original Declare statement correctly as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

<span data-ttu-id="fe64c-171">Mit diesem Datentyp und dem neuen **PtrSafe**-Attribut können Sie diese **Declare**-Anweisung sowohl auf 32-Bit- oder 64-Bit-Systemen verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-171">This data type and the new **PtrSafe** attribute enable you to use this **Declare** statement on either 32-bit or 64-bit systems.</span></span> <span data-ttu-id="fe64c-172">Das **PtrSafe**-Attribut gibt dem VBA-Compiler an, die die **Declare**-Anweisung auf die 64-Bit-Version von Office abzielt.</span><span class="sxs-lookup"><span data-stu-id="fe64c-172">The **PtrSafe** attribute indicates to the VBA compiler that the **Declare** statement is targeted for the 64-bit version of Office.</span></span> <span data-ttu-id="fe64c-173">Ohne dieses Attribut tritt beim Verwenden der **Declare**-Anweisung in einem 64-Bit-System ein Kompilierungszeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="fe64c-173">Without this attribute, using the **Declare** statement in a 64-bit system will result in a compile-time error.</span></span> <span data-ttu-id="fe64c-174">Das **PtrSafe**-Attribut ist bei der 32-Bit-Version von Office optional.</span><span class="sxs-lookup"><span data-stu-id="fe64c-174">The **PtrSafe** attribute is optional on the 32-bit version of Office.</span></span> <span data-ttu-id="fe64c-175">Dadurch funktionieren vorhandene **Declare**-Anweisungen wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="fe64c-175">This enables existing **Declare** statements to work as they always have.</span></span> 
  
<span data-ttu-id="fe64c-176">Die folgende Tabelle enthält weitere Informationen zum neuen Qualifizierer und Datentyp sowie zu einem weiteren Datentyp, zwei Konvertierungsoperatoren und drei Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-176">The following table provides more information on the new qualifier and data type already discussed as well as another data type, two conversion operators, and three functions.</span></span>
  
|<span data-ttu-id="fe64c-177">Typ</span><span class="sxs-lookup"><span data-stu-id="fe64c-177">Type</span></span>|<span data-ttu-id="fe64c-178">Element</span><span class="sxs-lookup"><span data-stu-id="fe64c-178">Item</span></span>|<span data-ttu-id="fe64c-179">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe64c-179">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fe64c-180">Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="fe64c-180">Qualifier</span></span>  <br/> |<span data-ttu-id="fe64c-181">**PtrSafe**</span><span class="sxs-lookup"><span data-stu-id="fe64c-181">**PtrSafe**</span></span> <br/> |<span data-ttu-id="fe64c-p119">Gibt an, dass die **Declare**-Anweisung mit der 64-Bit-Version kompatibel ist. Dieses Attribut ist auf 64-Bit-Systemen erforderlich.  </span><span class="sxs-lookup"><span data-stu-id="fe64c-p119">Indicates that the **Declare** statement is compatible with 64-bits. This attribute is mandatory on 64-bit systems.  </span></span><br/> |
|<span data-ttu-id="fe64c-184">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fe64c-184">Data Type</span></span>  <br/> |<span data-ttu-id="fe64c-185">**LongPtr**</span><span class="sxs-lookup"><span data-stu-id="fe64c-185">**LongPtr**</span></span> <br/> |<span data-ttu-id="fe64c-186">Ein Datentyp der Variablen, bei dem es sich um einen 4-Byte-Datentyp auf 32-Bit-Versionen und um einen 8-Byte-Datentyp auf 64-Bit-Versionen von Microsoft Office handelt.</span><span class="sxs-lookup"><span data-stu-id="fe64c-186">A variable data type which is a 4-bytes data type on 32-bit versions and an 8-byte data type on 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="fe64c-187">Dies ist die empfohlene Methode zum Deklarieren eines Zeigers oder eines Handles für neuen Code sowie für älteren Code, wenn er in der 64-Bit-Version von Office ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="fe64c-187">This is the recommended way of declaring a pointer or a handle for new code but also for legacy code if it has to run in the 64-bit version of Office.</span></span> <span data-ttu-id="fe64c-188">Er wird nur in der VBA 7-Laufzeit bei 32-Bit- und 64-Bit-Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe64c-188">It is only supported in the VBA 7 runtime on 32-bit and 64-bit.</span></span> <span data-ttu-id="fe64c-189">Beachten Sie, dass Sie diesem Datentyp numerische Werte, jedoch keine numerischen Typen zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="fe64c-189">Note that you can assign numeric values to it but not numeric types.</span></span>  <br/> |
|<span data-ttu-id="fe64c-190">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fe64c-190">Data Type</span></span>  <br/> |<span data-ttu-id="fe64c-191">**LongLong**</span><span class="sxs-lookup"><span data-stu-id="fe64c-191">**LongLong**</span></span> <br/> |<span data-ttu-id="fe64c-192">Dies ist ein 8-Byte-Datentyp, der nur in 64-Bit-Versionen von Microsoft Office verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fe64c-192">This is an 8-byte data type which is available only in 64-bit versions of off14short. You can assign numeric values but not numeric types (to avoid truncation).</span></span> <span data-ttu-id="fe64c-193">Sie können numerische Werte, jedoch keine numerischen Typen zuweisen (um Kürzungen zu vermeiden).</span><span class="sxs-lookup"><span data-stu-id="fe64c-193">This is an 8-byte data type which is available only in 64-bit versions of off14short. You can assign numeric values but not numeric types (to avoid truncation).</span></span>  <br/> |
|<span data-ttu-id="fe64c-194">Operator für die Konvertierung</span><span class="sxs-lookup"><span data-stu-id="fe64c-194">Conversion Operator</span></span>  <br/> |<span data-ttu-id="fe64c-195">**CLngPtr**</span><span class="sxs-lookup"><span data-stu-id="fe64c-195">**CLngPtr**</span></span> <br/> |<span data-ttu-id="fe64c-196">Konvertiert einen einfachen Ausdruck in einen **LongPtr**-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="fe64c-196">Converts a simple expression to a **LongPtr** data type.</span></span>  <br/> |
|<span data-ttu-id="fe64c-197">Operator für die Konvertierung</span><span class="sxs-lookup"><span data-stu-id="fe64c-197">Conversion Operator</span></span>  <br/> |<span data-ttu-id="fe64c-198">**CLngLng**</span><span class="sxs-lookup"><span data-stu-id="fe64c-198">**CLngLng**</span></span> <br/> |<span data-ttu-id="fe64c-199">Konvertiert einen einfachen Ausdruck in einen **LongLong**-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="fe64c-199">Converts a simple expression to a **LongLong** data type.</span></span>  <br/> |
|<span data-ttu-id="fe64c-200">Funktion</span><span class="sxs-lookup"><span data-stu-id="fe64c-200">Function</span></span>  <br/> |<span data-ttu-id="fe64c-201">**VarPtr**</span><span class="sxs-lookup"><span data-stu-id="fe64c-201">**VarPtr**</span></span> <br/> |<span data-ttu-id="fe64c-p122">Variantkonverter. Gibt einen **LongPtr**-Datentyp auf 64-Bit-Versionen zurück und einen **Long**-Datentyp auf 32-Bit-Versionen (4 Byte) zurück. </span><span class="sxs-lookup"><span data-stu-id="fe64c-p122">Variant converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="fe64c-204">Funktion</span><span class="sxs-lookup"><span data-stu-id="fe64c-204">Function</span></span>  <br/> |<span data-ttu-id="fe64c-205">**ObjPtr**</span><span class="sxs-lookup"><span data-stu-id="fe64c-205">**ObjPtr**</span></span> <br/> |<span data-ttu-id="fe64c-p123">Objektkonverter. Gibt einen **LongPtr**-Datentyp auf 64-Bit-Versionen zurück und einen **Long**-Datentyp auf 32-Bit-Versionen (4 Byte) zurück. </span><span class="sxs-lookup"><span data-stu-id="fe64c-p123">Object converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="fe64c-208">Funktion</span><span class="sxs-lookup"><span data-stu-id="fe64c-208">Function</span></span>  <br/> |<span data-ttu-id="fe64c-209">**StrPtr**</span><span class="sxs-lookup"><span data-stu-id="fe64c-209">**StrPtr**</span></span> <br/> |<span data-ttu-id="fe64c-p124">Zeichenfolgenkonverter. Gibt einen **LongPtr**-Datentyp auf 64-Bit-Versionen zurück und einen **Long**-Datentyp auf 32-Bit-Versionen (4 Byte) zurück. </span><span class="sxs-lookup"><span data-stu-id="fe64c-p124">String converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
   
<span data-ttu-id="fe64c-212">Im folgenden Beispiel wird gezeigt, wie Sie einige dieser Elemente in einer **Declare**-Anweisung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="fe64c-212">The follow example shows how to use some of these items in a **Declare** statement.</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

<span data-ttu-id="fe64c-213">Beachten Sie, dass **Declare**-Anweisungen ohne das **PtrSafe**-Attribut im Allgemeinen nicht mit der 64-Bit-Version von Office kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="fe64c-213">Note that Declare statements without the PtrSafe attribute are assumed not to be compatible with the 64-bit version of off14short.</span></span> 
  
<span data-ttu-id="fe64c-214">Es gibt zwei Konstanten für die bedingte Kompilierung: **VBA7** und **Win64**.</span><span class="sxs-lookup"><span data-stu-id="fe64c-214">There are two conditional compilation constants: **VBA7** and **Win64**.</span></span> <span data-ttu-id="fe64c-215">Um Abwärtskompatibilität mit älteren Versionen von Microsoft Office sicherzustellen, verwenden Sie die **VBA7**-Konstante (Dies ist der häufigere Fall), damit 64-Bit-Code nicht in älteren Versionen von Office verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe64c-215">To ensure backward compatibility with previous versions of Microsoft Office, you use the **VBA7** constant (this is the more typical case) to prevent 64-bit code from being used in the earlier version of Office.</span></span> <span data-ttu-id="fe64c-216">Bei Code, der zwischen der 32-Bit- und der 64-Bit-Version variiert, zum Beispiel beim Aufrufen einer Mathematik-API, die einen **LongLong**-Datentyp für die 64-Bit-Version und einen **Long**-Datentyp für die 32-Bit-Version verwendet, müssen Sie die **Win64**-Konstante verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-216">For code that is different between the 32-bit version and the 64-bit version, such as calling a math API that uses **LongLong** for its 64-bit version and **Long** for its 32-bit version, you use the **Win64** constant.</span></span> <span data-ttu-id="fe64c-217">Der folgende Code zeigt die Verwendung dieser beiden Konstanten.</span><span class="sxs-lookup"><span data-stu-id="fe64c-217">The following code shows the use of these two constants.</span></span> 
  
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

<span data-ttu-id="fe64c-218">Zusammenfassung: Wenn Sie 64-Bit-Code schreiben und dieser in älteren Versionen von Office verwendet werden soll, sollten Sie die **VBA7**-Konstante für die bedingte Kompilierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-218">To summarize, if you write 64-bit code and intend to use it in previous versions of Office, you will want to use the **VBA7** conditional compilation constant.</span></span> <span data-ttu-id="fe64c-219">Wenn Sie jedoch 32-Bit-Code in Office schreiben, kann dieser Code in älteren Versionen von Office verwendet werden, ohne dass Sie Änderungen vornehmen und ohne dass die Konstante für bedingte Kompilierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fe64c-219">However, if you write 32-bit code in Office, that code works as is in previous versions of Office without the need for the compilation constant.</span></span> <span data-ttu-id="fe64c-220">Wenn Sie sicherstellen möchten, dass Sie 32-Bit-Anweisungen für 32-Bit-Versionen und 64-Bit-Anweisungen für 64-Bit-Versionen verwenden, wird empfohlen, die **Win64**-Konstante für die bedingte Kompilierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-220">If you want to ensure that you are using 32-bit statements for 32-bit versions and 64-bit statements for 64-bit versions, your best option is to use the **Win64** conditional compilation constant.</span></span> 
  
## <a name="using-conditional-compilation-attributes"></a><span data-ttu-id="fe64c-221">Verwenden von bedingten Kompilierungsattributen</span><span class="sxs-lookup"><span data-stu-id="fe64c-221">Using Conditional Compilation Attributes</span></span>
<span data-ttu-id="fe64c-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span><span class="sxs-lookup"><span data-stu-id="fe64c-222"></span></span>

<span data-ttu-id="fe64c-223">Das folgende Beispiel zeigt für 32-Bit-Versionen geschriebenen VBA-Code, der aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="fe64c-223">The following example shows VBA code written for 32-bit that needs to be updated.</span></span> <span data-ttu-id="fe64c-224">Beachten Sie die Datentypen im älteren Code, die für die Verwendung von **LongPtr** aktualisiert werden, da sie auf Handles oder Zeiger verweisen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-224">The following code is an example of legacy VBA code that needs to be updated. Notice the data types in the legacy code that are updated to use **LongPtr** because they refer to handles or pointers</span></span> 
  
### <a name="vba-code-written-for-32-bit-versions"></a><span data-ttu-id="fe64c-225">Für 32-Bit-Versionen geschriebener VBA-Code</span><span class="sxs-lookup"><span data-stu-id="fe64c-225">VBA code written for 32-bit versions</span></span>
  
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

### <a name="vba-code-rewritten-for-64-bit-versions"></a><span data-ttu-id="fe64c-226">Für 64-Bit-Versionen neu geschriebener VBA-Code</span><span class="sxs-lookup"><span data-stu-id="fe64c-226">VBA code rewritten for 64-bit versions</span></span>
  
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

<span data-ttu-id="fe64c-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span><span class="sxs-lookup"><span data-stu-id="fe64c-227"></span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="fe64c-228">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="fe64c-228">Frequently asked questions</span></span>

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a><span data-ttu-id="fe64c-229">Wann sollte ich die 64-Bit-Version von Office verwenden?</span><span class="sxs-lookup"><span data-stu-id="fe64c-229">When should I use the 64-bit version of Office?</span></span>
  
<span data-ttu-id="fe64c-230">Dies ist eher eine Frage der Hostanwendung (Excel, Word usw.), die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-230">This is more a matter of which host application (Excel, Word, and so forth) you are using.</span></span> <span data-ttu-id="fe64c-231">Excel kann zum Beispiel viel größere Arbeitsblätter in der 64-Bit-Version von Microsoft Office verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fe64c-231">For example, Excel is able to handle much larger worksheets with the 64-bit version of Microsoft Office.</span></span>
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a><span data-ttu-id="fe64c-232">Kann ich sowohl die 64-Bit- als auch die 32-Bit-Version von Office gleichzeitig installieren?</span><span class="sxs-lookup"><span data-stu-id="fe64c-232">Can I install 64-bit and 32-bit versions of Office side-by-side?</span></span>
  
<span data-ttu-id="fe64c-233">Nein.</span><span class="sxs-lookup"><span data-stu-id="fe64c-233">No.</span></span>
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a><span data-ttu-id="fe64c-234">Wann sollte ich Long-Parameter in LongPtr-Parameter konvertieren?</span><span class="sxs-lookup"><span data-stu-id="fe64c-234">When should I convert Long parameters to LongPtr?</span></span>
  
<span data-ttu-id="fe64c-235">Lesen Sie hierzu die entsprechenden Informationen zu der Funktion, die Sie aufrufen möchten, in der Windows-API-Dokumentation im MSDN.</span><span class="sxs-lookup"><span data-stu-id="fe64c-235">You need to check the Windows API documentation on the Microsoft Developers Network for the function you want to call.</span></span> <span data-ttu-id="fe64c-236">Handles und Zeiger müssen in **LongPtr**-Datentypen konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="fe64c-236">Handles and pointers need to be converted to **LongPtr**.</span></span> <span data-ttu-id="fe64c-237">Die Dokumentation für [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) bietet zum Beispiel die folgende Signatur:</span><span class="sxs-lookup"><span data-stu-id="fe64c-237">As an example, the documentation for [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) provides the following signature:</span></span> 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

<span data-ttu-id="fe64c-238">Die Parameter sind wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="fe64c-238">The placeholders are defined as follows:</span></span>
  
|<span data-ttu-id="fe64c-239">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe64c-239">Parameter</span></span>|<span data-ttu-id="fe64c-240">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe64c-240">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe64c-241">hKey [in]</span><span class="sxs-lookup"><span data-stu-id="fe64c-241">hKey [in]</span></span>  <br/> |<span data-ttu-id="fe64c-242">Ein *Handle* zu einem geöffneten Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="fe64c-242">A  *handle*  to an open registry key.</span></span>  <br/> |
|<span data-ttu-id="fe64c-243">lpSubKey [in, optional]</span><span class="sxs-lookup"><span data-stu-id="fe64c-243">lpSubKey [in, optional]</span></span>  <br/> |<span data-ttu-id="fe64c-244">Der Name des Registrierungsunterschlüssels, der geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe64c-244">The name of the registry subkey to be opened.</span></span>  <br/> |
|<span data-ttu-id="fe64c-245">ulOptions</span><span class="sxs-lookup"><span data-stu-id="fe64c-245">ulOptions</span></span>  <br/> |<span data-ttu-id="fe64c-246">Dieser Parameter ist reserviert und muss 0 lauten.</span><span class="sxs-lookup"><span data-stu-id="fe64c-246">This parameter is reserved and must be zero.</span></span>  <br/> |
|<span data-ttu-id="fe64c-247">samDesired [in]</span><span class="sxs-lookup"><span data-stu-id="fe64c-247">samDesired [in]</span></span>  <br/> |<span data-ttu-id="fe64c-248">Eine Maske, die die gewünschten Zugriffsrechte für den Schlüssel angibt.</span><span class="sxs-lookup"><span data-stu-id="fe64c-248">A mask that specifies the desired access rights to the key.</span></span>  <br/> |
|<span data-ttu-id="fe64c-249">phkResult [out]</span><span class="sxs-lookup"><span data-stu-id="fe64c-249">phkResult [out]</span></span>  <br/> |<span data-ttu-id="fe64c-250">Ein *Zeiger* auf eine Variable, die ein Handle zum geöffneten Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="fe64c-250">A  *pointer*  to a variable that receives a handle to the opened key.</span></span>  <br/> |
   
<span data-ttu-id="fe64c-251">In der Datei [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b) wird die **Declare**-Anweisung wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="fe64c-251">In [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), the **Declare** statement is defined as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a><span data-ttu-id="fe64c-252">Muss ich Zeiger und Handles in Strukturen konvertieren?</span><span class="sxs-lookup"><span data-stu-id="fe64c-252">Should I convert pointers and handles in structures?</span></span>
  
<span data-ttu-id="fe64c-253">Ja.</span><span class="sxs-lookup"><span data-stu-id="fe64c-253">Yes.</span></span> <span data-ttu-id="fe64c-254">Informationen dazu finden Sie in der Datei „Win32API_PtrSafe.txt“ unter **MSG**-Typ:</span><span class="sxs-lookup"><span data-stu-id="fe64c-254">See the **MSG** type in Win32API_PtrSafe.txt:</span></span> 
  
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

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a><span data-ttu-id="fe64c-255">Wann sollte ich strptr, varpt und objptr verwenden?</span><span class="sxs-lookup"><span data-stu-id="fe64c-255">When should I use strptr, varpt, and objptr?</span></span>
  
<span data-ttu-id="fe64c-256">Sie sollten diese Funktionen verwenden, um Zeiger auf Zeichenfolgen, Variablen und Objekte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fe64c-256">You should use these functions to retrieve pointers to strings, variables and objects, respectively.</span></span> <span data-ttu-id="fe64c-257">In der 64-Bit-Version von Office geben diese Funktionen den 64-Bit-Datentyp **LongPtr**, der an die **Declare**-Anweisungen übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe64c-257">On the 64-bit version of Office, these functions will return a 64-bit **LongPtr**, which can be passed to **Declare** statements.</span></span> <span data-ttu-id="fe64c-258">Die Verwendung dieser Funktionen hat sich seit den älteren Versionen von VBA nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="fe64c-258">The use of these functions has not changed from previous versions of VBA.</span></span> <span data-ttu-id="fe64c-259">Der einzige Unterschied besteht darin, dass sie jetzt einen **LongPtr**-Datentyp zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fe64c-259">The only difference is that they now return a **LongPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe64c-260">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe64c-260">See also</span></span>
<span data-ttu-id="fe64c-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="fe64c-261"></span></span>

- [<span data-ttu-id="fe64c-262">Aufbau einer Declare-Anweisung</span><span class="sxs-lookup"><span data-stu-id="fe64c-262">Anatomy of a Declare Statement</span></span>](https://msdn.microsoft.com/library/office/aa671659.aspx)
    

