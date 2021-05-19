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
ms.openlocfilehash: 0fed51e264bfb21da25d4e91f20f4bc0803e46e8
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160258"
---
# <a name="angletopar-function"></a><span data-ttu-id="9fe8c-104">ANGLETOPAR Function</span><span class="sxs-lookup"><span data-stu-id="9fe8c-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="9fe8c-p102">Gibt einen transformierten Winkel im übergeordneten Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die übergeordneten Koordinaten eines Ziel-Shapes.
    
</span><span class="sxs-lookup"><span data-stu-id="9fe8c-p102">Returns a transformed angle in the destination shape's parent coordinate system. Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9fe8c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fe8c-107">Syntax</span></span>

<span data-ttu-id="9fe8c-108">ANGLETOPAR(***srcAngle***, ***srcRef***, ***dstRef*** )</span><span class="sxs-lookup"><span data-stu-id="9fe8c-108">ANGLETOPAR(***srcAngle***, ***srcRef***, ***dstRef*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9fe8c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fe8c-109">Parameters</span></span>

|<span data-ttu-id="9fe8c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="9fe8c-110">**Name**</span></span>|<span data-ttu-id="9fe8c-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="9fe8c-111">**Required/Optional**</span></span>|<span data-ttu-id="9fe8c-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9fe8c-112">**Data Type**</span></span>|<span data-ttu-id="9fe8c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fe8c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9fe8c-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="9fe8c-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="9fe8c-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9fe8c-115">Required</span></span>  <br/> |<span data-ttu-id="9fe8c-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="9fe8c-116">**Numeric**</span></span> <br/> |<span data-ttu-id="9fe8c-117">Ein Winkel im Quellkoordinatensystem.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="9fe8c-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="9fe8c-118">_srcRef_</span></span> <br/> |<span data-ttu-id="9fe8c-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9fe8c-119">Required</span></span>  <br/> |<span data-ttu-id="9fe8c-120">**String**</span><span class="sxs-lookup"><span data-stu-id="9fe8c-120">**String**</span></span> <br/> | <span data-ttu-id="9fe8c-121">Ein Bezug auf eine Zelle im Quellobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="9fe8c-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="9fe8c-122">_dstRef_</span></span> <br/> |<span data-ttu-id="9fe8c-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9fe8c-123">Required</span></span>  <br/> |<span data-ttu-id="9fe8c-124">**String**</span><span class="sxs-lookup"><span data-stu-id="9fe8c-124">**String**</span></span> <br/> |<span data-ttu-id="9fe8c-125">Ein Bezug auf eine Zelle im Zielobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fe8c-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fe8c-126">Remarks</span></span>

<span data-ttu-id="9fe8c-p103">Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="9fe8c-129">Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt sein.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="9fe8c-130">Wenn das Ziel ein Zeichenblatt ohne übergeordnetes Objekt ist, wird das Ergebnis in den lokalen Koordinaten des Zeichenblatts ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

