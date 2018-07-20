---
title: Abwärtskompatibilität
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Versionskompatibilität [excel 2007], XLL-Kompatibilität [Excel 2007], Abwärtskompatibilität [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 095961fa909a67b354ed43a7e093b79a9ebb4f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790394"
---
# <a name="backward-compatibility"></a><span data-ttu-id="aeaf1-104">Abwärtskompatibilität</span><span class="sxs-lookup"><span data-stu-id="aeaf1-104">Backward compatibility</span></span>

<span data-ttu-id="aeaf1-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="aeaf1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="aeaf1-106">In diesem Thema werden die XLL Kompatibilitätsprobleme in verschiedenen Versionen von Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="aeaf1-107">Nützliche Konstantendefinitionen</span><span class="sxs-lookup"><span data-stu-id="aeaf1-107">Useful constant definitions</span></span>

<span data-ttu-id="aeaf1-108">Berücksichtigen Sie Definitionen etwa wie folgt in Ihr Projekt XLL-Code, und ersetzen alle Instanzen von literalen Zahlen, die in diesem Kontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="aeaf1-109">Dies wird verdeutlichen Code, der bestimmte Version ist und die Wahrscheinlichkeit von Fehlern in Form von Zahlen harmlos professionell gestalteten Version bezogene reduzieren.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
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

## <a name="getting-the-running-version"></a><span data-ttu-id="aeaf1-110">Abrufen der ausgeführten version</span><span class="sxs-lookup"><span data-stu-id="aeaf1-110">Getting the running version</span></span>

<span data-ttu-id="aeaf1-111">Sie sollte erkennen, welche Version ausgeführt wird, mithilfe von `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, wobei `arg` ist eine numerische **XLOPER** auf 2 festgelegt und Version ist eine Zeichenfolge **XLOPER** , klicken Sie dann auf eine Ganzzahl umgewandelt werden können.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="aeaf1-112">Dies ist für Microsoft Excel 2013 15.0.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="aeaf1-113">Sie sollten Folgendes in oder über die Funktion [XlAutoOpen](xlautoopen.md) machen.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="aeaf1-114">Anschließend können Sie eine globale Variable festlegen, die alle Module in Ihrem Projekt darüber informiert, welche Version von Excel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="aeaf1-115">Code kann dann entscheiden, ob der C-API mit **Excel12** und **XLOPER12**s oder mit dem **Excel4** mit **XLOPER**s aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="aeaf1-116">Sie können **XLCallVer** zum Ermitteln der C-API Version aufrufen, aber dies wird nicht angeben, welche der den vor Excel 2007-Versionen, die Sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="aeaf1-117">Erstellen von Add-Ins, die duale Schnittstellen exportieren</span><span class="sxs-lookup"><span data-stu-id="aeaf1-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="aeaf1-118">Erwägen Sie eine XLL-Funktion, die eine Zeichenfolge und gibt einen Wert, der die Datentypen Arbeitsblatt angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="aeaf1-119">Sie konnte eine Funktion registrierten "PD" eingeben und Prototyp wie folgt exportieren, wobei die Zeichenfolge als eine Bytezeichenfolge der Länge gezählt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="aeaf1-120">Obwohl dies fehlerfrei funktioniert, es gibt verschiedene Gründe für Dies ist nicht die ideale-Schnittstelle für den Code in Excel 2007:</span><span class="sxs-lookup"><span data-stu-id="aeaf1-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="aeaf1-121">Sie unterliegt den Einschränkungen des C-API-Byte-Zeichenfolgen und die langen Unicode-Zeichenfolgen unterstützt, die ab Excel 2007 kann nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="aeaf1-122">Zwar beginnend in Excel 2007, Excel übergeben und **XLOPER**s akzeptiert werden kann, intern konvertiert werden in **XLOPER12**s, damit ein implizite Konvertierung zusätzlicher Aufwand ab Excel 2007, die beim Ausführen des Codes in früheren Versionen von Excel nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="aeaf1-123">Es kann sein, dass diese Funktion Thread sicherer, hergestellt werden, kann aber in der Zeichenfolge geändert wird, wenn `PD$`, Registrierung fehlschlägt, bevor Excel 2007 starten.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="aeaf1-124">Aus diesen Gründen idealerweise starten in Excel 2007 sollten exportieren eine Funktion für die Benutzer, die als registriert wurde `QD%$`, sofern Ihr Code ist sicherer und Prototyp wie folgt.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="aeaf1-125">Ein weiterer Grund, warum sollten Sie die Registrierung einer anderen Funktion ab Excel 2007, ist, dass genehmigt XLL-Funktionen bis zu 255 Argumente, anstatt den 30 Grenzwert von früheren Versionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="aeaf1-126">Zum Glück haben Sie die Vorteile beider durch beide Versionen aus Ihrem Projekt exportieren.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="aeaf1-127">Können Sie erkennen klicken Sie dann die Excel-Version ausgeführt wird und die am besten geeignete Funktion bedingt registrieren.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="aeaf1-128">Weitere Informationen und ein Beispiel für eine Implementierung finden Sie unter [Developing-Add-ins (XLLs) in Excel 2007](http://msdn.microsoft.com/de-de/library/aa730920.aspx).</span><span class="sxs-lookup"><span data-stu-id="aeaf1-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](http://msdn.microsoft.com/de-de/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="aeaf1-129">Diese Methode führt zu die Möglichkeit, dass unterschiedliche Ergebnisse als ab Excel 2007 mit demselben Blatt ein Arbeitsblatt in Excel 2003 ausgeführt angezeigt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="aeaf1-130">Beispielsweise würde für Excel 2003 ordnen Sie eine Unicode-Zeichenfolge in einer Arbeitsblattzelle Excel 2003 ASCII-Byte-Zeichenfolge und kürzen sie vor der Übergabe an eine XLL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="aeaf1-131">Ab Excel 2007, übergibt Excel eine nicht konvertierten Unicode-Zeichenfolge eine bequeme Weise registrierte XLL-Funktion an.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="aeaf1-132">Dies kann zu einem anderen Ergebnis führen.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-132">This could lead to a different result.</span></span> <span data-ttu-id="aeaf1-133">Sie sollten diese Möglichkeit und die Konsequenzen für die Benutzer, nicht nur bei der Aktualisierung beachten.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="aeaf1-134">Beispielsweise wurden einige integrierten numerischen Funktionen zwischen Excel 2000 und Excel 2003 verbessert.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="aeaf1-135">Neue Arbeitsblattfunktionen und Analyse-Funktionen</span><span class="sxs-lookup"><span data-stu-id="aeaf1-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="aeaf1-136">Analysis Toolpak (ATP) Funktionen sind Teil der Excel ab Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="aeaf1-137">Bisher konnte eine XLL nur eine ATP-Funktion rufen Sie mithilfe von [XlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="aeaf1-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="aeaf1-138">Ab Excel 2007, sollte die ATP-Funktionen aufgerufen werden mit der Funktion Enumerationen in xlcall.h definiert.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="aeaf1-139">Das Beispiel in Aufrufen von benutzerdefinierten Funktionen von DLLs werden die zwei verschiedene Verfahren veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aeaf1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aeaf1-140">See also</span></span>

- [<span data-ttu-id="aeaf1-141">C-API-R�ckruf funktioniert Excel4 Excel12</span><span class="sxs-lookup"><span data-stu-id="aeaf1-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="aeaf1-142">Programmieren mit der C-API in Excel</span><span class="sxs-lookup"><span data-stu-id="aeaf1-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="aeaf1-143">Was ist neu in der C-API für Excel 2013</span><span class="sxs-lookup"><span data-stu-id="aeaf1-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

