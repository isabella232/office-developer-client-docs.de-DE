---
title: Funktionen in allgemeinen DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generische dll [Excel 2007], Funktionen, Funktionen [Excel 2007], generische DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304088"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="e0f41-104">Funktionen in allgemeinen DLL</span><span class="sxs-lookup"><span data-stu-id="e0f41-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="e0f41-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e0f41-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e0f41-106">Der Ordner `\EXAMPLES\GENERIC\` enthält Microsoft Visual Studio-Projektdateien und Quellcodedateien, die zum Kompilieren der Beispiel-dll Generic. XLL benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="e0f41-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="e0f41-107">Sie können dieses Projekt als Vorlage zum Schreiben eigener Microsoft Excel-XLLs verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0f41-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="e0f41-108">Der Quellcode in diesem Projekt demonstriert viele der Features der Excel C-API.</span><span class="sxs-lookup"><span data-stu-id="e0f41-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="e0f41-109">Wenn Sie generische. XLL laden, wird ein neues **generisches** Menü mit vier Befehlen erstellt:</span><span class="sxs-lookup"><span data-stu-id="e0f41-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="e0f41-110">**Dialog** -zeigt ein Microsoft Excel-Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="e0f41-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="e0f41-111">**Dance** -verschiebt die Auswahl um, bis Sie die **ESC** -Taste drücken.</span><span class="sxs-lookup"><span data-stu-id="e0f41-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="e0f41-112">**Native Dialog** – zeigt ein Windows-Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="e0f41-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="e0f41-113">**Exit** -entlädt generische. XLL und entfernt das **generische** Menü.</span><span class="sxs-lookup"><span data-stu-id="e0f41-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="e0f41-114">GENERISCHE. XLL stellt auch drei Arbeitsblattfunktionen, func1, FuncSum und FuncFib, die verwendet werden können, wenn generische. XLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e0f41-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="e0f41-115">GENERISCHE. XLL kann mit dem Add-in-Manager geladen werden, oder Sie wird geladen, wenn Sie am normalen Ende der letzten Excel-Sitzung aktiv war.</span><span class="sxs-lookup"><span data-stu-id="e0f41-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="e0f41-116">Dieses Projekt verwendet die Framework-Bibliothek (FRMWRK32. lib).</span><span class="sxs-lookup"><span data-stu-id="e0f41-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="e0f41-117">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="e0f41-117">In this section</span></span>

[<span data-ttu-id="e0f41-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="e0f41-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="e0f41-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="e0f41-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="e0f41-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="e0f41-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="e0f41-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="e0f41-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="e0f41-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="e0f41-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="e0f41-123">fDance</span><span class="sxs-lookup"><span data-stu-id="e0f41-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="e0f41-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="e0f41-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="e0f41-125">fExit</span><span class="sxs-lookup"><span data-stu-id="e0f41-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="e0f41-126">Func1</span><span class="sxs-lookup"><span data-stu-id="e0f41-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="e0f41-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="e0f41-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="e0f41-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="e0f41-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="e0f41-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0f41-129">See also</span></span>



[<span data-ttu-id="e0f41-130">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="e0f41-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

