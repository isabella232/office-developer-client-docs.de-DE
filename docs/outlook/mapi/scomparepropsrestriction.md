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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6ebc4e9cbc79a71a91f1f2f3eec0d40de979ab18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795455"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="1ba63-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="1ba63-103">SComparePropsRestriction</span></span>

<span data-ttu-id="1ba63-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ba63-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ba63-105">Wird eine eigenschaftseinschränkung vergleichen, die getestet werden zwei Eigenschaften mit einem relationalen Operator beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1ba63-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ba63-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1ba63-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ba63-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ba63-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="1ba63-108">Members</span><span class="sxs-lookup"><span data-stu-id="1ba63-108">Members</span></span>

<span data-ttu-id="1ba63-109">**RelOp-Element**</span><span class="sxs-lookup"><span data-stu-id="1ba63-109">**relop**</span></span>
  
> <span data-ttu-id="1ba63-110">Relationale Operator, der zum Vergleichen von zwei Eigenschaften verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ba63-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="1ba63-111">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1ba63-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="1ba63-112">RELOP_GE: Der Vergleich wird basierend auf dem ersten Wert größer oder gleich vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="1ba63-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="1ba63-113">RELOP_GT: Der Vergleich wird basierend auf einen höheren Wert für die erste vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="1ba63-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="1ba63-114">RELOP_LE: Der Vergleich wird basierend auf dem ersten Wert kleiner oder gleich vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="1ba63-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="1ba63-115">RELOP_LT: Der Vergleich wird basierend auf einen kleineren Wert des ersten vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="1ba63-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="1ba63-116">RELOP_NE: Der Vergleich basierend auf Werten mit ungleicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1ba63-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="1ba63-117">RELOP_RE: Der Vergleich basierend auf wie Werte (reguläre Ausdrücke) erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1ba63-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="1ba63-118">RELOP_EQ: Der Vergleich wird basierend auf gleich große Werte vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="1ba63-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="1ba63-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="1ba63-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="1ba63-120">Eigenschaftentag der Eigenschaft verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ba63-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="1ba63-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="1ba63-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="1ba63-122">Eigenschaftentag der zweiten-Eigenschaft, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="1ba63-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ba63-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ba63-123">Remarks</span></span>

<span data-ttu-id="1ba63-124">Die Reihenfolge der Vergleich ist _(Eigenschafts-Tag (1) (relationalen Operator) (Eigenschaftentag 2)_.</span><span class="sxs-lookup"><span data-stu-id="1ba63-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="1ba63-125">Die Eigenschaften, die verglichen werden müssen den gleichen Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1ba63-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="1ba63-126">Bei dem Versuch, Eigenschaften mit unterschiedlichen Typen verglichen wird MAPI oder den Dienstanbieter den Fehlerwert MAPI_E_TOO_COMPLEX [IMAPITable](imapitableiunknown.md) -Methode zurückgegeben, der die Struktur als Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="1ba63-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="1ba63-127">Das Ergebnis der Einschränkung Wert Compare-Eigenschaft ist nicht definiert, wenn eine oder beide der Eigenschaften nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1ba63-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="1ba63-128">Wenn ein Client eindeutig definiertes Verhalten für eine solche Beschränkung erfordert und sich nicht sicher ist, ob die Eigenschaft vorhanden ist (beispielsweise, es ist keine erforderliche Spalte einer Tabelle) sollten sie eine Einschränkung **und** zum Teilnehmen an der eigenschaftseinschränkung vergleichen mit einen vorhanden erstellen Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="1ba63-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="1ba63-129">Verwenden Sie eine [SExistRestriction](sexistrestriction.md) -Struktur, um die Einschränkung vorhanden und eine [SAndRestriction](sandrestriction.md) -Struktur so definieren Sie die Einschränkung **und** definieren.</span><span class="sxs-lookup"><span data-stu-id="1ba63-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="1ba63-130">Die Member **ulPropTag1** und **ulPropTag2** angegebenen Eigenschaften können mit mehreren Werten sein, wenn der Dienstanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ba63-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="1ba63-131">Weitere Informationen zu den **SComparePropsRestriction** Struktur und Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="1ba63-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1ba63-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ba63-132">See also</span></span>

- [<span data-ttu-id="1ba63-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="1ba63-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="1ba63-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="1ba63-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="1ba63-135">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1ba63-135">MAPI Structures</span></span>](mapi-structures.md)
