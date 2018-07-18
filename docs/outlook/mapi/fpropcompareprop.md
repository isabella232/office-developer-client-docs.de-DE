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
ms.openlocfilehash: 69bbed644a8173bf9291ca48a63960f693108318
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791739"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="bc196-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="bc196-103">FPropCompareProp</span></span>

<span data-ttu-id="bc196-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc196-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc196-105">Vergleicht zwei Eigenschaftswerte, die mit einem angegebenen relationalen Operator.</span><span class="sxs-lookup"><span data-stu-id="bc196-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc196-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bc196-106">Header file:</span></span>  <br/> |<span data-ttu-id="bc196-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="bc196-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bc196-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="bc196-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bc196-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bc196-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bc196-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="bc196-110">Called by:</span></span>  <br/> |<span data-ttu-id="bc196-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="bc196-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="bc196-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc196-112">Parameters</span></span>

<span data-ttu-id="bc196-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="bc196-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="bc196-114">[in] Zeiger auf eine [SPropValue](spropvalue.md) -Struktur für den Vergleich den ersten Eigenschaftswert definieren.</span><span class="sxs-lookup"><span data-stu-id="bc196-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="bc196-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="bc196-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="bc196-116">[in] Der relationale Operator, im Vergleich zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc196-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="bc196-117">Zulässige Werte finden Sie unter der Struktur [SComparePropsRestriction](scomparepropsrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="bc196-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="bc196-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="bc196-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="bc196-119">[in] Zeiger auf eine **SPropValue** -Struktur für den Vergleich den zweiten Eigenschaftswert definieren.</span><span class="sxs-lookup"><span data-stu-id="bc196-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bc196-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="bc196-120">Return value</span></span>

<span data-ttu-id="bc196-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="bc196-121">TRUE</span></span> 
  
> <span data-ttu-id="bc196-122">Die Eigenschaftswerte erfüllen die angegebene Relation-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bc196-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="bc196-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="bc196-123">FALSE</span></span> 
  
> <span data-ttu-id="bc196-124">Die Eigenschaftswerte werden nicht die angegebene Relation-Objekt erfüllen.</span><span class="sxs-lookup"><span data-stu-id="bc196-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc196-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc196-125">Remarks</span></span>

<span data-ttu-id="bc196-126">Die Vergleichsmethode hängt die Eigenschaftentypen in die Definitionen der [SPropValue](spropvalue.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="bc196-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="bc196-127">Die Funktionen **FPropCompareProp** und [FPropContainsProp](fpropcontainsprop.md) können verwendet werden, um Einschränkungen zum Generieren einer Tabelle vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="bc196-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="bc196-128">Die Reihenfolge des Vergleichs ist _lpSPropValue1_, _ UlRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="bc196-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="bc196-129">Die **FPropCompareProp** -Funktion gibt FALSE zurück, wenn die Eigenschaftentypen der Eigenschaftswerte, die verglichen werden nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="bc196-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

