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
description: Gibt eine ganze Zahl von 0 bis 59 zurück, die die Sekundenkomponente von DateTime oder Expression darstellt.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332788"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="98d0c-103">SECOND-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="98d0c-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="98d0c-104">Gibt eine ganze Zahl von 0 bis 59 zurück, die die Sekundenkomponente von _DateTime_ oder _Expression_darstellt.</span><span class="sxs-lookup"><span data-stu-id="98d0c-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="98d0c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98d0c-105">Syntax</span></span>

<span data-ttu-id="98d0c-106">Sekunde ("\* \* *DateTime* \* \*" | \* \* *Expression* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="98d0c-106">SECOND(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="98d0c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="98d0c-107">Parameters</span></span>

|<span data-ttu-id="98d0c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="98d0c-108">**Name**</span></span>|<span data-ttu-id="98d0c-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="98d0c-109">**Required/Optional**</span></span>|<span data-ttu-id="98d0c-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="98d0c-110">**Data Type**</span></span>|<span data-ttu-id="98d0c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98d0c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="98d0c-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="98d0c-112">_datetime_</span></span> <br/> |<span data-ttu-id="98d0c-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="98d0c-113">Required</span></span>  <br/> |<span data-ttu-id="98d0c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="98d0c-114">**String**</span></span> <br/> |<span data-ttu-id="98d0c-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="98d0c-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="98d0c-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="98d0c-116">_expression_</span></span> <br/> |<span data-ttu-id="98d0c-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="98d0c-117">Required</span></span>  <br/> |<span data-ttu-id="98d0c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="98d0c-118">**String**</span></span> <br/> | <span data-ttu-id="98d0c-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="98d0c-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="98d0c-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="98d0c-120">_lcid_</span></span> <br/> |<span data-ttu-id="98d0c-121">Optional</span><span class="sxs-lookup"><span data-stu-id="98d0c-121">Optional</span></span>  <br/> |<span data-ttu-id="98d0c-122">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="98d0c-122">**Numeric**</span></span> <br/> |<span data-ttu-id="98d0c-123">Der Gebietsschemabezeichner, der beim Auswerten einer nicht lokalen _DateTime_verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98d0c-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="98d0c-124">Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="98d0c-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="98d0c-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98d0c-125">Return value</span></span>

<span data-ttu-id="98d0c-126">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="98d0c-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98d0c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98d0c-127">Remarks</span></span>

<span data-ttu-id="98d0c-128">Die Datumskomponente in _DateTime_ oder _Expression_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="98d0c-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="98d0c-129">Es findet kein Auf- oder Abrunden statt.</span><span class="sxs-lookup"><span data-stu-id="98d0c-129">No rounding is done.</span></span> <span data-ttu-id="98d0c-130">Wenn _DateTime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt diese Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="98d0c-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="98d0c-131">Die zweite Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tags seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="98d0c-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="98d0c-132">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98d0c-132">Example 1</span></span>

<span data-ttu-id="98d0c-133">SEKUNDE ("05/30/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="98d0c-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="98d0c-134">Gibt 32 zurück.</span><span class="sxs-lookup"><span data-stu-id="98d0c-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="98d0c-135">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="98d0c-135">Example 2</span></span>

<span data-ttu-id="98d0c-136">SECOND(ZEITWERT("30. Mai 1996 12:07:45")+7 as.)</span><span class="sxs-lookup"><span data-stu-id="98d0c-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="98d0c-137">Gibt 52 zurück.</span><span class="sxs-lookup"><span data-stu-id="98d0c-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="98d0c-138">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="98d0c-138">Example 3</span></span>

<span data-ttu-id="98d0c-139">SEKUNDE (0.6337)</span><span class="sxs-lookup"><span data-stu-id="98d0c-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="98d0c-140">Gibt 32 zurück.</span><span class="sxs-lookup"><span data-stu-id="98d0c-140">Returns 32.</span></span>
  

