---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406325"
---
# <a name="ssubrestriction"></a><span data-ttu-id="4989f-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="4989f-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="4989f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4989f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4989f-105">Beschreibt eine Unterobjekteinschränkung, die zum Filtern der Zeilen der Anlage oder Empfängertabelle einer Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4989f-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4989f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4989f-106">Header file:</span></span>  <br/> |<span data-ttu-id="4989f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4989f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="4989f-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="4989f-108">Members</span></span>

 <span data-ttu-id="4989f-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="4989f-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="4989f-110">Typ des Unterobjekts, das als Ziel für die Einschränkung dienen soll.</span><span class="sxs-lookup"><span data-stu-id="4989f-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="4989f-111">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4989f-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="4989f-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="4989f-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="4989f-113">Wenden Sie die Einschränkung auf die Empfängertabelle einer Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="4989f-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="4989f-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="4989f-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="4989f-115">Wenden Sie die Einschränkung auf die Anlagentabelle einer Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="4989f-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="4989f-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="4989f-116">**lpRes**</span></span>
  
> <span data-ttu-id="4989f-117">Zeiger auf eine [SRestriction-Struktur.](srestriction.md)</span><span class="sxs-lookup"><span data-stu-id="4989f-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4989f-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4989f-118">Remarks</span></span>

<span data-ttu-id="4989f-119">Unterobjekteinschränkungen werden nicht von allen Tabellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4989f-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="4989f-120">In der Regel werden sie nur von Ordnerinhaltstabellen und Suchergebnissen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4989f-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="4989f-121">Beispielsweise werden Unterobjekteinschränkungen verwendet, um eine Nachricht mit einem bestimmten Anlagen- oder Empfängertyp zu finden.</span><span class="sxs-lookup"><span data-stu-id="4989f-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="4989f-122">Wenn eine Implementierung keine Unterobjekteinschränkungen unterstützt, gibt sie MAPI_E_TOO_COMPLEX [der imAPITable::Restrict-](imapitable-restrict.md) oder [IMAPITable::FindRow-Methoden](imapitable-findrow.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="4989f-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="4989f-123">Eine allgemeine Diskussion über die Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="4989f-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4989f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4989f-124">See also</span></span>



[<span data-ttu-id="4989f-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="4989f-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="4989f-126">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4989f-126">MAPI Structures</span></span>](mapi-structures.md)

