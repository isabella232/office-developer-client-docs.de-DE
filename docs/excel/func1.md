---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- func1-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408915"
---
# <a name="func1"></a><span data-ttu-id="1f0bf-104">Func1</span><span class="sxs-lookup"><span data-stu-id="1f0bf-104">Func1</span></span>

 <span data-ttu-id="1f0bf-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1f0bf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1f0bf-106">Beispiel für eine benutzerdefinierte Arbeitsblattfunktion zeigt die Rückgabe eines statischen String-Werts.</span><span class="sxs-lookup"><span data-stu-id="1f0bf-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="1f0bf-107">Wenn generische. XLL geladen wird, wird diese Funktion registriert, sodass Sie vom Arbeitsblatt aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f0bf-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="1f0bf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f0bf-108">Parameters</span></span>

 <span data-ttu-id="1f0bf-109">_px_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="1f0bf-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="1f0bf-110">Dieses Argument wird ignoriert und dient nur dazu, Microsoft Excel auszulösen, um die Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1f0bf-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1f0bf-111">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f0bf-111">Property value/Return value</span></span>

 <span data-ttu-id="1f0bf-112">**LPXLOPER12**: immer die Zeichenfolge "func1"</span><span class="sxs-lookup"><span data-stu-id="1f0bf-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="1f0bf-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1f0bf-113">Example</span></span>

<span data-ttu-id="1f0bf-114">Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="1f0bf-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f0bf-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f0bf-115">See also</span></span>



[<span data-ttu-id="1f0bf-116">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="1f0bf-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

