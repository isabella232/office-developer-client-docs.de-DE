---
title: HOUR-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Gibt eine ganze Zahl von 0 bis 23 zurück, die die Stunde des Tages der Datumszeit oder des Ausdrucks darstellt.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429635"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="3c1aa-103">HOUR-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="3c1aa-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="3c1aa-104">Gibt eine ganze Zahl von 0 bis 23 zurück, die die Stunde des Tages der _Datumszeit_ oder des Ausdrucks _darstellt._</span><span class="sxs-lookup"><span data-stu-id="3c1aa-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3c1aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c1aa-105">Syntax</span></span>

<span data-ttu-id="3c1aa-106">HOUR(" \*\* *datetime* \*\* "| \*\* *Ausdruck* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="3c1aa-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3c1aa-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c1aa-107">Parameters</span></span>

|<span data-ttu-id="3c1aa-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3c1aa-108">**Name**</span></span>|<span data-ttu-id="3c1aa-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="3c1aa-109">**Required/Optional**</span></span>|<span data-ttu-id="3c1aa-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="3c1aa-110">**Data Type**</span></span>|<span data-ttu-id="3c1aa-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c1aa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3c1aa-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="3c1aa-112">_datetime_</span></span> <br/> |<span data-ttu-id="3c1aa-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3c1aa-113">Required</span></span>  <br/> |<span data-ttu-id="3c1aa-114">**String**</span><span class="sxs-lookup"><span data-stu-id="3c1aa-114">**String**</span></span> <br/> | <span data-ttu-id="3c1aa-115">Eine Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="3c1aa-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="3c1aa-116">_expression_</span></span> <br/> |<span data-ttu-id="3c1aa-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3c1aa-117">Required</span></span>  <br/> |<span data-ttu-id="3c1aa-118">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="3c1aa-118">**Varies**</span></span> <br/> |<span data-ttu-id="3c1aa-119">Ein Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="3c1aa-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="3c1aa-120">_lcid_</span></span> <br/> |<span data-ttu-id="3c1aa-121">Optional.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-121">Optional</span></span>  <br/> |<span data-ttu-id="3c1aa-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="3c1aa-122">**Number**</span></span> <br/> | <span data-ttu-id="3c1aa-p101">Ein lokaler Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-p101">A locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c1aa-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c1aa-125">Remarks</span></span>

<span data-ttu-id="3c1aa-126">Die Datumskomponente in  *datetime*  und  *ausdruck*  wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="3c1aa-127">Es findet kein Auf- oder Abrunden statt.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-127">No rounding is done.</span></span> <span data-ttu-id="3c1aa-128">Wenn  *datetime*  fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="3c1aa-129">Der zurückgegebene Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="3c1aa-130">Die HOUR-Funktion akzeptiert auch  einen einzelnen Zahlenwert für den Ausdruck, wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tages seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="3c1aa-131">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c1aa-131">Example 1</span></span>

<span data-ttu-id="3c1aa-132">HOUR("15:45")</span><span class="sxs-lookup"><span data-stu-id="3c1aa-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="3c1aa-133">Gibt 15 zurück.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3c1aa-134">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3c1aa-134">Example 2</span></span>

<span data-ttu-id="3c1aa-135">HOUR("30. Mai 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="3c1aa-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="3c1aa-136">Gibt 15 zurück.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3c1aa-137">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3c1aa-137">Example 3</span></span>

<span data-ttu-id="3c1aa-138">HOUR(0.5)</span><span class="sxs-lookup"><span data-stu-id="3c1aa-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="3c1aa-139">Gibt 12 zurück.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="3c1aa-140">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="3c1aa-140">Example 4</span></span>

<span data-ttu-id="3c1aa-141">HOUR("30.05.1997")</span><span class="sxs-lookup"><span data-stu-id="3c1aa-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="3c1aa-142">Gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-142">Returns 0.</span></span>
  

