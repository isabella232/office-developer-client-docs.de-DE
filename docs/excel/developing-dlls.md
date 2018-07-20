---
title: Entwickeln von DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dlls [excel 2007], creating,creating DLLs [Excel 2007]
localization_priority: Normal
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030cdd4358d9a71841eca6acfcef6e71839e02a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790415"
---
# <a name="developing-dlls"></a><span data-ttu-id="3d82d-104">Entwickeln von DLLs</span><span class="sxs-lookup"><span data-stu-id="3d82d-104">Developing DLLs</span></span>

<span data-ttu-id="3d82d-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3d82d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3d82d-p101">Eine Bibliothek ist ein Textkörper aus kompiliertem Code, der einige Funktionen sowie die Daten für eine ausführbare Anwendung bereitstellt. Bibliotheken können entweder statisch verknüpft oder dynamisch verknüpft sein, und sie weisen in der Regel die Dateinamenerweiterung LIB bzw. DLL auf. Statische Bibliotheken (z. B. die C-Laufzeitbibliothek) werden bei der Kompilierung mit der Anwendung verknüpft und werden so Teil der resultierenden ausführbaren Datei. Die Anwendung lädt eine DLL, wenn diese benötigt wird, in der Regel beim Start der Anwendung. Eine DLL-Datei kann eine weitere DLL laden und dynamisch mit dieser verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p101">A library is a body of compiled code that provides some functionality and data to an executable application. Libraries can be either statically linked or dynamically linked, and they conventionally have the file name extensions .lib and .dll respectively. Static libraries (such as the C run-time library) are linked to the application at compilation and so become part of the resulting executable. The application loads a DLL when it is needed, usually when the application starts up. One DLL can load and dynamically link to another DLL.</span></span>
  
## <a name="benefits-of-using-dlls"></a><span data-ttu-id="3d82d-111">Vorteile der Verwendung von DLLs</span><span class="sxs-lookup"><span data-stu-id="3d82d-111">Benefits of using DLLs</span></span>

<span data-ttu-id="3d82d-112">Die Hauptvorteile von DLL-Dateien sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3d82d-112">The main benefits of DLLs are as follows:</span></span>
  
- <span data-ttu-id="3d82d-113">Alle Anwendungen können ein einzelnes Dokument auf der Festplatte gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d82d-113">All applications can share a single copy on disk.</span></span>
    
- <span data-ttu-id="3d82d-114">Die ausführbaren Dateien von Anwendungen sind kleiner.</span><span class="sxs-lookup"><span data-stu-id="3d82d-114">Applications' executable files are kept smaller.</span></span>
    
- <span data-ttu-id="3d82d-p102">Gro�e Entwicklungsprojekte können aufgeteilt werden. Anwendungs- und die DLL-Entwickler müssen sich nur auf eine Schnittstelle zwischen ihren jeweiligen Teilen einigen. Diese Schnittstelle wird von der DLL exportiert.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p102">They enable large development projects to be broken down. Application and DLL developers only need agree an interface between their respective parts. This interface is exported by the DLL.</span></span>
    
- <span data-ttu-id="3d82d-118">DLL-Entwickler können DLLs aktualisieren � vielleicht, um sie effizienter zu gestalten oder um einen Fehler zu beheben � ohne, dass alle Anwendungen, die diese verwenden, aktualisiert werden müssen, vorausgesetzt, die exportierte Schnittstelle der DLL �ndert sich nicht.</span><span class="sxs-lookup"><span data-stu-id="3d82d-118">DLL developers can update DLLs—perhaps to make them more efficient or to fix a bug—without having to update all the applications that use it, provided that the exported interface of the DLL does not change.</span></span>
    
<span data-ttu-id="3d82d-119">Sie können DLLs verwenden, um Arbeitsblattfunktionen und Befehle in Microsoft Excel hinzuzuf�gen.</span><span class="sxs-lookup"><span data-stu-id="3d82d-119">You can use DLLs to add worksheet functions and commands in Microsoft Excel.</span></span>
  
## <a name="resources-for-creating-dlls"></a><span data-ttu-id="3d82d-120">Ressourcen zum Erstellen von DLLs</span><span class="sxs-lookup"><span data-stu-id="3d82d-120">Resources for creating DLLs</span></span>

<span data-ttu-id="3d82d-121">Um eine DLL-Datei zu erstellen, benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3d82d-121">To create a DLL, you need the following:</span></span>
  
