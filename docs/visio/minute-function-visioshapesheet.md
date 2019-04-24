---
title: MINUTE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Gibt eine ganze Zahl zwischen 0 und 59 zurück, die die Minutenkomponente von DateTime oder Expression darstellt.
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283972"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="f2983-103">MINUTE-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="f2983-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="f2983-104">Gibt eine ganze Zahl zwischen 0 und 59 zurück, die die Minutenkomponente von *DateTime* oder *Expression* darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2983-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f2983-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2983-105">Syntax</span></span>

<span data-ttu-id="f2983-106">MINUTE (" *DateTime* " |  *Ausdruck*  [, *LCID* ])</span><span class="sxs-lookup"><span data-stu-id="f2983-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f2983-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2983-107">Parameters</span></span>

|<span data-ttu-id="f2983-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f2983-108">**Name**</span></span>|<span data-ttu-id="f2983-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="f2983-109">**Required/Optional**</span></span>|<span data-ttu-id="f2983-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="f2983-110">**Data Type**</span></span>|<span data-ttu-id="f2983-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2983-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f2983-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="f2983-112">_datetime_</span></span> <br/> |<span data-ttu-id="f2983-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f2983-113">Required</span></span>  <br/> |<span data-ttu-id="f2983-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f2983-114">**String**</span></span> <br/> |<span data-ttu-id="f2983-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="f2983-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="f2983-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="f2983-116">_expression_</span></span> <br/> |<span data-ttu-id="f2983-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f2983-117">Required</span></span>  <br/> |<span data-ttu-id="f2983-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f2983-118">**String**</span></span> <br/> | <span data-ttu-id="f2983-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="f2983-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="f2983-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="f2983-120">_lcid_</span></span> <br/> |<span data-ttu-id="f2983-121">Optional</span><span class="sxs-lookup"><span data-stu-id="f2983-121">Optional</span></span>  <br/> |<span data-ttu-id="f2983-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="f2983-122">**Number**</span></span> <br/> |<span data-ttu-id="f2983-123">Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2983-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="f2983-124">Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f2983-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f2983-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2983-125">Return value</span></span>

<span data-ttu-id="f2983-126">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="f2983-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f2983-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2983-127">Remarks</span></span>

<span data-ttu-id="f2983-128">Die Datumskomponente in _DateTime_ und _Expression_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="f2983-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="f2983-129">Es findet kein Auf- oder Abrunden statt.</span><span class="sxs-lookup"><span data-stu-id="f2983-129">No rounding is done.</span></span> <span data-ttu-id="f2983-130">Wenn _DateTime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f2983-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="f2983-131">Der zurückgegebene Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f2983-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="f2983-132">Die MINUTE-Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der Dezimalteil den Bruchteil eines Tags seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2983-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f2983-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f2983-133">Example 1</span></span>

<span data-ttu-id="f2983-134">MINUTE ("7/7/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="f2983-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="f2983-135">Gibt 45 zurück.</span><span class="sxs-lookup"><span data-stu-id="f2983-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f2983-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f2983-136">Example 2</span></span>

<span data-ttu-id="f2983-137">MINUTE(ZEITWERT("25. Jan. 1999 12:07:45")+6 vm.)</span><span class="sxs-lookup"><span data-stu-id="f2983-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="f2983-138">Gibt 13 zurück.</span><span class="sxs-lookup"><span data-stu-id="f2983-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f2983-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f2983-139">Example 3</span></span>

<span data-ttu-id="f2983-140">MINUTE (0.575)</span><span class="sxs-lookup"><span data-stu-id="f2983-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="f2983-141">Gibt 48 zurück.</span><span class="sxs-lookup"><span data-stu-id="f2983-141">Returns 48.</span></span>
  

