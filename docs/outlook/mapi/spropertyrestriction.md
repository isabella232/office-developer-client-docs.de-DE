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
ms.openlocfilehash: f59b0041f271010e56dda2f73d2248f133bc1325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795601"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="88576-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="88576-103">SPropertyRestriction</span></span>

<span data-ttu-id="88576-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88576-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88576-105">Beschreibt eine eigenschaftseinschränkung, die verwendet wird, eine Konstante mit dem Wert einer Eigenschaft zuordnen.</span><span class="sxs-lookup"><span data-stu-id="88576-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88576-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="88576-106">Header file:</span></span>  <br/> |<span data-ttu-id="88576-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88576-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="88576-108">Members</span><span class="sxs-lookup"><span data-stu-id="88576-108">Members</span></span>

<span data-ttu-id="88576-109">**RelOp-Element**</span><span class="sxs-lookup"><span data-stu-id="88576-109">**relop**</span></span>
  
> <span data-ttu-id="88576-110">Relationale Operator, der in der Suche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="88576-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="88576-111">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="88576-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="88576-112">RELOP_GE: Der Vergleich wird basierend auf dem ersten Wert größer oder gleich vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="88576-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="88576-113">RELOP_GT: Der Vergleich wird basierend auf einen höheren Wert für die erste vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="88576-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="88576-114">RELOP_LE: Der Vergleich wird basierend auf dem ersten Wert kleiner oder gleich vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="88576-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="88576-115">RELOP_LT: Der Vergleich wird basierend auf einen kleineren Wert des ersten vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="88576-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="88576-116">RELOP_NE: Der Vergleich basierend auf Werten mit ungleicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="88576-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="88576-117">RELOP_RE: Der Vergleich basierend auf wie Werte (reguläre Ausdrücke) erfolgt.</span><span class="sxs-lookup"><span data-stu-id="88576-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="88576-118">RELOP_EQ: Der Vergleich wird basierend auf gleich große Werte vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="88576-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="88576-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="88576-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="88576-120">Eigenschafts-Tag, identifiziert die Eigenschaft verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="88576-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="88576-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="88576-121">**lpProp**</span></span>
  
> <span data-ttu-id="88576-122">Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die den konstanten Wert enthält, der im Vergleich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88576-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="88576-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88576-123">Remarks</span></span>

<span data-ttu-id="88576-124">Es sind zwei Eigenschaftentags in eine **SPropertyRestriction** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="88576-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="88576-125">Eine im **UlPropTag** -Member ist und der andere im **UlPropTag** -Member der **SPropValue** Struktur auf **LpProp**zeigt.</span><span class="sxs-lookup"><span data-stu-id="88576-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="88576-126">MAPI erfordert das Feld für den Bezeichner und die Eigenschaft Typ dar.</span><span class="sxs-lookup"><span data-stu-id="88576-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="88576-127">Die **UlPropTag** in **SPropertyRestriction** ist der Eigenschaft abgeglichen wird und der Zeiger **LpProp** der **SPropertyRestriction** der **UlPropTag**Art der **SPropValue** gibt an, wie der Member-Wert, der die **LpProp** Union interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="88576-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="88576-128">Die beiden Eigenschaftstypen müssen übereinstimmen, sonst den Fehlerwert MAPI_E_TOO_COMPLEX wird zurückgegeben, wenn die Einschränkung wieder in einem Aufruf von [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="88576-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="88576-129">Die Reihenfolge der Vergleich ist _(Eigenschaftswert) (relationalen Operator) (Konstantenwert)_.</span><span class="sxs-lookup"><span data-stu-id="88576-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="88576-130">Wenn eine eigenschaftseinschränkung **Methode IMAPITable:: Restrict** oder **IMAPITable** übergeben wird, und die Target-Eigenschaft ist nicht vorhanden, sind die Ergebnisse der Einschränkung nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="88576-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="88576-131">Erstellen Sie eine **AND** -Einschränkung, die die eigenschaftseinschränkung mit einer Einschränkung **vorhanden** verknüpft, kann ein Anrufer genaue Ergebnisse garantiert werden.</span><span class="sxs-lookup"><span data-stu-id="88576-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="88576-132">Verwenden Sie eine [SExistRestriction](sexistrestriction.md) -Struktur, um die Einschränkung **vorhanden** und eine [SAndRestriction](sandrestriction.md) -Struktur so definieren Sie die Einschränkung **und** definieren.</span><span class="sxs-lookup"><span data-stu-id="88576-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="88576-133">Mehrwertige Eigenschaftentags können in eigenschaftseinschränkungen verwendet werden, wenn der Dienstanbieter Implementieren der Tabelle, die sie unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88576-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="88576-134">Wenn unterstützt, können mit mehreren Werten Eigenschaftentags überall eingesetzt werden, ein einwertiges Eigenschaftentags verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="88576-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="88576-135">Mehrwertige Eigenschaftentags können in den folgenden Methoden verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="88576-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="88576-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="88576-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="88576-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="88576-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="88576-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="88576-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="88576-139">SortTable</span><span class="sxs-lookup"><span data-stu-id="88576-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="88576-140">Methode IMAPITable:: Restrict</span><span class="sxs-lookup"><span data-stu-id="88576-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="88576-141">Ist ein wichtiger Fall, wenn die zwei Eigenschaftentags übereinstimmt, wird nicht durch die Beschränkung auf eine mehrwertige Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="88576-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="88576-142">In diesem Fall muss Folgendes gelten.</span><span class="sxs-lookup"><span data-stu-id="88576-142">In this case the following must be true.</span></span> <span data-ttu-id="88576-143">> Wenn der Eigenschaftstyp von der **UlPropTag** des **SPropertyRestriction** das mehrwertige Eigenschaft Typ Bitflag MV_FLAG (0 x 1000) enthält, sollte der Eigenschaftstyp von der **UlPropTag** des **SPropValue** der erste Wert minus der MV_ übereinstimmen. FLAG Bitflag, d. h., die Umkehrung.</span><span class="sxs-lookup"><span data-stu-id="88576-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="88576-144">> Beispielsweise beschränken Sie die Verwendung einer mehrwertige Zeichenfolgeneigenschaft benutzerdefinierte wie eine Kategorie mit einer Eigenschaftentag für die Eigenschaft 0x8012101f, d. h., PROP_TAG (MV_FLAG | PT_UNICODE 0x8012)), als würde die entsprechende **SPropertyRestriction** angezeigt folgt.</span><span class="sxs-lookup"><span data-stu-id="88576-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="88576-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Beachten Sie, dass der Eigenschaftstyp von der **UlPropTag** des **SPropValue** das Bitflag MV_FLAG enthält, die wahrscheinlich Rückgabe MAPI_E_TOO_COMPLEX ist.</span><span class="sxs-lookup"><span data-stu-id="88576-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="88576-146">Weitere Informationen zur Struktur **SPropertyRestriction** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="88576-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="88576-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88576-147">See also</span></span>

- [<span data-ttu-id="88576-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="88576-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="88576-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="88576-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="88576-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="88576-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="88576-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="88576-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="88576-152">IMAPITable</span><span class="sxs-lookup"><span data-stu-id="88576-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="88576-153">Methode IMAPITable:: Restrict</span><span class="sxs-lookup"><span data-stu-id="88576-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="88576-154">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="88576-154">MAPI Structures</span></span>](mapi-structures.md)

