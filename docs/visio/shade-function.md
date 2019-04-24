---
title: SHADE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Ändert die Farbe, indem die Helligkeit um die im Parameter int angegebene Menge (positiv oder negativ) verringert wird.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326597"
---
# <a name="shade-function"></a><span data-ttu-id="5214a-103">SHADE Function</span><span class="sxs-lookup"><span data-stu-id="5214a-103">SHADE Function</span></span>

<span data-ttu-id="5214a-104">Ändert die Farbe, indem die Helligkeit um die im Parameter _int_ angegebene Menge (positiv oder negativ) verringert wird.</span><span class="sxs-lookup"><span data-stu-id="5214a-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5214a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5214a-105">Syntax</span></span>

<span data-ttu-id="5214a-106">SCHATTIERUNG (\* \* *Color* \* \*, \* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5214a-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5214a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5214a-107">Parameters</span></span>

|<span data-ttu-id="5214a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5214a-108">**Name**</span></span>|<span data-ttu-id="5214a-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5214a-109">**Required/Optional**</span></span>|<span data-ttu-id="5214a-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5214a-110">**Data Type**</span></span>|<span data-ttu-id="5214a-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5214a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5214a-112">_color_</span><span class="sxs-lookup"><span data-stu-id="5214a-112">_color_</span></span> <br/> |<span data-ttu-id="5214a-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5214a-113">Required</span></span>  <br/> |<span data-ttu-id="5214a-114">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="5214a-114">**Numeric**</span></span> <br/> |<span data-ttu-id="5214a-115">Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.</span><span class="sxs-lookup"><span data-stu-id="5214a-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="5214a-116">_int_</span><span class="sxs-lookup"><span data-stu-id="5214a-116">_int_</span></span> <br/> |<span data-ttu-id="5214a-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5214a-117">Required</span></span>  <br/> |<span data-ttu-id="5214a-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="5214a-118">**Integer**</span></span> <br/> |<span data-ttu-id="5214a-119">Der Wert, um den die Leuchtdichte der Farbe verringert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5214a-119">The amount by which to decrease the luminosity of the color.</span></span> <span data-ttu-id="5214a-120">Kann positiv oder negativ sein.</span><span class="sxs-lookup"><span data-stu-id="5214a-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5214a-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5214a-121">Return value</span></span>

 <span data-ttu-id="5214a-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="5214a-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5214a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5214a-123">Remarks</span></span>

<span data-ttu-id="5214a-124">Die unteren und oberen Grenzwerte der Leuchtdichte liegen jeweils bei 0 und 240.</span><span class="sxs-lookup"><span data-stu-id="5214a-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="5214a-125">Es gibt keine Begrenzung für die Größe der Ganzzahl, die Sie für den _int_ -Parameter übergeben können, aber die Luminanz überschreitet diese Grenzwerte nie.</span><span class="sxs-lookup"><span data-stu-id="5214a-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![Ober-und Untergrenze der Helligkeit](media/image199_ZA10173627.gif)
  

