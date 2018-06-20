---
title: DAYOFYEAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Gibt eine ganze Zahl 1 und 366, die den laufenden Tag des Jahres in Datetime oder Expression darstellt. Die DAYOFYEAR-Funktion verwendet den gregorianischen Kalender.
ms.openlocfilehash: 2fd80a2554c268d276deaa524a9d98eebc6a48d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796831"
---
# <a name="dayofyear-function"></a><span data-ttu-id="00cda-104">DAYOFYEAR Function</span><span class="sxs-lookup"><span data-stu-id="00cda-104">DAYOFYEAR Function</span></span>

<span data-ttu-id="00cda-105">Gibt eine ganze Zahl 1 und 366, die den laufenden Tag des Jahres in _Datetime_ oder _Expression_darstellt.</span><span class="sxs-lookup"><span data-stu-id="00cda-105">Returns an integer, 1 to 366, that represents the sequential day of the year in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="00cda-106">Die DAYOFYEAR-Funktion verwendet den gregorianischen Kalender.</span><span class="sxs-lookup"><span data-stu-id="00cda-106">The DAYOFYEAR function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="00cda-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="00cda-107">Syntax</span></span>

<span data-ttu-id="00cda-108">DAYOFYEAR ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **])</span><span class="sxs-lookup"><span data-stu-id="00cda-108">DAYOFYEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="00cda-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="00cda-109">Parameters</span></span>

|<span data-ttu-id="00cda-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="00cda-110">**Name**</span></span>|<span data-ttu-id="00cda-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="00cda-111">**Required/Optional**</span></span>|<span data-ttu-id="00cda-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="00cda-112">**Data Type**</span></span>|<span data-ttu-id="00cda-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00cda-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="00cda-114">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="00cda-114">_datetime_</span></span> <br/> |<span data-ttu-id="00cda-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="00cda-115">Required</span></span>  <br/> |<span data-ttu-id="00cda-116">**String**</span><span class="sxs-lookup"><span data-stu-id="00cda-116">**String**</span></span> <br/> |<span data-ttu-id="00cda-117">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="00cda-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="00cda-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="00cda-118">_expression_</span></span> <br/> |<span data-ttu-id="00cda-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="00cda-119">Required</span></span>  <br/> |<span data-ttu-id="00cda-120">**String**</span><span class="sxs-lookup"><span data-stu-id="00cda-120">**String**</span></span> <br/> |<span data-ttu-id="00cda-121">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="00cda-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="00cda-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="00cda-122">_lcid_</span></span> <br/> |<span data-ttu-id="00cda-123">Optional</span><span class="sxs-lookup"><span data-stu-id="00cda-123">Optional</span></span>  <br/> |<span data-ttu-id="00cda-124">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="00cda-124">**Number**</span></span> <br/> |<span data-ttu-id="00cda-p103">Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="00cda-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="00cda-127">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="00cda-127">Return value</span></span>

<span data-ttu-id="00cda-128">Integer</span><span class="sxs-lookup"><span data-stu-id="00cda-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00cda-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00cda-129">Remarks</span></span>

<span data-ttu-id="00cda-130">Alle Zeitkomponenten in _Datetime_ oder _Expression_ wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="00cda-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="00cda-131">Das Ergebnis entspricht dem 1. Januar und dem 31. Dezember.</span><span class="sxs-lookup"><span data-stu-id="00cda-131">The result corresponds to January 1 to December 31.</span></span> <span data-ttu-id="00cda-132">Keine Rundung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="00cda-132">No rounding is done.</span></span> <span data-ttu-id="00cda-133">Wenn _Datetime_ nicht vorhanden ist oder nicht als gültige Datum oder Uhrzeit interpretiert werden kann, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="00cda-133">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns an error.</span></span> 
  
<span data-ttu-id="00cda-134">Die DAYOFYEAR-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Ganzzahlteil des Ergebnisses für die Anzahl von Tagen seit dem 30. Dezember 1899 steht.</span><span class="sxs-lookup"><span data-stu-id="00cda-134">The DAYOFYEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="00cda-135">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00cda-135">Example 1</span></span>

<span data-ttu-id="00cda-136">DAYOFYEAR("30. Mai 1997 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="00cda-136">DAYOFYEAR("May 30, 1997 13:45:24")</span></span>
  
<span data-ttu-id="00cda-137">Gibt 150 zurück</span><span class="sxs-lookup"><span data-stu-id="00cda-137">Returns 150.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="00cda-138">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="00cda-138">Example 2</span></span>

<span data-ttu-id="00cda-139">DAYOFYEAR(DATUMSWERT("30. Mai 1997")+7 t.)</span><span class="sxs-lookup"><span data-stu-id="00cda-139">DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="00cda-140">Gibt 157 zurück.</span><span class="sxs-lookup"><span data-stu-id="00cda-140">Returns 157.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="00cda-141">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="00cda-141">Example 3</span></span>

<span data-ttu-id="00cda-142">DAYOFYEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="00cda-142">DAYOFYEAR(35580.6337)</span></span>
  
<span data-ttu-id="00cda-143">Gibt 150 zurück.</span><span class="sxs-lookup"><span data-stu-id="00cda-143">Returns 150.</span></span>
  

