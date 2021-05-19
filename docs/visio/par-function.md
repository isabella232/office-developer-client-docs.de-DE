---
title: PAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Gibt die XY-Koordinaten eines Punkts im Koordinatensystem des übergeordneten Shapes zurück.
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414508"
---
# <a name="par-function"></a><span data-ttu-id="a0c8a-103">PAR Function</span><span class="sxs-lookup"><span data-stu-id="a0c8a-103">PAR Function</span></span>

<span data-ttu-id="a0c8a-104">Gibt die  _XY-Koordinaten_ eines Punkts im Koordinatensystem des übergeordneten Shapes zurück.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a0c8a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0c8a-105">Syntax</span></span>

<span data-ttu-id="a0c8a-106">PAR(\*\* *point* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a0c8a-106">PAR(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a0c8a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0c8a-107">Parameters</span></span>

|<span data-ttu-id="a0c8a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-108">**Name**</span></span>|<span data-ttu-id="a0c8a-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-109">**Required/Optional**</span></span>|<span data-ttu-id="a0c8a-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-110">**Data Type**</span></span>|<span data-ttu-id="a0c8a-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a0c8a-112">_point_</span><span class="sxs-lookup"><span data-stu-id="a0c8a-112">_point_</span></span> <br/> |<span data-ttu-id="a0c8a-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a0c8a-113">Required</span></span>  <br/> |<span data-ttu-id="a0c8a-114">**Number, Number**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="a0c8a-115">Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0c8a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a0c8a-116">Remarks</span></span>

<span data-ttu-id="a0c8a-117">In Microsoft Visio ist ein Punkt ein einzelner Wert, der ein Paar *x-* und *y-Koordinaten* verkörpert.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="a0c8a-118">Wenn sich das Shape in einer Gruppe befindet, ist das übergeordnete Element die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="a0c8a-119">Befindet sich das Shape nicht in einer Gruppe, ist das übergeordnete Element das Zeichenblatt.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a0c8a-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a0c8a-120">Example</span></span>

<span data-ttu-id="a0c8a-121">PAR(PNT(PinX,PinY))</span><span class="sxs-lookup"><span data-stu-id="a0c8a-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="a0c8a-p102">In diesem Ausdruck konvertiert PKT ein Koordinatenpaar im aktuellen Shape in einen Punkt. PAR konvertiert den Punkt anschließend in ein Koordinatenpaar in Relation zu unteren linken Ecke des Zeichenblatts oder der Gruppe, in dem/der das aktuelle Shape enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-p102">In this expression, PNT converts a pair of coordinates in the current shape into a point. PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

