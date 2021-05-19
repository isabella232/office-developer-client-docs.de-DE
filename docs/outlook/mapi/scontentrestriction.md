---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423664"
---
# <a name="scontentrestriction"></a><span data-ttu-id="21543-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="21543-103">SContentRestriction</span></span>
 
<span data-ttu-id="21543-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21543-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21543-105">Beschreibt eine Inhaltseinschränkung, die verwendet wird, um eine Tabellenansicht auf die Zeilen zu beschränken, die eine Spalte mit Inhalten enthalten, die mit einer Suchzeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="21543-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21543-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="21543-106">Header file:</span></span>  <br/> |<span data-ttu-id="21543-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21543-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="21543-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="21543-108">Members</span></span>

<span data-ttu-id="21543-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="21543-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="21543-110">Optionseinstellungen, die den Grad der Exaktheit definieren, den die Inhaltseinschränkung erzwingen soll, wenn Sie eine Übereinstimmung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="21543-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="21543-111">Die **unteren 16** Bit des **ulFuzzyLevel-Members** gelten für Eigenschaften vom Typ PT_BINARY und PT_STRING8 und müssen auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="21543-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="21543-112">FL_FULLSTRING: Um eine Übereinstimmung zu finden, muss die **lpProp-Suchzeichenfolge** in der eigenschaft enthalten sein, die durch **ulPropTag identifiziert wird.**</span><span class="sxs-lookup"><span data-stu-id="21543-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="21543-113">FL_PREFIX : Um eine Übereinstimmung zu finden, muss die **lpProp-Suchzeichenfolge** am Anfang der durch **ulPropTag** identifizierten Eigenschaft angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="21543-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="21543-114">Die beiden Zeichenfolgen sollten nur bis zur Länge der durch lpProp angegebenen Suchzeichenfolge **verglichen werden.**</span><span class="sxs-lookup"><span data-stu-id="21543-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="21543-115">FL_SUBSTRING: Die **lpProp-Suchzeichenfolge** muss an einer beliebigen Stelle in der durch **ulPropTag** identifizierten Eigenschaft enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="21543-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="21543-116">Die **oberen 16** Bit des **ulFuzzyLevel-Members** gelten nur für Eigenschaften vom Typ PT_STRING8 und können in beliebiger Kombination auf die folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="21543-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="21543-117">FL_IGNORECASE: Der Vergleich sollte ohne Berücksichtigung der Fälle vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="21543-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="21543-118">FL_IGNORENONSPACE: Der Vergleich sollte Unicode-definierte Nichtabstandszeichen, z. B. diakritische Zeichen, ignorieren.</span><span class="sxs-lookup"><span data-stu-id="21543-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="21543-119">FL_LOOSE: Der Vergleich sollte Ihnen nach Möglichkeit eine Übereinstimmung bieten, wobei die Zeichen "Case" und "Non-Spacing" ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="21543-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="21543-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="21543-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="21543-121">Eigenschaftstag, das die Zeichenfolgeneigenschaft identifiziert, die auf das Vorkommen der Suchzeichenfolge überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="21543-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="21543-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="21543-122">**lpProp**</span></span>
  
> <span data-ttu-id="21543-123">Zeiger auf eine Eigenschaftswertstruktur, die den zeichenfolgenwert enthält, der als Suchzeichenfolge verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21543-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21543-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21543-124">Remarks</span></span>

<span data-ttu-id="21543-125">Es gibt zwei Eigenschaftstags in einer **SContentRestriction-Struktur:** eines im **ulPropTag-Element** und das andere im **ulPropTag-Element** der **SPropValue-Struktur,** auf die von **lpProp** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="21543-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="21543-126">In beiden Tags erfordert MAPI nur das Eigenschaftentypfeld und ignoriert das Eigenschaftenbezeichnerfeld.</span><span class="sxs-lookup"><span data-stu-id="21543-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="21543-127">Die beiden Eigenschaftstypen müssen jedoch übereinstimmen, sonst wird der Fehlerwert MAPI_E_TOO_COMPLEX zurückgegeben, wenn die Einschränkung in einem Aufruf von [IMAPITable::Restrict](imapitable-restrict.md) oder [IMAPITable::FindRow](imapitable-findrow.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21543-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="21543-128">Die Werte FL_FULLSTRING, FL_PREFIX und FL_SUBSTRING schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="21543-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="21543-129">Es kann nur einer von ihnen festgelegt werden, und eine davon muss festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="21543-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="21543-130">Ihre Bedeutungen sind festgelegt, und der Anbieter muss sie genau wie definiert implementieren.</span><span class="sxs-lookup"><span data-stu-id="21543-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="21543-131">Der Anbieter sollte MAPI_E_TOO_COMPLEX zurückgeben, wenn er diese Werte nicht unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="21543-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="21543-132">Die Werte FL_IGNORECASE, FL_IGNORENONSPACE und FL_LOOSE sind unabhängig.</span><span class="sxs-lookup"><span data-stu-id="21543-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="21543-133">Zwischen null und allen drei kann festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="21543-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="21543-134">Ihre Definitionen werden nur als Richtlinie bereitgestellt, und der Anbieter kann seine eigene spezifische Bedeutung jedes Flags implementieren.</span><span class="sxs-lookup"><span data-stu-id="21543-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="21543-135">Der Anbieter sollte keine Fehleranzeige zurückgeben, wenn er keine Implementierung eines angegebenen Flags besitzt.</span><span class="sxs-lookup"><span data-stu-id="21543-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="21543-136">Das Ergebnis einer Für eine Eigenschaft auferlegten Inhaltseinschränkung ist nicht definiert, wenn die Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="21543-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="21543-137">Wenn ein Client für eine solche Einschränkung ein definiertes Verhalten erfordert und nicht sicher ist, ob die Eigenschaft vorhanden ist, sollte er keine erforderliche Spalte einer Tabelle erstellen und eine **AND-Einschränkung** erstellen, um die Inhaltseinschränkung mit einer vorhandenen Einschränkung zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="21543-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="21543-138">Verwenden Sie eine [SExistRestriction-Struktur,](sexistrestriction.md) um die exist-Einschränkung und eine [SAndRestriction-Struktur](sandrestriction.md) zu definieren, um die **AND-Einschränkung zu** definieren.</span><span class="sxs-lookup"><span data-stu-id="21543-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="21543-139">Weitere Informationen zur Struktur und Einschränkungen **von SContentRestriction** im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="21543-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="21543-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21543-140">See also</span></span>

- [<span data-ttu-id="21543-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="21543-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="21543-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="21543-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="21543-143">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="21543-143">MAPI Structures</span></span>](mapi-structures.md)

