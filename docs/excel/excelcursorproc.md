---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- excelcursorproc-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432492"
---
# <a name="excelcursorproc"></a><span data-ttu-id="9897e-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="9897e-104">ExcelCursorProc</span></span>

 <span data-ttu-id="9897e-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9897e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9897e-106">Wenn ein modales Dialogfeld über das Microsoft Excel-Fenster angezeigt wird, ist der Cursor ein Beschäftigter Cursor über das Excel-Fenster.</span><span class="sxs-lookup"><span data-stu-id="9897e-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="9897e-107">Dieser **WndProc** -Traps WM_SETCURSOR Windows-Meldungen und ändert den Cursor zurück zu einem normalen Pfeil.</span><span class="sxs-lookup"><span data-stu-id="9897e-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="9897e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9897e-108">Parameters</span></span>

 <span data-ttu-id="9897e-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="9897e-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="9897e-110">Enthält das HWND-Windows-Handle des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="9897e-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="9897e-111">_Nachricht_ (**Uint**)</span><span class="sxs-lookup"><span data-stu-id="9897e-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="9897e-112">Die Nachricht, auf die geantwortet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9897e-112">The message to respond to.</span></span>
  
 <span data-ttu-id="9897e-113">_wParam_ (**WParam**)</span><span class="sxs-lookup"><span data-stu-id="9897e-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="9897e-114">_LPARAM_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="9897e-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="9897e-115">Von Windows übergebene Argumente.</span><span class="sxs-lookup"><span data-stu-id="9897e-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9897e-116">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9897e-116">Property value/Return value</span></span>

<span data-ttu-id="9897e-117">LRESULT: 0, wenn die Nachricht behandelt wurde, andernfalls das von der Standard- **WndProc**-Objekt zurückgegebene Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="9897e-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="9897e-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9897e-118">Example</span></span>

<span data-ttu-id="9897e-119">Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="9897e-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9897e-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9897e-120">See also</span></span>



[<span data-ttu-id="9897e-121">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="9897e-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

