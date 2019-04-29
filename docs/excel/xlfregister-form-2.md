---
title: xlfRegister (Formular 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfRegister-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416041"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="a0d7f-104">xlfRegister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="a0d7f-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="a0d7f-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a0d7f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a0d7f-106">Kann von einem DLL-oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a0d7f-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="a0d7f-107">Dies entspricht dem Aufrufen von **Register** aus einer Excel-XML-Makrovorlage.</span><span class="sxs-lookup"><span data-stu-id="a0d7f-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="a0d7f-108">Die **xlfRegister** -Funktion kann in zwei Formen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="a0d7f-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="a0d7f-109">[xlfRegister (Formular 1)](xlfregister-form-1.md): registriert einen einzelnen Befehl oder eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="a0d7f-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="a0d7f-110">xlfRegister (Formular 2): lädt und aktiviert eine XLL.</span><span class="sxs-lookup"><span data-stu-id="a0d7f-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="a0d7f-111">Diese Funktion kann nur zum Laden und Aktivieren einer XLL mit einer [xlAutoOpen](xlautoopen.md) -Prozedur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0d7f-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="a0d7f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0d7f-112">Parameters</span></span>

 <span data-ttu-id="a0d7f-113">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="a0d7f-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="a0d7f-114">Der Name der DLL, die geladen und aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0d7f-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a0d7f-115">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0d7f-115">Property value/Return value</span></span>

<span data-ttu-id="a0d7f-116">Bei erfolgreicher Ausführung gibt dieser Wert den Namen der DLL (**xltypeStr**) zurück.</span><span class="sxs-lookup"><span data-stu-id="a0d7f-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="a0d7f-117">Andernfalls wird ein #VALUE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0d7f-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="a0d7f-118">zurück.</span><span class="sxs-lookup"><span data-stu-id="a0d7f-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0d7f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0d7f-119">See also</span></span>



[<span data-ttu-id="a0d7f-120">Wichtige und nützliche C-API-XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a0d7f-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

