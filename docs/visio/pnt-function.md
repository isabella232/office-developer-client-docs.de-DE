---
title: PNT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Gibt den durch die Koordinaten x und y dargestellten Punkt als Single-Wert zurück.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322351"
---
# <a name="pnt-function"></a><span data-ttu-id="7a97f-103">PNT Function</span><span class="sxs-lookup"><span data-stu-id="7a97f-103">PNT Function</span></span>

<span data-ttu-id="7a97f-104">Gibt den durch die Koordinaten _x_ und _y_ dargestellten Punkt als Single-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7a97f-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7a97f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a97f-105">Syntax</span></span>

<span data-ttu-id="7a97f-106">PNT (\* \* *x, y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7a97f-106">PNT(\*\* *x,y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7a97f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a97f-107">Parameters</span></span>

|<span data-ttu-id="7a97f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7a97f-108">**Name**</span></span>|<span data-ttu-id="7a97f-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="7a97f-109">**Required/Optional**</span></span>|<span data-ttu-id="7a97f-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="7a97f-110">**Data Type**</span></span>|<span data-ttu-id="7a97f-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a97f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7a97f-112">_x, y_</span><span class="sxs-lookup"><span data-stu-id="7a97f-112">_x,y_</span></span> <br/> |<span data-ttu-id="7a97f-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7a97f-113">Required</span></span>  <br/> |<span data-ttu-id="7a97f-114">**Number, Number**</span><span class="sxs-lookup"><span data-stu-id="7a97f-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="7a97f-115">Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.</span><span class="sxs-lookup"><span data-stu-id="7a97f-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7a97f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a97f-116">Return value</span></span>

<span data-ttu-id="7a97f-117">Zeigen</span><span class="sxs-lookup"><span data-stu-id="7a97f-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7a97f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a97f-118">Remarks</span></span>

<span data-ttu-id="7a97f-119">Durch das Konvertieren von Koordinaten in Punkt können Sie die Geometrie eines Shapes ändern, ohne *x* -und *y* -Koordinaten separat bearbeiten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="7a97f-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7a97f-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7a97f-120">Example</span></span>

<span data-ttu-id="7a97f-121">PNT (PinX, PinY)</span><span class="sxs-lookup"><span data-stu-id="7a97f-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="7a97f-122">Gibt den durch DrehbezX und DrehbezY dargestellten Punkt zurück.</span><span class="sxs-lookup"><span data-stu-id="7a97f-122">Returns the point represented by PinX and PinY.</span></span> 
  

