---
title: BLEND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Mischt zwei Farben in dem durch den float-Parameter angegebenen Verhältnis.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432786"
---
# <a name="blend-function"></a><span data-ttu-id="ffedb-103">BLEND Function</span><span class="sxs-lookup"><span data-stu-id="ffedb-103">BLEND Function</span></span>

<span data-ttu-id="ffedb-104">Mischt zwei Farben in dem durch den  _float-Parameter angegebenen_ Verhältnis.</span><span class="sxs-lookup"><span data-stu-id="ffedb-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ffedb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffedb-105">Syntax</span></span>

<span data-ttu-id="ffedb-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ffedb-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ffedb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffedb-107">Parameters</span></span>

|<span data-ttu-id="ffedb-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ffedb-108">**Name**</span></span>|<span data-ttu-id="ffedb-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ffedb-109">**Required/Optional**</span></span>|<span data-ttu-id="ffedb-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ffedb-110">**Data Type**</span></span>|<span data-ttu-id="ffedb-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffedb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ffedb-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="ffedb-112">_color1_</span></span> <br/> |<span data-ttu-id="ffedb-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ffedb-113">Required</span></span>  <br/> |<span data-ttu-id="ffedb-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ffedb-114">**Numeric**</span></span> <br/> |<span data-ttu-id="ffedb-115">Der Farbindex von Visio oder der RGB-Wert der ersten Farbe.</span><span class="sxs-lookup"><span data-stu-id="ffedb-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="ffedb-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="ffedb-116">_color2_</span></span> <br/> |<span data-ttu-id="ffedb-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ffedb-117">Required</span></span>  <br/> |<span data-ttu-id="ffedb-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ffedb-118">**Numeric**</span></span> <br/> |<span data-ttu-id="ffedb-119">Der Farbindex von Visio oder der RGB-Wert der zweiten Farbe.</span><span class="sxs-lookup"><span data-stu-id="ffedb-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="ffedb-120">_float[0,1]_</span><span class="sxs-lookup"><span data-stu-id="ffedb-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="ffedb-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ffedb-121">Required</span></span>  <br/> |<span data-ttu-id="ffedb-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="ffedb-122">**Float**</span></span> <br/> |<span data-ttu-id="ffedb-123">Das Verhältnis, in dem  _Farbe2_ bzw.  _Farbe1_ gemischt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffedb-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="ffedb-124">Eine reelle Zahl zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="ffedb-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ffedb-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffedb-125">Return value</span></span>

 <span data-ttu-id="ffedb-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="ffedb-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffedb-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffedb-127">Remarks</span></span>

<span data-ttu-id="ffedb-128">Die zurückgegebene Farbe wird durch die relativen Proportionen bestimmt, in denen  _color2_ und  _color1_ bzw. , wie durch den  _float-Parameter angegeben, gemischt_ werden.</span><span class="sxs-lookup"><span data-stu-id="ffedb-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="ffedb-129">Wenn float  _z._ B. 0,25 ist, besteht die zurückgegebene Farbe aus 75 % von  _Color1_ und 25 %  _von Color2_.</span><span class="sxs-lookup"><span data-stu-id="ffedb-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="ffedb-130">Eine weitere Möglichkeit, sich darüber Gedanken zu machen, ist, dass der _Float-Wert_ dem Punkt entlang des Farbspektrums von _Color1_ bis _Color2 entspricht._</span><span class="sxs-lookup"><span data-stu-id="ffedb-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="ffedb-131">Daher werden kleinere Zahlen (näher  an Null) für float näher an _Farbe1_ erzeugt, während größere Zahlen (näher an 1) Blends näher an _Color2 erzeugen._</span><span class="sxs-lookup"><span data-stu-id="ffedb-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

