---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- unhookexcelwindow-Funktion
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409447"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="19ccf-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="19ccf-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="19ccf-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="19ccf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="19ccf-106">Entfernt **excelCursorProc,** das zuvor von **HookExcelWindow installiert wurde.**</span><span class="sxs-lookup"><span data-stu-id="19ccf-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="19ccf-107">Dies wäre so erfolgt, dass **ExcelCursorProc** vor dem Microsoft Excel **WndProc aufgerufen wurde.**</span><span class="sxs-lookup"><span data-stu-id="19ccf-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="19ccf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="19ccf-108">Parameters</span></span>

 <span data-ttu-id="19ccf-109">_hWndExcel_ (**HANDLE**)</span><span class="sxs-lookup"><span data-stu-id="19ccf-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="19ccf-110">Das Excel-Windows-Handle.</span><span class="sxs-lookup"><span data-stu-id="19ccf-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="19ccf-111">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19ccf-111">Property value/Return value</span></span>

<span data-ttu-id="19ccf-112">Die Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="19ccf-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19ccf-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19ccf-113">Remarks</span></span>

<span data-ttu-id="19ccf-114">Mit dieser Funktion wird die Excel **WndProc** mithilfe von **SetWindowLong()** wiederhergestellt, um die Adresse wiederherzustellen, die von **HookExcelWindow()** gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="19ccf-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="19ccf-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="19ccf-115">Example</span></span>

<span data-ttu-id="19ccf-116">Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="19ccf-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19ccf-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19ccf-117">See also</span></span>



[<span data-ttu-id="19ccf-118">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="19ccf-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

