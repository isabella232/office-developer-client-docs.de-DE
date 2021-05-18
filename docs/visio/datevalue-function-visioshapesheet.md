---
title: DATEVALUE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Gibt den Datumswert zurück, der durch datetime oder expression dargestellt wird.
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360312"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="20eca-103">DATEVALUE-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="20eca-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="20eca-104">Gibt den Datumswert zurück, der durch _datetime oder_ ausdruck dargestellt _wird._</span><span class="sxs-lookup"><span data-stu-id="20eca-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="20eca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20eca-105">Syntax</span></span>

<span data-ttu-id="20eca-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *Ausdruck* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="20eca-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="20eca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="20eca-107">Parameters</span></span>

|<span data-ttu-id="20eca-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="20eca-108">**Name**</span></span>|<span data-ttu-id="20eca-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="20eca-109">**Required/Optional**</span></span>|<span data-ttu-id="20eca-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="20eca-110">**Data Type**</span></span>|<span data-ttu-id="20eca-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20eca-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="20eca-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="20eca-112">_datetime_</span></span> <br/> |<span data-ttu-id="20eca-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="20eca-113">Required</span></span>  <br/> |<span data-ttu-id="20eca-114">**String**</span><span class="sxs-lookup"><span data-stu-id="20eca-114">**String**</span></span> <br/> |<span data-ttu-id="20eca-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="20eca-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="20eca-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="20eca-116">_expression_</span></span> <br/> |<span data-ttu-id="20eca-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="20eca-117">Required</span></span>  <br/> |<span data-ttu-id="20eca-118">**String**</span><span class="sxs-lookup"><span data-stu-id="20eca-118">**String**</span></span> <br/> |<span data-ttu-id="20eca-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="20eca-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="20eca-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="20eca-120">_lcid_</span></span> <br/> |<span data-ttu-id="20eca-121">Optional.</span><span class="sxs-lookup"><span data-stu-id="20eca-121">Optional</span></span>  <br/> |<span data-ttu-id="20eca-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="20eca-122">**Number**</span></span> <br/> |<span data-ttu-id="20eca-p101">Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="20eca-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="20eca-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20eca-125">Return value</span></span>

<span data-ttu-id="20eca-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="20eca-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20eca-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20eca-127">Remarks</span></span>

<span data-ttu-id="20eca-128">Jede Zeitkomponente in  *datetime*  oder  *ausdruck*  wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="20eca-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="20eca-129">Wenn  *datetime*  fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt DATEVALUE eine #VALUE!</span><span class="sxs-lookup"><span data-stu-id="20eca-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="20eca-130">zurück.</span><span class="sxs-lookup"><span data-stu-id="20eca-130">error.</span></span> 
  
<span data-ttu-id="20eca-131">Der Wert wird in dem Kurzdatumsformat angezeigt, der aktuell in den Ländereinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="20eca-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="20eca-132">Die DATEVALUE-Funktion akzeptiert auch  einen einzelnen Zahlenwert für ausdruck, wobei der ganzzahlige Teil des Ergebnisses die Tage seit dem 30. Dezember 1899 darstellt.</span><span class="sxs-lookup"><span data-stu-id="20eca-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="20eca-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20eca-133">Example 1</span></span>

<span data-ttu-id="20eca-134">DATEVALUE(JETZT( ))+5 ed.</span><span class="sxs-lookup"><span data-stu-id="20eca-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="20eca-135">Gibt das Datum fünf Tage nach dem aktuellen Datum zurück.</span><span class="sxs-lookup"><span data-stu-id="20eca-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="20eca-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="20eca-136">Example 2</span></span>

<span data-ttu-id="20eca-137">DATEVALUE("19.07.1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="20eca-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="20eca-138">Gibt das Datum zurück.</span><span class="sxs-lookup"><span data-stu-id="20eca-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="20eca-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="20eca-139">Example 3</span></span>

<span data-ttu-id="20eca-140">DATEVALUE("33. Mai 1997")</span><span class="sxs-lookup"><span data-stu-id="20eca-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="20eca-p103">Gibt einen Fehler vom Typ #WERT! zurück.</span><span class="sxs-lookup"><span data-stu-id="20eca-p103">Returns a #VALUE! error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="20eca-143">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="20eca-143">Example 4</span></span>

<span data-ttu-id="20eca-144">DATEVALUE(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="20eca-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="20eca-145">Gibt 30.5. 1997 zurück.</span><span class="sxs-lookup"><span data-stu-id="20eca-145">Returns 5/30/1997.</span></span>
  

