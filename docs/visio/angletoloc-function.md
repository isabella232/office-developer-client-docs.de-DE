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
ms.openlocfilehash: e971613d4fc33cd991e7e9aeba49ac47871ebe8f
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160265"
---
# <a name="angletoloc-function"></a><span data-ttu-id="8d3a0-104">ANGLETOLOC Function</span><span class="sxs-lookup"><span data-stu-id="8d3a0-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="8d3a0-105">Gibt einen transformierten Winkel im lokalen Koordinatensystem des Ziel-Shapes zurück.</span><span class="sxs-lookup"><span data-stu-id="8d3a0-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="8d3a0-106">Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die lokalen Koordinaten eines Ziel-Shapes.</span><span class="sxs-lookup"><span data-stu-id="8d3a0-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d3a0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d3a0-107">Syntax</span></span>

<span data-ttu-id="8d3a0-108">ANGLETOLOC (***srcAngle***, ***srcRef***, ***Zielbezug*** )</span><span class="sxs-lookup"><span data-stu-id="8d3a0-108">ANGLETOLOC(***srcAngle***, ***srcRef***, ***dstRef*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d3a0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d3a0-109">Parameters</span></span>

|<span data-ttu-id="8d3a0-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8d3a0-110">**Name**</span></span>|<span data-ttu-id="8d3a0-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8d3a0-111">**Required/Optional**</span></span>|<span data-ttu-id="8d3a0-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8d3a0-112">**Data Type**</span></span>|<span data-ttu-id="8d3a0-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d3a0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d3a0-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="8d3a0-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="8d3a0-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d3a0-115">Required</span></span>  <br/> |<span data-ttu-id="8d3a0-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="8d3a0-116">**Numeric**</span></span> <br/> |<span data-ttu-id="8d3a0-117">Ein Winkel im Quellkoordinatensystem.</span><span class="sxs-lookup"><span data-stu-id="8d3a0-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="8d3a0-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="8d3a0-118">_srcRef_</span></span> <br/> |<span data-ttu-id="8d3a0-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d3a0-119">Required</span></span>  <br/> |<span data-ttu-id="8d3a0-120">**String**</span><span class="sxs-lookup"><span data-stu-id="8d3a0-120">**String**</span></span> <br/> | <span data-ttu-id="8d3a0-121">Ein Bezug auf eine Zelle im Quellobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.</span><span class="sxs-lookup"><span data-stu-id="8d3a0-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="8d3a0-122">_Zielbezug_</span><span class="sxs-lookup"><span data-stu-id="8d3a0-122">_dstRef_</span></span> <br/> |<span data-ttu-id="8d3a0-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d3a0-123">Required</span></span>  <br/> |<span data-ttu-id="8d3a0-124">**String**</span><span class="sxs-lookup"><span data-stu-id="8d3a0-124">**String**</span></span> <br/> |<span data-ttu-id="8d3a0-125">Ein Bezug auf eine Zelle im Zielobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.</span><span class="sxs-lookup"><span data-stu-id="8d3a0-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d3a0-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d3a0-126">Remarks</span></span>

<span data-ttu-id="8d3a0-127">Mithilfe der ANGLETOLOC-Funktion können Sie lokale Winkelzellen in einem Shape in Form eines Winkels aus einer anderen Koordinatenstelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="8d3a0-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="8d3a0-p103">Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.</span><span class="sxs-lookup"><span data-stu-id="8d3a0-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="8d3a0-130">Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt liegen.</span><span class="sxs-lookup"><span data-stu-id="8d3a0-130">The source and destination coordinates must be on the same page.</span></span>
  

