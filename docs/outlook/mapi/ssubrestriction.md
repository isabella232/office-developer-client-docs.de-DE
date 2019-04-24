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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336414"
---
# <a name="ssubrestriction"></a><span data-ttu-id="f4e6b-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="f4e6b-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="f4e6b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4e6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4e6b-105">Beschreibt eine Unterobjekt Einschränkung, die zum Filtern der Zeilen der Anlage-oder Empfängertabelle einer Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4e6b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f4e6b-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4e6b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f4e6b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="f4e6b-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="f4e6b-108">Members</span></span>

 <span data-ttu-id="f4e6b-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="f4e6b-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="f4e6b-110">Der Typ des untergeordneten Objekts, das als Ziel für die Einschränkung dienen soll.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="f4e6b-111">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="f4e6b-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="f4e6b-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="f4e6b-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="f4e6b-113">Wendet die Einschränkung auf die Empfängertabelle einer Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="f4e6b-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="f4e6b-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="f4e6b-115">Wendet die Einschränkung auf die Anlagentabelle einer Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="f4e6b-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="f4e6b-116">**lpRes**</span></span>
  
> <span data-ttu-id="f4e6b-117">Zeiger auf eine [SRestriction](srestriction.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f4e6b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4e6b-118">Remarks</span></span>

<span data-ttu-id="f4e6b-119">Unterobjekt Einschränkungen werden von allen Tabellen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="f4e6b-120">In der Regel werden nur Ordnerinhaltstabellen und Suchergebnisordner unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="f4e6b-121">Unterobjekt Einschränkungen werden beispielsweise verwendet, um Nachrichten zu suchen, die einen bestimmten Anlagen-oder Empfängertyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="f4e6b-122">Wenn eine Implementierung Unterobjekt Einschränkungen nicht unterstützt, wird MAPI_E_TOO_COMPLEX von den [IMAPITable:: Restrict](imapitable-restrict.md) -oder [IMAPITable:: FindRow](imapitable-findrow.md) -Methoden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="f4e6b-123">Eine allgemeine Erläuterung der Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="f4e6b-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4e6b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4e6b-124">See also</span></span>



[<span data-ttu-id="f4e6b-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="f4e6b-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="f4e6b-126">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f4e6b-126">MAPI Structures</span></span>](mapi-structures.md)

