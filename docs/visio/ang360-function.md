---
title: ANG360-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Ein Winkel normalisiert.
ms.openlocfilehash: 01092e06b55c73953417fe7d0fa1c9f74d668922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796390"
---
# <a name="ang360-function"></a><span data-ttu-id="956e8-103">ANG360 Function</span><span class="sxs-lookup"><span data-stu-id="956e8-103">ANG360 Function</span></span>

<span data-ttu-id="956e8-104">Normalisiert eines Winkels 0 \<Ergebnis = \< 2PI Bogenmaß (0 \<Ergebnis = \< 360-Grad).</span><span class="sxs-lookup"><span data-stu-id="956e8-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="956e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="956e8-105">Syntax</span></span>

<span data-ttu-id="956e8-106">ANG360 (** *Winkel* **)</span><span class="sxs-lookup"><span data-stu-id="956e8-106">ANG360(** *angle* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="956e8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="956e8-107">Parameters</span></span>

|<span data-ttu-id="956e8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="956e8-108">**Name**</span></span>|<span data-ttu-id="956e8-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="956e8-109">**Required/Optional**</span></span>|<span data-ttu-id="956e8-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="956e8-110">**Data Type**</span></span>|<span data-ttu-id="956e8-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="956e8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="956e8-112">_Winkel_</span><span class="sxs-lookup"><span data-stu-id="956e8-112">_angle_</span></span> <br/> |<span data-ttu-id="956e8-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="956e8-113">Required</span></span>  <br/> |<span data-ttu-id="956e8-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="956e8-114">**Numeric**</span></span> <br/> |<span data-ttu-id="956e8-115">Der zu normalisierende Winkel.</span><span class="sxs-lookup"><span data-stu-id="956e8-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="956e8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="956e8-116">Remarks</span></span>

<span data-ttu-id="956e8-117">Wenn *Winkel* mithilfe von Winkel Einheiten nicht angegeben ist, wird er als Bogenmaß (Radiant) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="956e8-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="956e8-118">Wenn *Winkel* auf einen Wert, der ein #VALUE konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="956e8-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="956e8-119">Fehler wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="956e8-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="956e8-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="956e8-120">Example 1</span></span>

<span data-ttu-id="956e8-121">ANG360(395 deg)</span><span class="sxs-lookup"><span data-stu-id="956e8-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="956e8-122">Gibt 35 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="956e8-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="956e8-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="956e8-123">Example 2</span></span>

<span data-ttu-id="956e8-124">ANG360(-9,8 rad.)</span><span class="sxs-lookup"><span data-stu-id="956e8-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="956e8-125">Gibt 2,7664 Rad zurück.</span><span class="sxs-lookup"><span data-stu-id="956e8-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="956e8-126">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="956e8-126">Example 3</span></span>

<span data-ttu-id="956e8-127">ANG360(45)</span><span class="sxs-lookup"><span data-stu-id="956e8-127">ANG360(45)</span></span>
  
<span data-ttu-id="956e8-128">Gibt 58,31 deg (1,0177 Rad) zurück.</span><span class="sxs-lookup"><span data-stu-id="956e8-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

