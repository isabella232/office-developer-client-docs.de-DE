---
title: BLEND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Fügt zwei Farben in den durch den Parameter float angegebenen Anteil ein.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303297"
---
# <a name="blend-function"></a><span data-ttu-id="8d034-103">BLEND Function</span><span class="sxs-lookup"><span data-stu-id="8d034-103">BLEND Function</span></span>

<span data-ttu-id="8d034-104">Fügt zwei Farben in den durch den Parameter _float_ angegebenen Anteil ein.</span><span class="sxs-lookup"><span data-stu-id="8d034-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d034-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d034-105">Syntax</span></span>

<span data-ttu-id="8d034-106">BLEND (\* \* *color1* \* \*, \* \* *color2* \* \*, \* \* *float [0, 1]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8d034-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d034-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d034-107">Parameters</span></span>

|<span data-ttu-id="8d034-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8d034-108">**Name**</span></span>|<span data-ttu-id="8d034-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8d034-109">**Required/Optional**</span></span>|<span data-ttu-id="8d034-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8d034-110">**Data Type**</span></span>|<span data-ttu-id="8d034-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d034-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d034-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="8d034-112">_color1_</span></span> <br/> |<span data-ttu-id="8d034-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d034-113">Required</span></span>  <br/> |<span data-ttu-id="8d034-114">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="8d034-114">**Numeric**</span></span> <br/> |<span data-ttu-id="8d034-115">Der Farbindex von Visio oder der RGB-Wert der ersten Farbe.</span><span class="sxs-lookup"><span data-stu-id="8d034-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="8d034-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="8d034-116">_color2_</span></span> <br/> |<span data-ttu-id="8d034-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d034-117">Required</span></span>  <br/> |<span data-ttu-id="8d034-118">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="8d034-118">**Numeric**</span></span> <br/> |<span data-ttu-id="8d034-119">Der Farbindex von Visio oder der RGB-Wert der zweiten Farbe.</span><span class="sxs-lookup"><span data-stu-id="8d034-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="8d034-120">_float [0, 1]_</span><span class="sxs-lookup"><span data-stu-id="8d034-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="8d034-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d034-121">Required</span></span>  <br/> |<span data-ttu-id="8d034-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="8d034-122">**Float**</span></span> <br/> |<span data-ttu-id="8d034-123">Der Anteil, in dem _color2_ und _color1_.</span><span class="sxs-lookup"><span data-stu-id="8d034-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="8d034-124">Eine reelle Zahl zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="8d034-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8d034-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d034-125">Return value</span></span>

 <span data-ttu-id="8d034-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="8d034-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d034-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d034-127">Remarks</span></span>

<span data-ttu-id="8d034-128">Die zurückgegebene Farbe wird durch die relativen Proportionen bestimmt, in denen _color2_ und _color1_, wie durch den _float_ -Parameter angegeben, gemischt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d034-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="8d034-129">Wenn _float_ beispielsweise 0,25 ist, besteht die zurückgegebene farbe aus 75% aus _color1_ und 25% aus _color2_.</span><span class="sxs-lookup"><span data-stu-id="8d034-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="8d034-130">Eine andere Möglichkeit, darüber nachzudenken, ist, dass der _float_ -Wert dem Punkt entlang des Farbspektrums von _color1_ zu _color2_entspricht.</span><span class="sxs-lookup"><span data-stu-id="8d034-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="8d034-131">Daher werden kleinere Zahlen (näher an null) für _float_ -Produkte näher an _color1_angeglichen, während größere Zahlen (näher bei 1) eine Verschmelzung näher an _color2_erzeugen.</span><span class="sxs-lookup"><span data-stu-id="8d034-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

