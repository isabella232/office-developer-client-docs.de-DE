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
description: Gibt die Durch Stunde, Minute und Sekunde dargestellte Zeit zurück.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414473"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="ebcc8-103">TIME-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="ebcc8-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="ebcc8-104">Gibt die Durch _Stunde,_ Minute und Sekunde dargestellte Zeit _zurück._ </span><span class="sxs-lookup"><span data-stu-id="ebcc8-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ebcc8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebcc8-105">Syntax</span></span>

<span data-ttu-id="ebcc8-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ebcc8-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ebcc8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebcc8-107">Parameters</span></span>

|<span data-ttu-id="ebcc8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ebcc8-108">**Name**</span></span>|<span data-ttu-id="ebcc8-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ebcc8-109">**Required/Optional**</span></span>|<span data-ttu-id="ebcc8-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ebcc8-110">**Data Type**</span></span>|<span data-ttu-id="ebcc8-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebcc8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ebcc8-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="ebcc8-112">_hour_</span></span> <br/> |<span data-ttu-id="ebcc8-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebcc8-113">Required</span></span>  <br/> |<span data-ttu-id="ebcc8-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ebcc8-114">**Numeric**</span></span> <br/> |<span data-ttu-id="ebcc8-115">Die Stundenkomponente.</span><span class="sxs-lookup"><span data-stu-id="ebcc8-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="ebcc8-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="ebcc8-116">_minute_</span></span> <br/> |<span data-ttu-id="ebcc8-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebcc8-117">Required</span></span>  <br/> |<span data-ttu-id="ebcc8-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ebcc8-118">**Numeric**</span></span> <br/> |<span data-ttu-id="ebcc8-119">Die Minutenkomponente.</span><span class="sxs-lookup"><span data-stu-id="ebcc8-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="ebcc8-120">_second_</span><span class="sxs-lookup"><span data-stu-id="ebcc8-120">_second_</span></span> <br/> |<span data-ttu-id="ebcc8-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebcc8-121">Required</span></span>  <br/> |<span data-ttu-id="ebcc8-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ebcc8-122">**Numeric**</span></span> <br/> |<span data-ttu-id="ebcc8-123">Die Sekundenkomponente.</span><span class="sxs-lookup"><span data-stu-id="ebcc8-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ebcc8-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebcc8-124">Return value</span></span>

<span data-ttu-id="ebcc8-125">Numeric</span><span class="sxs-lookup"><span data-stu-id="ebcc8-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="ebcc8-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ebcc8-126">Example 1</span></span>

<span data-ttu-id="ebcc8-127">TIME(15,30,30)</span><span class="sxs-lookup"><span data-stu-id="ebcc8-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="ebcc8-128">Gibt den Wert für 15:30:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="ebcc8-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ebcc8-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ebcc8-129">Example 2</span></span>

<span data-ttu-id="ebcc8-130">FORMAT(TIME(15,30,30),"HH:mm")</span><span class="sxs-lookup"><span data-stu-id="ebcc8-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="ebcc8-131">Gibt den Wert für 15:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="ebcc8-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ebcc8-132">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ebcc8-132">Example 3</span></span>

<span data-ttu-id="ebcc8-133">TIME(15,30,30) + 8 vs.</span><span class="sxs-lookup"><span data-stu-id="ebcc8-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="ebcc8-134">Gibt den Wert für 23:30:30 zurück.</span><span class="sxs-lookup"><span data-stu-id="ebcc8-134">Returns the value representing 23:30:30.</span></span>
  

