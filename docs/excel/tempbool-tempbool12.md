---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- Tempbool-Funktion [excel 2007], TempBool12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790569"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="d9051-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="d9051-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="d9051-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d9051-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d9051-106">Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** mit **booleschen Wert** **TRUE** oder **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d9051-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="d9051-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9051-107">Parameters</span></span>

 <span data-ttu-id="d9051-108">_b_ (**Int**)</span><span class="sxs-lookup"><span data-stu-id="d9051-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="d9051-109">Verwenden Sie 0 **FALSE**zurückgegeben. Verwenden Sie einen anderen Wert **TRUE**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d9051-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d9051-110">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9051-110">Property value/Return value</span></span>

<span data-ttu-id="d9051-111">Gibt ein **XltypeBool** **Boolean** mit den logischen übergebenen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d9051-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d9051-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d9051-112">Example</span></span>

<span data-ttu-id="d9051-113">Im folgende Beispiel wird mithilfe die Funktion **TempBool12** die Statusleiste gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d9051-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="d9051-114">Temporärer Speicher freigegeben wird, wenn die [Excel/Excel12f](excel-excel12f.md) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d9051-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d9051-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9051-115">See also</span></span>



[<span data-ttu-id="d9051-116">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="d9051-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

