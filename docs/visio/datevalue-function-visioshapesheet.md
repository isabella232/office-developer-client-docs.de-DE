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
description: Gibt den durch DateTime oder Expression dargestellten Date-Wert zurück.
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360312"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="fe7fe-103">DATEVALUE-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fe7fe-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fe7fe-104">Gibt den durch _DateTime_ oder _Expression_dargestellten Date-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fe7fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe7fe-105">Syntax</span></span>

<span data-ttu-id="fe7fe-106">DATEvalue ("\* \* *DateTime* \* \*" | \* \* *Expression* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="fe7fe-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fe7fe-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe7fe-107">Parameters</span></span>

|<span data-ttu-id="fe7fe-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fe7fe-108">**Name**</span></span>|<span data-ttu-id="fe7fe-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="fe7fe-109">**Required/Optional**</span></span>|<span data-ttu-id="fe7fe-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="fe7fe-110">**Data Type**</span></span>|<span data-ttu-id="fe7fe-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe7fe-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fe7fe-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="fe7fe-112">_datetime_</span></span> <br/> |<span data-ttu-id="fe7fe-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fe7fe-113">Required</span></span>  <br/> |<span data-ttu-id="fe7fe-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fe7fe-114">**String**</span></span> <br/> |<span data-ttu-id="fe7fe-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="fe7fe-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="fe7fe-116">_expression_</span></span> <br/> |<span data-ttu-id="fe7fe-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fe7fe-117">Required</span></span>  <br/> |<span data-ttu-id="fe7fe-118">**String**</span><span class="sxs-lookup"><span data-stu-id="fe7fe-118">**String**</span></span> <br/> |<span data-ttu-id="fe7fe-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="fe7fe-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="fe7fe-120">_lcid_</span></span> <br/> |<span data-ttu-id="fe7fe-121">Optional</span><span class="sxs-lookup"><span data-stu-id="fe7fe-121">Optional</span></span>  <br/> |<span data-ttu-id="fe7fe-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="fe7fe-122">**Number**</span></span> <br/> |<span data-ttu-id="fe7fe-p101">Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fe7fe-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe7fe-125">Return value</span></span>

<span data-ttu-id="fe7fe-126">DateTime</span><span class="sxs-lookup"><span data-stu-id="fe7fe-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe7fe-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe7fe-127">Remarks</span></span>

<span data-ttu-id="fe7fe-128">Alle Zeitkomponenten in *DateTime* oder *Expression* werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="fe7fe-129">Wenn *DateTime* fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt DateValue eine #VALUE zurück!</span><span class="sxs-lookup"><span data-stu-id="fe7fe-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="fe7fe-130">zurück.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-130">error.</span></span> 
  
<span data-ttu-id="fe7fe-131">Der Wert wird in dem Kurzdatumsformat angezeigt, der aktuell in den Ländereinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="fe7fe-132">Die DATEvalue-Funktion akzeptiert auch einen einzelnen Zahlenwert für *Expression* , wobei der ganzzahlige Teil des Ergebnisses die Tage seit dem 30. Dezember 1899 darstellt.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fe7fe-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe7fe-133">Example 1</span></span>

<span data-ttu-id="fe7fe-134">DATEVALUE(JETZT( ))+5 ed.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="fe7fe-135">Gibt das Datum fünf Tage nach dem aktuellen Datum zurück.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fe7fe-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fe7fe-136">Example 2</span></span>

<span data-ttu-id="fe7fe-137">DATEVALUE ("7/19/1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="fe7fe-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="fe7fe-138">Gibt das Datum zurück.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fe7fe-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fe7fe-139">Example 3</span></span>

<span data-ttu-id="fe7fe-140">DATEVALUE("33. Mai 1997")</span><span class="sxs-lookup"><span data-stu-id="fe7fe-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="fe7fe-p103">Gibt einen Fehler vom Typ #WERT! zurück.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-p103">Returns a #VALUE! error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="fe7fe-143">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="fe7fe-143">Example 4</span></span>

<span data-ttu-id="fe7fe-144">DATEVALUE (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="fe7fe-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="fe7fe-145">Gibt 30.5. 1997 zurück.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-145">Returns 5/30/1997.</span></span>
  

