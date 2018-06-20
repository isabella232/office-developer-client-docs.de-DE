---
title: ASIN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Gibt den Arkussinus einer Zahl, beispielsweise der Winkel, dessen Sinus Zahl ist.
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796431"
---
# <a name="asin-function"></a><span data-ttu-id="e0a11-103">ASIN Function</span><span class="sxs-lookup"><span data-stu-id="e0a11-103">ASIN Function</span></span>

<span data-ttu-id="e0a11-104">Gibt den Arkussinus einer Zahl, beispielsweise der Winkel, dessen Sinus *Zahl* ist.</span><span class="sxs-lookup"><span data-stu-id="e0a11-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e0a11-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0a11-105">Syntax</span></span>

<span data-ttu-id="e0a11-106">ASIN (** *Anzahl* **)</span><span class="sxs-lookup"><span data-stu-id="e0a11-106">ASIN(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e0a11-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0a11-107">Parameters</span></span>

|<span data-ttu-id="e0a11-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e0a11-108">**Name**</span></span>|<span data-ttu-id="e0a11-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="e0a11-109">**Required/Optional**</span></span>|<span data-ttu-id="e0a11-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e0a11-110">**Data Type**</span></span>|<span data-ttu-id="e0a11-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e0a11-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e0a11-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="e0a11-112">_number_</span></span> <br/> |<span data-ttu-id="e0a11-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e0a11-113">Required</span></span>  <br/> |<span data-ttu-id="e0a11-114">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="e0a11-114">**Numeric**</span></span> <br/> |<span data-ttu-id="e0a11-115">Der Sinus des Winkels.</span><span class="sxs-lookup"><span data-stu-id="e0a11-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0a11-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0a11-116">Remarks</span></span>

<span data-ttu-id="e0a11-117">Der Wert muss im Bereich von-1 < = *Zahl* < = 1 oder ein #NUM!</span><span class="sxs-lookup"><span data-stu-id="e0a11-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="e0a11-118">Fehler wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0a11-118">error is returned.</span></span> <span data-ttu-id="e0a11-119">Der resultierende Winkel liegt im Bereich-PI/2 < = *Winkel* < = PI/2 Bogenmaß (-90 < = *Winkel* < = 90 Grad).</span><span class="sxs-lookup"><span data-stu-id="e0a11-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="e0a11-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e0a11-120">Example</span></span>

<span data-ttu-id="e0a11-121">ASIN(1)</span><span class="sxs-lookup"><span data-stu-id="e0a11-121">ASIN(1)</span></span>
  
<span data-ttu-id="e0a11-122">Gibt 90 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="e0a11-122">Returns 90 deg</span></span>
  

