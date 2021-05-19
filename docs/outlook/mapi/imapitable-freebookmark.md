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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409454"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="cbd8f-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="cbd8f-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="cbd8f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbd8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbd8f-105">Gibt den Speicher frei, der einer Textmarke zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cbd8f-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="cbd8f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbd8f-106">Parameters</span></span>

 <span data-ttu-id="cbd8f-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="cbd8f-107">_bkPosition_</span></span>
  
> <span data-ttu-id="cbd8f-108">[in] Das zu entfernende Lesezeichen, das durch Aufrufen der [IMAPITable::CreateBookmark-Methode erstellt](imapitable-createbookmark.md) wird.</span><span class="sxs-lookup"><span data-stu-id="cbd8f-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cbd8f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cbd8f-109">Return value</span></span>

<span data-ttu-id="cbd8f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbd8f-110">S_OK</span></span> 
  
> <span data-ttu-id="cbd8f-111">Die Textmarke wurde erfolgreich frei.</span><span class="sxs-lookup"><span data-stu-id="cbd8f-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="cbd8f-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="cbd8f-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="cbd8f-113">Die angegebene Textmarke ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cbd8f-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cbd8f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cbd8f-114">Remarks</span></span>

<span data-ttu-id="cbd8f-115">Die **IMAPITable::FreeBookmark-Methode** gibt ein Lesezeichen frei, das nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="cbd8f-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="cbd8f-116">Das Lesezeichen ist nach diesem Aufruf nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="cbd8f-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="cbd8f-117">Wenn eine Tabelle aus dem Arbeitsspeicher freigegeben wird, werden auch alle zugehörigen Lesezeichen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="cbd8f-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cbd8f-118">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="cbd8f-118">Notes to implementers</span></span>

<span data-ttu-id="cbd8f-119">Wenn der Aufrufer eine der drei vordefinierten Lesezeichen im  _bkPosition-Parameter_ übergibt, ignorieren Sie die Anforderung, und geben Sie S_OK.</span><span class="sxs-lookup"><span data-stu-id="cbd8f-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cbd8f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbd8f-120">See also</span></span>



[<span data-ttu-id="cbd8f-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="cbd8f-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="cbd8f-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbd8f-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

