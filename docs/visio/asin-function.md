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
description: Gibt den Bogensinus einer Zahl zurück, z. B. den Winkel, dessen Sinus Zahl ist.
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293506"
---
# <a name="asin-function"></a><span data-ttu-id="a9e94-103">ASIN Function</span><span class="sxs-lookup"><span data-stu-id="a9e94-103">ASIN Function</span></span>

<span data-ttu-id="a9e94-104">Gibt den Bogensinus einer Zahl zurück, z. B. den Winkel, dessen Sinus Zahl *ist.*</span><span class="sxs-lookup"><span data-stu-id="a9e94-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a9e94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9e94-105">Syntax</span></span>

<span data-ttu-id="a9e94-106">ASIN(***number*** )</span><span class="sxs-lookup"><span data-stu-id="a9e94-106">ASIN(***number*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a9e94-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9e94-107">Parameters</span></span>

|<span data-ttu-id="a9e94-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a9e94-108">**Name**</span></span>|<span data-ttu-id="a9e94-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a9e94-109">**Required/Optional**</span></span>|<span data-ttu-id="a9e94-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a9e94-110">**Data Type**</span></span>|<span data-ttu-id="a9e94-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9e94-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a9e94-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="a9e94-112">_number_</span></span> <br/> |<span data-ttu-id="a9e94-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a9e94-113">Required</span></span>  <br/> |<span data-ttu-id="a9e94-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="a9e94-114">**Numeric**</span></span> <br/> |<span data-ttu-id="a9e94-115">Der Sinus des Winkels.</span><span class="sxs-lookup"><span data-stu-id="a9e94-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9e94-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9e94-116">Remarks</span></span>

<span data-ttu-id="a9e94-117">Der Eingabewert muss sich im Bereich -1 <=  *Zahl*  <= 1 oder einer #NUM!</span><span class="sxs-lookup"><span data-stu-id="a9e94-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="a9e94-118">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9e94-118">error is returned.</span></span> <span data-ttu-id="a9e94-119">Der resultierende Winkel liegt im Bereich -PI/2 < *=*  Winkel <= PI/2 Bogenmaß (-90 < *=*  Winkel <= 90 Grad).</span><span class="sxs-lookup"><span data-stu-id="a9e94-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="a9e94-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9e94-120">Example</span></span>

<span data-ttu-id="a9e94-121">ASIN(1)</span><span class="sxs-lookup"><span data-stu-id="a9e94-121">ASIN(1)</span></span>
  
<span data-ttu-id="a9e94-122">Gibt 90 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="a9e94-122">Returns 90 deg</span></span>
  

