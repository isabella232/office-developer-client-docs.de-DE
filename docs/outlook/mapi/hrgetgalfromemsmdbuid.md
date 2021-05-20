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
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439107"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="2dc34-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="2dc34-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="2dc34-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dc34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dc34-105">Gibt den Eintragsbezeichner des globalen Adressbuchs für den Exchange, der von _pEmsmdbUID identifiziert wurde._</span><span class="sxs-lookup"><span data-stu-id="2dc34-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="2dc34-106">Der zurückgegebene Eintragsbezeichner sollte mithilfe von [MAPIFreeBuffer freigebe.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="2dc34-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2dc34-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2dc34-107">Header file:</span></span>  <br/> |<span data-ttu-id="2dc34-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="2dc34-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="2dc34-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2dc34-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="2dc34-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="2dc34-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="2dc34-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2dc34-111">Called by:</span></span>  <br/> |<span data-ttu-id="2dc34-112">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2dc34-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="2dc34-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dc34-113">Parameters</span></span>

 <span data-ttu-id="2dc34-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="2dc34-114">_pSess_</span></span>
  
> <span data-ttu-id="2dc34-115">[in] Die angemeldete IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="2dc34-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="2dc34-116">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2dc34-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="2dc34-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="2dc34-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="2dc34-118">[in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dc34-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="2dc34-119">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2dc34-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="2dc34-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="2dc34-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="2dc34-121">[in] Ein Zeiger auf eine **emsmdbUID,** die die GAL des abzurufenden Exchange identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2dc34-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="2dc34-122">Wenn _pEmsmdbUID_ NULL oder null UID ist, ruft diese Funktion die legacy-GAL des Exchange ab.</span><span class="sxs-lookup"><span data-stu-id="2dc34-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="2dc34-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="2dc34-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="2dc34-124">[out] Ein Zeiger auf die Byteanzahl des Eintragsbezeichners der globalen Adressliste.</span><span class="sxs-lookup"><span data-stu-id="2dc34-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="2dc34-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="2dc34-125">_lppeid_</span></span>
  
> <span data-ttu-id="2dc34-126">[out] Ein Zeiger auf die Eintrags-ID der globalen Adressliste.</span><span class="sxs-lookup"><span data-stu-id="2dc34-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="2dc34-127">Dies sollte mithilfe von [MAPIFreeBuffer frei werden.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="2dc34-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

