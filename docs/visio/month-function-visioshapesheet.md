---
title: MONTH Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Gibt eine Ganzzahl zwischen 1 und 12, die einen Monat darstellt.
ms.openlocfilehash: e17803a153b4aadec34aa751da7efa077963bba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797531"
---
# <a name="month-function-visioshapesheet"></a><span data-ttu-id="82aa7-103">MONTH Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="82aa7-103">MONTH Function (VisioShapeSheet)</span></span>

<span data-ttu-id="82aa7-104">Gibt eine Ganzzahl zwischen 1 und 12, die einen Monat darstellt.</span><span class="sxs-lookup"><span data-stu-id="82aa7-104">Returns an integer from 1 to 12 that represents a month.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="82aa7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82aa7-105">Syntax</span></span>

<span data-ttu-id="82aa7-106">Monat ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **])</span><span class="sxs-lookup"><span data-stu-id="82aa7-106">MONTH(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="82aa7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="82aa7-107">Parameters</span></span>

|<span data-ttu-id="82aa7-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="82aa7-108">**Name**</span></span>|<span data-ttu-id="82aa7-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="82aa7-109">**Required/Optional**</span></span>|<span data-ttu-id="82aa7-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="82aa7-110">**Data Type**</span></span>|<span data-ttu-id="82aa7-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="82aa7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="82aa7-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="82aa7-112">_datetime_</span></span> <br/> |<span data-ttu-id="82aa7-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="82aa7-113">Required</span></span>  <br/> |<span data-ttu-id="82aa7-114">**String**</span><span class="sxs-lookup"><span data-stu-id="82aa7-114">**String**</span></span> <br/> |<span data-ttu-id="82aa7-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="82aa7-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="82aa7-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="82aa7-116">_expression_</span></span> <br/> |<span data-ttu-id="82aa7-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="82aa7-117">Required</span></span>  <br/> |<span data-ttu-id="82aa7-118">**String**</span><span class="sxs-lookup"><span data-stu-id="82aa7-118">**String**</span></span> <br/> | <span data-ttu-id="82aa7-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="82aa7-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="82aa7-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="82aa7-120">_lcid_</span></span> <br/> |<span data-ttu-id="82aa7-121">Optional</span><span class="sxs-lookup"><span data-stu-id="82aa7-121">Optional</span></span>  <br/> |<span data-ttu-id="82aa7-122">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="82aa7-122">**Number**</span></span> <br/> |<span data-ttu-id="82aa7-p101">Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="82aa7-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="82aa7-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="82aa7-125">Return value</span></span>

<span data-ttu-id="82aa7-126">Integer</span><span class="sxs-lookup"><span data-stu-id="82aa7-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82aa7-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82aa7-127">Remarks</span></span>

<span data-ttu-id="82aa7-128">Die Zeitkomponente in _Datetime_ oder _Expression_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="82aa7-128">The time component of  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="82aa7-p102">Es findet kein Auf- oder Abrunden statt. Wenn die Eingabezeichenfolge nicht angegeben wurde oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die MONTH-Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="82aa7-p102">No rounding is done. If the input string is missing or cannot be converted to a valid result, the MONTH function returns an error.</span></span>
  
<span data-ttu-id="82aa7-131">Der Wert wird in dem Kurzdatumsformat zurückgegeben, der aktuell in den Ländereinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="82aa7-131">The returned value is formatted according to the short date style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="82aa7-132">MONTH-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Ganzzahlteil des Ergebnisses für die Anzahl von Tagen seit dem 30. Dezember 1899 steht.</span><span class="sxs-lookup"><span data-stu-id="82aa7-132">The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="82aa7-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82aa7-133">Example 1</span></span>

<span data-ttu-id="82aa7-134">MONTH("30. Mai 1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="82aa7-134">MONTH("May 30, 1999 13:45:24")</span></span>
  
<span data-ttu-id="82aa7-135">Gibt 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="82aa7-135">Returns 5.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="82aa7-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="82aa7-136">Example 2</span></span>

<span data-ttu-id="82aa7-137">MONTH(DATUMSWERT("30. Mai 1999")+7 t.)</span><span class="sxs-lookup"><span data-stu-id="82aa7-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span></span>
  
<span data-ttu-id="82aa7-138">Gibt 6 zurück.</span><span class="sxs-lookup"><span data-stu-id="82aa7-138">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="82aa7-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="82aa7-139">Example 3</span></span>

<span data-ttu-id="82aa7-140">MONTH(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="82aa7-140">MONTH(35580.6337)</span></span>
  
<span data-ttu-id="82aa7-141">Gibt 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="82aa7-141">Returns 5.</span></span>
  

