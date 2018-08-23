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
ms.openlocfilehash: 84fb79b1922669db9c8e5d518a833a6866f11cea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589182"
---
# <a name="scommentrestriction"></a><span data-ttu-id="12d96-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="12d96-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="12d96-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12d96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12d96-105">Beschreibt eine Einschränkung Kommentar, der verwendet wird, um eine Einschränkung kommentieren.</span><span class="sxs-lookup"><span data-stu-id="12d96-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="12d96-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="12d96-106">Header file:</span></span>  <br/> |<span data-ttu-id="12d96-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12d96-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="12d96-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="12d96-108">Members</span></span>

 <span data-ttu-id="12d96-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="12d96-109">**cValues**</span></span>
  
> <span data-ttu-id="12d96-110">Anzahl-Eigenschaftswerte im Array auf den Member **LpProp** zeigt.</span><span class="sxs-lookup"><span data-stu-id="12d96-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="12d96-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="12d96-111">**lpRes**</span></span>
  
> <span data-ttu-id="12d96-112">Zeiger auf eine [SRestriction](srestriction.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="12d96-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="12d96-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="12d96-113">**lpProp**</span></span>
  
> <span data-ttu-id="12d96-114">Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, mit der Eigenschafts-Tag und der Wert für eine benannte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="12d96-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="12d96-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="12d96-115">Remarks</span></span>

<span data-ttu-id="12d96-116">Die Struktur **SCommentRestriction** ordnet ein Objekt zusammen mit einer Gruppe von benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12d96-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="12d96-117">Kommentar Einschränkungen sind im Gegensatz zu anderen Einschränkungen, da sie nicht ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="12d96-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="12d96-118">D. h., werden sie von der [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode ignoriert.</span><span class="sxs-lookup"><span data-stu-id="12d96-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="12d96-119">Es ist keine Auswirkung auf die Zeilen, die von [der QueryRows](imapitable-queryrows.md) zurückgegeben wird, nachdem eine **Methode IMAPITable:: Restrict** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="12d96-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="12d96-120">Anwendungsspezifische Informationen mit einer Einschränkung beibehalten, wenn es auf dem Datenträger gespeichert wird, kann die **SCommentRestriction** -Struktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12d96-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="12d96-121">Beispielsweise kann ein Client, speichern den Namen einer benannten Eigenschaft in einer eigenschaftseinschränkung verwendet dazu eine **SCommentRestriction** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="12d96-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="12d96-122">Speichern einen Eigenschaftennamen ist nicht möglich, in einer eigenschaftseinschränkung, da die zugeordnete [SPropertyRestriction](spropertyrestriction.md) Struktur das Eigenschafts-Tag enthält.</span><span class="sxs-lookup"><span data-stu-id="12d96-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="12d96-123">Weitere Informationen zu den **SCommentRestriction** Struktur und Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="12d96-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12d96-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12d96-124">See also</span></span>



[<span data-ttu-id="12d96-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="12d96-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="12d96-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="12d96-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="12d96-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="12d96-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="12d96-128">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="12d96-128">MAPI Structures</span></span>](mapi-structures.md)

