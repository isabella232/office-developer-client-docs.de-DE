---
title: YEAR-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Gibt eine ganze Zahl zurück, die das gregorianische Jahr in DateTime oder Expression darstellt, formatiert entsprechend der kurzen Datumsformat Vorlage, die durch die aktuelle Regions-und Spracheinstellungen des Systems festgelegt ist.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420710"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="a368d-103">YEAR-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a368d-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a368d-104">Gibt eine ganze Zahl zurück, die das gregorianische Jahr in _DateTime_ oder _Expression_darstellt, formatiert entsprechend der kurzen Datumsformat Vorlage, die durch die aktuelle Regions-und Spracheinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a368d-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a368d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a368d-105">Syntax</span></span>

<span data-ttu-id="a368d-106">Jahr ("\* \* *DateTime* \* \*" | \* \* *Expression* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="a368d-106">YEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a368d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a368d-107">Parameters</span></span>

|<span data-ttu-id="a368d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a368d-108">**Name**</span></span>|<span data-ttu-id="a368d-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a368d-109">**Required/Optional**</span></span>|<span data-ttu-id="a368d-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a368d-110">**Data Type**</span></span>|<span data-ttu-id="a368d-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a368d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a368d-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="a368d-112">_datetime_</span></span> <br/> |<span data-ttu-id="a368d-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a368d-113">Required</span></span>  <br/> |<span data-ttu-id="a368d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a368d-114">**String**</span></span> <br/> | <span data-ttu-id="a368d-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="a368d-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="a368d-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="a368d-116">_expression_</span></span> <br/> |<span data-ttu-id="a368d-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a368d-117">Required</span></span>  <br/> |<span data-ttu-id="a368d-118">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="a368d-118">**Varies**</span></span> <br/> |<span data-ttu-id="a368d-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="a368d-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="a368d-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="a368d-120">_lcid_</span></span> <br/> |<span data-ttu-id="a368d-121">Optional</span><span class="sxs-lookup"><span data-stu-id="a368d-121">Optional</span></span>  <br/> |<span data-ttu-id="a368d-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="a368d-122">**Numeric**</span></span> <br/> |<span data-ttu-id="a368d-123">Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a368d-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="a368d-124">Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="a368d-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a368d-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a368d-125">Return value</span></span>

<span data-ttu-id="a368d-126">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="a368d-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a368d-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a368d-127">Remarks</span></span>

<span data-ttu-id="a368d-128">Die Zeitkomponente in _DateTime_ oder _Expression_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="a368d-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="a368d-129">Es findet kein Auf- oder Abrunden statt.</span><span class="sxs-lookup"><span data-stu-id="a368d-129">No rounding is done.</span></span> <span data-ttu-id="a368d-130">Wenn _DateTime_ fehlt oder nicht als gültige Datums-oder Uhrzeitangabe interpretiert werden kann, gibt Year einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a368d-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="a368d-131">Die YEAR-Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der ganzzahlige Teil des Ergebnisses die Anzahl von Tagen seit dem 30. Dezember 1899 darstellt.</span><span class="sxs-lookup"><span data-stu-id="a368d-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a368d-132">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a368d-132">Example 1</span></span>

<span data-ttu-id="a368d-133">JAHR ("10/27/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="a368d-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="a368d-134">Gibt 2007 zurück.</span><span class="sxs-lookup"><span data-stu-id="a368d-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a368d-135">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a368d-135">Example 2</span></span>

<span data-ttu-id="a368d-136">YEAR(DATUMSWERT("25. Dez. 2006") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="a368d-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="a368d-137">Gibt 2007 zurück.</span><span class="sxs-lookup"><span data-stu-id="a368d-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a368d-138">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a368d-138">Example 3</span></span>

<span data-ttu-id="a368d-139">JAHR (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="a368d-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="a368d-140">Gibt 1997 zurück.</span><span class="sxs-lookup"><span data-stu-id="a368d-140">Returns 1997.</span></span>
  

