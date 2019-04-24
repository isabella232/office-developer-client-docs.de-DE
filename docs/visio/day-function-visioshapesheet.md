---
title: DAY-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Gibt eine ganze Zahl von 1 bis 31 zurück, die den Tag in DateTime oder Expression darstellt. Die DAY-Funktion verwendet den gregorianischen Kalender.
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360296"
---
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="abea7-104">DAY-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="abea7-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="abea7-105">Gibt eine ganze Zahl von 1 bis 31 zurück, die den Tag in _DateTime_ oder _Expression_darstellt.</span><span class="sxs-lookup"><span data-stu-id="abea7-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="abea7-106">Die DAY-Funktion verwendet den gregorianischen Kalender.</span><span class="sxs-lookup"><span data-stu-id="abea7-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="abea7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="abea7-107">Syntax</span></span>

<span data-ttu-id="abea7-108">Tag ("\* \* *DateTime* \* \*" | \* \* *Expression* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="abea7-108">DAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="abea7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="abea7-109">Parameters</span></span>

|<span data-ttu-id="abea7-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="abea7-110">**Name**</span></span>|<span data-ttu-id="abea7-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="abea7-111">**Required/Optional**</span></span>|<span data-ttu-id="abea7-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="abea7-112">**Data Type**</span></span>|<span data-ttu-id="abea7-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abea7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="abea7-114">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="abea7-114">_datetime_</span></span> <br/> |<span data-ttu-id="abea7-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="abea7-115">Required</span></span>  <br/> |<span data-ttu-id="abea7-116">**String**</span><span class="sxs-lookup"><span data-stu-id="abea7-116">**String**</span></span> <br/> |<span data-ttu-id="abea7-117">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="abea7-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="abea7-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="abea7-118">_expression_</span></span> <br/> |<span data-ttu-id="abea7-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="abea7-119">Required</span></span>  <br/> |<span data-ttu-id="abea7-120">**String**</span><span class="sxs-lookup"><span data-stu-id="abea7-120">**String**</span></span> <br/> |<span data-ttu-id="abea7-121">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="abea7-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="abea7-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="abea7-122">_lcid_</span></span> <br/> |<span data-ttu-id="abea7-123">Optional</span><span class="sxs-lookup"><span data-stu-id="abea7-123">Optional</span></span>  <br/> |<span data-ttu-id="abea7-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="abea7-124">**Number**</span></span> <br/> |<span data-ttu-id="abea7-p103">Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="abea7-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="abea7-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abea7-127">Return value</span></span>

<span data-ttu-id="abea7-128">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="abea7-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="abea7-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abea7-129">Remarks</span></span>

<span data-ttu-id="abea7-130">Alle Zeitkomponenten in _DateTime_ oder _Expression_ werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="abea7-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="abea7-131">Es findet kein Auf- oder Abrunden statt.</span><span class="sxs-lookup"><span data-stu-id="abea7-131">No rounding is done.</span></span> <span data-ttu-id="abea7-132">Wenn _DateTime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="abea7-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="abea7-133">Die DAY-Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der ganzzahlige Teil des Ergebnisses die Anzahl von Tagen seit dem 30. Dezember 1899 darstellt.</span><span class="sxs-lookup"><span data-stu-id="abea7-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="abea7-134">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="abea7-134">Example 1</span></span>

<span data-ttu-id="abea7-135">DAY("30. Mai 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="abea7-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="abea7-136">Gibt 30 zurück.</span><span class="sxs-lookup"><span data-stu-id="abea7-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="abea7-137">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="abea7-137">Example 2</span></span>

<span data-ttu-id="abea7-138">DAY(DATUMSWERT("30. Mai 1997")+7 t.)</span><span class="sxs-lookup"><span data-stu-id="abea7-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="abea7-139">Gibt 6 zurück.</span><span class="sxs-lookup"><span data-stu-id="abea7-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="abea7-140">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="abea7-140">Example 3</span></span>

<span data-ttu-id="abea7-141">TAG (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="abea7-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="abea7-142">Gibt 30 zurück.</span><span class="sxs-lookup"><span data-stu-id="abea7-142">Returns 30.</span></span>
  

