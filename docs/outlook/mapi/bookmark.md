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
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318039"
---
# <a name="bookmark"></a><span data-ttu-id="6c084-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="6c084-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="6c084-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c084-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c084-105">Definiert Lesezeichen Daten für die Erinnerung an eine Position in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c084-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c084-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6c084-106">Header file:</span></span>  <br/> |<span data-ttu-id="6c084-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6c084-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6c084-108">Verwandte Methoden:</span><span class="sxs-lookup"><span data-stu-id="6c084-108">Related methods:</span></span>  <br/> |<span data-ttu-id="6c084-109">[IMAPITable:: CreateBookMark](imapitable-createbookmark.md) [IMAPITable:: FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="6c084-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="6c084-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c084-110">Remarks</span></span>

<span data-ttu-id="6c084-111">MAPI definiert drei Lesezeichen, die wie folgt aufgelistet sind:</span><span class="sxs-lookup"><span data-stu-id="6c084-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="6c084-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="6c084-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="6c084-113">Merkt sich die Anfangsposition der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c084-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="6c084-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="6c084-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="6c084-115">Merkt sich die aktuelle Position der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c084-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="6c084-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="6c084-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="6c084-117">Merkt sich die Endposition der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c084-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="6c084-118">Clients können andere Lesezeichen zum erinnern anderer Tabellenpositionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="6c084-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="6c084-119">Textmarken sind nur gültig, wenn die Tabelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="6c084-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="6c084-120">Clients müssen alle Lesezeichen freigeben, die Sie erstellt haben, bevor Sie die zugeordnete Tabelle schließen.</span><span class="sxs-lookup"><span data-stu-id="6c084-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c084-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c084-121">See also</span></span>



[<span data-ttu-id="6c084-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="6c084-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="6c084-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="6c084-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="6c084-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="6c084-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="6c084-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="6c084-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="6c084-126">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="6c084-126">MAPI Data Types</span></span>](mapi-data-types.md)

