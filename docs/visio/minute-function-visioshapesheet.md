---
title: MINUTE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Gibt eine ganze Zahl von 0 bis 59, die die Minutenkomponente in Datetime oder Expression darstellt.
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797528"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="35c46-103">MINUTE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="35c46-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="35c46-104">Gibt eine ganze Zahl von 0 bis 59, die die Minutenkomponente in *Datetime* oder *Expression* darstellt.</span><span class="sxs-lookup"><span data-stu-id="35c46-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="35c46-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35c46-105">Syntax</span></span>

<span data-ttu-id="35c46-106">MINUTE (" *Datetime* " |  *Ausdruck*  [, *Lcid* ])</span><span class="sxs-lookup"><span data-stu-id="35c46-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="35c46-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="35c46-107">Parameters</span></span>

|<span data-ttu-id="35c46-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="35c46-108">**Name**</span></span>|<span data-ttu-id="35c46-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="35c46-109">**Required/Optional**</span></span>|<span data-ttu-id="35c46-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="35c46-110">**Data Type**</span></span>|<span data-ttu-id="35c46-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35c46-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="35c46-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="35c46-112">_datetime_</span></span> <br/> |<span data-ttu-id="35c46-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="35c46-113">Required</span></span>  <br/> |<span data-ttu-id="35c46-114">**String**</span><span class="sxs-lookup"><span data-stu-id="35c46-114">**String**</span></span> <br/> |<span data-ttu-id="35c46-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="35c46-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="35c46-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="35c46-116">_expression_</span></span> <br/> |<span data-ttu-id="35c46-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="35c46-117">Required</span></span>  <br/> |<span data-ttu-id="35c46-118">**String**</span><span class="sxs-lookup"><span data-stu-id="35c46-118">**String**</span></span> <br/> | <span data-ttu-id="35c46-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="35c46-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="35c46-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="35c46-120">_lcid_</span></span> <br/> |<span data-ttu-id="35c46-121">Optional</span><span class="sxs-lookup"><span data-stu-id="35c46-121">Optional</span></span>  <br/> |<span data-ttu-id="35c46-122">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="35c46-122">**Number**</span></span> <br/> |<span data-ttu-id="35c46-p101">Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="35c46-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="35c46-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35c46-125">Return value</span></span>

<span data-ttu-id="35c46-126">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="35c46-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35c46-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35c46-127">Remarks</span></span>

<span data-ttu-id="35c46-128">Die Datumskomponente in _Datetime_ und _Expression_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="35c46-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="35c46-129">Keine Rundung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="35c46-129">No rounding is done.</span></span> <span data-ttu-id="35c46-130">Wenn _Datetime_ nicht vorhanden ist oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="35c46-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="35c46-131">Der zurückgegebene  Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="35c46-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="35c46-132">Die MINUTE-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Dezimalteil für den Bruchteil eines Tages seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="35c46-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="35c46-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35c46-133">Example 1</span></span>

<span data-ttu-id="35c46-134">MINUTE("7/7/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="35c46-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="35c46-135">Gibt 45 zurück.</span><span class="sxs-lookup"><span data-stu-id="35c46-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="35c46-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="35c46-136">Example 2</span></span>

<span data-ttu-id="35c46-137">MINUTE(ZEITWERT("25. Jan. 1999 12:07:45")+6 vm.)</span><span class="sxs-lookup"><span data-stu-id="35c46-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="35c46-138">Gibt 13 zurück.</span><span class="sxs-lookup"><span data-stu-id="35c46-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="35c46-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="35c46-139">Example 3</span></span>

<span data-ttu-id="35c46-140">MINUTE(0.575)</span><span class="sxs-lookup"><span data-stu-id="35c46-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="35c46-141">Gibt 48 zurück.</span><span class="sxs-lookup"><span data-stu-id="35c46-141">Returns 48.</span></span>
  

