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
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310311"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="808fb-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="808fb-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="808fb-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="808fb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="808fb-106">Entfernt die **ExcelCursorProc** , die zuvor von **HookExcelWindow**installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="808fb-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="808fb-107">Dies wäre getan worden, damit **ExcelCursorProc** vor dem Haupt- **WndProc**von Microsoft Excel aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="808fb-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="808fb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="808fb-108">Parameters</span></span>

 <span data-ttu-id="808fb-109">_hWndExcel_ (**Handle**)</span><span class="sxs-lookup"><span data-stu-id="808fb-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="808fb-110">Der Excel-Hauptfenster-handle.</span><span class="sxs-lookup"><span data-stu-id="808fb-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="808fb-111">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="808fb-111">Property value/Return value</span></span>

<span data-ttu-id="808fb-112">Die Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="808fb-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="808fb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="808fb-113">Remarks</span></span>

<span data-ttu-id="808fb-114">Diese Funktion stellt die Excel-Standard- **WndProc** mithilfe von **SetWindowLong ()** wieder her, um die von **HookExcelWindow ()** gespeicherte Adresse wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="808fb-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="808fb-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="808fb-115">Example</span></span>

<span data-ttu-id="808fb-116">Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="808fb-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="808fb-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="808fb-117">See also</span></span>



[<span data-ttu-id="808fb-118">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="808fb-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

