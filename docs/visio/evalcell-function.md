---
title: EVALCELL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Ruft einen Verweis auf eine Zelle ab, die eine benutzerdefinierte Funktion enthält, sowie ein oder mehrere Name-Wert-Paare, die an die benutzerdefinierte Funktion als Argumente übergeben werden (optional). Gibt das berechnete Ergebnis der benutzerdefinierten Funktion bei den angegebenen Argumenten und Werten zurück.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418904"
---
# <a name="evalcell-function"></a><span data-ttu-id="3de2f-104">EVALCELL Function</span><span class="sxs-lookup"><span data-stu-id="3de2f-104">EVALCELL Function</span></span>

<span data-ttu-id="3de2f-105">Ruft einen Verweis auf eine Zelle ab, die eine benutzerdefinierte Funktion enthält, sowie ein oder mehrere Name-Wert-Paare, die an die benutzerdefinierte Funktion als Argumente übergeben werden (optional).</span><span class="sxs-lookup"><span data-stu-id="3de2f-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="3de2f-106">Gibt das berechnete Ergebnis der benutzerdefinierten Funktion bei den angegebenen Argumenten und Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="3de2f-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3de2f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3de2f-107">Syntax</span></span>

<span data-ttu-id="3de2f-108">EVALCELL (\* \* *cellRef* \* *, [* \* *arg1Name, arg1* \* *], [* \* *arg2Name, arg2* \* \*],...)</span><span class="sxs-lookup"><span data-stu-id="3de2f-108">EVALCELL(\*\* *cellRef* \*\*,[ \*\* *arg1Name,arg1* \*\* ],[ \*\* *arg2Name,arg2* \*\* ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3de2f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3de2f-109">Parameters</span></span>

|<span data-ttu-id="3de2f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="3de2f-110">**Name**</span></span>|<span data-ttu-id="3de2f-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="3de2f-111">**Required/Optional**</span></span>|<span data-ttu-id="3de2f-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="3de2f-112">**Data Type**</span></span>|<span data-ttu-id="3de2f-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3de2f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3de2f-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="3de2f-114">_cellRef_</span></span> <br/> |<span data-ttu-id="3de2f-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3de2f-115">Required</span></span>  <br/> |<span data-ttu-id="3de2f-116">**String**</span><span class="sxs-lookup"><span data-stu-id="3de2f-116">**String**</span></span> <br/> |<span data-ttu-id="3de2f-117">Ein Bezug auf die Zelle, die die benutzerdefinierte Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="3de2f-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="3de2f-118">Tabellenübergreifende Bezüge sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="3de2f-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="3de2f-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="3de2f-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="3de2f-120">Optional</span><span class="sxs-lookup"><span data-stu-id="3de2f-120">Optional</span></span>  <br/> |<span data-ttu-id="3de2f-121">**String**</span><span class="sxs-lookup"><span data-stu-id="3de2f-121">**String**</span></span> <br/> |<span data-ttu-id="3de2f-122">Der Name des ersten Arguments, das an die benutzerdefinierte Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3de2f-122">The name of the first argument to be passed to the custom function.</span></span> <span data-ttu-id="3de2f-123">Leerzeichen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="3de2f-123">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="3de2f-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="3de2f-124">_arg1_</span></span> <br/> |<span data-ttu-id="3de2f-125">Optional</span><span class="sxs-lookup"><span data-stu-id="3de2f-125">Optional</span></span>  <br/> |<span data-ttu-id="3de2f-126">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="3de2f-126">**Varies**</span></span> <br/> |<span data-ttu-id="3de2f-127">Wert des _arg1_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="3de2f-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="3de2f-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="3de2f-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="3de2f-129">Optional</span><span class="sxs-lookup"><span data-stu-id="3de2f-129">Optional</span></span>  <br/> |<span data-ttu-id="3de2f-130">**String**</span><span class="sxs-lookup"><span data-stu-id="3de2f-130">**String**</span></span> <br/> |<span data-ttu-id="3de2f-131">Der Name des zweiten Arguments, das an die benutzerdefinierte Funktion übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3de2f-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="3de2f-132">Leerzeichen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="3de2f-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="3de2f-133">_arg2_</span><span class="sxs-lookup"><span data-stu-id="3de2f-133">_arg2_</span></span> <br/> |<span data-ttu-id="3de2f-134">Optional</span><span class="sxs-lookup"><span data-stu-id="3de2f-134">Optional</span></span>  <br/> |<span data-ttu-id="3de2f-135">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="3de2f-135">**Varies**</span></span> <br/> |<span data-ttu-id="3de2f-136">Wert des _arg2_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="3de2f-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3de2f-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3de2f-137">Return value</span></span>

<span data-ttu-id="3de2f-138">Zahl</span><span class="sxs-lookup"><span data-stu-id="3de2f-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3de2f-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3de2f-139">Remarks</span></span>

<span data-ttu-id="3de2f-140">In der aufrufenden Zelle muss nicht jedes von der benutzerdefinierten Funktion verwendete Argument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3de2f-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3de2f-141">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3de2f-141">Example</span></span>

<span data-ttu-id="3de2f-142">Im folgenden Beispiel wird gezeigt, wie Sie mit der EVALCELL-Funktion in Verbindung mit der ARG-Funktion den Mittelwert aus einer Menge von drei Werte finden.</span><span class="sxs-lookup"><span data-stu-id="3de2f-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="3de2f-143">Fügen Sie in die Ausdruckszelle den folgenden Code ein, der die benutzerdefinierte Funktion definiert:</span><span class="sxs-lookup"><span data-stu-id="3de2f-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="3de2f-144">Fügen Sie in die aufrufenden Zellen den folgenden Code ein, der die benutzerdefinierte Funktion aufruft:</span><span class="sxs-lookup"><span data-stu-id="3de2f-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


