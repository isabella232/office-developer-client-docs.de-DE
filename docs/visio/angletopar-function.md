---
title: ANGLETOPAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Gibt einen transformierten Winkel im übergeordneten Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die übergeordneten Koordinaten eines Ziel-Shapes.
ms.openlocfilehash: e411cbae21d832039e2fbda93393a8fe0bd1f9f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404323"
---
# <a name="angletopar-function"></a><span data-ttu-id="14067-104">ANGLETOPAR Function</span><span class="sxs-lookup"><span data-stu-id="14067-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="14067-105">Gibt einen transformierten Winkel im übergeordneten Koordinatensystem des Ziel-Shapes zurück.</span><span class="sxs-lookup"><span data-stu-id="14067-105">Returns a transformed angle in the destination shape's parent coordinate system.</span></span> <span data-ttu-id="14067-106">Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die übergeordneten Koordinaten eines Ziel-Shapes.</span><span class="sxs-lookup"><span data-stu-id="14067-106">Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="14067-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="14067-107">Syntax</span></span>

<span data-ttu-id="14067-108">ANGLETOPAR (\* \* *srcAngle* \* \*, \* \* *srcRef* \* \*, \* \* *Zielbezug* \* \*)</span><span class="sxs-lookup"><span data-stu-id="14067-108">ANGLETOPAR(\*\* *srcAngle* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="14067-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="14067-109">Parameters</span></span>

|<span data-ttu-id="14067-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="14067-110">**Name**</span></span>|<span data-ttu-id="14067-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="14067-111">**Required/Optional**</span></span>|<span data-ttu-id="14067-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="14067-112">**Data Type**</span></span>|<span data-ttu-id="14067-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="14067-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="14067-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="14067-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="14067-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="14067-115">Required</span></span>  <br/> |<span data-ttu-id="14067-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="14067-116">**Numeric**</span></span> <br/> |<span data-ttu-id="14067-117">Ein Winkel im Quellkoordinatensystem.</span><span class="sxs-lookup"><span data-stu-id="14067-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="14067-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="14067-118">_srcRef_</span></span> <br/> |<span data-ttu-id="14067-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="14067-119">Required</span></span>  <br/> |<span data-ttu-id="14067-120">**String**</span><span class="sxs-lookup"><span data-stu-id="14067-120">**String**</span></span> <br/> | <span data-ttu-id="14067-121">Ein Bezug auf eine Zelle im Quellobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.</span><span class="sxs-lookup"><span data-stu-id="14067-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="14067-122">_Zielbezug_</span><span class="sxs-lookup"><span data-stu-id="14067-122">_dstRef_</span></span> <br/> |<span data-ttu-id="14067-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="14067-123">Required</span></span>  <br/> |<span data-ttu-id="14067-124">**String**</span><span class="sxs-lookup"><span data-stu-id="14067-124">**String**</span></span> <br/> |<span data-ttu-id="14067-125">Ein Bezug auf eine Zelle im Zielobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.</span><span class="sxs-lookup"><span data-stu-id="14067-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14067-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14067-126">Remarks</span></span>

<span data-ttu-id="14067-p103">Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.</span><span class="sxs-lookup"><span data-stu-id="14067-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="14067-129">Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt sein.</span><span class="sxs-lookup"><span data-stu-id="14067-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="14067-130">Wenn das Ziel ein Zeichenblatt ohne übergeordnetes Objekt ist, wird das Ergebnis in den lokalen Koordinaten des Zeichenblatts ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="14067-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

