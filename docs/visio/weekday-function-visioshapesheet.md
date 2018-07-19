---
title: WEEKDAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Gibt eine ganze Zahl von 1 bis 7, die den Wochentag in Datetime oder Expression darstellt.
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798412"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="fbc25-103">WEEKDAY Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fbc25-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fbc25-104">Gibt eine ganze Zahl von 1 bis 7, die den Wochentag in _Datetime_ oder _Expression_darstellt.</span><span class="sxs-lookup"><span data-stu-id="fbc25-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fbc25-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbc25-105">Syntax</span></span>

<span data-ttu-id="fbc25-106">Wochentag ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **])</span><span class="sxs-lookup"><span data-stu-id="fbc25-106">WEEKDAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fbc25-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbc25-107">Parameters</span></span>

|<span data-ttu-id="fbc25-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fbc25-108">**Name**</span></span>|<span data-ttu-id="fbc25-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="fbc25-109">**Required/Optional**</span></span>|<span data-ttu-id="fbc25-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="fbc25-110">**Data Type**</span></span>|<span data-ttu-id="fbc25-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fbc25-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fbc25-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="fbc25-112">_datetime_</span></span> <br/> |<span data-ttu-id="fbc25-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbc25-113">Required</span></span>  <br/> |<span data-ttu-id="fbc25-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fbc25-114">**String**</span></span> <br/> | <span data-ttu-id="fbc25-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="fbc25-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="fbc25-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="fbc25-116">_expression_</span></span> <br/> |<span data-ttu-id="fbc25-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbc25-117">Required</span></span>  <br/> |<span data-ttu-id="fbc25-118">**Varies**</span><span class="sxs-lookup"><span data-stu-id="fbc25-118">**Varies**</span></span> <br/> |<span data-ttu-id="fbc25-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="fbc25-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="fbc25-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="fbc25-120">_lcid_</span></span> <br/> |<span data-ttu-id="fbc25-121">Optional</span><span class="sxs-lookup"><span data-stu-id="fbc25-121">Optional</span></span>  <br/> |<span data-ttu-id="fbc25-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="fbc25-122">**Numeric**</span></span> <br/> |<span data-ttu-id="fbc25-p101">Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="fbc25-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fbc25-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbc25-125">Return value</span></span>

<span data-ttu-id="fbc25-126">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="fbc25-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fbc25-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbc25-127">Remarks</span></span>

<span data-ttu-id="fbc25-128">Die Zeitkomponente in _Datetime_ oder _Expression_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="fbc25-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="fbc25-129">Das Ergebnis entspricht Montag (1) bis Sonntag (7).</span><span class="sxs-lookup"><span data-stu-id="fbc25-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="fbc25-130">Keine Rundung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="fbc25-130">No rounding is done.</span></span> <span data-ttu-id="fbc25-131">Wenn _Datetime_ nicht vorhanden ist oder nicht als gültige Datum oder Uhrzeit interpretiert werden kann, gibt die Funktion einer #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fbc25-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="fbc25-132">Fehler.</span><span class="sxs-lookup"><span data-stu-id="fbc25-132">error.</span></span> 
  
<span data-ttu-id="fbc25-133">Die WEEKDAY-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Ganzzahlteil des Ergebnisses für die Anzahl von Tagen seit dem 30. Dezember 1899 steht.</span><span class="sxs-lookup"><span data-stu-id="fbc25-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fbc25-134">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fbc25-134">Example 1</span></span>

<span data-ttu-id="fbc25-135">WEEKDAY("30. Mai 1999")</span><span class="sxs-lookup"><span data-stu-id="fbc25-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="fbc25-136">Gibt 7 zurück.</span><span class="sxs-lookup"><span data-stu-id="fbc25-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fbc25-137">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fbc25-137">Example 2</span></span>

<span data-ttu-id="fbc25-138">WEEKDAY(DATUMSWERT("30. Mai 1999")+2 vt.)</span><span class="sxs-lookup"><span data-stu-id="fbc25-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="fbc25-139">Gibt 2 zurück.</span><span class="sxs-lookup"><span data-stu-id="fbc25-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fbc25-140">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fbc25-140">Example 3</span></span>

<span data-ttu-id="fbc25-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="fbc25-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="fbc25-142">Gibt 4 zurück.</span><span class="sxs-lookup"><span data-stu-id="fbc25-142">Returns 4.</span></span>
  