- <span data-ttu-id="3d82d-122">Einen Quellcode-Editor.</span><span class="sxs-lookup"><span data-stu-id="3d82d-122">A source code editor.</span></span>
    
- <span data-ttu-id="3d82d-123">Einen Compiler, um Quellcode in Objektcode umzuwandeln, der mit Ihrer Hardware kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="3d82d-123">A compiler to turn source code into object code that is compatible with your hardware.</span></span>
    
- <span data-ttu-id="3d82d-124">Einen Linker, um Code aus statischen Bibliotheken hinzuzuf�gen, falls verwendet, und um die ausführbare DLL-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d82d-124">A linker to add code from static libraries, where used, and to create the executable DLL file.</span></span>
    
<span data-ttu-id="3d82d-p103">Moderne integrierte Entwicklungsumgebungen, wie z. B. Microsoft Visual Studio, stellen all dies bereit. Sie bieten außerdem noch viel mehr: intelligente Editoren, Tools zum Debuggen des Codes, Tools für die Verwaltung mehrerer Projekte, neue Projektassistenten und viele weitere wichtige Tools.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p103">Modern integrated development environments (IDEs), such as Microsoft Visual Studio, provide all of these things. They also provide a great deal more: smart editors, tools to debug your code, tools to manage multiple projects, new project wizards, and many other important tools.</span></span>
  
<span data-ttu-id="3d82d-p104">Sie können die DLL-Dateien in verschiedenen Sprachen erstellen, z. B. C/C++, Pascal und Visual Basic. Aufgrund der Tatsache, dass der in Excel bereitgestellte API-Quellcode C und C++ ist, werden in dieser Dokumentation nur diese beiden Sprachen ber�cksichtigt.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p104">You can create DLLs in several languages, for example, C/C++, Pascal and Visual Basic. Given that the API source code provided with Excel is C and C++, only these two languages are considered in this documentation.</span></span>
  
## <a name="exporting-functions-and-commands"></a><span data-ttu-id="3d82d-129">Exportieren von Funktionen und Befehle</span><span class="sxs-lookup"><span data-stu-id="3d82d-129">Exporting functions and commands</span></span>

<span data-ttu-id="3d82d-p105">Beim Kompilieren eines DLL-Projekts müssen der Compiler und der Linker wissen, welche Funktionen exportiert werden sollen, damit sie sie für die Anwendung verfügbar machen können. Dieser Abschnitt beschreibt die Methoden hierfür.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p105">When compiling a DLL project, the compiler and linker need to know what functions are to be exported so that they can make them available to the application. This section describes the ways this can be done.</span></span>
  
<span data-ttu-id="3d82d-p106">Wenn Compiler Quellcode kompilieren, �ndern sie in der Regel die Namen der Funktionen von deren Darstellung im Quellcode. Normalerweise erfolgt dies, indem etwas an den Anfang und/oder das Ende hinzugefügt wird, ein Prozess, der als Namenserg�nzung bezeichnet wird. Sie müssen sicherstellen, dass die Funktion mit einem Namen exportiert wird, der für die Anwendung erkennbar ist, die die DLL lädt. Dies kann bedeuten, dass der Linker angewiesen werden muss, dass der ergänzte Name einem einfacheren Exportnamen zugeordnet wird. Der Exportname kann der Name sein, wie er ursprünglich im Quellcode angezeigt wurde, oder ein anderer Name.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p106">When compilers compile source code, in general, they change the names of the functions from their appearance in the source code. They usually do this by adding to the beginning and/or end of the name, in a process known as name decoration. You need to make sure that the function is exported with a name that is recognizable to the application loading the DLL. This can mean telling the linker to associate the decorated name with a simpler export name. The export name can be the name as it originally appeared in the source code, or something else.</span></span>
  
<span data-ttu-id="3d82d-p107">Wie der Name ergänzt wird, hängt von der Sprache ab und davon, wie der Compiler angewiesen wird, die Funktion bereitzustellen, also von der Aufrufkonvention. Die standardm��ige Aufrufkonvention zwischen den Prozessen für Windows, die von DLL-Dateien verwendet wird, wird als WinAPI-Konvention bezeichnet. Sie ist in Windows-Headerdateien als **WINAPI** definiert, was wiederum mithilfe des Win32-Deklarators **__stdcall** definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p107">The way the name is decorated depends on the language and how the compiler is instructed to make the function available, that is, the calling convention. The standard inter-process calling convention for Windows used by DLLs is known as the WinAPI convention. It is defined in Windows header files as **WINAPI**, which is in turn defined using the Win32 declarator **__stdcall**.</span></span>
  
