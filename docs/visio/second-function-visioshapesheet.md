---
title: SECOND-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Gibt eine ganze Zahl von 0 bis 59 zurück, die die Sekundenkomponente von datetime oder ausdruck darstellt.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404876"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="bb842-103">SECOND-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="bb842-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="bb842-104">Gibt eine ganze Zahl von 0 bis 59 zurück, die die Sekundenkomponente von _datetime oder_ _Ausdruck darstellt._</span><span class="sxs-lookup"><span data-stu-id="bb842-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bb842-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb842-105">Syntax</span></span>

<span data-ttu-id="bb842-106">SECOND(" \*\* *datetime* \*\* "| \*\* *Ausdruck* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="bb842-106">SECOND(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bb842-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb842-107">Parameters</span></span>

|<span data-ttu-id="bb842-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="bb842-108">**Name**</span></span>|<span data-ttu-id="bb842-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="bb842-109">**Required/Optional**</span></span>|<span data-ttu-id="bb842-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="bb842-110">**Data Type**</span></span>|<span data-ttu-id="bb842-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb842-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bb842-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="bb842-112">_datetime_</span></span> <br/> |<span data-ttu-id="bb842-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="bb842-113">Required</span></span>  <br/> |<span data-ttu-id="bb842-114">**String**</span><span class="sxs-lookup"><span data-stu-id="bb842-114">**String**</span></span> <br/> |<span data-ttu-id="bb842-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="bb842-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="bb842-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="bb842-116">_expression_</span></span> <br/> |<span data-ttu-id="bb842-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="bb842-117">Required</span></span>  <br/> |<span data-ttu-id="bb842-118">**String**</span><span class="sxs-lookup"><span data-stu-id="bb842-118">**String**</span></span> <br/> | <span data-ttu-id="bb842-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="bb842-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="bb842-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="bb842-120">_lcid_</span></span> <br/> |<span data-ttu-id="bb842-121">Optional.</span><span class="sxs-lookup"><span data-stu-id="bb842-121">Optional</span></span>  <br/> |<span data-ttu-id="bb842-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="bb842-122">**Numeric**</span></span> <br/> |<span data-ttu-id="bb842-123">Der Locale-Bezeichner, der bei der Auswertung einer nicht lokalen _Datetime verwendet werden soll._</span><span class="sxs-lookup"><span data-stu-id="bb842-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="bb842-124">Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="bb842-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bb842-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb842-125">Return value</span></span>

<span data-ttu-id="bb842-126">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="bb842-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb842-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb842-127">Remarks</span></span>

<span data-ttu-id="bb842-128">Die Datumskomponente in  _datetime_ oder  _ausdruck_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="bb842-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="bb842-129">Es findet kein Auf- oder Abrunden statt.</span><span class="sxs-lookup"><span data-stu-id="bb842-129">No rounding is done.</span></span> <span data-ttu-id="bb842-130">Wenn  _datetime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt diese Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="bb842-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="bb842-131">Die SECOND-Funktion akzeptiert auch  einen einzelnen Zahlenwert für den Ausdruck, wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tages seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb842-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="bb842-132">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb842-132">Example 1</span></span>

<span data-ttu-id="bb842-133">SECOND("30.05.1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="bb842-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="bb842-134">Gibt 32 zurück.</span><span class="sxs-lookup"><span data-stu-id="bb842-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bb842-135">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bb842-135">Example 2</span></span>

<span data-ttu-id="bb842-136">SECOND(ZEITWERT("30. Mai 1996 12:07:45")+7 as.)</span><span class="sxs-lookup"><span data-stu-id="bb842-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="bb842-137">Gibt 52 zurück.</span><span class="sxs-lookup"><span data-stu-id="bb842-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bb842-138">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="bb842-138">Example 3</span></span>

<span data-ttu-id="bb842-139">SECOND(0.6337)</span><span class="sxs-lookup"><span data-stu-id="bb842-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="bb842-140">Gibt 32 zurück.</span><span class="sxs-lookup"><span data-stu-id="bb842-140">Returns 32.</span></span>
  

