---
title: TIMEVALUE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Gibt den Zeitwert zurück, der durch Datetime oder Ausdruck dargestellt wird, basierend auf den Einstellungen region und language des Systems.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432324"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="84de1-103">TIMEVALUE-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="84de1-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="84de1-104">Gibt den Zeitwert zurück, der durch  _datetime_ oder  _ausdruck_ dargestellt wird, basierend auf den Einstellungen region und language des Systems.</span><span class="sxs-lookup"><span data-stu-id="84de1-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="84de1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84de1-105">Syntax</span></span>

<span data-ttu-id="84de1-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *Ausdruck* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="84de1-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="84de1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="84de1-107">Parameters</span></span>

|<span data-ttu-id="84de1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="84de1-108">**Name**</span></span>|<span data-ttu-id="84de1-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="84de1-109">**Required/Optional**</span></span>|<span data-ttu-id="84de1-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="84de1-110">**Data Type**</span></span>|<span data-ttu-id="84de1-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="84de1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="84de1-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="84de1-112">_datetime_</span></span> <br/> |<span data-ttu-id="84de1-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="84de1-113">Required</span></span>  <br/> |<span data-ttu-id="84de1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="84de1-114">**String**</span></span> <br/> | <span data-ttu-id="84de1-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="84de1-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="84de1-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="84de1-116">_expression_</span></span> <br/> |<span data-ttu-id="84de1-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="84de1-117">Required</span></span>  <br/> |<span data-ttu-id="84de1-118">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="84de1-118">**Varies**</span></span> <br/> | <span data-ttu-id="84de1-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="84de1-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="84de1-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="84de1-120">_lcid_</span></span> <br/> |<span data-ttu-id="84de1-121">Optional.</span><span class="sxs-lookup"><span data-stu-id="84de1-121">Optional</span></span>  <br/> |<span data-ttu-id="84de1-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="84de1-122">**Number**</span></span> <br/> |<span data-ttu-id="84de1-p101">Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="84de1-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84de1-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="84de1-125">Remarks</span></span>

<span data-ttu-id="84de1-126">Jede Datumskomponente in  _datetime_ oder  _ausdruck_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="84de1-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="84de1-127">Wenn  _datetime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt diese Funktion eine #VALUE!</span><span class="sxs-lookup"><span data-stu-id="84de1-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="84de1-128">zurück.</span><span class="sxs-lookup"><span data-stu-id="84de1-128">error.</span></span> 
  
<span data-ttu-id="84de1-129">Die TIMEVALUE-Funktion akzeptiert auch  einen einzelnen Zahlenwert für ausdruck, wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tages seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="84de1-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="84de1-130">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="84de1-130">Example 1</span></span>

<span data-ttu-id="84de1-131">TIMEVALUE("06:00")</span><span class="sxs-lookup"><span data-stu-id="84de1-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="84de1-132">Gibt den Wert für 06:00 zurück.</span><span class="sxs-lookup"><span data-stu-id="84de1-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="84de1-133">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="84de1-133">Example 2</span></span>

<span data-ttu-id="84de1-134">TIMEVALUE("14:30")+4 vs.+30 vm.</span><span class="sxs-lookup"><span data-stu-id="84de1-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="84de1-135">Gibt den Wert für 19:00:00 zurück.</span><span class="sxs-lookup"><span data-stu-id="84de1-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="84de1-136">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="84de1-136">Example 3</span></span>

<span data-ttu-id="84de1-137">TIMEVALUE("11:00, 1. Juli 1997")</span><span class="sxs-lookup"><span data-stu-id="84de1-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="84de1-138">Gibt den Wert für 11:00 zurück.</span><span class="sxs-lookup"><span data-stu-id="84de1-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="84de1-139">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="84de1-139">Example 4</span></span>

<span data-ttu-id="84de1-140">TIMEVALUE(0,6337)</span><span class="sxs-lookup"><span data-stu-id="84de1-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="84de1-141">Gibt den Wert für 15:12:32 zurück.</span><span class="sxs-lookup"><span data-stu-id="84de1-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="84de1-142">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="84de1-142">Example 5</span></span>

<span data-ttu-id="84de1-143">TIMEVALUE("7:89")</span><span class="sxs-lookup"><span data-stu-id="84de1-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="84de1-p103">Gibt einen Fehler vom Typ #WERT! zurück.</span><span class="sxs-lookup"><span data-stu-id="84de1-p103">Returns a #VALUE! error.</span></span>
  

