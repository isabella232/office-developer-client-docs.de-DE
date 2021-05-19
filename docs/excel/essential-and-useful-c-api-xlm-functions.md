---
title: Wichtige und nützliche C-API-XLM-Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funktionen [excel 2007], c api xlm
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d6acd5bb171fb2494f2adb23584f4e7f088e1b83
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434515"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="b171a-104">Wichtige und nützliche C-API-XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="b171a-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="b171a-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b171a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b171a-106">Die in diesem Abschnitt beschriebenen Funktionen sind Microsoft Excel Rückruffunktionen, die für DLL- und XLL-Entwickler besonders nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="b171a-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="b171a-107">Davon ist **die xlfRegister-Funktion** für XLLs und DLLs, die ihre Funktionen und Befehle registrieren möchten, wichtig, damit sie direkt von der Excel.</span><span class="sxs-lookup"><span data-stu-id="b171a-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="b171a-108">Die Funktionen **xlfUnregister und** **xlfSetName** werden in Kombination zum Aufheben der Registrierung von DLL- und XLL-Funktionen und -Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b171a-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="b171a-109">Viele weitere Funktionen werden von Excel über die C-API verfügbar gemacht, die beim Entwickeln von XLLs hilfreich sind.</span><span class="sxs-lookup"><span data-stu-id="b171a-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="b171a-110">Sie entsprechen den Excel funktionen und Befehlen des Arbeitsblatts, die in XLM-Makroblättern verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b171a-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="b171a-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="b171a-111">In this section</span></span>

[<span data-ttu-id="b171a-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="b171a-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="b171a-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="b171a-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="b171a-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="b171a-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="b171a-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="b171a-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="b171a-116">xlfRegister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="b171a-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="b171a-117">xlfRegister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="b171a-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="b171a-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="b171a-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="b171a-119">xlfUnregister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="b171a-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="b171a-120">xlfUnregister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="b171a-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="b171a-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="b171a-121">xlfSetName</span></span>](xlfsetname.md)
  

