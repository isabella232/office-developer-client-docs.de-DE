---
title: TINT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Ändert die Farbe, indem deren Helligkeit um den Wert (positiven oder negativen) im Int-Parameter angegeben.
ms.openlocfilehash: a4b15596a4742edb4f9e4746929f19d2eafe94d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798288"
---
# <a name="tint-function"></a><span data-ttu-id="b6aef-103">TINT-Funktion</span><span class="sxs-lookup"><span data-stu-id="b6aef-103">TINT Function</span></span>

<span data-ttu-id="b6aef-104">Ändert die Farbe, indem deren Helligkeit um den Wert (positiven oder negativen) im _Int_ -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="b6aef-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b6aef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6aef-105">Syntax</span></span>

<span data-ttu-id="b6aef-106">FARBTON (** *Farbe* **, ** *Int* **)</span><span class="sxs-lookup"><span data-stu-id="b6aef-106">TINT(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b6aef-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6aef-107">Parameters</span></span>

|<span data-ttu-id="b6aef-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b6aef-108">**Name**</span></span>|<span data-ttu-id="b6aef-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="b6aef-109">**Required/Optional**</span></span>|<span data-ttu-id="b6aef-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="b6aef-110">**Data Type**</span></span>|<span data-ttu-id="b6aef-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6aef-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b6aef-112">_Farbe_</span><span class="sxs-lookup"><span data-stu-id="b6aef-112">_color_</span></span> <br/> |<span data-ttu-id="b6aef-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b6aef-113">Required</span></span>  <br/> |<span data-ttu-id="b6aef-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="b6aef-114">**Numeric**</span></span> <br/> |<span data-ttu-id="b6aef-115">Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.</span><span class="sxs-lookup"><span data-stu-id="b6aef-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="b6aef-116">_int_</span><span class="sxs-lookup"><span data-stu-id="b6aef-116">_int_</span></span> <br/> |<span data-ttu-id="b6aef-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b6aef-117">Required</span></span>  <br/> |<span data-ttu-id="b6aef-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="b6aef-118">**Integer**</span></span> <br/> |<span data-ttu-id="b6aef-p101">Der Wert, um den die Leuchtdichte der Farbe erhöht werden soll. Kann positiv oder negativ sein.
</span><span class="sxs-lookup"><span data-stu-id="b6aef-p101">The amount by which to increase the luminosity of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b6aef-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6aef-121">Return value</span></span>

 <span data-ttu-id="b6aef-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="b6aef-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6aef-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6aef-123">Remarks</span></span>

<span data-ttu-id="b6aef-124">Die unteren und oberen Grenzwerte der Helligkeit sind 0 und 240.</span><span class="sxs-lookup"><span data-stu-id="b6aef-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="b6aef-125">Es gibt keine Beschränkung der Größe von die ganze Zahl, die Sie für den Parameter _Int_ weitergeben können, aber Helligkeit überschreitet nie diese Grenzwerte.</span><span class="sxs-lookup"><span data-stu-id="b6aef-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

