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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: adccbaf65adec2c517c4890f722198e8262092cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564605"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="c11d6-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="c11d6-103">FPropCompareProp</span></span>

<span data-ttu-id="c11d6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c11d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c11d6-105">Vergleicht zwei Eigenschaftswerte, die mit einem angegebenen relationalen Operator.</span><span class="sxs-lookup"><span data-stu-id="c11d6-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c11d6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c11d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="c11d6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c11d6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c11d6-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c11d6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c11d6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c11d6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c11d6-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c11d6-110">Called by:</span></span>  <br/> |<span data-ttu-id="c11d6-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c11d6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="c11d6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c11d6-112">Parameters</span></span>

<span data-ttu-id="c11d6-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="c11d6-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="c11d6-114">[in] Zeiger auf eine [SPropValue](spropvalue.md) -Struktur für den Vergleich den ersten Eigenschaftswert definieren.</span><span class="sxs-lookup"><span data-stu-id="c11d6-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="c11d6-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="c11d6-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="c11d6-116">[in] Der relationale Operator, im Vergleich zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c11d6-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="c11d6-117">Zulässige Werte finden Sie unter der Struktur [SComparePropsRestriction](scomparepropsrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="c11d6-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="c11d6-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="c11d6-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="c11d6-119">[in] Zeiger auf eine **SPropValue** -Struktur für den Vergleich den zweiten Eigenschaftswert definieren.</span><span class="sxs-lookup"><span data-stu-id="c11d6-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c11d6-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c11d6-120">Return value</span></span>

<span data-ttu-id="c11d6-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="c11d6-121">TRUE</span></span> 
  
> <span data-ttu-id="c11d6-122">Die Eigenschaftswerte erfüllen die angegebene Relation-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c11d6-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="c11d6-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="c11d6-123">FALSE</span></span> 
  
> <span data-ttu-id="c11d6-124">Die Eigenschaftswerte werden nicht die angegebene Relation-Objekt erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c11d6-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c11d6-125">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c11d6-125">Remarks</span></span>

<span data-ttu-id="c11d6-126">Die Vergleichsmethode hängt die Eigenschaftentypen in die Definitionen der [SPropValue](spropvalue.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="c11d6-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="c11d6-127">Die Funktionen **FPropCompareProp** und [FPropContainsProp](fpropcontainsprop.md) können verwendet werden, um Einschränkungen zum Generieren einer Tabelle vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="c11d6-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="c11d6-128">Die Reihenfolge des Vergleichs ist _lpSPropValue1_, _ UlRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="c11d6-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="c11d6-129">Die **FPropCompareProp** -Funktion gibt FALSE zurück, wenn die Eigenschaftentypen der Eigenschaftswerte, die verglichen werden nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c11d6-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

