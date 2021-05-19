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
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427157"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="d762b-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="d762b-103">FPropCompareProp</span></span>

<span data-ttu-id="d762b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d762b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d762b-105">Vergleicht zwei Eigenschaftswerte mit einem angegebenen relationalen Operator.</span><span class="sxs-lookup"><span data-stu-id="d762b-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d762b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d762b-106">Header file:</span></span>  <br/> |<span data-ttu-id="d762b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d762b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d762b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d762b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d762b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d762b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d762b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d762b-110">Called by:</span></span>  <br/> |<span data-ttu-id="d762b-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d762b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="d762b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d762b-112">Parameters</span></span>

<span data-ttu-id="d762b-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="d762b-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="d762b-114">[in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die den ersten Eigenschaftswert für den Vergleich definiert.</span><span class="sxs-lookup"><span data-stu-id="d762b-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="d762b-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="d762b-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="d762b-116">[in] Der relationale Operator, der im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d762b-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="d762b-117">Zulässige Werte finden Sie in der [SComparePropsRestriction-Struktur.](scomparepropsrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="d762b-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="d762b-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="d762b-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="d762b-119">[in] Zeiger auf eine **SPropValue-Struktur,** die den zweiten Eigenschaftswert für den Vergleich definiert.</span><span class="sxs-lookup"><span data-stu-id="d762b-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d762b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d762b-120">Return value</span></span>

<span data-ttu-id="d762b-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="d762b-121">TRUE</span></span> 
  
> <span data-ttu-id="d762b-122">Die Eigenschaftswerte erfüllen die angegebene Beziehung.</span><span class="sxs-lookup"><span data-stu-id="d762b-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="d762b-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="d762b-123">FALSE</span></span> 
  
> <span data-ttu-id="d762b-124">Die Eigenschaftswerte erfüllen nicht die angegebene Beziehung.</span><span class="sxs-lookup"><span data-stu-id="d762b-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d762b-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d762b-125">Remarks</span></span>

<span data-ttu-id="d762b-126">Die Vergleichsmethode hängt von den in den [SPropValue-Eigenschaftsdefinitionen angegebenen Eigenschaftstypen](spropvalue.md) ab.</span><span class="sxs-lookup"><span data-stu-id="d762b-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="d762b-127">Die **Funktionen FPropCompareProp** und [FPropContainsProp](fpropcontainsprop.md) können verwendet werden, um Einschränkungen für das Generieren einer Tabelle vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="d762b-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="d762b-128">Die Reihenfolge des Vergleichs ist  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="d762b-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="d762b-129">Wenn die Eigenschaftstypen der zu vergleichende Eigenschaftswerte nicht übereinstimmen, gibt **die FPropCompareProp-Funktion** FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="d762b-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

