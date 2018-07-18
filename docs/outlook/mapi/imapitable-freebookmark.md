---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d6621e2bcd7831016efd7ac43f93ef83aaf41c29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792461"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="92412-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="92412-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="92412-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="92412-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="92412-105">Gibt ein Lesezeichen zugeordneten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="92412-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="92412-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="92412-106">Parameters</span></span>

 <span data-ttu-id="92412-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="92412-107">_bkPosition_</span></span>
  
> <span data-ttu-id="92412-108">[in] Die Textmarke freigegeben werden, werden durch Aufrufen der [IMAPITable::CreateBookmark](imapitable-createbookmark.md) -Methode erstellt.</span><span class="sxs-lookup"><span data-stu-id="92412-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="92412-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="92412-109">Return value</span></span>

<span data-ttu-id="92412-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="92412-110">S_OK</span></span> 
  
> <span data-ttu-id="92412-111">Die Textmarke wurde erfolgreich freigegeben.</span><span class="sxs-lookup"><span data-stu-id="92412-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="92412-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="92412-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="92412-113">Die angegebene Textmarke ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="92412-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92412-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92412-114">Remarks</span></span>

<span data-ttu-id="92412-115">Die **IMAPITable::FreeBookmark** -Methode gibt eine Textmarke, die nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="92412-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="92412-116">Die Textmarke ist nach diesem Aufruf nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="92412-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="92412-117">Wenn eine Tabelle aus dem Speicher freigegeben wird, werden dessen zugehörige Lesezeichen ebenfalls freigegeben.</span><span class="sxs-lookup"><span data-stu-id="92412-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="92412-118">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="92412-118">Notes to implementers</span></span>

<span data-ttu-id="92412-119">Wenn der Aufrufer eine der drei vordefinierten Textmarken im Parameter _BkPosition_ übergibt, ignorieren Sie die Anforderung, und geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="92412-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92412-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92412-120">See also</span></span>



[<span data-ttu-id="92412-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="92412-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="92412-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="92412-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

