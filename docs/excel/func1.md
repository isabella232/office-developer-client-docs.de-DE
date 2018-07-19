---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- func1-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790503"
---
# <a name="func1"></a><span data-ttu-id="2c078-104">Func1</span><span class="sxs-lookup"><span data-stu-id="2c078-104">Func1</span></span>

 <span data-ttu-id="2c078-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2c078-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2c078-106">Benutzerdefinierte Tabellenfunktion Beispiel veranschaulicht die Rückgabe von einen statischen String-Wert.</span><span class="sxs-lookup"><span data-stu-id="2c078-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="2c078-107">Wenn GENERIC.xll geladen wird, registriert sie diese Funktion, damit sie aus dem Arbeitsblatt aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c078-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="2c078-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c078-108">Parameters</span></span>

 <span data-ttu-id="2c078-109">_px_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="2c078-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="2c078-110">Dieses Argument wird ignoriert, und nur für Microsoft Excel die Funktion Trigger dient.</span><span class="sxs-lookup"><span data-stu-id="2c078-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2c078-111">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c078-111">Property value/Return value</span></span>

 <span data-ttu-id="2c078-112">**LPXLOPER12**: immer die Zeichenfolge "Func1"</span><span class="sxs-lookup"><span data-stu-id="2c078-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="2c078-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2c078-113">Example</span></span>

<span data-ttu-id="2c078-114">Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="2c078-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c078-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c078-115">See also</span></span>



[<span data-ttu-id="2c078-116">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="2c078-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

