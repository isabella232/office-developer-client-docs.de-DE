---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- Excelcursorproc-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790495"
---
# <a name="excelcursorproc"></a><span data-ttu-id="20e5a-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="20e5a-104">ExcelCursorProc</span></span>

 <span data-ttu-id="20e5a-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="20e5a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="20e5a-106">Wenn ein modales Dialogfeld über das Microsoft Excel-Fenster angezeigt wird, ist der Cursor Mauszeiger über das Excel-Fenster.</span><span class="sxs-lookup"><span data-stu-id="20e5a-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="20e5a-107">Diese **WndProc** Traps WM_SETCURSOR Geben Sie Windows-Nachrichten und ändert sich der Mauszeiger in einen normalen Pfeil sichern.</span><span class="sxs-lookup"><span data-stu-id="20e5a-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="20e5a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="20e5a-108">Parameters</span></span>

 <span data-ttu-id="20e5a-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="20e5a-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="20e5a-110">Enthält das HWND Windows Handle des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="20e5a-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="20e5a-111">_Nachricht_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="20e5a-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="20e5a-112">Die Nachricht zu antworten.</span><span class="sxs-lookup"><span data-stu-id="20e5a-112">The message to respond to.</span></span>
  
 <span data-ttu-id="20e5a-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="20e5a-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="20e5a-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="20e5a-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="20e5a-115">Durch Windows übergebene Argumente.</span><span class="sxs-lookup"><span data-stu-id="20e5a-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="20e5a-116">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20e5a-116">Property value/Return value</span></span>

<span data-ttu-id="20e5a-117">LRESULT: 0, wenn die Meldung behandelt wurde, zurückgegeben, andernfalls das Ergebnis standardmäßig **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="20e5a-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="20e5a-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="20e5a-118">Example</span></span>

<span data-ttu-id="20e5a-119">Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="20e5a-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20e5a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20e5a-120">See also</span></span>



[<span data-ttu-id="20e5a-121">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="20e5a-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

