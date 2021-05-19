---
title: POLYLINE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Gibt eine Polylinie zurück. Diese Funktion wird in der Zelle A der PolyLineTo-Geometriezeilen verwendet.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426296"
---
# <a name="polyline-function"></a><span data-ttu-id="034b2-104">POLYLINE Function</span><span class="sxs-lookup"><span data-stu-id="034b2-104">POLYLINE Function</span></span>

<span data-ttu-id="034b2-105">Gibt eine Polylinie zurück.</span><span class="sxs-lookup"><span data-stu-id="034b2-105">Returns a polyline.</span></span> <span data-ttu-id="034b2-106">Diese Funktion wird in der Zelle A der PolyLineTo-Geometriezeilen verwendet.</span><span class="sxs-lookup"><span data-stu-id="034b2-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="034b2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="034b2-107">Syntax</span></span>

<span data-ttu-id="034b2-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span><span class="sxs-lookup"><span data-stu-id="034b2-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="034b2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="034b2-109">Parameters</span></span>

|<span data-ttu-id="034b2-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="034b2-110">**Name**</span></span>|<span data-ttu-id="034b2-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="034b2-111">**Required/Optional**</span></span>|<span data-ttu-id="034b2-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="034b2-112">**Data Type**</span></span>|<span data-ttu-id="034b2-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="034b2-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="034b2-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="034b2-114">_xType_</span></span> <br/> |<span data-ttu-id="034b2-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="034b2-115">Required</span></span>  <br/> |<span data-ttu-id="034b2-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="034b2-116">**Boolean**</span></span> <br/> |<span data-ttu-id="034b2-117">Gibt an, wie die  _x-Eingabedaten_ interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="034b2-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="034b2-118">Wenn _xType_ 0 ist, werden die x-data-Eingaben als Prozentsatz der Breite interpretiert. </span><span class="sxs-lookup"><span data-stu-id="034b2-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="034b2-119">Wenn _xType_ 1 ist, werden die x-data-Eingaben als lokale Koordinate interpretiert. </span><span class="sxs-lookup"><span data-stu-id="034b2-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="034b2-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="034b2-120">_yType_</span></span> <br/> |<span data-ttu-id="034b2-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="034b2-121">Required</span></span>  <br/> |<span data-ttu-id="034b2-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="034b2-122">**Boolean**</span></span> <br/> |<span data-ttu-id="034b2-123">Gibt an, wie die  _y-Eingabedaten_ interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="034b2-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="034b2-124">Wenn  _yType_ 0 ist, werden die  _Eingabe-y-Daten_ als Prozentsatz von Height interpretiert.</span><span class="sxs-lookup"><span data-stu-id="034b2-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="034b2-125">Wenn  _yType_ 1 ist, werden die  _Eingaben y_-data als lokale Koordinate interpretiert.</span><span class="sxs-lookup"><span data-stu-id="034b2-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="034b2-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="034b2-126">_x1_</span></span> <br/> |<span data-ttu-id="034b2-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="034b2-127">Required</span></span>  <br/> |<span data-ttu-id="034b2-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="034b2-128">**Number**</span></span> <br/> | <span data-ttu-id="034b2-129">Eine x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="034b2-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="034b2-130">_y1_</span><span class="sxs-lookup"><span data-stu-id="034b2-130">_y1_</span></span> <br/> |<span data-ttu-id="034b2-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="034b2-131">Required</span></span>  <br/> |<span data-ttu-id="034b2-132">**Number**</span><span class="sxs-lookup"><span data-stu-id="034b2-132">**Number**</span></span> <br/> |<span data-ttu-id="034b2-133">Eine y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="034b2-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="034b2-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="034b2-134">Remarks</span></span>

<span data-ttu-id="034b2-135">Für jedes  *x-Argument*  muss ein  *y-Argument verwendet*  werden. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="034b2-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="034b2-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="034b2-136">Example</span></span>

<span data-ttu-id="034b2-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="034b2-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="034b2-138">Gibt ein Rechteck der Dimensionen Breite x Höhe zurück.</span><span class="sxs-lookup"><span data-stu-id="034b2-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

