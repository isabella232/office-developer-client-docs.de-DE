---
title: ANGLETOLOC-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
localization_priority: Normal
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Gibt einen transformierten Winkel im lokalen Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die lokalen Koordinaten eines Ziel-Shapes.
ms.openlocfilehash: 804faeb24932e414ad03bc9e8487c62ca08bd7d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341475"
---
# <a name="angletoloc-function"></a><span data-ttu-id="039cf-104">ANGLETOLOC Function</span><span class="sxs-lookup"><span data-stu-id="039cf-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="039cf-105">Gibt einen transformierten Winkel im lokalen Koordinatensystem des Ziel-Shapes zurück.</span><span class="sxs-lookup"><span data-stu-id="039cf-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="039cf-106">Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die lokalen Koordinaten eines Ziel-Shapes.</span><span class="sxs-lookup"><span data-stu-id="039cf-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="039cf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="039cf-107">Syntax</span></span>

<span data-ttu-id="039cf-108">ANGLETOLOC (\* \* *srcAngle* \* \*, \* \* *srcRef* \* \*, \* \* *Zielbezug* \* \*)</span><span class="sxs-lookup"><span data-stu-id="039cf-108">ANGLETOLOC(\*\* *srcAngle* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="039cf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="039cf-109">Parameters</span></span>

|<span data-ttu-id="039cf-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="039cf-110">**Name**</span></span>|<span data-ttu-id="039cf-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="039cf-111">**Required/Optional**</span></span>|<span data-ttu-id="039cf-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="039cf-112">**Data Type**</span></span>|<span data-ttu-id="039cf-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="039cf-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="039cf-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="039cf-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="039cf-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="039cf-115">Required</span></span>  <br/> |<span data-ttu-id="039cf-116">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="039cf-116">**Numeric**</span></span> <br/> |<span data-ttu-id="039cf-117">Ein Winkel im Quellkoordinatensystem.</span><span class="sxs-lookup"><span data-stu-id="039cf-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="039cf-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="039cf-118">_srcRef_</span></span> <br/> |<span data-ttu-id="039cf-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="039cf-119">Required</span></span>  <br/> |<span data-ttu-id="039cf-120">**String**</span><span class="sxs-lookup"><span data-stu-id="039cf-120">**String**</span></span> <br/> | <span data-ttu-id="039cf-121">Ein Bezug auf eine Zelle im Quellobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.</span><span class="sxs-lookup"><span data-stu-id="039cf-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="039cf-122">_Zielbezug_</span><span class="sxs-lookup"><span data-stu-id="039cf-122">_dstRef_</span></span> <br/> |<span data-ttu-id="039cf-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="039cf-123">Required</span></span>  <br/> |<span data-ttu-id="039cf-124">**String**</span><span class="sxs-lookup"><span data-stu-id="039cf-124">**String**</span></span> <br/> |<span data-ttu-id="039cf-125">Ein Bezug auf eine Zelle im Zielobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.</span><span class="sxs-lookup"><span data-stu-id="039cf-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="039cf-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="039cf-126">Remarks</span></span>

<span data-ttu-id="039cf-127">Mithilfe der ANGLETOLOC-Funktion können Sie lokale Winkelzellen in einem Shape in Form eines Winkels aus einer anderen Koordinatenstelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="039cf-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="039cf-p103">Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.</span><span class="sxs-lookup"><span data-stu-id="039cf-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="039cf-130">Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt liegen.</span><span class="sxs-lookup"><span data-stu-id="039cf-130">The source and destination coordinates must be on the same page.</span></span>
  

