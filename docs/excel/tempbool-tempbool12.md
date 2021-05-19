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
- tempbool-Funktion [excel 2007],TempBool12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433717"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="9c62f-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="9c62f-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="9c62f-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9c62f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9c62f-106">Framework library function that creates a temporary **XLOPER** /  **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9c62f-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="9c62f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c62f-107">Parameters</span></span>

 <span data-ttu-id="9c62f-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="9c62f-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="9c62f-109">Verwenden Sie 0, um **FALSE zurück zu geben;** verwenden Sie einen beliebigen anderen Wert, um **TRUE zurück zu geben.**</span><span class="sxs-lookup"><span data-stu-id="9c62f-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9c62f-110">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c62f-110">Property value/Return value</span></span>

<span data-ttu-id="9c62f-111">Gibt einen **xltypeBool** **Boolean-Wert zurück,** der den übergebenen logischen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="9c62f-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9c62f-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9c62f-112">Example</span></span>

<span data-ttu-id="9c62f-113">Im folgenden Beispiel wird die **TempBool12-Funktion** verwendet, um die Statusleiste zu löschen.</span><span class="sxs-lookup"><span data-stu-id="9c62f-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="9c62f-114">Temporärer Speicher wird beim [Excel/Excel12f-Funktion](excel-excel12f.md) frei.</span><span class="sxs-lookup"><span data-stu-id="9c62f-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="9c62f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c62f-115">See also</span></span>



[<span data-ttu-id="9c62f-116">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="9c62f-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

