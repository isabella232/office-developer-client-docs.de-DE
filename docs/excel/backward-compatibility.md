---
title: Abwärtskompatibilität
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Versionskompatibilität [Excel 2007], XLL-Kompatibilität [Excel 2007], Abwärtskompatibilität [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301680"
---
# <a name="backward-compatibility"></a><span data-ttu-id="594b1-104">Abwärtskompatibilität</span><span class="sxs-lookup"><span data-stu-id="594b1-104">Backward compatibility</span></span>

<span data-ttu-id="594b1-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="594b1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="594b1-106">In diesem Thema werden Probleme der XLL-Kompatibilität in unterschiedlichen Versionen von Microsoft Excel behandelt.</span><span class="sxs-lookup"><span data-stu-id="594b1-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="594b1-107">Nützliche Konstante Definitionen</span><span class="sxs-lookup"><span data-stu-id="594b1-107">Useful constant definitions</span></span>

<span data-ttu-id="594b1-108">Erwägen Sie, Definitionen, die diesen ähneln, in den XLL-Projekt Code einzufügen und alle Instanzen von Literalzahlen zu ersetzen, die in diesem Kontext verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="594b1-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="594b1-109">Dadurch wird der versionsspezifische Code erläutert und die Wahrscheinlichkeit von versionsbezogenen Fehlern in Form von harmlos aussehenden Zahlen reduziert.</span><span class="sxs-lookup"><span data-stu-id="594b1-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a><span data-ttu-id="594b1-110">Aufrufen der laufenden Version</span><span class="sxs-lookup"><span data-stu-id="594b1-110">Getting the running version</span></span>

<span data-ttu-id="594b1-111">Sie sollten feststellen, welche Version mit `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`verwendet wird `arg` , wobei es sich um eine numerische **XLOPER** auf 2 und Version ist eine Zeichenfolge **XLOPER** , die dann in eine ganze Zahl umgewandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="594b1-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="594b1-112">Für Microsoft Excel 2013 ist dies 15,0.</span><span class="sxs-lookup"><span data-stu-id="594b1-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="594b1-113">Sie sollten dies in oder aus der [xlAutoOpen](xlautoopen.md) -Funktion tun.</span><span class="sxs-lookup"><span data-stu-id="594b1-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="594b1-114">Sie können dann eine globale Variable festlegen, die alle Module in Ihrem Projekt über die Ausführung von Excel informiert.</span><span class="sxs-lookup"><span data-stu-id="594b1-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="594b1-115">Der Code kann dann entscheiden, ob die C-API mit **Excel12** und **XLOPER12**s oder mithilfe von **Excel4** mit **XLOPER**s aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="594b1-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="594b1-116">Sie können **XLCallVer** aufrufen, um die C-API-Version zu ermitteln, aber dies gibt nicht an, welche der Versionen vor Excel 2007 Sie gerade laufen.</span><span class="sxs-lookup"><span data-stu-id="594b1-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="594b1-117">Erstellen von Add-Ins, die duale Schnittstellen exportieren</span><span class="sxs-lookup"><span data-stu-id="594b1-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="594b1-118">Betrachten Sie eine XLL-Funktion, die eine Zeichenfolge akzeptiert und einen Wert zurückgibt, der einen beliebigen Arbeitsblatt Datentyp aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="594b1-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="594b1-119">Sie können eine als Typ "PD" registrierte Funktion exportieren und wie folgt Prototypieren, wobei die Zeichenfolge als Längenbyte-Zeichenfolge übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="594b1-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="594b1-120">Obwohl dies sehr gut funktioniert, gibt es mehrere Gründe, warum dies nicht die ideale Schnittstelle zu Ihrem Code ab Excel 2007 ist:</span><span class="sxs-lookup"><span data-stu-id="594b1-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="594b1-121">Sie unterliegt den Einschränkungen der C-API-Byte Zeichenfolgen und kann nicht auf die langen Unicode-Zeichenfolgen zugreifen, die ab Excel 2007 unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="594b1-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="594b1-122">Obwohl Excel ab Excel 2007 **XLOPER**s passieren und annehmen kann, wandelt es Sie intern in **XLOPER12**s um, sodass es einen impliziten Konvertierungsaufwand ab Excel 2007 gibt, der nicht vorhanden ist, wenn der Code in früheren Versionen von Excel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="594b1-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="594b1-123">Es kann sein, dass diese Funktion threadsicher gemacht werden kann, aber wenn die Typ `PD$`-Zeichenfolge geändert wird, schlägt die Registrierung beim Starten vor Excel 2007 fehl.</span><span class="sxs-lookup"><span data-stu-id="594b1-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="594b1-124">Aus diesen Gründen sollten Sie idealerweise ab Excel 2007 eine Funktion für die Benutzer exportieren, die registriert wurde `QD%$`, sofern Ihr Code threadsicher und wie folgt prototypiert ist.</span><span class="sxs-lookup"><span data-stu-id="594b1-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="594b1-125">Ein anderer Grund, warum Sie eine andere Funktion ab Excel 2007 registrieren möchten, ist, dass XLL-Funktionen bis zu 255 Argumente statt der 30-Grenze früherer Versionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="594b1-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="594b1-126">Glücklicherweise können Sie die Vorteile beider Versionen aus dem Projekt exportieren.</span><span class="sxs-lookup"><span data-stu-id="594b1-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="594b1-127">Sie können dann die laufende Excel-Version feststellen und die am besten geeignete Funktion abhängig registrieren.</span><span class="sxs-lookup"><span data-stu-id="594b1-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="594b1-128">Weitere Informationen und eine Beispielimplementierung finden Sie unter [developIng Add-Ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span><span class="sxs-lookup"><span data-stu-id="594b1-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="594b1-129">Dieser Ansatz führt zu der Möglichkeit, dass ein Arbeitsblatt, das in Excel 2003 läuft, unterschiedliche Ergebnisse anzeigen kann als im gleichen Arbeitsblatt, das ab Excel 2007 beginnt.</span><span class="sxs-lookup"><span data-stu-id="594b1-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="594b1-130">Beispielsweise würde Excel 2003 eine Unicode-Zeichenfolge in einer Excel 2003-Arbeitsblattzelle einer ASCII-Byte-Zeichenfolge zuordnen und Abschneiden, bevor Sie an eine XLL-Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="594b1-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="594b1-131">Ab Excel 2007 übergibt Excel eine nicht konvertierte Unicode-Zeichenfolge an eine auf die richtige Weise registrierte XLL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="594b1-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="594b1-132">Dies kann zu einem anderen Ergebnis führen.</span><span class="sxs-lookup"><span data-stu-id="594b1-132">This could lead to a different result.</span></span> <span data-ttu-id="594b1-133">Sie sollten diese Möglichkeit und die Konsequenzen für Ihre Benutzer beachten, nicht nur für das Upgrade.</span><span class="sxs-lookup"><span data-stu-id="594b1-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="594b1-134">Beispielsweise wurden einige integrierte numerische Funktionen zwischen Excel 2000 und Excel 2003 verbessert.</span><span class="sxs-lookup"><span data-stu-id="594b1-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="594b1-135">Neue Arbeitsblattfunktionen und Analyse-Funktionen</span><span class="sxs-lookup"><span data-stu-id="594b1-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="594b1-136">Die Funktionen von Analysis-Funktionen (ATP) sind Teil von Excel ab Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="594b1-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="594b1-137">Zuvor konnte eine XLL nur mithilfe von [xlUDF](xludf.md)eine ATP-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="594b1-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="594b1-138">Ab Excel 2007 sollten die ATP-Funktionen mithilfe der in xlcall. h definierten Funktions Aufzählungen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="594b1-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="594b1-139">Das Beispiel unter Aufrufen von benutzerdefinierten Funktionen aus DLLs demonstriert die zwei verschiedenen Methoden.</span><span class="sxs-lookup"><span data-stu-id="594b1-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="594b1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="594b1-140">See also</span></span>

- [<span data-ttu-id="594b1-141">C-API-R�ckruf funktioniert Excel4 Excel12</span><span class="sxs-lookup"><span data-stu-id="594b1-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="594b1-142">Programmieren mit der C-API in Excel</span><span class="sxs-lookup"><span data-stu-id="594b1-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="594b1-143">Was ist neu in der C-API f�r Excel 2013</span><span class="sxs-lookup"><span data-stu-id="594b1-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

