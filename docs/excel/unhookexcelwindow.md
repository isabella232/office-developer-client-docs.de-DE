---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- Unhookexcelwindow-Funktion
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790582"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="a890d-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="a890d-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="a890d-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a890d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a890d-106">Entfernt die **ExcelCursorProc** , die zuvor durch **HookExcelWindow**installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a890d-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="a890d-107">Dies würde ausgeführt werden, damit **ExcelCursorProc** vor der wichtigsten **WndProc**von Microsoft Excel aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a890d-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="a890d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a890d-108">Parameters</span></span>

 <span data-ttu-id="a890d-109">_hWndExcel_ (**BEHANDELN**)</span><span class="sxs-lookup"><span data-stu-id="a890d-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="a890d-110">Die wichtigsten Excel-Fenster behandeln.</span><span class="sxs-lookup"><span data-stu-id="a890d-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a890d-111">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a890d-111">Property value/Return value</span></span>

<span data-ttu-id="a890d-112">Die Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a890d-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a890d-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a890d-113">Remarks</span></span>

<span data-ttu-id="a890d-114">Diese Funktion stellt Excel standardmäßig **WndProc** wiederherstellen die Adresse, die von **HookExcelWindow()** gespeichert wurde mithilfe von **SetWindowLong()** wieder her.</span><span class="sxs-lookup"><span data-stu-id="a890d-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="a890d-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a890d-115">Example</span></span>

<span data-ttu-id="a890d-116">Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="a890d-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a890d-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a890d-117">See also</span></span>



[<span data-ttu-id="a890d-118">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="a890d-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

