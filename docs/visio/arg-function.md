---
title: ARG-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Gibt ein Argument an, das von der aufrufenden Zelle an eine benutzerdefinierte Funktion übergeben werden kann, sowie den Standardwert, der von der benutzerdefinierten Funktion zurückgegeben wird, wenn die aufrufende Zelle keinen Wert für das Argument übergibt. Gibt den Wert zurück, der durch die aufrufende Zelle und den entsprechenden argname-Parameter angegeben wird.
ms.openlocfilehash: 3cde7fe55d7bc60d15f32d7ad954443e545af914
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293485"
---
# <a name="arg-function"></a><span data-ttu-id="8c83f-104">ARG Function</span><span class="sxs-lookup"><span data-stu-id="8c83f-104">ARG Function</span></span>

<span data-ttu-id="8c83f-105">Gibt ein Argument an, das von der aufrufenden Zelle an eine benutzerdefinierte Funktion übergeben werden kann, sowie den Standardwert, der von der benutzerdefinierten Funktion zurückgegeben wird, wenn die aufrufende Zelle keinen Wert für das Argument übergibt.</span><span class="sxs-lookup"><span data-stu-id="8c83f-105">Specifies an argument that the calling cell can pass to a custom function, as well as the default value returned by the custom function if the calling cell does not pass in a value for the argument.</span></span> <span data-ttu-id="8c83f-106">Gibt den Wert zurück, der durch die aufrufende Zelle und den entsprechenden argname-Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c83f-106">Returns the value specified by the calling cell and the matching argName parameter.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8c83f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c83f-107">Syntax</span></span>

<span data-ttu-id="8c83f-108">ARG (***argname***, [ ***DefaultValue*** ])</span><span class="sxs-lookup"><span data-stu-id="8c83f-108">ARG(***argName***,[ ***defaultValue*** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8c83f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c83f-109">Parameters</span></span>

|<span data-ttu-id="8c83f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8c83f-110">**Name**</span></span>|<span data-ttu-id="8c83f-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8c83f-111">**Required/Optional**</span></span>|<span data-ttu-id="8c83f-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8c83f-112">**Data Type**</span></span>|<span data-ttu-id="8c83f-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c83f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8c83f-114">_argName_</span><span class="sxs-lookup"><span data-stu-id="8c83f-114">_argName_</span></span> <br/> |<span data-ttu-id="8c83f-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8c83f-115">Required</span></span>  <br/> |<span data-ttu-id="8c83f-116">**String**</span><span class="sxs-lookup"><span data-stu-id="8c83f-116">**String**</span></span> <br/> |<span data-ttu-id="8c83f-117">Der Name eines Arguments, das die aufrufende Zelle an die Funktion übergeben kann.</span><span class="sxs-lookup"><span data-stu-id="8c83f-117">The name of an argument that the calling cell can pass into the function.</span></span>  <br/> |
| <span data-ttu-id="8c83f-118">_Standardwert_</span><span class="sxs-lookup"><span data-stu-id="8c83f-118">_default Value_</span></span> <br/> |<span data-ttu-id="8c83f-119">Optional</span><span class="sxs-lookup"><span data-stu-id="8c83f-119">Optional</span></span>  <br/> |<span data-ttu-id="8c83f-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="8c83f-120">**Numeric**</span></span> <br/> |<span data-ttu-id="8c83f-121">Der von arg zurückgegebene Wert, wenn die aufrufende Zelle keinen Wert für den  _argname_ -Parameter übergeben hat.</span><span class="sxs-lookup"><span data-stu-id="8c83f-121">The value returned by ARG if the calling cell did not pass in a value for the  _argName_ parameter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c83f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c83f-122">Remarks</span></span>

<span data-ttu-id="8c83f-p103">Als Entwickler von Shapes können Sie benutzerdefinierte Funktionen erstellen, indem Sie einen Ausdruck in eine Zelle einfügen und diesen Ausdruck von anderen Zellen aus aufrufen. Der Ausdruck kann literale Zeichenfolgen, ShapeSheet-Funktionen und Zellbezüge enthalten. Außerdem kann der Ausdruck bestimmte Argumente enthalten, die von der aufrufenden Zelle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8c83f-p103">As a shape developer, you can create custom functions by placing an expression in one cell and calling that expression from one or more other cells. The expression can include literal strings, ShapeSheet functions, and cell references. The expression can also include specific arguments that are passed in by the calling cell.</span></span> 
  
<span data-ttu-id="8c83f-126">Die aufrufende Zelle gibt die Zelle mit der benutzerdefinierten Funktion sowie Argumente an, die an die Funktion übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c83f-126">The calling cell specifies the cell that contains the custom function as well as any arguments that it wants to pass to the function.</span></span> <span data-ttu-id="8c83f-127">Die Ausdruckszelle wird ausgewertet, und das Ergebnis wird an die aufrufende Zelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c83f-127">The expression cell is evaluated and the result returned to the calling cell.</span></span>
  
## <a name="example"></a><span data-ttu-id="8c83f-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8c83f-128">Example</span></span>

<span data-ttu-id="8c83f-129">Im folgenden Beispiel wird gezeigt, wie Sie mit der ARG-Funktion in Verbindung mit der EVALCELL-Funktion den Mittelwert aus einer Menge von drei Werte finden.</span><span class="sxs-lookup"><span data-stu-id="8c83f-129">The following example shows how to use the ARG function in conjunction with the EVALCELL function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="8c83f-130">Fügen Sie in die Ausdruckszelle den folgenden Code ein, der die benutzerdefinierte Funktion definiert:</span><span class="sxs-lookup"><span data-stu-id="8c83f-130">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="8c83f-131">Fügen Sie in die aufrufenden Zellen den folgenden Code ein, der die benutzerdefinierte Funktion aufruft:</span><span class="sxs-lookup"><span data-stu-id="8c83f-131">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


