---
title: Funktionen in der generische DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generische Dll [excel 2007], Funktionen, Funktionen [Excel 2007], generische DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790521"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="fd7a1-104">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="fd7a1-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="fd7a1-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fd7a1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fd7a1-106">Der Ordner `\EXAMPLES\GENERIC\` enthält Microsoft Visual Studio-Projektdateien und Quellcodedateien, die erforderlich sind, um das Beispiel GENERIC.xll DLL zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="fd7a1-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="fd7a1-107">Sie können dieses Projekt als Vorlage verwenden, für das Schreiben von eigenen Microsoft Excel-XLLs.</span><span class="sxs-lookup"><span data-stu-id="fd7a1-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="fd7a1-108">Der Quellcode in diesem Projekt werden viele der Funktionen von Excel-C-API veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fd7a1-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="fd7a1-109">Wenn Sie GENERIC.xll laden, wird mit vier Befehle **generische** im Menü neues erstellt:</span><span class="sxs-lookup"><span data-stu-id="fd7a1-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="fd7a1-110">**Dialogfeld** - ein Microsoft Excel-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd7a1-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="fd7a1-111">**Tanz** - verschiebt die Auswahl um, bis Sie die **ESC** -Taste drücken.</span><span class="sxs-lookup"><span data-stu-id="fd7a1-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="fd7a1-112">**Systemeigene Dialogfeld** - ein Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd7a1-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="fd7a1-113">**Exit** - entlädt GENERIC.xll, und klicken Sie im Menü **generische** entfernt.</span><span class="sxs-lookup"><span data-stu-id="fd7a1-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="fd7a1-114">GENERIC.xll bietet auch drei Tabellenfunktionen, Func1, FuncSum und FuncFib, die verwendet werden kann, wenn GENERIC.xll geladen wird.</span><span class="sxs-lookup"><span data-stu-id="fd7a1-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="fd7a1-115">GENERIC.xll können mit dem Add-In-Manager geladen werden, oder es wird geladen, wenn es am Ende der letzten Excel-Sitzung normalen aktiv war.</span><span class="sxs-lookup"><span data-stu-id="fd7a1-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="fd7a1-116">Dieses Projekt wird der Framework-Klassenbibliothek (FRMWRK32.lib) verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd7a1-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="fd7a1-117">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="fd7a1-117">In this section</span></span>

[<span data-ttu-id="fd7a1-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="fd7a1-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="fd7a1-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="fd7a1-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="fd7a1-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="fd7a1-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="fd7a1-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="fd7a1-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="fd7a1-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="fd7a1-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="fd7a1-123">fDance</span><span class="sxs-lookup"><span data-stu-id="fd7a1-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="fd7a1-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="fd7a1-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="fd7a1-125">fExit</span><span class="sxs-lookup"><span data-stu-id="fd7a1-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="fd7a1-126">Func1</span><span class="sxs-lookup"><span data-stu-id="fd7a1-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="fd7a1-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="fd7a1-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="fd7a1-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="fd7a1-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="fd7a1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd7a1-129">See also</span></span>



[<span data-ttu-id="fd7a1-130">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="fd7a1-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

