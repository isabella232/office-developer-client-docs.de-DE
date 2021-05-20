---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430609"
---
# <a name="scommentrestriction"></a><span data-ttu-id="0aa48-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="0aa48-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="0aa48-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aa48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aa48-105">Beschreibt eine Kommentareinschränkung, die zum Kommentieren einer Einschränkung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0aa48-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0aa48-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0aa48-106">Header file:</span></span>  <br/> |<span data-ttu-id="0aa48-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0aa48-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="0aa48-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="0aa48-108">Members</span></span>

 <span data-ttu-id="0aa48-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0aa48-109">**cValues**</span></span>
  
> <span data-ttu-id="0aa48-110">Anzahl der Eigenschaftswerte im Array, auf das das **lpProp-Element verweist.**</span><span class="sxs-lookup"><span data-stu-id="0aa48-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="0aa48-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="0aa48-111">**lpRes**</span></span>
  
> <span data-ttu-id="0aa48-112">Zeiger auf eine [SRestriction-Struktur.](srestriction.md)</span><span class="sxs-lookup"><span data-stu-id="0aa48-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="0aa48-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="0aa48-113">**lpProp**</span></span>
  
> <span data-ttu-id="0aa48-114">Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die jeweils das Eigenschaftstag und den Wert für eine benannte Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="0aa48-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0aa48-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0aa48-115">Remarks</span></span>

<span data-ttu-id="0aa48-116">Die **SCommentRestriction-Struktur** ordnet ein Objekt einem Satz benannter Eigenschaften zu.</span><span class="sxs-lookup"><span data-stu-id="0aa48-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="0aa48-117">Kommentareinschränkungen sind im Gegensatz zu anderen Einschränkungen, da sie nicht ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="0aa48-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="0aa48-118">Das heißt, sie werden von der [IMAPITable::Restrict-Methode](imapitable-restrict.md) ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0aa48-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="0aa48-119">Es gibt keine Auswirkungen auf die Zeilen, die von der [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) zurückgegeben werden, nachdem ein **IMAPITable::Restrict-Aufruf** ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0aa48-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="0aa48-120">Die **SCommentRestriction-Struktur** kann verwendet werden, um anwendungsspezifische Informationen mit einer Einschränkung zu speichern, wenn sie auf dem Datenträger gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0aa48-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="0aa48-121">Beispielsweise kann ein Client, der den Namen einer benannten Eigenschaft, die in einer Eigenschaftseinschränkung verwendet wird, speichern, dies in einer **SCommentRestriction-Struktur** tun.</span><span class="sxs-lookup"><span data-stu-id="0aa48-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="0aa48-122">Das Speichern eines Eigenschaftennamens ist in einer Eigenschaftseinschränkung nicht möglich, da die zugeordnete [SPropertyRestriction-Struktur](spropertyrestriction.md) nur das Eigenschaftstag enthält.</span><span class="sxs-lookup"><span data-stu-id="0aa48-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="0aa48-123">Weitere Informationen zur Struktur und Einschränkungen **von SCommentRestriction** im Allgemeinen finden Sie unter [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="0aa48-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0aa48-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0aa48-124">See also</span></span>



[<span data-ttu-id="0aa48-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0aa48-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="0aa48-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="0aa48-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="0aa48-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="0aa48-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="0aa48-128">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0aa48-128">MAPI Structures</span></span>](mapi-structures.md)

