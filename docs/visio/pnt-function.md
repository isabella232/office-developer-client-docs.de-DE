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
description: Gibt den Punkt, dargestellt durch die Koordinaten X und y als einen single-Wert.
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797688"
---
# <a name="pnt-function"></a><span data-ttu-id="1c62c-103">PNT Function</span><span class="sxs-lookup"><span data-stu-id="1c62c-103">PNT Function</span></span>

<span data-ttu-id="1c62c-104">Gibt den durch die Koordinaten _X_ und _y_ als einzelner Wert dargestellten Punkt zurück.</span><span class="sxs-lookup"><span data-stu-id="1c62c-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1c62c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c62c-105">Syntax</span></span>

<span data-ttu-id="1c62c-106">PNT (** *x, y* **)</span><span class="sxs-lookup"><span data-stu-id="1c62c-106">PNT(** *x,y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1c62c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c62c-107">Parameters</span></span>

|<span data-ttu-id="1c62c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1c62c-108">**Name**</span></span>|<span data-ttu-id="1c62c-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="1c62c-109">**Required/Optional**</span></span>|<span data-ttu-id="1c62c-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="1c62c-110">**Data Type**</span></span>|<span data-ttu-id="1c62c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c62c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1c62c-112">_X, y_</span><span class="sxs-lookup"><span data-stu-id="1c62c-112">_x,y_</span></span> <br/> |<span data-ttu-id="1c62c-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1c62c-113">Required</span></span>  <br/> |<span data-ttu-id="1c62c-114">**Number, Number**</span><span class="sxs-lookup"><span data-stu-id="1c62c-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="1c62c-115">Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.</span><span class="sxs-lookup"><span data-stu-id="1c62c-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1c62c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c62c-116">Return value</span></span>

<span data-ttu-id="1c62c-117">Punkt</span><span class="sxs-lookup"><span data-stu-id="1c62c-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1c62c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c62c-118">Remarks</span></span>

<span data-ttu-id="1c62c-119">Konvertierung von Koordinaten in Punkte können Sie die Geometrie eines Shapes ändern, ohne dass zum Bearbeiten von *X* - und *y* -Koordinaten getrennt.</span><span class="sxs-lookup"><span data-stu-id="1c62c-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1c62c-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1c62c-120">Example</span></span>

<span data-ttu-id="1c62c-121">PNT(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="1c62c-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="1c62c-122">Gibt den durch DrehbezX und DrehbezY dargestellten Punkt zurück.</span><span class="sxs-lookup"><span data-stu-id="1c62c-122">Returns the point represented by PinX and PinY.</span></span> 
  

