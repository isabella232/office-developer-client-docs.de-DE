---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357855"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="4da53-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="4da53-103">SPropertyRestriction</span></span>

<span data-ttu-id="4da53-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4da53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4da53-105">Beschreibt eine Eigenschaftseinschränkung, die verwendet wird, um eine Konstante mit dem Wert einer Eigenschaft zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="4da53-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4da53-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4da53-106">Header file:</span></span>  <br/> |<span data-ttu-id="4da53-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4da53-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="4da53-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="4da53-108">Members</span></span>

<span data-ttu-id="4da53-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="4da53-109">**relop**</span></span>
  
> <span data-ttu-id="4da53-110">Relationaler Operator, der bei der Suche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4da53-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="4da53-111">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="4da53-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="4da53-112">RELOP_GE: der Vergleich erfolgt basierend auf einem größer oder gleich dem ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="4da53-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="4da53-113">RELOP_GT: der Vergleich erfolgt basierend auf einem höheren ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="4da53-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="4da53-114">RELOP_LE: der Vergleich erfolgt basierend auf einem niedrigeren oder gleichen ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="4da53-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="4da53-115">RELOP_LT: der Vergleich erfolgt basierend auf einem niedrigeren ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="4da53-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="4da53-116">RELOP_NE: der Vergleich erfolgt basierend auf ungleich Werten.</span><span class="sxs-lookup"><span data-stu-id="4da53-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="4da53-117">RELOP_RE: der Vergleich basiert auf LIKE (Regular Expression)-Werten.</span><span class="sxs-lookup"><span data-stu-id="4da53-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="4da53-118">RELOP_EQ: der Vergleich erfolgt basierend auf gleichen Werten.</span><span class="sxs-lookup"><span data-stu-id="4da53-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="4da53-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="4da53-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="4da53-120">Property-Tag, das die zu vergleichende Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4da53-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="4da53-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="4da53-121">**lpProp**</span></span>
  
> <span data-ttu-id="4da53-122">Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die den konstanten Wert enthält, der im Vergleich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4da53-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4da53-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4da53-123">Remarks</span></span>

<span data-ttu-id="4da53-124">Es gibt zwei Property-Tags in einer **SPropertyRestriction** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4da53-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="4da53-125">Eine befindet sich im **ulPropTag** -Element und die andere befindet sich im **ulPropTag** -Element der **SPropValue** -Struktur, auf die durch **lpProp**verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4da53-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="4da53-126">MAPI erfordert sowohl das Feld Eigenschafts-ID als auch das Feld Eigenschafts.</span><span class="sxs-lookup"><span data-stu-id="4da53-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="4da53-127">Die **ulPropTag** in **SPropertyRestriction** ist die Eigenschaft, die verglichen werden soll, und der **lpProp** -Zeiger des **SPropertyRestriction** auf den **ulPropTag**-Typ des **SPropValue** gibt an, wie der Members-Wert des **lpProp** Union werden interpretiert.</span><span class="sxs-lookup"><span data-stu-id="4da53-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="4da53-128">Die beiden Eigenschaftentypen müssen übereinstimmen, andernfalls wird der Fehlerwert MAPI_E_TOO_COMPLEX zurückgegeben, wenn die Einschränkung in einem Aufruf von [IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable:: FindRow](imapitable-findrow.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4da53-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="4da53-129">Die Vergleichsreihenfolge ist _(Eigenschaftswert) (relationaler Operator) (konstanter Wert)_.</span><span class="sxs-lookup"><span data-stu-id="4da53-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="4da53-130">Wenn eine Eigenschaftseinschränkung an **IMAPITable:: Restrict** oder **IMAPITable:: FindRow** übergeben wird und die Target-Eigenschaft nicht vorhanden ist, sind die Ergebnisse der Einschränkung nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4da53-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="4da53-131">Durch das Erstellen einer **and** -Einschränkung, die die Eigenschaftseinschränkung mit einer **exist** -Einschränkung verknüpft, kann ein Aufrufer exakte Ergebnisse garantieren.</span><span class="sxs-lookup"><span data-stu-id="4da53-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="4da53-132">Verwenden Sie eine [SExistRestriction](sexistrestriction.md) -Struktur, um die **exist** -Einschränkung und eine [SAndRestriction](sandrestriction.md) -Struktur zum Definieren der **und-** Einschränkung zu definieren.</span><span class="sxs-lookup"><span data-stu-id="4da53-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="4da53-133">Mehrwertige Eigenschaftstags können in Eigenschaftseinschränkungen verwendet werden, wenn der Dienstanbieter, der die Tabelle implementiert, diese unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4da53-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="4da53-134">Wenn unterstützt, mehrwertige Eigenschaftstags können verwendet werden, wo einwertige Eigenschaftstags verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4da53-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="4da53-135">Mehrwertige Eigenschaftstags können in den folgenden Methoden verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="4da53-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="4da53-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="4da53-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="4da53-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="4da53-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="4da53-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="4da53-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="4da53-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="4da53-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="4da53-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="4da53-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="4da53-141">Ein bemerkenswerter Fall, wenn die beiden Eigenschaftstags nicht übereinstimmen, ist die Beschränkung auf eine mehrwertige Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4da53-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="4da53-142">In diesem Fall muss Folgendes zutreffen.</span><span class="sxs-lookup"><span data-stu-id="4da53-142">In this case the following must be true.</span></span> <span data-ttu-id="4da53-143">> wenn der Eigenschaftentyp des **ulPropTag** von **SPropertyRestriction** den mehrwertigen Eigenschaftentyp Bit Flag MV_FLAG (0x1000) enthält, muss der Eigenschaftentyp des **ulPropTag** von **SPropValue** mit dem vorherigen minus der MV_ übereinstimmen. FLAG-Bitflags, das heißt, seine Umkehrfunktion.</span><span class="sxs-lookup"><span data-stu-id="4da53-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="4da53-144">> Wenn Sie beispielsweise eine benutzerdefinierte Zeichenfolgeneigenschaft mit mehreren Werten wie eine Kategorie mit einem Property-Tag für die Eigenschaft 0x8012101f, also PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)) einschränken möchten, wird die entsprechende **SPropertyRestriction** als folgt.</span><span class="sxs-lookup"><span data-stu-id="4da53-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="4da53-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property\`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid\`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";\`> beachten Sie, dass, wenn der Eigenschaftentyp des *\*ulPropTag** von *\*SPropValue** das MV_FLAG-Bitflags enthält, die Wahrscheinlichkeit MAPI_E_TOO_COMPLEX zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4da53-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property\`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid\`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";\`> Note that if the property type of the *\*ulPropTag** of *\*SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="4da53-146">Weitere Informationen zur **SPropertyRestriction** -Struktur finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="4da53-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4da53-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4da53-147">See also</span></span>

- [<span data-ttu-id="4da53-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="4da53-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="4da53-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="4da53-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="4da53-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4da53-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="4da53-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="4da53-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="4da53-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="4da53-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="4da53-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="4da53-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="4da53-154">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4da53-154">MAPI Structures</span></span>](mapi-structures.md)

