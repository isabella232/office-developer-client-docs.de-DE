---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8f5f3bc454e18b1dbab434fc1b7cc094b0d6a360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791529"
---
# <a name="bookmark"></a><span data-ttu-id="79f08-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="79f08-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="79f08-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79f08-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79f08-105">Definiert die Textmarken Daten zum Erinnern an einer Position in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="79f08-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79f08-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="79f08-106">Header file:</span></span>  <br/> |<span data-ttu-id="79f08-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79f08-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="79f08-108">Zusammenhängenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="79f08-108">Related methods:</span></span>  <br/> |<span data-ttu-id="79f08-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="79f08-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="79f08-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79f08-110">Remarks</span></span>

<span data-ttu-id="79f08-111">MAPI sind drei Textmarken, wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="79f08-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="79f08-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="79f08-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="79f08-113">Speichert die Anfangsposition der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="79f08-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="79f08-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="79f08-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="79f08-115">Speichert die aktuelle Position in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="79f08-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="79f08-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="79f08-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="79f08-117">Speichert die Endposition der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="79f08-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="79f08-118">Clients können weitere Textmarken zum Erinnern an andere Positionen Tabelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="79f08-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="79f08-119">Textmarken sind nur ab, wenn die Tabelle geöffnet ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="79f08-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="79f08-120">Clients müssen Textmarken frei, die sie vor dem Schließen der verknüpften Tabelle erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="79f08-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79f08-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79f08-121">See also</span></span>



[<span data-ttu-id="79f08-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="79f08-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="79f08-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="79f08-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="79f08-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="79f08-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="79f08-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="79f08-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="79f08-126">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="79f08-126">MAPI Data Types</span></span>](mapi-data-types.md)

