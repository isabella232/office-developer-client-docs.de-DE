---
title: MONTH-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Gibt eine ganze Zahl zwischen 1 und 12 zurück, die einen Monat darstellt.
ms.openlocfilehash: 71ecc7992839c871780e9b703377db37279246e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335273"
---
# <a name="month-function-visioshapesheet"></a><span data-ttu-id="d23f8-103">MONTH-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d23f8-103">MONTH Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d23f8-104">Gibt eine ganze Zahl zwischen 1 und 12 zurück, die einen Monat darstellt.</span><span class="sxs-lookup"><span data-stu-id="d23f8-104">Returns an integer from 1 to 12 that represents a month.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d23f8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d23f8-105">Syntax</span></span>

<span data-ttu-id="d23f8-106">MONTH ("\* \* *DateTime* \* \*" | \* \* *Expression* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="d23f8-106">MONTH(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d23f8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d23f8-107">Parameters</span></span>

|<span data-ttu-id="d23f8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d23f8-108">**Name**</span></span>|<span data-ttu-id="d23f8-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="d23f8-109">**Required/Optional**</span></span>|<span data-ttu-id="d23f8-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d23f8-110">**Data Type**</span></span>|<span data-ttu-id="d23f8-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d23f8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d23f8-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="d23f8-112">_datetime_</span></span> <br/> |<span data-ttu-id="d23f8-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d23f8-113">Required</span></span>  <br/> |<span data-ttu-id="d23f8-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d23f8-114">**String**</span></span> <br/> |<span data-ttu-id="d23f8-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="d23f8-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="d23f8-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="d23f8-116">_expression_</span></span> <br/> |<span data-ttu-id="d23f8-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d23f8-117">Required</span></span>  <br/> |<span data-ttu-id="d23f8-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d23f8-118">**String**</span></span> <br/> | <span data-ttu-id="d23f8-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="d23f8-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="d23f8-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="d23f8-120">_lcid_</span></span> <br/> |<span data-ttu-id="d23f8-121">Optional</span><span class="sxs-lookup"><span data-stu-id="d23f8-121">Optional</span></span>  <br/> |<span data-ttu-id="d23f8-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="d23f8-122">**Number**</span></span> <br/> |<span data-ttu-id="d23f8-123">Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d23f8-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="d23f8-124">Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="d23f8-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d23f8-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d23f8-125">Return value</span></span>

<span data-ttu-id="d23f8-126">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="d23f8-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d23f8-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d23f8-127">Remarks</span></span>

<span data-ttu-id="d23f8-128">Die Zeitkomponente von _DateTime_ oder _Expression_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="d23f8-128">The time component of  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="d23f8-p102">Es findet kein Auf- oder Abrunden statt. Wenn die Eingabezeichenfolge nicht angegeben wurde oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die MONTH-Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d23f8-p102">No rounding is done. If the input string is missing or cannot be converted to a valid result, the MONTH function returns an error.</span></span>
  
<span data-ttu-id="d23f8-131">Der Wert wird in dem Kurzdatumsformat zurückgegeben, der aktuell in den Ländereinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d23f8-131">The returned value is formatted according to the short date style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="d23f8-132">Die MONTH-Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der ganzzahlige Teil des Ergebnisses die Anzahl von Tagen seit dem 30. Dezember 1899 darstellt.</span><span class="sxs-lookup"><span data-stu-id="d23f8-132">The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d23f8-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d23f8-133">Example 1</span></span>

<span data-ttu-id="d23f8-134">MONTH("30. Mai 1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="d23f8-134">MONTH("May 30, 1999 13:45:24")</span></span>
  
<span data-ttu-id="d23f8-135">Gibt 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="d23f8-135">Returns 5.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d23f8-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d23f8-136">Example 2</span></span>

<span data-ttu-id="d23f8-137">MONTH(DATUMSWERT("30. Mai 1999")+7 t.)</span><span class="sxs-lookup"><span data-stu-id="d23f8-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span></span>
  
<span data-ttu-id="d23f8-138">Gibt 6 zurück.</span><span class="sxs-lookup"><span data-stu-id="d23f8-138">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d23f8-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d23f8-139">Example 3</span></span>

<span data-ttu-id="d23f8-140">MONAT (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="d23f8-140">MONTH(35580.6337)</span></span>
  
<span data-ttu-id="d23f8-141">Gibt 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="d23f8-141">Returns 5.</span></span>
  

