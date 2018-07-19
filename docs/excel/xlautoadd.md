---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- Xlautoadd-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790579"
---
# <a name="xlautoadd"></a><span data-ttu-id="6e429-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="6e429-104">xlAutoAdd</span></span>

 <span data-ttu-id="6e429-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6e429-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6e429-106">Von Microsoft Excel hinzugefügt, wenn der Benutzer die XLL während einer Sitzung Excel aktiviert, mit dem Add-In-Manager.</span><span class="sxs-lookup"><span data-stu-id="6e429-106">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="6e429-107">Diese Funktion wird nicht aufgerufen, wenn Excel gestartet und ein vorinstallierte Add-In lädt.</span><span class="sxs-lookup"><span data-stu-id="6e429-107">This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="6e429-108">Diese Funktion kann verwendet werden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das dem Benutzer teilt mit, dass das Add-In aktiviert wurde, oder zum Lesen oder Schreiben in die Registrierung Lizenzinformationen, beispielsweise überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6e429-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="6e429-109">Excel erfordert eine XLL zu implementieren und exportieren Sie diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="6e429-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="6e429-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e429-110">Parameters</span></span>

<span data-ttu-id="6e429-111">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="6e429-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6e429-112">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e429-112">Property value/Return value</span></span>

<span data-ttu-id="6e429-113">1 sollte die Implementierung von dieser Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e429-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="6e429-114">(**Int**).</span><span class="sxs-lookup"><span data-stu-id="6e429-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e429-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e429-115">Remarks</span></span>

<span data-ttu-id="6e429-116">Verwenden Sie diese Funktion, wenn vorhanden ist nichts, die Ihre XLL benötigt, wenn es vom Add-In-Manager hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6e429-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="6e429-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e429-117">Example</span></span>

<span data-ttu-id="6e429-118">Finden Sie unter `\SAMPLES\EXAMPLE\EXAMPLE.C` und `\SAMPLES\GENERIC\GENERIC.C` beispielsweise Implementierungen von dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="6e429-118">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="6e429-119">Der folgende Code ist aus `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="6e429-119">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="6e429-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e429-120">See also</span></span>



[<span data-ttu-id="6e429-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="6e429-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="6e429-122">Add-In-Manager und Funktionen von XLL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e429-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

