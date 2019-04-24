---
title: MIN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251463
localization_priority: Normal
ms.assetid: b945b7c2-153f-2fc3-b768-1e975254ddf5
description: Gibt die kleinste Zahl aus einer Liste zurück. Kleinstes Mittel ist der negativen Unendlichkeit am nächsten.
ms.openlocfilehash: 7c9eb1a8d4ce30e7ab9253c2864ecd38474e8ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360648"
---
# <a name="min-function"></a><span data-ttu-id="3b28b-104">MIN Function</span><span class="sxs-lookup"><span data-stu-id="3b28b-104">MIN Function</span></span>

<span data-ttu-id="3b28b-105">Gibt die kleinste Zahl aus einer Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="3b28b-105">Returns the smallest number from a list.</span></span> <span data-ttu-id="3b28b-106">Kleinstes Mittel ist der negativen Unendlichkeit am nächsten.</span><span class="sxs-lookup"><span data-stu-id="3b28b-106">Smallest means closest to negative infinity.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3b28b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b28b-107">Syntax</span></span>

<span data-ttu-id="3b28b-108">MIN (\* \* *number1* \* \*, \* \* *number2* \* \*,..., \* \* *numbern* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3b28b-108">MIN(\*\* *number1* \*\*, \*\* *number2* \*\*,..., \*\* *numberN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3b28b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b28b-109">Parameters</span></span>

|<span data-ttu-id="3b28b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="3b28b-110">**Name**</span></span>|<span data-ttu-id="3b28b-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="3b28b-111">**Required/Optional**</span></span>|<span data-ttu-id="3b28b-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="3b28b-112">**Data Type**</span></span>|<span data-ttu-id="3b28b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b28b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3b28b-114">_Zahl1_</span><span class="sxs-lookup"><span data-stu-id="3b28b-114">_number1_</span></span> <br/> |<span data-ttu-id="3b28b-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3b28b-115">Required</span></span>  <br/> |<span data-ttu-id="3b28b-116">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="3b28b-116">**Varies**</span></span> <br/> |<span data-ttu-id="3b28b-117">Die erste Zahl in der Liste.</span><span class="sxs-lookup"><span data-stu-id="3b28b-117">The first number in the list.</span></span>  <br/> |
| <span data-ttu-id="3b28b-118">_Zahl2_</span><span class="sxs-lookup"><span data-stu-id="3b28b-118">_number2_</span></span> <br/> |<span data-ttu-id="3b28b-119">Optional</span><span class="sxs-lookup"><span data-stu-id="3b28b-119">Optional</span></span>  <br/> |<span data-ttu-id="3b28b-120">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="3b28b-120">**Varies**</span></span> <br/> | <span data-ttu-id="3b28b-121">Die zweite Zahl in der Liste.</span><span class="sxs-lookup"><span data-stu-id="3b28b-121">The second number in the list.</span></span>  <br/> |
| <span data-ttu-id="3b28b-122">_Nummerierung_</span><span class="sxs-lookup"><span data-stu-id="3b28b-122">_numberN_</span></span> <br/> |<span data-ttu-id="3b28b-123">Optional</span><span class="sxs-lookup"><span data-stu-id="3b28b-123">Optional</span></span>  <br/> |<span data-ttu-id="3b28b-124">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="3b28b-124">**Varies**</span></span> <br/> |<span data-ttu-id="3b28b-125">Die n-te Zahl in der Liste.</span><span class="sxs-lookup"><span data-stu-id="3b28b-125">The nth number in the list.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3b28b-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b28b-126">Return value</span></span>

<span data-ttu-id="3b28b-127">Variiert</span><span class="sxs-lookup"><span data-stu-id="3b28b-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="3b28b-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3b28b-128">Example</span></span>

<span data-ttu-id="3b28b-129">MIN(35 cm, 0,3mm , 20 cm)</span><span class="sxs-lookup"><span data-stu-id="3b28b-129">MIN(13 in,1 ft, 20 cm)</span></span> 
  
<span data-ttu-id="3b28b-130">Gibt 20 cm zurück.</span><span class="sxs-lookup"><span data-stu-id="3b28b-130">Returns 20 centimeters.</span></span> 
  

