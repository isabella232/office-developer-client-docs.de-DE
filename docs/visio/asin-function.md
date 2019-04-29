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
description: Gibt den arcsine einer Zahl zurück, beispielsweise den Winkel, dessen Sinus Nummer ist.
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432821"
---
# <a name="asin-function"></a><span data-ttu-id="361e3-103">ASIN Function</span><span class="sxs-lookup"><span data-stu-id="361e3-103">ASIN Function</span></span>

<span data-ttu-id="361e3-104">Gibt den arcsine einer Zahl zurück, beispielsweise den Winkel, dessen Sinus *Nummer* ist.</span><span class="sxs-lookup"><span data-stu-id="361e3-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="361e3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="361e3-105">Syntax</span></span>

<span data-ttu-id="361e3-106">Arcs (\* \* *Number* \* \*)</span><span class="sxs-lookup"><span data-stu-id="361e3-106">ASIN(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="361e3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="361e3-107">Parameters</span></span>

|<span data-ttu-id="361e3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="361e3-108">**Name**</span></span>|<span data-ttu-id="361e3-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="361e3-109">**Required/Optional**</span></span>|<span data-ttu-id="361e3-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="361e3-110">**Data Type**</span></span>|<span data-ttu-id="361e3-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="361e3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="361e3-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="361e3-112">_number_</span></span> <br/> |<span data-ttu-id="361e3-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="361e3-113">Required</span></span>  <br/> |<span data-ttu-id="361e3-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="361e3-114">**Numeric**</span></span> <br/> |<span data-ttu-id="361e3-115">Der Sinus des Winkels.</span><span class="sxs-lookup"><span data-stu-id="361e3-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="361e3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="361e3-116">Remarks</span></span>

<span data-ttu-id="361e3-117">Der Eingabewert muss im Range-1 < = *Number* < = 1 oder ein #NUM!</span><span class="sxs-lookup"><span data-stu-id="361e3-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="361e3-118">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="361e3-118">error is returned.</span></span> <span data-ttu-id="361e3-119">Der resultierende Winkel befindet sich im Range-PI/2 < \*\* = Angle _LT_ = Pi/2 Radiant (-90 < = *winkel* < = 90 Grad).</span><span class="sxs-lookup"><span data-stu-id="361e3-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="361e3-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="361e3-120">Example</span></span>

<span data-ttu-id="361e3-121">ARCS (1)</span><span class="sxs-lookup"><span data-stu-id="361e3-121">ASIN(1)</span></span>
  
<span data-ttu-id="361e3-122">Gibt 90 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="361e3-122">Returns 90 deg</span></span>
  

