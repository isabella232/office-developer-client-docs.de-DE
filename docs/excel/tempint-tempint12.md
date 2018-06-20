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
- tempint12-Funktion [excel 2007], TempInt-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790575"
---
# <a name="tempinttempint12"></a><span data-ttu-id="75460-104">TempInt/TempInt12</span><span class="sxs-lookup"><span data-stu-id="75460-104">TempInt/TempInt12</span></span>

 <span data-ttu-id="75460-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="75460-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="75460-106">Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** , die eine ganze Zahl enthält.</span><span class="sxs-lookup"><span data-stu-id="75460-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** that contains an integer.</span></span> 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a><span data-ttu-id="75460-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="75460-107">Parameters</span></span>

 <span data-ttu-id="75460-108">_Ich_</span><span class="sxs-lookup"><span data-stu-id="75460-108">_i_</span></span>
  
<span data-ttu-id="75460-109">Die vorgesehene Integer-Wert.</span><span class="sxs-lookup"><span data-stu-id="75460-109">The intended integer value.</span></span> <span data-ttu-id="75460-110">Beachten Sie, dass die **XLOPER** ganze Zahl, eine 16-Bit-Ganzzahl mit Vorzeichen (short Int) ist die **XLOPER12** ganze Zahl ist eine 32-Bit-Ganzzahl ([lange] Int).</span><span class="sxs-lookup"><span data-stu-id="75460-110">Note that the **XLOPER** integer is a signed 16-bit integer (short int), whereas the **XLOPER12** integer is a signed 32-bit integer ([long] int).</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="75460-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="75460-111">Return value</span></span>

<span data-ttu-id="75460-112">Gibt einen Integer **vom Typ XltypeInt** mit dem übergebenen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="75460-112">Returns an **xltypeInt** integer containing the value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="75460-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="75460-113">Example</span></span>

<span data-ttu-id="75460-114">In diesem Beispiel wird die **TempInt12** -Funktion verwendet, um **XlfGetWorkspace**ein Argument übergeben.</span><span class="sxs-lookup"><span data-stu-id="75460-114">This example uses the **TempInt12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="75460-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75460-115">See also</span></span>



[<span data-ttu-id="75460-116">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="75460-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

