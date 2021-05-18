---
title: WEEKDAY-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Gibt eine ganze Zahl von 1 bis 7 zurück, die den Wochentag in Datetime oder Ausdruck darstellt.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404806"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="75147-103">WEEKDAY-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="75147-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="75147-104">Gibt eine ganze Zahl von 1 bis 7 zurück, die den Wochentag in _Datetime oder_ Ausdruck _darstellt._</span><span class="sxs-lookup"><span data-stu-id="75147-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="75147-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75147-105">Syntax</span></span>

<span data-ttu-id="75147-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *Ausdruck* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="75147-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="75147-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="75147-107">Parameters</span></span>

|<span data-ttu-id="75147-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="75147-108">**Name**</span></span>|<span data-ttu-id="75147-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="75147-109">**Required/Optional**</span></span>|<span data-ttu-id="75147-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="75147-110">**Data Type**</span></span>|<span data-ttu-id="75147-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75147-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="75147-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="75147-112">_datetime_</span></span> <br/> |<span data-ttu-id="75147-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="75147-113">Required</span></span>  <br/> |<span data-ttu-id="75147-114">**String**</span><span class="sxs-lookup"><span data-stu-id="75147-114">**String**</span></span> <br/> | <span data-ttu-id="75147-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="75147-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="75147-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="75147-116">_expression_</span></span> <br/> |<span data-ttu-id="75147-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="75147-117">Required</span></span>  <br/> |<span data-ttu-id="75147-118">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="75147-118">**Varies**</span></span> <br/> |<span data-ttu-id="75147-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="75147-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="75147-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="75147-120">_lcid_</span></span> <br/> |<span data-ttu-id="75147-121">Optional.</span><span class="sxs-lookup"><span data-stu-id="75147-121">Optional</span></span>  <br/> |<span data-ttu-id="75147-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="75147-122">**Numeric**</span></span> <br/> |<span data-ttu-id="75147-p101">Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="75147-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="75147-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75147-125">Return value</span></span>

<span data-ttu-id="75147-126">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="75147-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75147-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75147-127">Remarks</span></span>

<span data-ttu-id="75147-128">Die Zeitkomponente in  _datetime_ oder  _ausdruck_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="75147-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="75147-129">Das Ergebnis entspricht Montag (1) bis Sonntag (7).</span><span class="sxs-lookup"><span data-stu-id="75147-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="75147-130">Es findet kein Auf- oder Abrunden statt.</span><span class="sxs-lookup"><span data-stu-id="75147-130">No rounding is done.</span></span> <span data-ttu-id="75147-131">Wenn  _datetime_ fehlt oder nicht als gültiges Datum oder eine gültige Uhrzeit interpretiert werden kann, gibt die Funktion eine #VALUE!</span><span class="sxs-lookup"><span data-stu-id="75147-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="75147-132">zurück.</span><span class="sxs-lookup"><span data-stu-id="75147-132">error.</span></span> 
  
<span data-ttu-id="75147-133">Die WEEKDAY-Funktion akzeptiert auch  einen einzelnen Zahlenwert für ausdruck, wobei der ganzzahlige Teil des Ergebnisses die Anzahl der Tage seit dem 30. Dezember 1899 darstellt.</span><span class="sxs-lookup"><span data-stu-id="75147-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="75147-134">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75147-134">Example 1</span></span>

<span data-ttu-id="75147-135">WEEKDAY("30. Mai 1999")</span><span class="sxs-lookup"><span data-stu-id="75147-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="75147-136">Gibt 7 zurück.</span><span class="sxs-lookup"><span data-stu-id="75147-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="75147-137">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="75147-137">Example 2</span></span>

<span data-ttu-id="75147-138">WEEKDAY(DATUMSWERT("30. Mai 1999")+2 vt.)</span><span class="sxs-lookup"><span data-stu-id="75147-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="75147-139">Gibt 2 zurück.</span><span class="sxs-lookup"><span data-stu-id="75147-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="75147-140">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="75147-140">Example 3</span></span>

<span data-ttu-id="75147-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="75147-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="75147-142">Gibt 4 zurück.</span><span class="sxs-lookup"><span data-stu-id="75147-142">Returns 4.</span></span>
  