<span data-ttu-id="3d82d-p108">Eine DLL-Exportfunktion für die Verwendung mit Excel (ganz gleich, ob Arbeitsblattfunktion, Makrovorlagenfunktion oder benutzerdefinierter Befehl) sollte immer die Aufrufkonvention **WINAPI** / **__stdcall** verwenden. Der **WINAPI**-Bezeichner muss explizit in die Definition der Funktion eingeschlossen werden, da der Standard bei Win32-Compilern darin besteht, die **__cdecl**-Aufrufkonvention zu verwenden, die auch als **WINAPIV** definiert ist, wenn keine angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p108">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention. It is necessary to include the **WINAPI** specifier explicitly in the function's definition as the default in Win32 compilers is to use the **__cdecl** calling convention, also defined as **WINAPIV**, if none is specified.</span></span>
  
<span data-ttu-id="3d82d-142">Sie haben mehrere Möglichkeiten, den Linker anzuweisen, dass eine Funktion exportiert werden soll, und ihm den Namen, unter dem diese extern bekannt sein soll, mitzuteilen:</span><span class="sxs-lookup"><span data-stu-id="3d82d-142">You can tell the linker that a function is to be exported, and the name it is to be known by externally in one of several ways:</span></span>
  
- <span data-ttu-id="3d82d-143">Platzieren Sie die Funktion in einer DEF-Datei nach dem **EXPORTS**-Schlüsselwort, und legen Sie die Einstellung Ihres DLL-Projekts so fest, dass beim Verknüpfen auf diese Datei verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3d82d-143">Place the function in a DEF file after the **EXPORTS** keyword, and set your DLL project setting to reference this file when linking.</span></span> 
    
- <span data-ttu-id="3d82d-144">Verwenden Sie den **__declspec(dllexport)**-Deklarator in der Definition der Funktion.</span><span class="sxs-lookup"><span data-stu-id="3d82d-144">Use the **__declspec(dllexport)** declarator in the function's definition.</span></span> 
    
- <span data-ttu-id="3d82d-145">Verwenden Sie eine **#pragma**-Präprozessordirektive, um eine Nachricht an den Linker zu senden.</span><span class="sxs-lookup"><span data-stu-id="3d82d-145">Use a **#pragma** preprocessor directive to send a message to the linker.</span></span> 
    
<span data-ttu-id="3d82d-146">Ihr Projekt kann zwar alle drei Methoden verwenden, und der Compiler und der Linken können diese unterstützen, Sie sollten jedoch nicht versuchen, eine Funktion auf mehrere Arten zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="3d82d-146">Although your project can use all three methods and your compiler and linker support them, you should not try to export one function in more than one of these ways.</span></span> <span data-ttu-id="3d82d-147">Angenommen, dass eine DLL enthält zwei Quelle Codemodule, eine C und einer C++ die beiden Funktionen zu exportierenden enthalten, **Meine\_C\_exportieren** und **Meine\_Cpp\_exportieren** fest.</span><span class="sxs-lookup"><span data-stu-id="3d82d-147">For example, suppose that a DLL contains two source code modules, one C and one C++, which contain two functions to be exported, **my\_C\_export** and **my\_Cpp\_export** respectively.</span></span> <span data-ttu-id="3d82d-148">Der Einfachheit halber nehmen wir an, dass jede Funktion ein einzelnes numerisches Argument mit doppelter Genauigkeit verwendet und denselben Datentyp zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3d82d-148">For simplicity, suppose that each function takes a single double-precision numerical argument and returns the same data type.</span></span> <span data-ttu-id="3d82d-149">In den folgenden Abschnitten werden die alternativen für den Export von jede Funktion mit den einzelnen Methoden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3d82d-149">The alternatives for exporting each function by using each of these methods are outlined in the following sections.</span></span> 
  
### <a name="using-a-def-file"></a><span data-ttu-id="3d82d-150">Verwenden einer DEF-Datei</span><span class="sxs-lookup"><span data-stu-id="3d82d-150">Using a DEF file</span></span>

```C
double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

```cpp
double WINAPI my_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<br/>

<span data-ttu-id="3d82d-151">Die DEF-Datei müsste dann die folgenden Zeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3d82d-151">The DEF file would then need to contain these lines.</span></span>
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

