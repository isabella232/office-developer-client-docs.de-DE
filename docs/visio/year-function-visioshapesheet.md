---
title: YEAR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Gibt eine ganze Zahl, die das gregorianische Jahr in Datetime oder Expression, formatiert entsprechend der im kurzen Datumsformat festlegen, indem die Standardeinstellungen des Systems aktuellen Region und Sprache darstellt.
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798469"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="10dc0-103">YEAR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="10dc0-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="10dc0-104">Gibt eine ganze Zahl, die das gregorianische Jahr in _Datetime_ oder _Ausdruck_, der im kurzen Datumsformat festlegen, indem die Standardeinstellungen des Systems aktuellen Region und Sprache darstellt.</span><span class="sxs-lookup"><span data-stu-id="10dc0-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="10dc0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10dc0-105">Syntax</span></span>

<span data-ttu-id="10dc0-106">Jahr ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **])</span><span class="sxs-lookup"><span data-stu-id="10dc0-106">YEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="10dc0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="10dc0-107">Parameters</span></span>

|<span data-ttu-id="10dc0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="10dc0-108">**Name**</span></span>|<span data-ttu-id="10dc0-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="10dc0-109">**Required/Optional**</span></span>|<span data-ttu-id="10dc0-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="10dc0-110">**Data Type**</span></span>|<span data-ttu-id="10dc0-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10dc0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="10dc0-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="10dc0-112">_datetime_</span></span> <br/> |<span data-ttu-id="10dc0-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="10dc0-113">Required</span></span>  <br/> |<span data-ttu-id="10dc0-114">**String**</span><span class="sxs-lookup"><span data-stu-id="10dc0-114">**String**</span></span> <br/> | <span data-ttu-id="10dc0-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="10dc0-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="10dc0-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="10dc0-116">_expression_</span></span> <br/> |<span data-ttu-id="10dc0-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="10dc0-117">Required</span></span>  <br/> |<span data-ttu-id="10dc0-118">**Varies**</span><span class="sxs-lookup"><span data-stu-id="10dc0-118">**Varies**</span></span> <br/> |<span data-ttu-id="10dc0-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="10dc0-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="10dc0-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="10dc0-120">_lcid_</span></span> <br/> |<span data-ttu-id="10dc0-121">Optional</span><span class="sxs-lookup"><span data-stu-id="10dc0-121">Optional</span></span>  <br/> |<span data-ttu-id="10dc0-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="10dc0-122">**Numeric**</span></span> <br/> |<span data-ttu-id="10dc0-p101">Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="10dc0-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="10dc0-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10dc0-125">Return value</span></span>

<span data-ttu-id="10dc0-126">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="10dc0-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="10dc0-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10dc0-127">Remarks</span></span>

<span data-ttu-id="10dc0-128">Die Zeitkomponente in _Datetime_ oder _Expression_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="10dc0-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="10dc0-129">Keine Rundung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="10dc0-129">No rounding is done.</span></span> <span data-ttu-id="10dc0-130">Wenn _Datetime_ nicht vorhanden ist oder nicht als gültige Datum oder Uhrzeit interpretiert werden kann, gibt Jahr einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="10dc0-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="10dc0-131">Die YEAR-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Ganzzahlteil des Ergebnisses für die Anzahl von Tagen seit dem 30. Dezember 1899 steht.</span><span class="sxs-lookup"><span data-stu-id="10dc0-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="10dc0-132">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10dc0-132">Example 1</span></span>

<span data-ttu-id="10dc0-133">YEAR("27/10/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="10dc0-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="10dc0-134">Gibt 2007 zurück.</span><span class="sxs-lookup"><span data-stu-id="10dc0-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="10dc0-135">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="10dc0-135">Example 2</span></span>

<span data-ttu-id="10dc0-136">YEAR(DATUMSWERT("25. Dez. 2006") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="10dc0-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="10dc0-137">Gibt 2007 zurück.</span><span class="sxs-lookup"><span data-stu-id="10dc0-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="10dc0-138">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="10dc0-138">Example 3</span></span>

<span data-ttu-id="10dc0-139">YEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="10dc0-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="10dc0-140">Gibt 1997 zurück.</span><span class="sxs-lookup"><span data-stu-id="10dc0-140">Returns 1997.</span></span>
  

