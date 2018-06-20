---
title: SHADE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Ändert die Farbe durch Verringern der Helligkeit um den Betrag (positiven oder negativen) im Int-Parameter angegebene.
ms.openlocfilehash: 4a02aa41050c3cf36b567c238670b5f61074bd7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798002"
---
# <a name="shade-function"></a><span data-ttu-id="995f4-103">SHADE Function</span><span class="sxs-lookup"><span data-stu-id="995f4-103">SHADE Function</span></span>

<span data-ttu-id="995f4-104">Ändert die Farbe durch Verringern der Helligkeit um den Betrag (positiven oder negativen) im _Int_ -Parameter angegebene.</span><span class="sxs-lookup"><span data-stu-id="995f4-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="995f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="995f4-105">Syntax</span></span>

<span data-ttu-id="995f4-106">SCHATTEN (** *Farbe* **, ** *Int* **)</span><span class="sxs-lookup"><span data-stu-id="995f4-106">SHADE(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="995f4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="995f4-107">Parameters</span></span>

|<span data-ttu-id="995f4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="995f4-108">**Name**</span></span>|<span data-ttu-id="995f4-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="995f4-109">**Required/Optional**</span></span>|<span data-ttu-id="995f4-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="995f4-110">**Data Type**</span></span>|<span data-ttu-id="995f4-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="995f4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="995f4-112">_Farbe_</span><span class="sxs-lookup"><span data-stu-id="995f4-112">_color_</span></span> <br/> |<span data-ttu-id="995f4-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="995f4-113">Required</span></span>  <br/> |<span data-ttu-id="995f4-114">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="995f4-114">**Numeric**</span></span> <br/> |<span data-ttu-id="995f4-115">Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.</span><span class="sxs-lookup"><span data-stu-id="995f4-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="995f4-116">_int_</span><span class="sxs-lookup"><span data-stu-id="995f4-116">_int_</span></span> <br/> |<span data-ttu-id="995f4-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="995f4-117">Required</span></span>  <br/> |<span data-ttu-id="995f4-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="995f4-118">**Integer**</span></span> <br/> |<span data-ttu-id="995f4-p101">Der Wert, um den die Leuchtdichte der Farbe verringert werden soll. Kann positiv oder negativ sein.</span><span class="sxs-lookup"><span data-stu-id="995f4-p101">The amount by which to decrease the luminosity of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="995f4-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="995f4-121">Return value</span></span>

 <span data-ttu-id="995f4-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="995f4-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="995f4-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="995f4-123">Remarks</span></span>

<span data-ttu-id="995f4-124">Die unteren und oberen Grenzwerte der Helligkeit sind 0 und 240.</span><span class="sxs-lookup"><span data-stu-id="995f4-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="995f4-125">Es gibt keine Beschränkung der Größe von die ganze Zahl, die Sie für den Parameter _Int_ weitergeben können, aber Helligkeit überschreitet nie diese Grenzwerte.</span><span class="sxs-lookup"><span data-stu-id="995f4-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![](media/image199_ZA10173627.gif)
  

