---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlAutoAdd-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303990"
---
# <a name="xlautoadd"></a><span data-ttu-id="8e3cb-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="8e3cb-104">xlAutoAdd</span></span>

 <span data-ttu-id="8e3cb-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8e3cb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8e3cb-106">Von Microsoft Excel HinzugeFügt, wenn der Benutzer die XLL während einer Excel-Sitzung mithilfe des Add-in-Managers aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-106">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="8e3cb-107">Diese Funktion wird nicht aufgerufen, wenn Excel gestartet wird und ein vorinstalliertes Add-in lädt.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-107">This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="8e3cb-108">Diese Funktion kann verwendet werden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das dem Benutzer mitteilt, dass das Add-in aktiviert wurde, oder um aus der Registrierung zu lesen oder zu schreiben, oder beispielsweise Lizenzierungsinformationen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="8e3cb-109">Excel benötigt keine XLL, um diese Funktion zu implementieren und zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="8e3cb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e3cb-110">Parameters</span></span>

<span data-ttu-id="8e3cb-111">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="8e3cb-112">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e3cb-112">Property value/Return value</span></span>

<span data-ttu-id="8e3cb-113">Ihre Implementierung dieser Funktion sollte 1 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="8e3cb-114">(**int**).</span><span class="sxs-lookup"><span data-stu-id="8e3cb-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e3cb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e3cb-115">Remarks</span></span>

<span data-ttu-id="8e3cb-116">Verwenden Sie diese Funktion, wenn Ihre XLL etwas tun muss, wenn Sie vom Add-in-Manager hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="8e3cb-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8e3cb-117">Example</span></span>

<span data-ttu-id="8e3cb-118">Siehe `\SAMPLES\EXAMPLE\EXAMPLE.C` auch `\SAMPLES\GENERIC\GENERIC.C` Implementierungen dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-118">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="8e3cb-119">Der folgende Code stammt aus `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-119">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="8e3cb-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e3cb-120">See also</span></span>



[<span data-ttu-id="8e3cb-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="8e3cb-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="8e3cb-122">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="8e3cb-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

