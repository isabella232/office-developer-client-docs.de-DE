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
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418134"
---
# <a name="bookmark"></a><span data-ttu-id="89a51-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="89a51-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="89a51-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89a51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89a51-105">Definiert Lesezeichendaten zum Speichern einer Position in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="89a51-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89a51-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="89a51-106">Header file:</span></span>  <br/> |<span data-ttu-id="89a51-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89a51-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="89a51-108">Verwandte Methoden:</span><span class="sxs-lookup"><span data-stu-id="89a51-108">Related methods:</span></span>  <br/> |<span data-ttu-id="89a51-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="89a51-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="89a51-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89a51-110">Remarks</span></span>

<span data-ttu-id="89a51-111">MAPI definiert drei Lesezeichen, die wie folgt aufgeführt sind:</span><span class="sxs-lookup"><span data-stu-id="89a51-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="89a51-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="89a51-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="89a51-113">Erinnert sich an die Anfangsposition der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="89a51-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="89a51-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="89a51-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="89a51-115">Erinnert sich an die aktuelle Position der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="89a51-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="89a51-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="89a51-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="89a51-117">Erinnert sich an die Endposition der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="89a51-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="89a51-118">Clients können andere Lesezeichen zum Merken anderer Tabellenpositionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="89a51-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="89a51-119">Lesezeichen sind nur gültig, wenn die Tabelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="89a51-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="89a51-120">Clients müssen alle Lesezeichen frei, die sie erstellt haben, bevor sie die zugeordnete Tabelle schließen.</span><span class="sxs-lookup"><span data-stu-id="89a51-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89a51-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89a51-121">See also</span></span>



[<span data-ttu-id="89a51-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="89a51-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="89a51-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="89a51-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="89a51-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="89a51-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="89a51-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="89a51-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="89a51-126">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="89a51-126">MAPI Data Types</span></span>](mapi-data-types.md)

