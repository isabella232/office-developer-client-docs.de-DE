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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 34177aee48adad7eecb40836a247705fc22d2a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795463"
---
# <a name="scontentrestriction"></a><span data-ttu-id="af835-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="af835-103">SContentRestriction</span></span>
 
<span data-ttu-id="af835-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af835-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af835-105">Beschreibt eine Content Einschränkung, die verwendet wird, um einer Tabellenansicht, um nur die Zeilen zu begrenzen, die eine Spalte mit eine Suchzeichenfolge übereinstimmenden Inhalt enthalten.</span><span class="sxs-lookup"><span data-stu-id="af835-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af835-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="af835-106">Header file:</span></span>  <br/> |<span data-ttu-id="af835-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af835-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="af835-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="af835-108">Members</span></span>

<span data-ttu-id="af835-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="af835-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="af835-110">Einstellungen für die Option definieren Sie die Ebene der Webseitenentwicklung, die Content erzwingen sollten, wenn Sie nach einer Übereinstimmung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="af835-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="af835-111">Die **unteren 16 Bit** des Elements **UlFuzzyLevel** gelten für Eigenschaften vom Typ PT_BINARY und PT_STRING8 und muss auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="af835-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="af835-112">FL_FULLSTRING: Um übereinstimmen, muss die **LpProp** zu suchende Zeichenfolge in der Eigenschaft identifizierten **UlPropTag**befinden.</span><span class="sxs-lookup"><span data-stu-id="af835-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="af835-113">FL_PREFIX: Entsprechend, muss die Suchzeichenfolge **LpProp** am Anfang der **UlPropTag**identifizierten-Eigenschaft angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="af835-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="af835-114">Die beiden Zeichenfolgen sollte nur bis zur Länge der Suchzeichenfolge angegeben durch **LpProp**verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="af835-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="af835-115">FL_SUBSTRING: Entsprechend, muss die Suchzeichenfolge **LpProp** an einer beliebigen Stelle in der Eigenschaft identifizierten **UlPropTag**enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="af835-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="af835-116">Die **oberen 16 Bit** des Elements **UlFuzzyLevel** gelten nur für Eigenschaften vom Typ PT_STRING8 und kann auf in beliebiger Kombination der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="af835-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="af835-117">FL_IGNORECASE: Ohne Berücksichtigung der Fall sollte der Vergleich durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af835-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="af835-118">FL_IGNORENONSPACE: Der Vergleich sollten Unicode-defined nicht-gesperrte Zeichen wie etwa diakritischen Zeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="af835-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="af835-119">FL_LOOSE: Der Vergleich, sollten Sie eine Übereinstimmung nach Möglichkeit Groß-/Kleinschreibung und nicht-gesperrte Zeichen ignorieren verfügen.</span><span class="sxs-lookup"><span data-stu-id="af835-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="af835-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="af835-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="af835-121">Eigenschafts-Tag, identifiziert der Zeichenfolgeneigenschaft nach Vorkommen der Suchzeichenfolge überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="af835-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="af835-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="af835-122">**lpProp**</span></span>
  
> <span data-ttu-id="af835-123">Zeiger auf eine Eigenschaft-Wert-Struktur, die den Zeichenfolgenwert für die Verwendung als die zu suchende Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="af835-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af835-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af835-124">Remarks</span></span>

<span data-ttu-id="af835-125">Es gibt zwei Eigenschaftentags in eine **SContentRestriction** -Struktur: eine in das **UlPropTag** -Element, und der andere im **UlPropTag** -Member der Struktur **SPropValue** auf die **LpProp**zeigt.</span><span class="sxs-lookup"><span data-stu-id="af835-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="af835-126">In beiden Kategorien MAPI erfordert nur das Eigenschaftenfeld und das Feld für den Bezeichner ignoriert.</span><span class="sxs-lookup"><span data-stu-id="af835-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="af835-127">Jedoch müssen die beiden Eigenschaftstypen übereinstimmen, sonst den Fehlerwert MAPI_E_TOO_COMPLEX wird zurückgegeben, wenn die Einschränkung wieder in einem Aufruf von [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af835-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="af835-128">Die Werte FL_FULLSTRING, FL_PREFIX und FL_SUBSTRING schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="af835-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="af835-129">Nur eine von ihnen festgelegt werden kann, und einer von ihnen festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="af835-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="af835-130">Ihre Bedeutung behoben werden, und der Anbieter muss diese genau wie definiert implementieren.</span><span class="sxs-lookup"><span data-stu-id="af835-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="af835-131">Der Anbieter sollte MAPI_E_TOO_COMPLEX zurückgegeben, wenn diese Werte unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="af835-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="af835-132">Die Werte FL_IGNORECASE, FL_IGNORENONSPACE und FL_LOOSE sind unabhängig.</span><span class="sxs-lookup"><span data-stu-id="af835-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="af835-133">An einer beliebigen Stelle kann zwischen 0 (null), um alle drei festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="af835-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="af835-134">Ihre Definitionen als nur eine Richtlinie bereitgestellt werden, und der Anbieter kann eine eigene spezifische Bedeutung von jedes Flag implementieren.</span><span class="sxs-lookup"><span data-stu-id="af835-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="af835-135">Der Anbieter sollte keine Fehler weist darauf hin zurück, wenn es keine Implementierung eines angegebenen Flags vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af835-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="af835-136">Das Ergebnis der Inhalt beschränkt gegen eine Eigenschaft ist nicht definiert, wenn die Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af835-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="af835-137">Wenn ein Client eindeutig definiertes Verhalten für eine solche Beschränkung erfordert und nicht sicher ist, ob die Eigenschaft beispielsweise vorhanden ist, sie keine erforderliche Spalte einer Tabelle ist, sollten sie eine Einschränkung **und** zum Beitreten der Content Beschränkung mit einer Einschränkung vorhanden erstellen.</span><span class="sxs-lookup"><span data-stu-id="af835-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="af835-138">Verwenden Sie eine [SExistRestriction](sexistrestriction.md) -Struktur, um die Einschränkung vorhanden und eine [SAndRestriction](sandrestriction.md) -Struktur so definieren Sie die Einschränkung **und** definieren.</span><span class="sxs-lookup"><span data-stu-id="af835-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="af835-139">Weitere Informationen zu den **SContentRestriction** Struktur und Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="af835-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af835-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af835-140">See also</span></span>

- [<span data-ttu-id="af835-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="af835-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="af835-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="af835-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="af835-143">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="af835-143">MAPI Structures</span></span>](mapi-structures.md)

