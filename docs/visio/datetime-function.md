---
title: DATETIME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Gibt den Datums- und Uhrzeitwert zurück, der durch datetime oder expression dargestellt wird.
ms.openlocfilehash: 2da084f685c044d48495b04f727a877140b51004
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360319"
---
# <a name="datetime-function"></a><span data-ttu-id="614c6-103">DATETIME-Funktion</span><span class="sxs-lookup"><span data-stu-id="614c6-103">DATETIME Function</span></span>

<span data-ttu-id="614c6-104">Gibt den Datums- und Uhrzeitwert zurück, der durch _datetime oder_ expression dargestellt _wird._</span><span class="sxs-lookup"><span data-stu-id="614c6-104">Returns the date and time value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="614c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="614c6-105">Syntax</span></span>

<span data-ttu-id="614c6-106">DATETIME(" \*\* *datetime* \*\* "| \*\* *Ausdruck* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="614c6-106">DATETIME(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="614c6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="614c6-107">Parameters</span></span>

|<span data-ttu-id="614c6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="614c6-108">**Name**</span></span>|<span data-ttu-id="614c6-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="614c6-109">**Required/Optional**</span></span>|<span data-ttu-id="614c6-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="614c6-110">**Data Type**</span></span>|<span data-ttu-id="614c6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="614c6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="614c6-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="614c6-112">_datetime_</span></span> <br/> |<span data-ttu-id="614c6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="614c6-113">Required</span></span>  <br/> |<span data-ttu-id="614c6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="614c6-114">**String**</span></span> <br/> |<span data-ttu-id="614c6-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="614c6-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="614c6-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="614c6-116">_expression_</span></span> <br/> |<span data-ttu-id="614c6-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="614c6-117">Required</span></span>  <br/> |<span data-ttu-id="614c6-118">**String**</span><span class="sxs-lookup"><span data-stu-id="614c6-118">**String**</span></span> <br/> |<span data-ttu-id="614c6-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="614c6-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="614c6-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="614c6-120">_lcid_</span></span> <br/> |<span data-ttu-id="614c6-121">Optional.</span><span class="sxs-lookup"><span data-stu-id="614c6-121">Optional</span></span>  <br/> |<span data-ttu-id="614c6-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="614c6-122">**Number**</span></span> <br/> |<span data-ttu-id="614c6-p101">Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="614c6-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="614c6-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="614c6-125">Return value</span></span>

<span data-ttu-id="614c6-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="614c6-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="614c6-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="614c6-127">Remarks</span></span>

<span data-ttu-id="614c6-128">Wenn  *datetime*  fehlt oder nicht als gültiges Datum oder eine gültige Uhrzeit interpretiert werden kann, gibt DATETIME eine #VALUE!</span><span class="sxs-lookup"><span data-stu-id="614c6-128">If  *datetime*  is missing or cannot be interpreted as a valid date or time, DATETIME returns a #VALUE!</span></span> <span data-ttu-id="614c6-129">zurück.</span><span class="sxs-lookup"><span data-stu-id="614c6-129">error.</span></span> 
  
<span data-ttu-id="614c6-130">Der Wert wird in dem kurzen Zeit- und Datumsformat geliefert, das aktuell in den länderspezifischen Systemeinstellungen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="614c6-130">The returned value is formatted according to the short date style and time style in the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="614c6-131">Die DATETIME-Funktion akzeptiert auch  einen einzelnen Zahlenwert für den Ausdruck, wobei der ganzzahlige Teil des Ergebnisses die Anzahl der Tage seit dem 30. Dezember 1899 darstellt, und der Dezimalteil den Bruchteil eines Tages seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="614c6-131">The DATETIME function also accepts a single number value for  *expression*  where the integer portion of the result represents the number of days since December 30, 1899, and the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="614c6-132">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="614c6-132">Example 1</span></span>

<span data-ttu-id="614c6-133">DATETIME("30. Mai 1997")+5 t.</span><span class="sxs-lookup"><span data-stu-id="614c6-133">DATETIME("May 30, 1997")+5 ed.</span></span>
  
<span data-ttu-id="614c6-134">Liefert den Wert, der 04.06.97 darstellt.</span><span class="sxs-lookup"><span data-stu-id="614c6-134">Returns the value representing 6/4/1997.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="614c6-135">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="614c6-135">Example 2</span></span>

<span data-ttu-id="614c6-136">FORMAT(DATETIME("20/5/1997 14:30:45"),"C")</span><span class="sxs-lookup"><span data-stu-id="614c6-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span></span>
  
<span data-ttu-id="614c6-137">Liefert die Zeichenfolge "Dienstag, 20, Mai 1997, 14:30:45."</span><span class="sxs-lookup"><span data-stu-id="614c6-137">Returns the string "Tuesday, May 20, 1997 2:30:45 PM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="614c6-138">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="614c6-138">Example 3</span></span>

<span data-ttu-id="614c6-139">DATETIME("13:30 Juli 19")</span><span class="sxs-lookup"><span data-stu-id="614c6-139">DATETIME("1:30 PM July 19")</span></span>
  
<span data-ttu-id="614c6-140">Liefert den Wert, der den 19.7.2001 13:30:00 darstellt (wenn als aktuelles Jahr 2001 unterstellt wird).</span><span class="sxs-lookup"><span data-stu-id="614c6-140">Returns the value representing 7/19/2001 1:30:00 PM (assuming the current year is 2001).</span></span>
  
## <a name="example-4"></a><span data-ttu-id="614c6-141">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="614c6-141">Example 4</span></span>

<span data-ttu-id="614c6-142">DATETIME(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="614c6-142">DATETIME(35580.6337)</span></span>
  
<span data-ttu-id="614c6-143">Liefert den Wert, der den 30.5.1997 15:12:32 darstellt.</span><span class="sxs-lookup"><span data-stu-id="614c6-143">Returns the value representing 5/30/1997 3:12:32 PM.</span></span>
  

