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
description: Gibt den Wert Datum und Uhrzeit, die durch Datetime oder Expression dargestellt.
ms.openlocfilehash: 001430acaf9fcb670e95157380e474e12b9728cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796808"
---
# <a name="datetime-function"></a><span data-ttu-id="d3689-103">DATETIME-Funktion</span><span class="sxs-lookup"><span data-stu-id="d3689-103">DATETIME Function</span></span>

<span data-ttu-id="d3689-104">Gibt den Wert Datum und Uhrzeit, die durch _Datetime_ oder _Expression_dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d3689-104">Returns the date and time value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d3689-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3689-105">Syntax</span></span>

<span data-ttu-id="d3689-106">DATETIME ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **])</span><span class="sxs-lookup"><span data-stu-id="d3689-106">DATETIME(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d3689-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3689-107">Parameters</span></span>

|<span data-ttu-id="d3689-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d3689-108">**Name**</span></span>|<span data-ttu-id="d3689-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="d3689-109">**Required/Optional**</span></span>|<span data-ttu-id="d3689-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d3689-110">**Data Type**</span></span>|<span data-ttu-id="d3689-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3689-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d3689-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="d3689-112">_datetime_</span></span> <br/> |<span data-ttu-id="d3689-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d3689-113">Required</span></span>  <br/> |<span data-ttu-id="d3689-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d3689-114">**String**</span></span> <br/> |<span data-ttu-id="d3689-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="d3689-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="d3689-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="d3689-116">_expression_</span></span> <br/> |<span data-ttu-id="d3689-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d3689-117">Required</span></span>  <br/> |<span data-ttu-id="d3689-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d3689-118">**String**</span></span> <br/> |<span data-ttu-id="d3689-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="d3689-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="d3689-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="d3689-120">_lcid_</span></span> <br/> |<span data-ttu-id="d3689-121">Optional</span><span class="sxs-lookup"><span data-stu-id="d3689-121">Optional</span></span>  <br/> |<span data-ttu-id="d3689-122">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="d3689-122">**Number**</span></span> <br/> |<span data-ttu-id="d3689-p101">Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="d3689-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d3689-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d3689-125">Return value</span></span>

<span data-ttu-id="d3689-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="d3689-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d3689-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3689-127">Remarks</span></span>

<span data-ttu-id="d3689-128">Wenn *Datetime* nicht vorhanden ist oder nicht als gültige Datum oder Uhrzeit interpretiert werden kann, gibt DATETIME einen #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d3689-128">If  *datetime*  is missing or cannot be interpreted as a valid date or time, DATETIME returns a #VALUE!</span></span> <span data-ttu-id="d3689-129">Fehler.</span><span class="sxs-lookup"><span data-stu-id="d3689-129">error.</span></span> 
  
<span data-ttu-id="d3689-130">Der Wert wird in dem kurzen Zeit- und Datumsformat geliefert, das aktuell in den länderspezifischen Systemeinstellungen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d3689-130">The returned value is formatted according to the short date style and time style in the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="d3689-131">Die DATETIME-Funktion nimmt auch einen einzelnen Zahlenwert für *Expression* , wobei der Ganzzahlteil des Ergebnisses für die Anzahl von Tagen seit dem 30. Dezember 1899 und der Dezimalteil den Bruchteil eines Tages seit Mitternacht darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3689-131">The DATETIME function also accepts a single number value for  *expression*  where the integer portion of the result represents the number of days since December 30, 1899, and the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d3689-132">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d3689-132">Example 1</span></span>

<span data-ttu-id="d3689-133">DATETIME("30. Mai 1997")+5 t.</span><span class="sxs-lookup"><span data-stu-id="d3689-133">DATETIME("May 30, 1997")+5 ed.</span></span>
  
<span data-ttu-id="d3689-134">Liefert den Wert, der 04.06.97 darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3689-134">Returns the value representing 6/4/1997.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d3689-135">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d3689-135">Example 2</span></span>

<span data-ttu-id="d3689-136">FORMAT(DATETIME("20/5/1997 14:30:45"),"C")</span><span class="sxs-lookup"><span data-stu-id="d3689-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span></span>
  
<span data-ttu-id="d3689-137">Liefert die Zeichenfolge "Dienstag, 20, Mai 1997, 14:30:45."</span><span class="sxs-lookup"><span data-stu-id="d3689-137">Returns the string "Tuesday, May 20, 1997 2:30:45 PM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d3689-138">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d3689-138">Example 3</span></span>

<span data-ttu-id="d3689-139">DATETIME("13:30 Juli 19")</span><span class="sxs-lookup"><span data-stu-id="d3689-139">DATETIME("1:30 PM July 19")</span></span>
  
<span data-ttu-id="d3689-140">Liefert den Wert, der den 19.7.2001 13:30:00 darstellt (wenn als aktuelles Jahr 2001 unterstellt wird).</span><span class="sxs-lookup"><span data-stu-id="d3689-140">Returns the value representing 7/19/2001 1:30:00 PM (assuming the current year is 2001).</span></span>
  
## <a name="example-4"></a><span data-ttu-id="d3689-141">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d3689-141">Example 4</span></span>

<span data-ttu-id="d3689-142">DATETIME(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="d3689-142">DATETIME(35580.6337)</span></span>
  
<span data-ttu-id="d3689-143">Liefert den Wert, der den 30.5.1997 15:12:32 darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3689-143">Returns the value representing 5/30/1997 3:12:32 PM.</span></span>
  

