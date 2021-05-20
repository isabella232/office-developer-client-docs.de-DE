---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436433"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="be337-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="be337-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="be337-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be337-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be337-105">Vergleicht zwei **AdressbucheintragIDs** sicher in einem Multiple Exchange Profil.</span><span class="sxs-lookup"><span data-stu-id="be337-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="be337-106">Diese Funktion ist eine Ersetzungsfunktion für [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="be337-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be337-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="be337-107">Header file:</span></span>  <br/> |<span data-ttu-id="be337-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="be337-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="be337-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="be337-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="be337-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="be337-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="be337-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="be337-111">Called by:</span></span>  <br/> |<span data-ttu-id="be337-112">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="be337-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="be337-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="be337-113">Parameters</span></span>

 <span data-ttu-id="be337-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="be337-114">_pmsess_</span></span>
  
> <span data-ttu-id="be337-115">[in] Die angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="be337-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="be337-116">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="be337-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="be337-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="be337-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="be337-118">[in] Ein Zeiger auf eine **emsmdbUID,** die den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, den diese Funktion verwenden soll, um Details zur Eintrags-ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be337-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="be337-119">Wenn der Bezeichner für eingehende Eingaben kein eintragsbezeichner Exchange Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="be337-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="be337-120">Wenn dieser Parameter NULL oder null MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="be337-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="be337-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="be337-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="be337-122">[in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be337-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="be337-123">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="be337-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="be337-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="be337-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="be337-125">[in] Die Byteanzahl des ersten Eintragsbezeichners, der durch den  _lpEntryID1-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="be337-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="be337-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="be337-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="be337-127">[in] Ein Zeiger auf den ersten Eintragsbezeichner, der den zu vergleichende Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="be337-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="be337-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="be337-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="be337-129">[in] Die Byteanzahl des zweiten Eintragsbezeichners, der durch den  _lpEntryID2-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="be337-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="be337-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="be337-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="be337-131">[in] Ein Zeiger auf den zweiten Eintragsbezeichner, der im Vergleich verwendet wird und den zu vergleichende Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="be337-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="be337-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be337-132">_ulFlags_</span></span>
  
> <span data-ttu-id="be337-133">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="be337-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="be337-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="be337-134">_lpulResult_</span></span>
  
> <span data-ttu-id="be337-135">[out] Ein Zeiger auf die Position, die die Ergebnisse des Vergleichs enthält.</span><span class="sxs-lookup"><span data-stu-id="be337-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

