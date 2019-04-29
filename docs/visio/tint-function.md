---
title: TINT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Ändert die Farbe, indem die Helligkeit um die im Parameter int angegebene Menge (positiv oder negativ) erhöht wird.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406577"
---
# <a name="tint-function"></a><span data-ttu-id="2f6f3-103">TINT-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f6f3-103">TINT Function</span></span>

<span data-ttu-id="2f6f3-104">Ändert die Farbe, indem die Helligkeit um die im Parameter _int_ angegebene Menge (positiv oder negativ) erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2f6f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f6f3-105">Syntax</span></span>

<span data-ttu-id="2f6f3-106">Farbton (\* \* *Farbe* \* \*, \* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="2f6f3-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2f6f3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f6f3-107">Parameters</span></span>

|<span data-ttu-id="2f6f3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2f6f3-108">**Name**</span></span>|<span data-ttu-id="2f6f3-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2f6f3-109">**Required/Optional**</span></span>|<span data-ttu-id="2f6f3-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2f6f3-110">**Data Type**</span></span>|<span data-ttu-id="2f6f3-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f6f3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2f6f3-112">_color_</span><span class="sxs-lookup"><span data-stu-id="2f6f3-112">_color_</span></span> <br/> |<span data-ttu-id="2f6f3-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2f6f3-113">Required</span></span>  <br/> |<span data-ttu-id="2f6f3-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="2f6f3-114">**Numeric**</span></span> <br/> |<span data-ttu-id="2f6f3-115">Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="2f6f3-116">_int_</span><span class="sxs-lookup"><span data-stu-id="2f6f3-116">_int_</span></span> <br/> |<span data-ttu-id="2f6f3-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2f6f3-117">Required</span></span>  <br/> |<span data-ttu-id="2f6f3-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="2f6f3-118">**Integer**</span></span> <br/> |<span data-ttu-id="2f6f3-119">Der Wert, um den die Leuchtdichte der Farbe erhöht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-119">The amount by which to increase the luminosity of the color.</span></span> <span data-ttu-id="2f6f3-120">Kann positiv oder negativ sein.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2f6f3-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f6f3-121">Return value</span></span>

 <span data-ttu-id="2f6f3-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="2f6f3-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f6f3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f6f3-123">Remarks</span></span>

<span data-ttu-id="2f6f3-124">Die unteren und oberen Grenzwerte der Leuchtdichte liegen jeweils bei 0 und 240.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="2f6f3-125">Es gibt keine Begrenzung für die Größe der Ganzzahl, die Sie für den _int_ -Parameter übergeben können, aber die Luminanz überschreitet diese Grenzwerte nie.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

