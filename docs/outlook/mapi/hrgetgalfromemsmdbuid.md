---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5db1b45f42365837d7b0e7af91f859f221ff687b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791919"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="535ef-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="535ef-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="535ef-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="535ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="535ef-105">Gibt die Eintrags-ID der im globalen Adressbuch für den Exchange-Dienst _pEmsmdbUID_identifizierten zurück.</span><span class="sxs-lookup"><span data-stu-id="535ef-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="535ef-106">Die zurückgegebene Eintrags-ID sollte mithilfe der [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="535ef-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="535ef-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="535ef-107">Header file:</span></span>  <br/> |<span data-ttu-id="535ef-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="535ef-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="535ef-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="535ef-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="535ef-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="535ef-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="535ef-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="535ef-111">Called by:</span></span>  <br/> |<span data-ttu-id="535ef-112">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="535ef-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="535ef-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="535ef-113">Parameters</span></span>

 <span data-ttu-id="535ef-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="535ef-114">_pSess_</span></span>
  
> <span data-ttu-id="535ef-115">[in] Die angemeldete IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="535ef-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="535ef-116">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="535ef-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="535ef-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="535ef-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="535ef-118">[in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="535ef-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="535ef-119">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="535ef-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="535ef-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="535ef-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="535ef-121">[in] Ein Zeiger auf eine **EmsmdbUID** , die identifiziert die globale Adressliste des Exchange-Diensts abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="535ef-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="535ef-122">Wenn _pEmsmdbUID_ NULL oder die UID 0 (null) ist, gibt diese Funktion die Vorgängerversion GAL von der Exchange-Dienst.</span><span class="sxs-lookup"><span data-stu-id="535ef-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="535ef-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="535ef-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="535ef-124">[out] Ein Zeiger auf die Byteanzahl des Eintrags-ID der globalen Adressliste.</span><span class="sxs-lookup"><span data-stu-id="535ef-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="535ef-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="535ef-125">_lppeid_</span></span>
  
> <span data-ttu-id="535ef-126">[out] Ein Zeiger auf die Eintrags-ID der globalen Adressliste.</span><span class="sxs-lookup"><span data-stu-id="535ef-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="535ef-127">Dies sollte mithilfe der [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="535ef-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

