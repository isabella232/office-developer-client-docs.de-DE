---
title: HOUR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Gibt eine ganze Zahl von 0 bis 23 für die Stunde des Tages in Datetime oder Expression zurück.
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797162"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="373af-103">HOUR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="373af-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="373af-104">Gibt eine ganze Zahl von 0 bis 23 für die Stunde des Tages in _Datetime_ oder _Expression_zurück.</span><span class="sxs-lookup"><span data-stu-id="373af-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="373af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="373af-105">Syntax</span></span>

<span data-ttu-id="373af-106">Stunde ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **])</span><span class="sxs-lookup"><span data-stu-id="373af-106">HOUR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="373af-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="373af-107">Parameters</span></span>

|<span data-ttu-id="373af-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="373af-108">**Name**</span></span>|<span data-ttu-id="373af-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="373af-109">**Required/Optional**</span></span>|<span data-ttu-id="373af-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="373af-110">**Data Type**</span></span>|<span data-ttu-id="373af-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="373af-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="373af-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="373af-112">_datetime_</span></span> <br/> |<span data-ttu-id="373af-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="373af-113">Required</span></span>  <br/> |<span data-ttu-id="373af-114">**String**</span><span class="sxs-lookup"><span data-stu-id="373af-114">**String**</span></span> <br/> | <span data-ttu-id="373af-115">Eine Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="373af-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="373af-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="373af-116">_expression_</span></span> <br/> |<span data-ttu-id="373af-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="373af-117">Required</span></span>  <br/> |<span data-ttu-id="373af-118">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="373af-118">**Varies**</span></span> <br/> |<span data-ttu-id="373af-119">Ein Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="373af-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="373af-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="373af-120">_lcid_</span></span> <br/> |<span data-ttu-id="373af-121">Optional</span><span class="sxs-lookup"><span data-stu-id="373af-121">Optional</span></span>  <br/> |<span data-ttu-id="373af-122">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="373af-122">**Number**</span></span> <br/> | <span data-ttu-id="373af-p101">Ein lokaler Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="373af-p101">A locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="373af-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="373af-125">Remarks</span></span>

<span data-ttu-id="373af-126">Die Datumskomponente in *Datetime* und *Expression* wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="373af-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="373af-127">Keine Rundung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="373af-127">No rounding is done.</span></span> <span data-ttu-id="373af-128">Die *Datetime* ist nicht vorhanden oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="373af-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="373af-129">Der zurückgegebene  Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="373af-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="373af-130">Die HOUR-Funktion nimmt auch einen einzelnen Zahlenwert für *Expression* , wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tages seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="373af-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="373af-131">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="373af-131">Example 1</span></span>

<span data-ttu-id="373af-132">HOUR("15:45")</span><span class="sxs-lookup"><span data-stu-id="373af-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="373af-133">Gibt 15 zurück.</span><span class="sxs-lookup"><span data-stu-id="373af-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="373af-134">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="373af-134">Example 2</span></span>

<span data-ttu-id="373af-135">HOUR("30. Mai 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="373af-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="373af-136">Gibt 15 zurück.</span><span class="sxs-lookup"><span data-stu-id="373af-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="373af-137">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="373af-137">Example 3</span></span>

<span data-ttu-id="373af-138">HOUR(0.5)</span><span class="sxs-lookup"><span data-stu-id="373af-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="373af-139">Gibt 12 zurück.</span><span class="sxs-lookup"><span data-stu-id="373af-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="373af-140">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="373af-140">Example 4</span></span>

<span data-ttu-id="373af-141">HOUR("30/5/1997")</span><span class="sxs-lookup"><span data-stu-id="373af-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="373af-142">Gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="373af-142">Returns 0.</span></span>
  

