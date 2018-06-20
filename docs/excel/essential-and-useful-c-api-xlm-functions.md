---
title: Wichtige und nützliche C-API XLM-Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Funktionen [excel 2007], C-API-xlm
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 410a6009bf6bbb8146dcc1354e7f5688c28d96c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790416"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="9abf3-104">Wichtige und nützliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9abf3-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="9abf3-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9abf3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9abf3-106">In diesem Abschnitt beschriebenen Funktionen handelt es sich um Microsoft Excel Callback-Funktionen, die besonders nützlich, um die DLL und XLL-Entwickler sind.</span><span class="sxs-lookup"><span data-stu-id="9abf3-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="9abf3-107">Dieser ist die Funktion **XlfRegister** unverzichtbar für XLLs und DLLs, die zu ihren Funktionen und Befehle zu registrieren, sodass sie direkt in Excel aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="9abf3-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="9abf3-108">Die Funktionen **XlfUnregister** und **XlfSetName** in Kombination dienen zum Aufheben der Registrierung DLL und XLL-Funktionen und Befehle.</span><span class="sxs-lookup"><span data-stu-id="9abf3-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="9abf3-109">Viele weitere Funktionen werden von Excel über die C-API, die bei der Entwicklung von XLLs nützlich sind verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="9abf3-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="9abf3-110">Excel-Arbeitsblatt entsprechen Funktionen und die Funktionen und Befehle, die von XLM-Makrovorlagen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9abf3-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="9abf3-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="9abf3-111">In this section</span></span>

[<span data-ttu-id="9abf3-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="9abf3-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="9abf3-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="9abf3-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="9abf3-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="9abf3-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="9abf3-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="9abf3-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="9abf3-116">XlfRegister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="9abf3-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="9abf3-117">XlfRegister (Form 2)</span><span class="sxs-lookup"><span data-stu-id="9abf3-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="9abf3-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="9abf3-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="9abf3-119">XlfUnregister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="9abf3-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="9abf3-120">XlfUnregister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="9abf3-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="9abf3-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="9abf3-121">xlfSetName</span></span>](xlfsetname.md)
  

