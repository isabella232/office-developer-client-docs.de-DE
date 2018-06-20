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
description: Gibt die X, y-Koordinaten eines Punkts im Koordinatensystem des übergeordneten Shapes zurück.
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797598"
---
# <a name="par-function"></a><span data-ttu-id="5bd2e-103">PAR Function</span><span class="sxs-lookup"><span data-stu-id="5bd2e-103">PAR Function</span></span>

<span data-ttu-id="5bd2e-104">Gibt die _X, y_ -Koordinaten eines Punkts im Koordinatensystem des übergeordneten Shapes zurück.</span><span class="sxs-lookup"><span data-stu-id="5bd2e-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5bd2e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bd2e-105">Syntax</span></span>

<span data-ttu-id="5bd2e-106">PAR (** *zeigen* **)</span><span class="sxs-lookup"><span data-stu-id="5bd2e-106">PAR(** *point* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5bd2e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bd2e-107">Parameters</span></span>

|<span data-ttu-id="5bd2e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-108">**Name**</span></span>|<span data-ttu-id="5bd2e-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-109">**Required/Optional**</span></span>|<span data-ttu-id="5bd2e-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-110">**Data Type**</span></span>|<span data-ttu-id="5bd2e-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5bd2e-112">_Zeigen Sie_</span><span class="sxs-lookup"><span data-stu-id="5bd2e-112">_point_</span></span> <br/> |<span data-ttu-id="5bd2e-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5bd2e-113">Required</span></span>  <br/> |<span data-ttu-id="5bd2e-114">**Anzahl**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="5bd2e-115">Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.</span><span class="sxs-lookup"><span data-stu-id="5bd2e-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bd2e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5bd2e-116">Remarks</span></span>

<span data-ttu-id="5bd2e-117">In Microsoft Visio ist ein Punkt einen single-Wert, der verkörpert ein Paar von *X* - und *y* -Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="5bd2e-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="5bd2e-118">Wenn das Shape in einer Gruppe ist, ist die übergeordnete Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5bd2e-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="5bd2e-119">Wenn das Shape nicht in einer Gruppe ist, ist die übergeordnete der Seite.</span><span class="sxs-lookup"><span data-stu-id="5bd2e-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5bd2e-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5bd2e-120">Example</span></span>

<span data-ttu-id="5bd2e-121">PAR(PNT(PinX,PinY))</span><span class="sxs-lookup"><span data-stu-id="5bd2e-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="5bd2e-p102">In diesem Ausdruck konvertiert PKT ein Koordinatenpaar im aktuellen Shape in einen Punkt. PAR konvertiert den Punkt anschließend in ein Koordinatenpaar in Relation zu unteren linken Ecke des Zeichenblatts oder der Gruppe, in dem/der das aktuelle Shape enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5bd2e-p102">In this expression, PNT converts a pair of coordinates in the current shape into a point. PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

