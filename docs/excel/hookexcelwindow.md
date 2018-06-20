---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- Hookexcelwindow-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790514"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="06233-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="06233-104">HookExcelWindow</span></span>

 <span data-ttu-id="06233-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="06233-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="06233-106">Wird **ExcelCursorProc** installiert, sodass sie vor dem Hauptfenster **WndProc**Microsoft Excel aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="06233-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="06233-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="06233-107">Parameters</span></span>

 <span data-ttu-id="06233-108">_hWndExcel_ (**BEHANDELN**)</span><span class="sxs-lookup"><span data-stu-id="06233-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="06233-109">Die wichtigsten Excel-Fenster behandeln.</span><span class="sxs-lookup"><span data-stu-id="06233-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="06233-110">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06233-110">Property value/Return value</span></span>

<span data-ttu-id="06233-111">Die Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="06233-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06233-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06233-112">Remarks</span></span>

<span data-ttu-id="06233-113">Die Funktion erhält die Adresse des Excel **WndProc** durch Verwendung **GetWindowLong()**.</span><span class="sxs-lookup"><span data-stu-id="06233-113">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**.</span></span> <span data-ttu-id="06233-114">Speichert diesen Wert in ein globales, die das **WndProc** aufrufen und auch wiederherstellen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="06233-114">It stores this value in a global that can be used to call the default **WndProc** and also to restore it.</span></span> <span data-ttu-id="06233-115">Schließlich wird diese Adresse mit der Adresse des **ExcelCursorProc** mit **SetWindowLong()** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="06233-115">Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="06233-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="06233-116">Example</span></span>

<span data-ttu-id="06233-117">Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="06233-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06233-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06233-118">See also</span></span>



[<span data-ttu-id="06233-119">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="06233-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

