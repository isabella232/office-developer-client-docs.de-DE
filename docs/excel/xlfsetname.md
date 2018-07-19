---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- XlfSetName-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790595"
---
# <a name="xlfsetname"></a><span data-ttu-id="1fef4-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="1fef4-104">xlfSetName</span></span>

<span data-ttu-id="1fef4-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1fef4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1fef4-106">Verwendet zum Erstellen und Löschen von definierten Namen der DLL zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1fef4-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="1fef4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fef4-107">Parameters</span></span>

<span data-ttu-id="1fef4-108">_pxNameText_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="1fef4-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="1fef4-109">Der Name des Bereichs, die der üblichen eingeschränkten in Microsoft Excel gültigen Namen entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="1fef4-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="1fef4-110">_pxNameDefinition_ (**XltypeStr**, **XltypeNum**, **XltypeBool**, **XltypeErr**, **XltypeMulti**, **XltypeSRef**, **XltypeRef**oder **vom Typ XltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="1fef4-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="1fef4-111">(Optional).</span><span class="sxs-lookup"><span data-stu-id="1fef4-111">(Optional).</span></span> <span data-ttu-id="1fef4-112">Der Wert, den Satz von Werten, Zelle oder einen Zellbereich ist als dieser _PxNameText_ definiert.</span><span class="sxs-lookup"><span data-stu-id="1fef4-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="1fef4-113">Wenn Length angegeben, wird der Name gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1fef4-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1fef4-114">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fef4-114">Property value/Return value</span></span>

<span data-ttu-id="1fef4-115">_pxRes_ (**XltypeBool** oder **XltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="1fef4-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="1fef4-116">True, wenn der Vorgang erfolgreich war oder FALSE, wenn der Name nicht erstellt oder gelöscht werden konnte.</span><span class="sxs-lookup"><span data-stu-id="1fef4-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="1fef4-117">Gibt #VALUE!</span><span class="sxs-lookup"><span data-stu-id="1fef4-117">Returns #VALUE!</span></span> <span data-ttu-id="1fef4-118">Wenn eine oder mehrere der Argumente ungültig war.</span><span class="sxs-lookup"><span data-stu-id="1fef4-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1fef4-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1fef4-119">Remarks</span></span>

<span data-ttu-id="1fef4-120">Wenn eine Funktion oder einen Befehl mit einem gültigen _PxFunctionText_ -Argument **XlfRegister** verwenden registriert ist, erstellt Excel einen Namen der DLL-Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1fef4-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="1fef4-121">Die DLL entladen wird, sollten diese Namen mit der [Funktion XlfSetName](xlfsetname.md)gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1fef4-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="1fef4-122">Jedoch aufgrund ein bekanntes Problem in Excel schlägt dieser Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="1fef4-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="1fef4-123">Weitere Informationen finden Sie unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="1fef4-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="1fef4-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1fef4-124">Example</span></span>

<span data-ttu-id="1fef4-125">Finden Sie im Code die Funktion **XlAutoClose** in `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="1fef4-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1fef4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fef4-126">See also</span></span>

- [<span data-ttu-id="1fef4-127">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1fef4-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

