---
title: DATEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Der Date-Wert dargestellt durch Datetime oder Expression zurückgegeben.
ms.openlocfilehash: 7fcfd625b5e4e3da71a1b160c074401b672e0be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796806"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="5f08a-103">DATEVALUE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="5f08a-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="5f08a-104">Der Date-Wert dargestellt durch _Datetime_ oder _Expression_zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f08a-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5f08a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f08a-105">Syntax</span></span>

<span data-ttu-id="5f08a-106">DATEVALUE ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **])</span><span class="sxs-lookup"><span data-stu-id="5f08a-106">DATEVALUE(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5f08a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f08a-107">Parameters</span></span>

|<span data-ttu-id="5f08a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5f08a-108">**Name**</span></span>|<span data-ttu-id="5f08a-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5f08a-109">**Required/Optional**</span></span>|<span data-ttu-id="5f08a-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5f08a-110">**Data Type**</span></span>|<span data-ttu-id="5f08a-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f08a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5f08a-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="5f08a-112">_datetime_</span></span> <br/> |<span data-ttu-id="5f08a-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5f08a-113">Required</span></span>  <br/> |<span data-ttu-id="5f08a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5f08a-114">**String**</span></span> <br/> |<span data-ttu-id="5f08a-115">Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.</span><span class="sxs-lookup"><span data-stu-id="5f08a-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="5f08a-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="5f08a-116">_expression_</span></span> <br/> |<span data-ttu-id="5f08a-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5f08a-117">Required</span></span>  <br/> |<span data-ttu-id="5f08a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="5f08a-118">**String**</span></span> <br/> |<span data-ttu-id="5f08a-119">Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.</span><span class="sxs-lookup"><span data-stu-id="5f08a-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="5f08a-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="5f08a-120">_lcid_</span></span> <br/> |<span data-ttu-id="5f08a-121">Optional</span><span class="sxs-lookup"><span data-stu-id="5f08a-121">Optional</span></span>  <br/> |<span data-ttu-id="5f08a-122">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="5f08a-122">**Number**</span></span> <br/> |<span data-ttu-id="5f08a-p101">Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5f08a-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5f08a-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f08a-125">Return value</span></span>

<span data-ttu-id="5f08a-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="5f08a-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f08a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f08a-127">Remarks</span></span>

<span data-ttu-id="5f08a-128">Alle Zeitkomponenten in *Datetime* oder *Expression* wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="5f08a-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="5f08a-129">Wenn *Datetime* nicht vorhanden ist oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt DATEVALUE ein #VALUE!</span><span class="sxs-lookup"><span data-stu-id="5f08a-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="5f08a-130">Fehler.</span><span class="sxs-lookup"><span data-stu-id="5f08a-130">error.</span></span> 
  
<span data-ttu-id="5f08a-131">Der Wert wird in dem Kurzdatumsformat angezeigt, der aktuell in den Ländereinstellungen des Systems festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5f08a-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="5f08a-132">DATEVALUE-Funktion nimmt auch einen einzelnen Zahlenwert für *Expression* , wobei der Ganzzahlteil des Ergebnisses die Tagen seit dem 30. Dezember 1899 steht.</span><span class="sxs-lookup"><span data-stu-id="5f08a-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="5f08a-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f08a-133">Example 1</span></span>

<span data-ttu-id="5f08a-134">DATEVALUE(JETZT( ))+5 ed.</span><span class="sxs-lookup"><span data-stu-id="5f08a-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="5f08a-135">Gibt das Datum fünf Tage nach dem aktuellen Datum zurück.</span><span class="sxs-lookup"><span data-stu-id="5f08a-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5f08a-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5f08a-136">Example 2</span></span>

<span data-ttu-id="5f08a-137">DATEVALUE("19/7/1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="5f08a-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="5f08a-138">Gibt das Datum zurück.</span><span class="sxs-lookup"><span data-stu-id="5f08a-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5f08a-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5f08a-139">Example 3</span></span>

<span data-ttu-id="5f08a-140">DATEVALUE("33. Mai 1997")</span><span class="sxs-lookup"><span data-stu-id="5f08a-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="5f08a-p103">Gibt einen Fehler vom Typ #WERT! zurück.</span><span class="sxs-lookup"><span data-stu-id="5f08a-p103">Returns a #VALUE! error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="5f08a-143">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="5f08a-143">Example 4</span></span>

<span data-ttu-id="5f08a-144">DATEVALUE(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="5f08a-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="5f08a-145">Gibt 30.5. 1997 zurück.</span><span class="sxs-lookup"><span data-stu-id="5f08a-145">Returns 5/30/1997.</span></span>
  

