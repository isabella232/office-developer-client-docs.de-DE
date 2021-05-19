---
title: EVALCELL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Verwendet einen Verweis auf eine Zelle, die eine benutzerdefinierte Funktion enthält, sowie ein oder mehrere Name-Wert-Paare, die als Argumente an die benutzerdefinierte Funktion übergeben werden (optional). Gibt das berechnete Ergebnis der benutzerdefinierten Funktion mit den angegebenen Argumenten und Werten zurück.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418904"
---
# <a name="evalcell-function"></a><span data-ttu-id="95bf4-104">EVALCELL Function</span><span class="sxs-lookup"><span data-stu-id="95bf4-104">EVALCELL Function</span></span>

<span data-ttu-id="95bf4-105">Verwendet einen Verweis auf eine Zelle, die eine benutzerdefinierte Funktion enthält, sowie ein oder mehrere Name-Wert-Paare, die als Argumente an die benutzerdefinierte Funktion übergeben werden (optional).</span><span class="sxs-lookup"><span data-stu-id="95bf4-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="95bf4-106">Gibt das berechnete Ergebnis der benutzerdefinierten Funktion mit den angegebenen Argumenten und Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="95bf4-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="95bf4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="95bf4-107">Syntax</span></span>

<span data-ttu-id="95bf4-108">EVALCELL(\*\* *cellRef* \*\*,[ \*\* *arg1Name,arg1* \*\* ],[ \*\* *arg2Name,arg2* \*\* ],...)</span><span class="sxs-lookup"><span data-stu-id="95bf4-108">EVALCELL(\*\* *cellRef* \*\*,[ \*\* *arg1Name,arg1* \*\* ],[ \*\* *arg2Name,arg2* \*\* ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="95bf4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="95bf4-109">Parameters</span></span>

|<span data-ttu-id="95bf4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="95bf4-110">**Name**</span></span>|<span data-ttu-id="95bf4-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="95bf4-111">**Required/Optional**</span></span>|<span data-ttu-id="95bf4-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="95bf4-112">**Data Type**</span></span>|<span data-ttu-id="95bf4-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95bf4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="95bf4-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="95bf4-114">_cellRef_</span></span> <br/> |<span data-ttu-id="95bf4-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="95bf4-115">Required</span></span>  <br/> |<span data-ttu-id="95bf4-116">**String**</span><span class="sxs-lookup"><span data-stu-id="95bf4-116">**String**</span></span> <br/> |<span data-ttu-id="95bf4-117">Ein Bezug auf die Zelle, die die benutzerdefinierte Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="95bf4-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="95bf4-118">Tabellenübergreifende Bezüge sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="95bf4-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="95bf4-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="95bf4-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="95bf4-120">Optional</span><span class="sxs-lookup"><span data-stu-id="95bf4-120">Optional</span></span>  <br/> |<span data-ttu-id="95bf4-121">**String**</span><span class="sxs-lookup"><span data-stu-id="95bf4-121">**String**</span></span> <br/> |<span data-ttu-id="95bf4-p104">Der Name des ersten Arguments, das an die benutzerdefinierte Funktion übergeben wird. Leerzeichen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="95bf4-p104">The name of the first argument to be passed to the custom function. Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="95bf4-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="95bf4-124">_arg1_</span></span> <br/> |<span data-ttu-id="95bf4-125">Optional.</span><span class="sxs-lookup"><span data-stu-id="95bf4-125">Optional</span></span>  <br/> |<span data-ttu-id="95bf4-126">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="95bf4-126">**Varies**</span></span> <br/> |<span data-ttu-id="95bf4-127">Wert des _arg1-Parameters._</span><span class="sxs-lookup"><span data-stu-id="95bf4-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="95bf4-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="95bf4-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="95bf4-129">Optional</span><span class="sxs-lookup"><span data-stu-id="95bf4-129">Optional</span></span>  <br/> |<span data-ttu-id="95bf4-130">**String**</span><span class="sxs-lookup"><span data-stu-id="95bf4-130">**String**</span></span> <br/> |<span data-ttu-id="95bf4-131">Der Name des zweiten Arguments, das an die benutzerdefinierte Funktion übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="95bf4-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="95bf4-132">Leerzeichen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="95bf4-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="95bf4-133">_arg2_</span><span class="sxs-lookup"><span data-stu-id="95bf4-133">_arg2_</span></span> <br/> |<span data-ttu-id="95bf4-134">Optional.</span><span class="sxs-lookup"><span data-stu-id="95bf4-134">Optional</span></span>  <br/> |<span data-ttu-id="95bf4-135">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="95bf4-135">**Varies**</span></span> <br/> |<span data-ttu-id="95bf4-136">Wert des _arg2-Parameters._</span><span class="sxs-lookup"><span data-stu-id="95bf4-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="95bf4-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95bf4-137">Return value</span></span>

<span data-ttu-id="95bf4-138">Nummer</span><span class="sxs-lookup"><span data-stu-id="95bf4-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95bf4-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="95bf4-139">Remarks</span></span>

<span data-ttu-id="95bf4-140">In der aufrufenden Zelle muss nicht jedes von der benutzerdefinierten Funktion verwendete Argument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="95bf4-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="95bf4-141">Beispiel</span><span class="sxs-lookup"><span data-stu-id="95bf4-141">Example</span></span>

<span data-ttu-id="95bf4-142">Im folgenden Beispiel wird gezeigt, wie Sie mit der EVALCELL-Funktion in Verbindung mit der ARG-Funktion den Mittelwert aus einer Menge von drei Werte finden.</span><span class="sxs-lookup"><span data-stu-id="95bf4-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="95bf4-143">Fügen Sie in die Ausdruckszelle den folgenden Code ein, der die benutzerdefinierte Funktion definiert:</span><span class="sxs-lookup"><span data-stu-id="95bf4-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="95bf4-144">Fügen Sie in die aufrufenden Zellen den folgenden Code ein, der die benutzerdefinierte Funktion aufruft:</span><span class="sxs-lookup"><span data-stu-id="95bf4-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


