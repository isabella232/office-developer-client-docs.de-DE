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
description: Normalisiert den Range eines Winkels.
ms.openlocfilehash: 017dd89bd3b814c10422cd32eea1ee7e343eaf50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341489"
---
# <a name="ang360-function"></a><span data-ttu-id="053b7-103">ANG360 Function</span><span class="sxs-lookup"><span data-stu-id="053b7-103">ANG360 Function</span></span>

<span data-ttu-id="053b7-104">Normalisiert den \<Range eines Winkels auf 0 = Ergebnis \< 2pi Bogenmaß (0 \<= Ergebnis \< 360 Grad).</span><span class="sxs-lookup"><span data-stu-id="053b7-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="053b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="053b7-105">Syntax</span></span>

<span data-ttu-id="053b7-106">ANG360 (\* \* *Winkel* \* \*)</span><span class="sxs-lookup"><span data-stu-id="053b7-106">ANG360(\*\* *angle* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="053b7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="053b7-107">Parameters</span></span>

|<span data-ttu-id="053b7-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="053b7-108">**Name**</span></span>|<span data-ttu-id="053b7-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="053b7-109">**Required/Optional**</span></span>|<span data-ttu-id="053b7-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="053b7-110">**Data Type**</span></span>|<span data-ttu-id="053b7-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="053b7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="053b7-112">_Winkel_</span><span class="sxs-lookup"><span data-stu-id="053b7-112">_angle_</span></span> <br/> |<span data-ttu-id="053b7-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="053b7-113">Required</span></span>  <br/> |<span data-ttu-id="053b7-114">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="053b7-114">**Numeric**</span></span> <br/> |<span data-ttu-id="053b7-115">Der zu normalisierende Winkel.</span><span class="sxs-lookup"><span data-stu-id="053b7-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="053b7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="053b7-116">Remarks</span></span>

<span data-ttu-id="053b7-117">Wenn *Angle* nicht mithilfe von Winkeleinheiten angegeben wird, wird er als Bogenmaß interpretiert.</span><span class="sxs-lookup"><span data-stu-id="053b7-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="053b7-118">Wenn *Angle* nicht in einen Wert konvertiert werden kann, wird ein #VALUE!</span><span class="sxs-lookup"><span data-stu-id="053b7-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="053b7-119">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="053b7-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="053b7-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="053b7-120">Example 1</span></span>

<span data-ttu-id="053b7-121">ANG360(395 deg)</span><span class="sxs-lookup"><span data-stu-id="053b7-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="053b7-122">Gibt 35 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="053b7-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="053b7-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="053b7-123">Example 2</span></span>

<span data-ttu-id="053b7-124">ANG360(-9,8 rad.)</span><span class="sxs-lookup"><span data-stu-id="053b7-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="053b7-125">Gibt 2,7664 Rad zurück.</span><span class="sxs-lookup"><span data-stu-id="053b7-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="053b7-126">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="053b7-126">Example 3</span></span>

<span data-ttu-id="053b7-127">ANG360 (45)</span><span class="sxs-lookup"><span data-stu-id="053b7-127">ANG360(45)</span></span>
  
<span data-ttu-id="053b7-128">Gibt 58,31 deg (1,0177 Rad) zurück.</span><span class="sxs-lookup"><span data-stu-id="053b7-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