<span data-ttu-id="3d82d-152">Die allgemeine Syntax einer Zeile, die auf eine **EXPORTS**-Anweisung folgt, lautet folgenderma�en:</span><span class="sxs-lookup"><span data-stu-id="3d82d-152">The general syntax of a line that follows an **EXPORTS** statement is as follows.</span></span> 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

<span data-ttu-id="3d82d-p110">Beachten Sie, dass die C-Funktion ergänzt wurde, aber die DEF-Datei den Linker explizit zwingt, die Funktion mit dem Namen des ursprünglichen Quellcodes verfügbar zu machen (in diesem Beispiel). Der Linker exportiert die C++-Funktion implizit mit dem ursprünglichen Codenamen, es ist daher nicht notwendig, den ergänzten Namen in die DEF-Datei einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p110">Note that the C function has been decorated, but the DEF file explicitly forces the linker to expose the function using the original source code name (in this example). The linker implicitly exports the C++ function using the original code name, so that it is not necessary to include the decorated name in the DEF file.</span></span>
  
<span data-ttu-id="3d82d-155">Bei 32-Bit-Windows-API-Funktionsaufrufen ist die Konvention für die Ergänzung von C-kompilierten Funktionen wie folgt: **function_name** wird _ **function_name@** _n_, wobei  _n_ der Anzahl von Bytes entspricht, ausgedrückt als Dezimalzahl, die von allen Argumenten verwendet wird, und die Bytes jeweils auf das kleinste Vielfache von vier aufgerundet wurden.</span><span class="sxs-lookup"><span data-stu-id="3d82d-155">For 32-bit Windows API function calls, the convention for the decoration of C-compiled functions is as follows: **function_name** becomes _ **function_name@** _n_ where  _n_ is the number of bytes expressed as a decimal taken up by all the arguments, with the bytes for each rounded up to the nearest multiple of four.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3d82d-p111">Alle Zeiger weisen in Win32 eine Breite von vier Bytes auf. Der Rückgabetyp hat keinen Einfluss auf die Namenserg�nzung.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p111">All pointers are four bytes wide in Win32. The return type has no impact on name decoration.</span></span> 
  
<span data-ttu-id="3d82d-p112">Der C++-Compiler kann gezwungen werden, nicht ergänzte Namen für C++-Funktionen verfügbar zu machen, indem die Funktion und alle Funktionsprototypen in einen externen �C" {�}-Block eingeschlossen werden, wie in diesem Beispiel gezeigt. (Die geschweiften Klammern **{}** werden hier ausgelassen, da die Deklaration nur auf den Funktionscodeblock Funktion verweist, der unmittelbar darauf folgt).</span><span class="sxs-lookup"><span data-stu-id="3d82d-p112">It is possible to force the C++ compiler to expose undecorated names for C++ functions by enclosing the function, and any function prototypes, within an extern "C" {…} block, as shown in this example. (The braces **{}** are omitted here because the declaration only refers to the function code block that immediately follows it).</span></span> 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

<span data-ttu-id="3d82d-161">Wenn Sie C-Funktionsprototypen in Headerdateien platzieren, die in C- oder C++-Quelldateien eingeschlossen werden könnten, sollten Sie die folgende Präprozessordirektive einschließen.</span><span class="sxs-lookup"><span data-stu-id="3d82d-161">When you are placing C function prototypes in header files that could be included in C or C++ source files, you should include the following pre-processor directive.</span></span>
  
```cpp
#ifdef __cplusplus
extern "C" {
#endif
double WINAPI my_C_export(double x);
double WINAPI my_Cdecorated_Cpp_export(double x);
#ifdef __cplusplus
}
#endif
```

### <a name="using-the-declspecdllexport-declarator"></a><span data-ttu-id="3d82d-162">Verwenden von __declspec(dllexport) declarator</span><span class="sxs-lookup"><span data-stu-id="3d82d-162">Using the __declspec(dllexport) declarator</span></span>

<span data-ttu-id="3d82d-163">Das **__declspec(dllexport)**-Schlüsselwort kann in der Deklaration der Funktion wie folgt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d82d-163">The **__declspec(dllexport)** keyword can be used in the declaration of the function as follows.</span></span> 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="3d82d-p113">Das **__declspec(dllexport)**-Schlüsselwort am �u�ersten linken Rand der Deklaration hinzugefügt werden. Die Vorteile dieses Ansatzes sind, dass die Funktion nicht unbedingt in einer DEF-Datei aufgelistet sein muss, und dass der Exportstatus mit der Definition richtig ist.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p113">The **__declspec(dllexport)** keyword must be added at the extreme left of the declaration. The advantages of this approach are that the function does not need to be listed in a DEF file, and that the export status is right with the definition.</span></span> 
  
