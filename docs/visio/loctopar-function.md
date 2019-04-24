---
title: LOCTOPAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Gibt einen transformierten Punkt in übergeordneten Koordinaten im Zielkoordinatensystem zurück.
ms.openlocfilehash: 65a08837d7d026836ebc8d5e35938ea049d005e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314847"
---
# <a name="loctopar-function"></a><span data-ttu-id="c0749-103">LOCTOPAR Function</span><span class="sxs-lookup"><span data-stu-id="c0749-103">LOCTOPAR Function</span></span>

<span data-ttu-id="c0749-104">Gibt einen transformierten Punkt in übergeordneten Koordinaten im Zielkoordinatensystem zurück.</span><span class="sxs-lookup"><span data-stu-id="c0749-104">Returns a transformed point in parent coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c0749-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0749-105">Syntax</span></span>

<span data-ttu-id="c0749-106">LOCTOPAR (\* \* *srcPoint* \* \*, \* \* *srcRef* \* \*, \* \* *Zielbezug* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c0749-106">LOCTOPAR(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c0749-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0749-107">Parameters</span></span>

|<span data-ttu-id="c0749-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c0749-108">**Name**</span></span>|<span data-ttu-id="c0749-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c0749-109">**Required/Optional**</span></span>|<span data-ttu-id="c0749-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c0749-110">**Data Type**</span></span>|<span data-ttu-id="c0749-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0749-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c0749-112">_srcPoint_</span><span class="sxs-lookup"><span data-stu-id="c0749-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="c0749-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c0749-113">Required</span></span>  <br/> |<span data-ttu-id="c0749-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c0749-114">**String**</span></span> <br/> | <span data-ttu-id="c0749-115">Ein Punkt in den lokalen Koordinaten des Quellkoordinatensystems.</span><span class="sxs-lookup"><span data-stu-id="c0749-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="c0749-116">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="c0749-116">_srcRef_</span></span> <br/> |<span data-ttu-id="c0749-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c0749-117">Required</span></span>  <br/> |<span data-ttu-id="c0749-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c0749-118">**String**</span></span> <br/> | <span data-ttu-id="c0749-119">Ein Bezug auf eine Zelle im Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="c0749-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="c0749-120">_Zielbezug_</span><span class="sxs-lookup"><span data-stu-id="c0749-120">_dstRef_</span></span> <br/> |<span data-ttu-id="c0749-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c0749-121">Required</span></span>  <br/> |<span data-ttu-id="c0749-122">**String**</span><span class="sxs-lookup"><span data-stu-id="c0749-122">**String**</span></span> <br/> | <span data-ttu-id="c0749-123">Ein Bezug auf eine Zelle im Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="c0749-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c0749-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0749-124">Return value</span></span>

<span data-ttu-id="c0749-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c0749-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0749-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0749-126">Remarks</span></span>

<span data-ttu-id="c0749-p101">Die Funktion konvertiert einen Punkt aus lokalen Koordinaten in einem Quell-Shape in die übergeordneten Koordinaten eines Ziel-Shapes. Sie können die Funktion LOCTOPAR verwenden, um übergeordnete Koordinaten in Zellen eines Shapes, wie z.B. PinX, PinY, BeginX und BeginY festzulegen und dabei einen anderen Punkt von einem anderen Koordinatensystem zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0749-p101">Converts a point from local coordinates in a source shape to parent coordinates in a destination shape. You can use the LOCTOPAR function to set parent coordinates in cells, such as PinX, PinY, BeginX, and BeginY in a shape using another point from another coordinate system.</span></span> 
  
<span data-ttu-id="c0749-p102">Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.</span><span class="sxs-lookup"><span data-stu-id="c0749-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span> 
  
<span data-ttu-id="c0749-131">Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt liegen.</span><span class="sxs-lookup"><span data-stu-id="c0749-131">The source and destination coordinates must be on the same page.</span></span> 
  
<span data-ttu-id="c0749-132">Wenn das Ziel ein Zeichenblatt ohne übergeordnetes Objekt ist, wird das Ergebnis in den lokalen Koordinaten des Zeichenblatts ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c0749-132">If the destination is a page, which has no parent, the result is expressed in the page's local coordinates.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c0749-133">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c0749-133">Example</span></span>

<span data-ttu-id="c0749-134">LOCTOPAR(PKT(LokDrehbezX, LokDrehbezY), Breite, Sheet.4!Breite)</span><span class="sxs-lookup"><span data-stu-id="c0749-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width)</span></span> 
  
<span data-ttu-id="c0749-135">Konvertiert den lokalen Drehpunkt des Shapes, die mit der Formel verknüpft ist, in die übergeordneten Koordinaten von Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="c0749-135">Converts the local pin of the shape associated with the formula to parent coordinates of Sheet.4.</span></span> 
  

