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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: be41a9916b6b231d5715cf18fe2b0d804434f2ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594481"
---
# <a name="bookmark"></a><span data-ttu-id="8811e-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="8811e-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="8811e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8811e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8811e-105">Definiert die Textmarken Daten zum Erinnern an einer Position in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8811e-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8811e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8811e-106">Header file:</span></span>  <br/> |<span data-ttu-id="8811e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8811e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8811e-108">Zusammenhängenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="8811e-108">Related methods:</span></span>  <br/> |<span data-ttu-id="8811e-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="8811e-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="8811e-110">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="8811e-110">Remarks</span></span>

<span data-ttu-id="8811e-111">MAPI sind drei Textmarken, wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="8811e-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="8811e-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="8811e-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="8811e-113">Speichert die Anfangsposition der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="8811e-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="8811e-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="8811e-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="8811e-115">Speichert die aktuelle Position in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8811e-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="8811e-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="8811e-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="8811e-117">Speichert die Endposition der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="8811e-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="8811e-118">Clients können weitere Textmarken zum Erinnern an andere Positionen Tabelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="8811e-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="8811e-119">Textmarken sind nur ab, wenn die Tabelle geöffnet ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8811e-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="8811e-120">Clients müssen Textmarken frei, die sie vor dem Schließen der verknüpften Tabelle erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8811e-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8811e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8811e-121">See also</span></span>



[<span data-ttu-id="8811e-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="8811e-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="8811e-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="8811e-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="8811e-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="8811e-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="8811e-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="8811e-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="8811e-126">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="8811e-126">MAPI Data Types</span></span>](mapi-data-types.md)

