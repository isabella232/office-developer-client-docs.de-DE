---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 730c24a179cc6aaf8dc2068199ffc206d30156b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791898"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="70082-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="70082-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="70082-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="70082-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="70082-105">Vergleicht zwei Address Book **EntryIDs** sicher in einem Profil mehrere Exchange.</span><span class="sxs-lookup"><span data-stu-id="70082-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="70082-106">Diese Funktion ist eine Funktion Ersatz für [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="70082-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70082-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="70082-107">Header file:</span></span>  <br/> |<span data-ttu-id="70082-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="70082-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="70082-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="70082-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="70082-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="70082-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="70082-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="70082-111">Called by:</span></span>  <br/> |<span data-ttu-id="70082-112">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="70082-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="70082-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="70082-113">Parameters</span></span>

 <span data-ttu-id="70082-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="70082-114">_pmsess_</span></span>
  
> <span data-ttu-id="70082-115">[in] Die angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="70082-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="70082-116">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="70082-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="70082-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="70082-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="70082-118">[in] Ein Zeiger auf eine **EmsmdbUID** , die den Exchange-Dienst identifiziert, die die Exchange-Adressbuchanbieter enthält, die diese Funktion zum Anzeigen von Details auf die Eintrags-ID verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70082-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="70082-119">Wenn eingehende Eintrags-ID nicht um ein Exchange-Adressbuchanbieter Eintrags-ID ist, dieser Parameter wird ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="70082-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="70082-120">Wenn dieser Parameter auf NULL oder eine MAPIUID NULL ist, verhält sich diese Funktion wie [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="70082-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="70082-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="70082-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="70082-122">[in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="70082-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="70082-123">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="70082-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="70082-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="70082-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="70082-125">[in] Die Byteanzahl des ersten Eintrags-ID, die durch den Parameter _lpEntryID1_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="70082-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="70082-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="70082-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="70082-127">[in] Ein Zeiger auf die erste Eintrags-ID, die den Adresseintrag Adressbuch zum Vergleichen von eigenständigen darstellt.</span><span class="sxs-lookup"><span data-stu-id="70082-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="70082-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="70082-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="70082-129">[in] Anzahl von Bytes aus der zweite Eintrags-ID, die durch den Parameter _lpEntryID2_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="70082-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="70082-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="70082-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="70082-131">[in] Ein Zeiger auf die zweite Eintrags-ID im Vergleich verwendete darstellt, der den Adresseintrag Adressbuch, verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="70082-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="70082-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="70082-132">_ulFlags_</span></span>
  
> <span data-ttu-id="70082-133">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="70082-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="70082-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="70082-134">_lpulResult_</span></span>
  
> <span data-ttu-id="70082-135">[out] Ein Zeiger auf den Speicherort, der die Ergebnisse des Vergleichs enthält.</span><span class="sxs-lookup"><span data-stu-id="70082-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

