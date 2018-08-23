---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4b05baf1f819a821da3496cc63c2b2980894efd7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575714"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="2c967-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="2c967-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="2c967-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c967-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c967-105">Gibt die Eintrags-ID der im globalen Adressbuch für den Exchange-Dienst _pEmsmdbUID_identifizierten zurück.</span><span class="sxs-lookup"><span data-stu-id="2c967-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="2c967-106">Die zurückgegebene Eintrags-ID sollte mithilfe der [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c967-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c967-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2c967-107">Header file:</span></span>  <br/> |<span data-ttu-id="2c967-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="2c967-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="2c967-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2c967-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="2c967-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="2c967-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="2c967-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2c967-111">Called by:</span></span>  <br/> |<span data-ttu-id="2c967-112">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2c967-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="2c967-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c967-113">Parameters</span></span>

 <span data-ttu-id="2c967-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="2c967-114">_pSess_</span></span>
  
> <span data-ttu-id="2c967-115">[in] Die angemeldete IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="2c967-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="2c967-116">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2c967-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="2c967-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="2c967-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="2c967-118">[in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c967-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="2c967-119">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2c967-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="2c967-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="2c967-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="2c967-121">[in] Ein Zeiger auf eine **EmsmdbUID** , die identifiziert die globale Adressliste des Exchange-Diensts abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2c967-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="2c967-122">Wenn _pEmsmdbUID_ NULL oder die UID 0 (null) ist, gibt diese Funktion die Vorgängerversion GAL von der Exchange-Dienst.</span><span class="sxs-lookup"><span data-stu-id="2c967-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="2c967-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="2c967-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="2c967-124">[out] Ein Zeiger auf die Byteanzahl des Eintrags-ID der globalen Adressliste.</span><span class="sxs-lookup"><span data-stu-id="2c967-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="2c967-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="2c967-125">_lppeid_</span></span>
  
> <span data-ttu-id="2c967-126">[out] Ein Zeiger auf die Eintrags-ID der globalen Adressliste.</span><span class="sxs-lookup"><span data-stu-id="2c967-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="2c967-127">Dies sollte mithilfe der [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c967-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

