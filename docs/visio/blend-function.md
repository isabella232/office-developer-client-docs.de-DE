---
title: BLEND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Mischt zwei Farben in dem Verhältnis, das vom Float-Parameter angegeben.
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796522"
---
# <a name="blend-function"></a><span data-ttu-id="5fc37-103">BLEND-Funktion</span><span class="sxs-lookup"><span data-stu-id="5fc37-103">BLEND Function</span></span>

<span data-ttu-id="5fc37-104">Mischt zwei Farben in dem Verhältnis, das vom _Float_ -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="5fc37-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5fc37-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fc37-105">Syntax</span></span>

<span data-ttu-id="5fc37-106">BLEND (** *color1* **, ** *color2* **, ** *Float [0,1]* **)</span><span class="sxs-lookup"><span data-stu-id="5fc37-106">BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5fc37-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fc37-107">Parameters</span></span>

|<span data-ttu-id="5fc37-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5fc37-108">**Name**</span></span>|<span data-ttu-id="5fc37-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5fc37-109">**Required/Optional**</span></span>|<span data-ttu-id="5fc37-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5fc37-110">**Data Type**</span></span>|<span data-ttu-id="5fc37-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5fc37-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5fc37-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="5fc37-112">_color1_</span></span> <br/> |<span data-ttu-id="5fc37-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5fc37-113">Required</span></span>  <br/> |<span data-ttu-id="5fc37-114">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="5fc37-114">**Numeric**</span></span> <br/> |<span data-ttu-id="5fc37-115">Der Farbindex von Visio oder der RGB-Wert der ersten Farbe.</span><span class="sxs-lookup"><span data-stu-id="5fc37-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="5fc37-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="5fc37-116">_color2_</span></span> <br/> |<span data-ttu-id="5fc37-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5fc37-117">Required</span></span>  <br/> |<span data-ttu-id="5fc37-118">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="5fc37-118">**Numeric**</span></span> <br/> |<span data-ttu-id="5fc37-119">Der Farbindex von Visio oder der RGB-Wert der zweiten Farbe.</span><span class="sxs-lookup"><span data-stu-id="5fc37-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="5fc37-120">_Float [0,1]_</span><span class="sxs-lookup"><span data-stu-id="5fc37-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="5fc37-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5fc37-121">Required</span></span>  <br/> |<span data-ttu-id="5fc37-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="5fc37-122">**Float**</span></span> <br/> |<span data-ttu-id="5fc37-123">Das Verhältnis, in dem _color2_ und _color1_, jeweils gemischt.</span><span class="sxs-lookup"><span data-stu-id="5fc37-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="5fc37-124">Eine reelle Zahl zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="5fc37-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5fc37-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5fc37-125">Return value</span></span>

 <span data-ttu-id="5fc37-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="5fc37-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fc37-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5fc37-127">Remarks</span></span>

<span data-ttu-id="5fc37-128">Die zurückgegebene Farbe wird durch die relativen Proportionen in dem _color2_ und _color1_, als vom _Float_ -Parameter angegebenen gemischt bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5fc37-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="5fc37-129">Beispielsweise ist _Float_ 0,25, die zurückgegebene Farbe zusammengesetzten 75 % der _color1_ und 25 % der _color2_.</span><span class="sxs-lookup"><span data-stu-id="5fc37-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="5fc37-130">Eine andere Möglichkeit, denken ist, dass der Punkt entlang der Color-Spektrum von _color1_ _color2_ _Float_ -Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="5fc37-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="5fc37-131">Aus diesem Grund Zahlen kleiner (näher null) für _Float_ erzeugen Farbverlauf näher zu _color1_, während größere (näher 1) Zahlen Farbverlauf näher zu _color2_erstellen.</span><span class="sxs-lookup"><span data-stu-id="5fc37-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

