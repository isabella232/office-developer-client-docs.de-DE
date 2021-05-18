---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- xlfsetname-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404260"
---
# <a name="xlfsetname"></a><span data-ttu-id="43892-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="43892-104">xlfSetName</span></span>

<span data-ttu-id="43892-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="43892-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="43892-106">Wird verwendet, um der DLL zugeordnete definierte Namen zu erstellen und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="43892-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="43892-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="43892-107">Parameters</span></span>

<span data-ttu-id="43892-108">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="43892-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="43892-109">Der Name des Bereichs, der den üblichen Einschränkungen in der Microsoft Excel gültigen Namen entsprechen sollte.</span><span class="sxs-lookup"><span data-stu-id="43892-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="43892-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef** oder **xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="43892-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="43892-111">(Optional).</span><span class="sxs-lookup"><span data-stu-id="43892-111">(Optional).</span></span> <span data-ttu-id="43892-112">Der Wert, der Wertesatz, die Zelle oder der Zellbereich, als  _die pxNameText_ definiert ist.</span><span class="sxs-lookup"><span data-stu-id="43892-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="43892-113">Wenn sie nicht angegeben wird, wird der Name gelöscht.</span><span class="sxs-lookup"><span data-stu-id="43892-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="43892-114">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43892-114">Property value/Return value</span></span>

<span data-ttu-id="43892-115">_pxRes_ (**xltypeBool** oder **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="43892-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="43892-116">TRUE, wenn der Vorgang erfolgreich war, oder FALSE, wenn der Name nicht erstellt oder gelöscht werden konnte.</span><span class="sxs-lookup"><span data-stu-id="43892-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="43892-117">Gibt #VALUE!</span><span class="sxs-lookup"><span data-stu-id="43892-117">Returns #VALUE!</span></span> <span data-ttu-id="43892-118">wenn mindestens eines der Argumente ungültig war.</span><span class="sxs-lookup"><span data-stu-id="43892-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43892-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="43892-119">Remarks</span></span>

<span data-ttu-id="43892-120">Wenn eine Funktion oder ein Befehl mithilfe von **xlfRegister** mit einem gültigen _pxFunctionText-Argument_ registriert wird, erstellt Excel einen Namen, der der DLL-Ressource zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="43892-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="43892-121">Wenn Ihre DLL entladen wird, sollten diese Namen mit der [xlfSetName-Funktion gelöscht werden.](xlfsetname.md)</span><span class="sxs-lookup"><span data-stu-id="43892-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="43892-122">Aufgrund eines bekannten Problems in Excel fehler dieser Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="43892-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="43892-123">Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="43892-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="43892-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="43892-124">Example</span></span>

<span data-ttu-id="43892-125">Weitere Informationen finden Sie im Code für die **xlAutoClose-Funktion** in  `\SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="43892-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43892-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43892-126">See also</span></span>

- [<span data-ttu-id="43892-127">Wichtige und nützliche C-API-XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="43892-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

