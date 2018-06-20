---
title: SECOND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Gibt eine ganze Zahl 0 und 59, die die Sekundenkomponente in Datetime oder Expression darstellt.
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797977"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="36a05-103">SECOND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="36a05-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="36a05-104">Gibt eine ganze Zahl 0 und 59, die die Sekundenkomponente in _Datetime_ oder _Expression_darstellt.</span><span class="sxs-lookup"><span data-stu-id="36a05-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="36a05-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36a05-105">Syntax</span></span>

<span data-ttu-id="36a05-106">ZWEITE ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **])</span><span class="sxs-lookup"><span data-stu-id="36a05-106">SECOND(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="36a05-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="36a05-107">Parameters</span></span>

|<span data-ttu-id="36a05-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="36a05-108">**Name**</span></span>|<span data-ttu-id="36a05-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="36a05-109">**Required/Optional**</span></span>|<span data-ttu-id="36a05-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="36a05-110">**Data Type**</span></span>|<span data-ttu-id="36a05-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36a05-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="36a05-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="36a05-112">_datetime_</span></span> <br/> |<span data-ttu-id="36a05-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="36a05-113">Required</span></span>  <br/> |<span data-ttu-id="36a05-114">**String**</span><span class="sxs-lookup"><span data-stu-id="36a05-114">**String**</span></span> <br/> |<span data-ttu-id="36a05-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="36a05-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="36a05-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="36a05-116">_expression_</span></span> <br/> |<span data-ttu-id="36a05-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="36a05-117">Required</span></span>  <br/> |<span data-ttu-id="36a05-118">**String**</span><span class="sxs-lookup"><span data-stu-id="36a05-118">**String**</span></span> <br/> | <span data-ttu-id="36a05-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="36a05-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="36a05-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="36a05-120">_lcid_</span></span> <br/> |<span data-ttu-id="36a05-121">Optional</span><span class="sxs-lookup"><span data-stu-id="36a05-121">Optional</span></span>  <br/> |<span data-ttu-id="36a05-122">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="36a05-122">**Numeric**</span></span> <br/> |<span data-ttu-id="36a05-123">Die Gebietsschema-ID an, bei der Bewertung von Währungssymbole _Datetime_verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36a05-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="36a05-124">Die Gebietsschema-ID ist eine Zahl, die in den Headerdateien System beschrieben.</span><span class="sxs-lookup"><span data-stu-id="36a05-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="36a05-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="36a05-125">Return value</span></span>

<span data-ttu-id="36a05-126">Integer</span><span class="sxs-lookup"><span data-stu-id="36a05-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36a05-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36a05-127">Remarks</span></span>

<span data-ttu-id="36a05-128">Die Datumskomponente in _Datetime_ oder _Expression_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="36a05-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="36a05-129">Keine Rundung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="36a05-129">No rounding is done.</span></span> <span data-ttu-id="36a05-130">Wenn _Datetime_ nicht vorhanden ist oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt diese Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="36a05-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="36a05-131">Die SECOND-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tages seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="36a05-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="36a05-132">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36a05-132">Example 1</span></span>

<span data-ttu-id="36a05-133">SECOND("30/05/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="36a05-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="36a05-134">Gibt 32 zurück.</span><span class="sxs-lookup"><span data-stu-id="36a05-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="36a05-135">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="36a05-135">Example 2</span></span>

<span data-ttu-id="36a05-136">SECOND(ZEITWERT("30. Mai 1996 12:07:45")+7 as.)</span><span class="sxs-lookup"><span data-stu-id="36a05-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="36a05-137">Gibt 52 zurück.</span><span class="sxs-lookup"><span data-stu-id="36a05-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="36a05-138">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="36a05-138">Example 3</span></span>

<span data-ttu-id="36a05-139">SECOND(0.6337)</span><span class="sxs-lookup"><span data-stu-id="36a05-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="36a05-140">Gibt 32 zurück.</span><span class="sxs-lookup"><span data-stu-id="36a05-140">Returns 32.</span></span>
  

