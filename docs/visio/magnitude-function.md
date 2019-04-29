---
title: MAGNITUDE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Gibt die Größe des Vektors zurück, dessen Anstieg A ist und dessen Ausführung B ist, multipliziert mit den entsprechenden Konstanten constantA und Konstanteb.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420458"
---
# <a name="magnitude-function"></a><span data-ttu-id="2876c-103">MAGNITUDE Function</span><span class="sxs-lookup"><span data-stu-id="2876c-103">MAGNITUDE Function</span></span>

<span data-ttu-id="2876c-104">Gibt die Größe des Vektors zurück, dessen Anstieg _A_ ist und dessen Ausführung _B_ist, multipliziert mit den entsprechenden Konstanten _constantA_ und _konstanteb_.</span><span class="sxs-lookup"><span data-stu-id="2876c-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2876c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2876c-105">Syntax</span></span>

<span data-ttu-id="2876c-106">MAGNITUDE (\* \* *constantA* \* \*, \* \* *a* \* \*, \* \* *konstanteb* \* \*, \* \* *B* \* \*)</span><span class="sxs-lookup"><span data-stu-id="2876c-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2876c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2876c-107">Parameters</span></span>

|<span data-ttu-id="2876c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2876c-108">**Name**</span></span>|<span data-ttu-id="2876c-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2876c-109">**Required/Optional**</span></span>|<span data-ttu-id="2876c-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2876c-110">**Data Type**</span></span>|<span data-ttu-id="2876c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2876c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2876c-112">_constantA_</span><span class="sxs-lookup"><span data-stu-id="2876c-112">_constantA_</span></span> <br/> |<span data-ttu-id="2876c-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2876c-113">Required</span></span>  <br/> |<span data-ttu-id="2876c-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="2876c-114">**Number**</span></span> <br/> |<span data-ttu-id="2876c-115">Die Konstante, mit der die Steigung multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2876c-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="2876c-116">_A_</span><span class="sxs-lookup"><span data-stu-id="2876c-116">_A_</span></span> <br/> |<span data-ttu-id="2876c-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2876c-117">Required</span></span>  <br/> |<span data-ttu-id="2876c-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="2876c-118">**Number**</span></span> <br/> |<span data-ttu-id="2876c-119">Die Steigung.</span><span class="sxs-lookup"><span data-stu-id="2876c-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="2876c-120">_Konstanteb_</span><span class="sxs-lookup"><span data-stu-id="2876c-120">_constantB_</span></span> <br/> |<span data-ttu-id="2876c-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2876c-121">Required</span></span>  <br/> |<span data-ttu-id="2876c-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="2876c-122">**Number**</span></span> <br/> |<span data-ttu-id="2876c-123">Die Konstante, mit der die Länge multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2876c-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="2876c-124">_B_</span><span class="sxs-lookup"><span data-stu-id="2876c-124">_B_</span></span> <br/> |<span data-ttu-id="2876c-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2876c-125">Required</span></span>  <br/> |<span data-ttu-id="2876c-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="2876c-126">**Number**</span></span> <br/> |<span data-ttu-id="2876c-127">Die Länge.</span><span class="sxs-lookup"><span data-stu-id="2876c-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2876c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2876c-128">Remarks</span></span>

<span data-ttu-id="2876c-129">MAGNITUDE wird nach folgender Formel berechnet:</span><span class="sxs-lookup"><span data-stu-id="2876c-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="2876c-130">SQRT ((constantA \* A) ^ 2 + (konstanteb \* B) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="2876c-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="2876c-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2876c-131">Example</span></span>

<span data-ttu-id="2876c-132">MAGNITUDE(1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="2876c-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="2876c-133">Gibt 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="2876c-133">Returns 5.</span></span> 
  