<span data-ttu-id="3d82d-166">Wenn Sie verhindern möchten, dass eine C++-Funktion mit der C++-Namenserg�nzung verfügbar gemacht wird, müssen Sie die Funktion wie folgt deklarieren.</span><span class="sxs-lookup"><span data-stu-id="3d82d-166">If you want to avoid a C++ function being made available with the C++ name decoration, you must declare the function as follows.</span></span>
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="3d82d-167">Der Link macht die Funktion als �my_undecorated_Cpp_export" verfügbar, d. h. mit dem Namen, wie er im Quellcode angezeigt wird, ohne Ergänzung.</span><span class="sxs-lookup"><span data-stu-id="3d82d-167">The linker will make the function available as my_undecorated_Cpp_export, that is, the name as it appears in the source code with no decoration.</span></span>
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a><span data-ttu-id="3d82d-168">Mithilfe einer #pragma Präprozessor Linker-Direktive</span><span class="sxs-lookup"><span data-stu-id="3d82d-168">Using a #pragma preprocessor linker directive</span></span>

<span data-ttu-id="3d82d-p114">Neuere Versionen von Microsoft Visual Studio unterstützen zwei vordefinierte Makros, die es in Verbindung mit einer **#pragma**-Direktive ermöglichen, den Linker anzuweisen, die Funktion direkt aus dem Funktionscode zu exportieren. Die Makros sind __FUNCTION__ und __FUNCDNAME__ (Beachten Sie den doppelten Unterstrich an jedem Ende), die zu den nicht ergänzten bzw. ergänzten Funktionsnamen erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p114">Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code. The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> 
  
<span data-ttu-id="3d82d-171">Wenn Sie z. B. Microsoft Visual Studio verwenden, können diese Zeilen wie folgt in eine gemeinsame Headerdatei integriert werden.</span><span class="sxs-lookup"><span data-stu-id="3d82d-171">For example, when you are using Microsoft Visual Studio, these lines can be incorporated into a common header file as follows.</span></span>
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

<span data-ttu-id="3d82d-172">Wenn diese Kopfzeile in den Quelldateien enthalten ist, können die zwei Beispielfunktionen wie folgt exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="3d82d-172">If this header is included in the source files, the two example functions can then be exported as follows.</span></span>
  
<span data-ttu-id="3d82d-173">C-Code:</span><span class="sxs-lookup"><span data-stu-id="3d82d-173">C code:</span></span>
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="3d82d-174">C++-Code:</span><span class="sxs-lookup"><span data-stu-id="3d82d-174">C++ code:</span></span>
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="3d82d-p115">Beachten Sie, dass die Direktive im Textkörper der Funktion platziert werden muss und nur erweitert wird, wenn keine der Compileroptionen **/EP** oder **/P** festgelegt sind. Bei dieser Technik entfällt die Notwendigkeit einer DEF-Datei oder **__declspec(dllexport)**-Deklaration, und die Angabe des Exportstatus verbleibt beim Funktionscode.</span><span class="sxs-lookup"><span data-stu-id="3d82d-p115">Note that the directive must be placed within the body of the function and is only expanded when neither of the compiler options **/EP** or **/P** is set. This technique removes the need for a DEF file, or **__declspec(dllexport)** declaration, and keeps the specification of its export status with the function code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d82d-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d82d-177">See also</span></span>

- [<span data-ttu-id="3d82d-178">Zugriff auf DLLs in Excel</span><span class="sxs-lookup"><span data-stu-id="3d82d-178">Access DLLs in Excel</span></span>](how-to-access-dlls-in-excel.md)
- [<span data-ttu-id="3d82d-179">Aufrufen von Excel von der DLL oder XLL aus</span><span class="sxs-lookup"><span data-stu-id="3d82d-179">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
- [<span data-ttu-id="3d82d-180">Excel-Programmierkonzepte</span><span class="sxs-lookup"><span data-stu-id="3d82d-180">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="3d82d-181">Entwickeln von Excel-XLLs</span><span class="sxs-lookup"><span data-stu-id="3d82d-181">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

