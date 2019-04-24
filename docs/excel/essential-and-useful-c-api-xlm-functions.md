---
title: Wichtige und nützliche C-API-XML-Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Funktionen [Excel 2007], c-API-XML-Code
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d6acd5bb171fb2494f2adb23584f4e7f088e1b83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311123"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="55287-104">Wichtige und nützliche C-API-XML-Funktionen</span><span class="sxs-lookup"><span data-stu-id="55287-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="55287-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="55287-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="55287-106">Die in diesem Abschnitt beschriebenen Funktionen sind Microsoft Excel-Rückruffunktionen, die für DLL-und XLL-Entwickler besonders nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="55287-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="55287-107">Von diesen ist die **xlfRegister** -Funktion für XLLs und DLLs unerlässlich, die ihre Funktionen und Befehle registrieren möchten, damit Sie direkt aus Excel aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="55287-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="55287-108">Die Funktionen **xlfUnregister** und **xlfSetName** werden in Kombination mit dem aufHEBEN der Registrierung von dll-und XLL-Funktionen und-Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="55287-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="55287-109">Viele weitere Funktionen werden von Excel über die C-API zur Verfügung gestellt, die beim Entwickeln von XLLs nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="55287-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="55287-110">Sie entsprechen den Excel-Arbeitsblattfunktionen und-Funktionen und Befehlen, die in XML-Makro Blättern zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="55287-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="55287-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="55287-111">In this section</span></span>

[<span data-ttu-id="55287-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="55287-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="55287-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="55287-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="55287-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="55287-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="55287-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="55287-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="55287-116">xlfRegister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="55287-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="55287-117">xlfRegister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="55287-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="55287-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="55287-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="55287-119">xlfUnregister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="55287-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="55287-120">xlfUnregister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="55287-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="55287-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="55287-121">xlfSetName</span></span>](xlfsetname.md)
  

