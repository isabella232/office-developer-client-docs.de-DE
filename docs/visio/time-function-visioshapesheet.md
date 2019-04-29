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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414473"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="fb0f4-103">TIME-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fb0f4-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fb0f4-104">Gibt die von _Stunde_, _Minute_und _Sekunde_dargestellte Zeit zurück.</span><span class="sxs-lookup"><span data-stu-id="fb0f4-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fb0f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb0f4-105">Syntax</span></span>

<span data-ttu-id="fb0f4-106">Uhrzeit (\* \* *Stunde* \* \*, \* \* *Minute* \* \*, \* \* *Sekunde* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fb0f4-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fb0f4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb0f4-107">Parameters</span></span>

|<span data-ttu-id="fb0f4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fb0f4-108">**Name**</span></span>|<span data-ttu-id="fb0f4-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="fb0f4-109">**Required/Optional**</span></span>|<span data-ttu-id="fb0f4-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="fb0f4-110">**Data Type**</span></span>|<span data-ttu-id="fb0f4-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb0f4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fb0f4-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="fb0f4-112">_hour_</span></span> <br/> |<span data-ttu-id="fb0f4-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fb0f4-113">Required</span></span>  <br/> |<span data-ttu-id="fb0f4-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="fb0f4-114">**Numeric**</span></span> <br/> |<span data-ttu-id="fb0f4-115">Die Stundenkomponente.</span><span class="sxs-lookup"><span data-stu-id="fb0f4-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="fb0f4-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="fb0f4-116">_minute_</span></span> <br/> |<span data-ttu-id="fb0f4-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fb0f4-117">Required</span></span>  <br/> |<span data-ttu-id="fb0f4-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="fb0f4-118">**Numeric**</span></span> <br/> |<span data-ttu-id="fb0f4-119">Die Minutenkomponente.</span><span class="sxs-lookup"><span data-stu-id="fb0f4-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="fb0f4-120">_second_</span><span class="sxs-lookup"><span data-stu-id="fb0f4-120">_second_</span></span> <br/> |<span data-ttu-id="fb0f4-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fb0f4-121">Required</span></span>  <br/> |<span data-ttu-id="fb0f4-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="fb0f4-122">**Numeric**</span></span> <br/> |<span data-ttu-id="fb0f4-123">Die Sekundenkomponente.</span><span class="sxs-lookup"><span data-stu-id="fb0f4-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fb0f4-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb0f4-124">Return value</span></span>

<span data-ttu-id="fb0f4-125">Numeric</span><span class="sxs-lookup"><span data-stu-id="fb0f4-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="fb0f4-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fb0f4-126">Example 1</span></span>

<span data-ttu-id="fb0f4-127">ZEIT (15, 30, 30)</span><span class="sxs-lookup"><span data-stu-id="fb0f4-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="fb0f4-128">Gibt den Wert für 15:30:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="fb0f4-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fb0f4-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fb0f4-129">Example 2</span></span>

<span data-ttu-id="fb0f4-130">FORMAT (Zeit (15, 30, 30), "HH: mm")</span><span class="sxs-lookup"><span data-stu-id="fb0f4-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="fb0f4-131">Gibt den Wert für 15:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="fb0f4-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fb0f4-132">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fb0f4-132">Example 3</span></span>

<span data-ttu-id="fb0f4-133">TIME(15,30,30) + 8 vs.</span><span class="sxs-lookup"><span data-stu-id="fb0f4-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="fb0f4-134">Gibt den Wert für 23:30:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="fb0f4-134">Returns the value representing 23:30:30.</span></span>
  

