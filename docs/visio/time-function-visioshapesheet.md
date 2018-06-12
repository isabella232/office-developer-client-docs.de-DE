---
title: TIME Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Gibt die Uhrzeit als Stunden, Minuten und Sekunden.
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798290"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="7d15c-103">TIME Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="7d15c-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="7d15c-104">Gibt die Zeit, die durch _Stunde_, _Minute_und _Sekunde_dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d15c-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7d15c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d15c-105">Syntax</span></span>

<span data-ttu-id="7d15c-106">Zeit (** *Stunde* **, ** *Minute* **, ** *zweiten* **)</span><span class="sxs-lookup"><span data-stu-id="7d15c-106">TIME(** *hour* **, ** *minute* **, ** *second* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7d15c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d15c-107">Parameters</span></span>

|<span data-ttu-id="7d15c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7d15c-108">**Name**</span></span>|<span data-ttu-id="7d15c-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="7d15c-109">**Required/Optional**</span></span>|<span data-ttu-id="7d15c-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="7d15c-110">**Data Type**</span></span>|<span data-ttu-id="7d15c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7d15c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7d15c-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="7d15c-112">_hour_</span></span> <br/> |<span data-ttu-id="7d15c-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7d15c-113">Required</span></span>  <br/> |<span data-ttu-id="7d15c-114">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="7d15c-114">**Numeric**</span></span> <br/> |<span data-ttu-id="7d15c-115">Die Stundenkomponente.</span><span class="sxs-lookup"><span data-stu-id="7d15c-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="7d15c-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="7d15c-116">_minute_</span></span> <br/> |<span data-ttu-id="7d15c-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7d15c-117">Required</span></span>  <br/> |<span data-ttu-id="7d15c-118">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="7d15c-118">**Numeric**</span></span> <br/> |<span data-ttu-id="7d15c-119">Die Minutenkomponente.</span><span class="sxs-lookup"><span data-stu-id="7d15c-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="7d15c-120">_second_</span><span class="sxs-lookup"><span data-stu-id="7d15c-120">_second_</span></span> <br/> |<span data-ttu-id="7d15c-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7d15c-121">Required</span></span>  <br/> |<span data-ttu-id="7d15c-122">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="7d15c-122">**Numeric**</span></span> <br/> |<span data-ttu-id="7d15c-123">Die Sekundenkomponente.</span><span class="sxs-lookup"><span data-stu-id="7d15c-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7d15c-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7d15c-124">Return value</span></span>

<span data-ttu-id="7d15c-125">Numeric</span><span class="sxs-lookup"><span data-stu-id="7d15c-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="7d15c-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d15c-126">Example 1</span></span>

<span data-ttu-id="7d15c-127">TIME(15,30,30)</span><span class="sxs-lookup"><span data-stu-id="7d15c-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="7d15c-128">Gibt den Wert für 15:30:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="7d15c-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7d15c-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7d15c-129">Example 2</span></span>

<span data-ttu-id="7d15c-130">FORMAT(ZEIT(15,30,30),"HH:mm")</span><span class="sxs-lookup"><span data-stu-id="7d15c-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="7d15c-131">Gibt den Wert für 15:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="7d15c-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7d15c-132">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7d15c-132">Example 3</span></span>

<span data-ttu-id="7d15c-133">TIME(15,30,30) + 8 vs.</span><span class="sxs-lookup"><span data-stu-id="7d15c-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="7d15c-134">Gibt den Wert für 23:30:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="7d15c-134">Returns the value representing 23:30:30.</span></span>
  

