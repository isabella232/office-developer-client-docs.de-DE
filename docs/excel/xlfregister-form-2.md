---
title: XlfRegister (Form 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- XlfRegister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790596"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="98129-104">XlfRegister (Form 2)</span><span class="sxs-lookup"><span data-stu-id="98129-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="98129-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="98129-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="98129-106">Kann aus einem Befehl DLL oder XLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="98129-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="98129-107">Dies ist gleichbedeutend mit dem **Registrieren** aus einer Excel-XLM-Makrovorlage.</span><span class="sxs-lookup"><span data-stu-id="98129-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="98129-108">Die Funktion **XlfRegister** kann in zwei Formen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="98129-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="98129-109">[XlfRegister (Formular 1)](xlfregister-form-1.md): registriert einen einzelnen Befehl oder eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="98129-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="98129-110">XlfRegister (Form 2): Lasten und aktiviert eine XLL.</span><span class="sxs-lookup"><span data-stu-id="98129-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="98129-111">In Form 2 aufgerufen wird, kann diese Funktion nur verwendet werden zum Laden und aktivieren eine XLL, eine Prozedur [XlAutoOpen](xlautoopen.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="98129-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="98129-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="98129-112">Parameters</span></span>

 <span data-ttu-id="98129-113">_pxModuleText_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="98129-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="98129-114">Der Name der DLL geladen und aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="98129-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="98129-115">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98129-115">Property value/Return value</span></span>

<span data-ttu-id="98129-116">Bei erfolgreicher zurückgegeben dies der Name der DLL (**XltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="98129-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="98129-117">Andernfalls gibt es eine #VALUE!</span><span class="sxs-lookup"><span data-stu-id="98129-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="98129-118">Fehler.</span><span class="sxs-lookup"><span data-stu-id="98129-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98129-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98129-119">See also</span></span>



[<span data-ttu-id="98129-120">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="98129-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

