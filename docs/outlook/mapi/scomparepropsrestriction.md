---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440003"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="a81ae-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="a81ae-103">SComparePropsRestriction</span></span>

<span data-ttu-id="a81ae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a81ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a81ae-105">Beschreibt eine Compare-Eigenschaftseinschränkung, die zwei Eigenschaften mithilfe eines relationalen Operators testet.</span><span class="sxs-lookup"><span data-stu-id="a81ae-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a81ae-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a81ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="a81ae-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a81ae-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="a81ae-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="a81ae-108">Members</span></span>

<span data-ttu-id="a81ae-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="a81ae-109">**relop**</span></span>
  
> <span data-ttu-id="a81ae-110">Relationaler Operator, der zum Vergleichen der beiden Eigenschaften verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a81ae-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="a81ae-111">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a81ae-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="a81ae-112">RELOP_GE: Der Vergleich basiert auf einem höheren oder gleichen ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="a81ae-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="a81ae-113">RELOP_GT: Der Vergleich basiert auf einem größeren ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="a81ae-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="a81ae-114">RELOP_LE: Der Vergleich basiert auf einem kleineren oder gleichen ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="a81ae-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="a81ae-115">RELOP_LT: Der Vergleich basiert auf einem niedrigeren ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="a81ae-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="a81ae-116">RELOP_NE: Der Vergleich basiert auf ungleichen Werten.</span><span class="sxs-lookup"><span data-stu-id="a81ae-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="a81ae-117">RELOP_RE: Der Vergleich wird basierend auf LIKE -Werten (regulärer Ausdruck) vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="a81ae-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="a81ae-118">RELOP_EQ: Der Vergleich basiert auf gleichen Werten.</span><span class="sxs-lookup"><span data-stu-id="a81ae-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="a81ae-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="a81ae-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="a81ae-120">Eigenschaftstag der ersten zu vergleichende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a81ae-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="a81ae-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="a81ae-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="a81ae-122">Eigenschaftstag der zweiten zu vergleichende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a81ae-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a81ae-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a81ae-123">Remarks</span></span>

<span data-ttu-id="a81ae-124">Die Vergleichsreihenfolge ist  _(Eigenschaftstag 1) (relationaler Operator) (Eigenschaftstag 2)_.</span><span class="sxs-lookup"><span data-stu-id="a81ae-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="a81ae-125">Die zu vergleichenden Eigenschaften müssen vom gleichen Typ sein.</span><span class="sxs-lookup"><span data-stu-id="a81ae-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="a81ae-126">Wenn Sie versuchen, Eigenschaften verschiedener Typen zu vergleichen, gibt MAPI oder der Dienstanbieter den Fehlerwert MAPI_E_TOO_COMPLEX aus der [IMAPITable-Methode](imapitableiunknown.md) zurück, an die die Struktur als Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a81ae-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="a81ae-127">Das Ergebnis einer Einschränkung des Werts einer Compare-Eigenschaft ist nicht definiert, wenn eine oder beide Eigenschaften nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a81ae-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="a81ae-128">Wenn ein Client ein wohldefiniertes Verhalten für eine solche Einschränkung erfordert und nicht sicher ist, ob die Eigenschaft vorhanden ist (z. B. ist es keine erforderliche Spalte einer Tabelle), sollte er eine **AND-Einschränkung** erstellen, um die Eigenschaftseinschränkung compare mit einer vorhandenen Einschränkung zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="a81ae-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="a81ae-129">Verwenden Sie eine [SExistRestriction-Struktur,](sexistrestriction.md) um die exist-Einschränkung und eine [SAndRestriction-Struktur](sandrestriction.md) zu definieren, um die **AND-Einschränkung zu** definieren.</span><span class="sxs-lookup"><span data-stu-id="a81ae-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="a81ae-130">Die in den **Mitgliedern ulPropTag1** und **ulPropTag2** angegebenen Eigenschaften können mehrwertig sein, wenn der Dienstanbieter sie unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a81ae-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="a81ae-131">Weitere Informationen zur Struktur und Einschränkungen **von SComparePropsRestriction** im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="a81ae-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a81ae-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a81ae-132">See also</span></span>

- [<span data-ttu-id="a81ae-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="a81ae-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="a81ae-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="a81ae-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="a81ae-135">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a81ae-135">MAPI Structures</span></span>](mapi-structures.md)

