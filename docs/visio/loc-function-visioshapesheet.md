---
title: LOC-Funktion(VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Akzeptiert einen Punkt, der in den lokalen Koordinaten eines Shapes definiert ist, und gibt den entsprechenden Punkt in den lokalen Koordinaten der Form zurück, die der Formel zugeordnet ist.
ms.openlocfilehash: 4728e5f8301c6ef10ddb0c14b6c0868a7a48b2a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344429"
---
# <a name="loc-function-visioshapesheet"></a><span data-ttu-id="65a67-103">LOC-Funktion(VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="65a67-103">LOC Function (VisioShapeSheet)</span></span>

<span data-ttu-id="65a67-104">Akzeptiert einen Punkt, der in den lokalen Koordinaten eines Shapes definiert ist, und gibt den entsprechenden Punkt in den lokalen Koordinaten der Form zurück, die der Formel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="65a67-104">Takes a point defined in one shape's local coordinates and returns the equivalent point expressed in the local coordinates of the shape associated with the formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="65a67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65a67-105">Syntax</span></span>

<span data-ttu-id="65a67-106">LOC (\* \* *Point* \* \*)</span><span class="sxs-lookup"><span data-stu-id="65a67-106">LOC(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="65a67-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="65a67-107">Parameters</span></span>

|<span data-ttu-id="65a67-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="65a67-108">**Name**</span></span>|<span data-ttu-id="65a67-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="65a67-109">**Required/Optional**</span></span>|<span data-ttu-id="65a67-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="65a67-110">**Data Type**</span></span>|<span data-ttu-id="65a67-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65a67-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="65a67-112">_Punkt_</span><span class="sxs-lookup"><span data-stu-id="65a67-112">_point_</span></span> <br/> |<span data-ttu-id="65a67-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="65a67-113">Required</span></span>  <br/> |<span data-ttu-id="65a67-114">**String**</span><span class="sxs-lookup"><span data-stu-id="65a67-114">**String**</span></span> <br/> | <span data-ttu-id="65a67-115">Ein Punkt, der in den lokalen Koordinaten eines Shapes definiert ist.</span><span class="sxs-lookup"><span data-stu-id="65a67-115">A point defined in one shape's local coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="65a67-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65a67-116">Return value</span></span>

<span data-ttu-id="65a67-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65a67-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65a67-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65a67-118">Remarks</span></span>

<span data-ttu-id="65a67-p101">Lokale Koordinaten werden von der unteren linken Ecke des Auswahlrechtecks eines Shapes gemessen. Beide Shapes müssen sich auf demselben Zeichenblatt befinden.</span><span class="sxs-lookup"><span data-stu-id="65a67-p101">Local coordinates are measured from the lower-left corner of the shape's selection rectangle. Both shapes must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="65a67-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="65a67-121">Example</span></span>

<span data-ttu-id="65a67-122">LOC (PNT (Blatt. 5! Zelle LocPinX, Sheet. 5! Zelle LocPinY))</span><span class="sxs-lookup"><span data-stu-id="65a67-122">LOC(PNT(Sheet.5!LocPinX, Sheet.5!LocPinY))</span></span> 
  
<span data-ttu-id="65a67-p102">In diesem Ausdruck konvertiert PKT ein Paar lokaler Koordinaten in Sheet.5 in einen Punkt. (Bei Sheet.5 handelt es sich um ein weiteres Shape auf demselben Zeichenblatt.) LOC konvertiert diesen Punkt dann in einen äquivalenten Punkt in dem lokalen Koordinatensystem des aktuellen Shapes - relativ zur unteren linken Ecke des Auswahlrechtecks des aktuellen Shapes.</span><span class="sxs-lookup"><span data-stu-id="65a67-p102">In this expression, PNT converts a set of local coordinates in Sheet.5 to a point. (Sheet.5 is another shape on the same drawing page.) LOC then converts that point to an equivalent point in the current shape's local coordinate system, relative to the lower-left corner of the selection rectangle of the current shape.</span></span> 
  
<span data-ttu-id="65a67-125">Die 5 in Sheet.5 ist die ID für das Shape, das im Dialogfeld **Shape-Name** (Registerkarte **Entwickler**) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="65a67-125">The 5 in Sheet.5 is the ID number for the shape, which is displayed in the **Shape Name** dialog box (**Developer** tab).</span></span> 
  

