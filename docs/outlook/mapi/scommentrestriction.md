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
# <a name="scommentrestriction"></a><span data-ttu-id="bf3a4-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="bf3a4-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="bf3a4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf3a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf3a4-105">Beschreibt eine Kommentar Einschränkung, die zum kommentieren einer Einschränkung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf3a4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bf3a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf3a4-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bf3a4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="bf3a4-108">Members</span><span class="sxs-lookup"><span data-stu-id="bf3a4-108">Members</span></span>

 <span data-ttu-id="bf3a4-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="bf3a4-109">**cValues**</span></span>
  
> <span data-ttu-id="bf3a4-110">Die Anzahl der Eigenschaftswerte im Array, auf die durch das **lpProp** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="bf3a4-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="bf3a4-111">**lpRes**</span></span>
  
> <span data-ttu-id="bf3a4-112">Zeiger auf eine [SRestriction](srestriction.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="bf3a4-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="bf3a4-113">**lpProp**</span></span>
  
> <span data-ttu-id="bf3a4-114">Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die jeweils das Property-Tag und den Wert für eine benannte Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bf3a4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf3a4-115">Remarks</span></span>

<span data-ttu-id="bf3a4-116">Die **SCommentRestriction** -Struktur ordnet ein Objekt einer Gruppe benannter Eigenschaften zu.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="bf3a4-117">Kommentar Einschränkungen sind im Gegensatz zu anderen Einschränkungen, da Sie nicht ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="bf3a4-118">Das heißt, Sie werden von der [IMAPITable:: Restrict](imapitable-restrict.md) -Methode ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="bf3a4-119">Es gibt keine Auswirkung auf die Zeilen, die von der [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode zurückgegeben werden, nachdem ein **IMAPITable:: Restrict** -Aufruf ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="bf3a4-120">Die **SCommentRestriction** -Struktur kann verwendet werden, um anwendungsspezifische Informationen mit einer Einschränkung beizubehalten, wenn Sie auf dem Datenträger gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="bf3a4-121">Beispielsweise kann ein Client, der den Namen einer benannten Eigenschaft speichert, die in einer Eigenschaftseinschränkung verwendet wird, dies in einer **SCommentRestriction** -Struktur tun.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="bf3a4-122">Das Speichern eines Eigenschaftennamens ist in einer Eigenschaftseinschränkung nicht möglich, da die zugeordnete [SPropertyRestriction](spropertyrestriction.md) -Struktur nur das Tag der Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="bf3a4-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="bf3a4-123">Weitere Informationen zur **SCommentRestriction** -Struktur und zu Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="bf3a4-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf3a4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf3a4-124">See also</span></span>



[<span data-ttu-id="bf3a4-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bf3a4-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="bf3a4-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="bf3a4-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="bf3a4-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="bf3a4-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="bf3a4-128">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="bf3a4-128">MAPI Structures</span></span>](mapi-structures.md)

