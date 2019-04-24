---
title: TIME-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Gibt die von Stunde, Minute und Sekunde dargestellte Zeit zurück.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280997"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="c5c4d-103">TIME-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="c5c4d-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="c5c4d-104">Gibt die von _Stunde_, _Minute_und _Sekunde_dargestellte Zeit zurück.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c5c4d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5c4d-105">Syntax</span></span>

<span data-ttu-id="c5c4d-106">Uhrzeit (\* \* *Stunde* \* \*, \* \* *Minute* \* \*, \* \* *Sekunde* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c5c4d-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c5c4d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5c4d-107">Parameters</span></span>

|<span data-ttu-id="c5c4d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c5c4d-108">**Name**</span></span>|<span data-ttu-id="c5c4d-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c5c4d-109">**Required/Optional**</span></span>|<span data-ttu-id="c5c4d-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c5c4d-110">**Data Type**</span></span>|<span data-ttu-id="c5c4d-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5c4d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c5c4d-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="c5c4d-112">_hour_</span></span> <br/> |<span data-ttu-id="c5c4d-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c5c4d-113">Required</span></span>  <br/> |<span data-ttu-id="c5c4d-114">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="c5c4d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="c5c4d-115">Die Stundenkomponente.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="c5c4d-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="c5c4d-116">_minute_</span></span> <br/> |<span data-ttu-id="c5c4d-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c5c4d-117">Required</span></span>  <br/> |<span data-ttu-id="c5c4d-118">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="c5c4d-118">**Numeric**</span></span> <br/> |<span data-ttu-id="c5c4d-119">Die Minutenkomponente.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="c5c4d-120">_second_</span><span class="sxs-lookup"><span data-stu-id="c5c4d-120">_second_</span></span> <br/> |<span data-ttu-id="c5c4d-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c5c4d-121">Required</span></span>  <br/> |<span data-ttu-id="c5c4d-122">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="c5c4d-122">**Numeric**</span></span> <br/> |<span data-ttu-id="c5c4d-123">Die Sekundenkomponente.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c5c4d-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5c4d-124">Return value</span></span>

<span data-ttu-id="c5c4d-125">Numerisch</span><span class="sxs-lookup"><span data-stu-id="c5c4d-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="c5c4d-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5c4d-126">Example 1</span></span>

<span data-ttu-id="c5c4d-127">ZEIT (15, 30, 30)</span><span class="sxs-lookup"><span data-stu-id="c5c4d-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="c5c4d-128">Gibt den Wert für 15:30:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c5c4d-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c5c4d-129">Example 2</span></span>

<span data-ttu-id="c5c4d-130">FORMAT (Zeit (15, 30, 30), "HH: mm")</span><span class="sxs-lookup"><span data-stu-id="c5c4d-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="c5c4d-131">Gibt den Wert für 15:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c5c4d-132">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c5c4d-132">Example 3</span></span>

<span data-ttu-id="c5c4d-133">TIME(15,30,30) + 8 vs.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="c5c4d-134">Gibt den Wert für 23:30:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-134">Returns the value representing 23:30:30.</span></span>
  

