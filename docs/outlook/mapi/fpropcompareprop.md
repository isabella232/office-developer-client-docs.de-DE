---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328070"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="7b0f4-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="7b0f4-103">FPropCompareProp</span></span>

<span data-ttu-id="7b0f4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b0f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b0f4-105">Vergleicht zwei Eigenschaftswerte mit einem angegebenen relationalen Operator.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b0f4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7b0f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b0f4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="7b0f4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7b0f4-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7b0f4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b0f4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b0f4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b0f4-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7b0f4-110">Called by:</span></span>  <br/> |<span data-ttu-id="7b0f4-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7b0f4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="7b0f4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b0f4-112">Parameters</span></span>

<span data-ttu-id="7b0f4-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="7b0f4-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="7b0f4-114">in Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die den ersten Eigenschaftswert für den Vergleich definiert.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="7b0f4-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="7b0f4-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="7b0f4-116">in Der relationale Operator, der im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="7b0f4-117">Informationen zu zulässigen Werten finden Sie in der [SComparePropsRestriction](scomparepropsrestriction.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="7b0f4-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="7b0f4-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="7b0f4-119">in Zeiger auf eine **SPropValue** -Struktur, die den zweiten Eigenschaftswert für den Vergleich definiert.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7b0f4-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b0f4-120">Return value</span></span>

<span data-ttu-id="7b0f4-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="7b0f4-121">TRUE</span></span> 
  
> <span data-ttu-id="7b0f4-122">Die Eigenschaftswerte erfüllen die angegebene Beziehung.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="7b0f4-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="7b0f4-123">FALSE</span></span> 
  
> <span data-ttu-id="7b0f4-124">Die Eigenschaftswerte erfüllen nicht die angegebene Beziehung.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b0f4-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b0f4-125">Remarks</span></span>

<span data-ttu-id="7b0f4-126">Die Vergleichsmethode hängt von den Eigenschaftentypen ab, die in den [SPropValue](spropvalue.md) -Eigenschaftsdefinitionen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="7b0f4-127">Die **FPropCompareProp** -und [FPropContainsProp](fpropcontainsprop.md) -Funktionen können verwendet werden, um Einschränkungen für das Generieren einer Tabelle vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="7b0f4-128">Die Reihenfolge des Vergleichs ist _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="7b0f4-129">Wenn die Eigenschaftentypen der zu vergleichenden Eigenschaftswerte nicht übereinstimmen, gibt die **FPropCompareProp** -Funktion false zurück.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

