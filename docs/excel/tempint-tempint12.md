---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- tempint12-Funktion [Excel 2007], TempInt-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 16a2222dbc51ad9480dbd5941ca2ed13f65b55e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310479"
---
# <a name="tempinttempint12"></a><span data-ttu-id="97d42-104">TempInt/TempInt12</span><span class="sxs-lookup"><span data-stu-id="97d42-104">TempInt/TempInt12</span></span>

 <span data-ttu-id="97d42-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="97d42-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="97d42-106">Framework-Bibliotheksfunktion, die eine temporäre **XLOPER**/ -**XLOPER12** erstellt, die eine ganze Zahl enthält.</span><span class="sxs-lookup"><span data-stu-id="97d42-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** that contains an integer.</span></span> 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a><span data-ttu-id="97d42-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="97d42-107">Parameters</span></span>

 <span data-ttu-id="97d42-108">_i_</span><span class="sxs-lookup"><span data-stu-id="97d42-108">_i_</span></span>
  
<span data-ttu-id="97d42-109">Der vorgesehene ganzzahlige Wert.</span><span class="sxs-lookup"><span data-stu-id="97d42-109">The intended integer value.</span></span> <span data-ttu-id="97d42-110">Beachten Sie, dass die **XLOPER** -Ganzzahl eine signierte 16-Bit-Ganzzahl (short int) ist, wohingegen die **XLOPER12** -ganzzahl eine signierte 32-Bit-Ganzzahl ([Long] int) ist.</span><span class="sxs-lookup"><span data-stu-id="97d42-110">Note that the **XLOPER** integer is a signed 16-bit integer (short int), whereas the **XLOPER12** integer is a signed 32-bit integer ([long] int).</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="97d42-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97d42-111">Return value</span></span>

<span data-ttu-id="97d42-112">Gibt eine **xltypeInt** -Ganzzahl zurück, die den übergebenen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="97d42-112">Returns an **xltypeInt** integer containing the value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="97d42-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="97d42-113">Example</span></span>

<span data-ttu-id="97d42-114">In diesem Beispiel wird die **TempInt12** -Funktion verwendet, um ein Argument an **xlfGetWorkspace**zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="97d42-114">This example uses the **TempInt12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="97d42-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97d42-115">See also</span></span>



[<span data-ttu-id="97d42-116">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="97d42-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

