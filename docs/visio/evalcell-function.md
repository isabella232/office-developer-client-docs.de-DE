---
title: EVALCELL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Übernimmt einen Verweis auf eine Zelle, die eine benutzerdefinierte Funktion enthält als auch eine oder mehrere Name / Wert-Paare an die benutzerdefinierte Funktion als Argumente (optional) übergeben. Gibt das berechnete Ergebnis der benutzerdefinierten Funktion mit den angegebenen Argumenten und Werten zurück.
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796942"
---
# <a name="evalcell-function"></a><span data-ttu-id="bfa5d-104">EVALCELL Function</span><span class="sxs-lookup"><span data-stu-id="bfa5d-104">EVALCELL Function</span></span>

<span data-ttu-id="bfa5d-105">Übernimmt einen Verweis auf eine Zelle, die eine benutzerdefinierte Funktion enthält als auch eine oder mehrere Name / Wert-Paare an die benutzerdefinierte Funktion als Argumente (optional) übergeben.</span><span class="sxs-lookup"><span data-stu-id="bfa5d-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="bfa5d-106">Gibt das berechnete Ergebnis der benutzerdefinierten Funktion mit den angegebenen Argumenten und Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="bfa5d-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bfa5d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfa5d-107">Syntax</span></span>

<span data-ttu-id="bfa5d-108">EVALCELL (** *CellRef* **, [** *arg1Name, arg1* **], [** *arg2Name, arg2* **],...)</span><span class="sxs-lookup"><span data-stu-id="bfa5d-108">EVALCELL(** *cellRef* **,[ ** *arg1Name,arg1* ** ],[ ** *arg2Name,arg2* ** ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bfa5d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfa5d-109">Parameters</span></span>

|<span data-ttu-id="bfa5d-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="bfa5d-110">**Name**</span></span>|<span data-ttu-id="bfa5d-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="bfa5d-111">**Required/Optional**</span></span>|<span data-ttu-id="bfa5d-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="bfa5d-112">**Data Type**</span></span>|<span data-ttu-id="bfa5d-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfa5d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bfa5d-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="bfa5d-114">_cellRef_</span></span> <br/> |<span data-ttu-id="bfa5d-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="bfa5d-115">Required</span></span>  <br/> |<span data-ttu-id="bfa5d-116">**String**</span><span class="sxs-lookup"><span data-stu-id="bfa5d-116">**String**</span></span> <br/> |<span data-ttu-id="bfa5d-117">Ein Verweis auf die Zelle, die benutzerdefinierte Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="bfa5d-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="bfa5d-118">Blattübergreifende Verweise sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="bfa5d-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="bfa5d-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="bfa5d-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="bfa5d-120">Optional</span><span class="sxs-lookup"><span data-stu-id="bfa5d-120">Optional</span></span>  <br/> |<span data-ttu-id="bfa5d-121">**String**</span><span class="sxs-lookup"><span data-stu-id="bfa5d-121">**String**</span></span> <br/> |<span data-ttu-id="bfa5d-p104">Der Name des ersten Arguments, das an die benutzerdefinierte Funktion übergeben wird. Leerzeichen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="bfa5d-p104">The name of the first argument to be passed to the custom function. Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="bfa5d-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="bfa5d-124">_arg1_</span></span> <br/> |<span data-ttu-id="bfa5d-125">Optional</span><span class="sxs-lookup"><span data-stu-id="bfa5d-125">Optional</span></span>  <br/> |<span data-ttu-id="bfa5d-126">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="bfa5d-126">**Varies**</span></span> <br/> |<span data-ttu-id="bfa5d-127">Der Wert des Parameters _arg1_ .</span><span class="sxs-lookup"><span data-stu-id="bfa5d-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="bfa5d-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="bfa5d-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="bfa5d-129">Optional</span><span class="sxs-lookup"><span data-stu-id="bfa5d-129">Optional</span></span>  <br/> |<span data-ttu-id="bfa5d-130">**String**</span><span class="sxs-lookup"><span data-stu-id="bfa5d-130">**String**</span></span> <br/> |<span data-ttu-id="bfa5d-131">Der Name des zweiten Arguments an die benutzerdefinierte Funktion übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bfa5d-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="bfa5d-132">Leerzeichen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="bfa5d-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="bfa5d-133">_Arg2_</span><span class="sxs-lookup"><span data-stu-id="bfa5d-133">_arg2_</span></span> <br/> |<span data-ttu-id="bfa5d-134">Optional</span><span class="sxs-lookup"><span data-stu-id="bfa5d-134">Optional</span></span>  <br/> |<span data-ttu-id="bfa5d-135">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="bfa5d-135">**Varies**</span></span> <br/> |<span data-ttu-id="bfa5d-136">Der Wert des Parameters _arg2_ .</span><span class="sxs-lookup"><span data-stu-id="bfa5d-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bfa5d-137">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="bfa5d-137">Return value</span></span>

<span data-ttu-id="bfa5d-138">Zahl</span><span class="sxs-lookup"><span data-stu-id="bfa5d-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bfa5d-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfa5d-139">Remarks</span></span>

<span data-ttu-id="bfa5d-140">In der aufrufenden Zelle muss nicht jedes von der benutzerdefinierten Funktion verwendete Argument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bfa5d-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bfa5d-141">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bfa5d-141">Example</span></span>

<span data-ttu-id="bfa5d-142">Im folgenden Beispiel wird gezeigt, wie Sie mit der EVALCELL-Funktion in Verbindung mit der ARG-Funktion den Mittelwert aus einer Menge von drei Werte finden.</span><span class="sxs-lookup"><span data-stu-id="bfa5d-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="bfa5d-143">Fügen Sie in die Ausdruckszelle den folgenden Code ein, der die benutzerdefinierte Funktion definiert:</span><span class="sxs-lookup"><span data-stu-id="bfa5d-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="bfa5d-144">Fügen Sie in die aufrufenden Zellen den folgenden Code ein, der die benutzerdefinierte Funktion aufruft:</span><span class="sxs-lookup"><span data-stu-id="bfa5d-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


