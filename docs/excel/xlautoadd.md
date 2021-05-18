---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlautoadd-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413759"
---
# <a name="xlautoadd"></a><span data-ttu-id="9709c-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="9709c-104">xlAutoAdd</span></span>

 <span data-ttu-id="9709c-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9709c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9709c-106">Hinzugefügt von Microsoft Excel, wenn der Benutzer die XLL während einer Excel mit dem Add-In aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9709c-106">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="9709c-107">Diese Funktion wird nicht aufgerufen, Excel gestartet und ein vorinstalliertes Add-In geladen wird.</span><span class="sxs-lookup"><span data-stu-id="9709c-107">This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="9709c-108">Diese Funktion kann verwendet werden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, in dem der Benutzer informiert wird, dass das Add-In aktiviert wurde, oder um aus der Registrierung zu lesen oder in die Registrierung zu schreiben oder z. B. Lizenzierungsinformationen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9709c-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="9709c-109">Excel erfordert keine XLL, um diese Funktion zu implementieren und zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="9709c-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="9709c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9709c-110">Parameters</span></span>

<span data-ttu-id="9709c-111">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9709c-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9709c-112">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9709c-112">Property value/Return value</span></span>

<span data-ttu-id="9709c-113">Ihre Implementierung dieser Funktion sollte 1 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9709c-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="9709c-114">(**int**).</span><span class="sxs-lookup"><span data-stu-id="9709c-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9709c-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9709c-115">Remarks</span></span>

<span data-ttu-id="9709c-116">Verwenden Sie diese Funktion, wenn Ihre XLL etwas tun muss, wenn sie vom Add-In hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9709c-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="9709c-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9709c-117">Example</span></span>

<span data-ttu-id="9709c-118">Sehen  `\SAMPLES\EXAMPLE\EXAMPLE.C` Sie sich beispielsweise  `\SAMPLES\GENERIC\GENERIC.C` Implementierungen dieser Funktion an.</span><span class="sxs-lookup"><span data-stu-id="9709c-118">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="9709c-119">Der folgende Code stammt aus `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="9709c-119">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="9709c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9709c-120">See also</span></span>



[<span data-ttu-id="9709c-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="9709c-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="9709c-122">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="9709c-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

