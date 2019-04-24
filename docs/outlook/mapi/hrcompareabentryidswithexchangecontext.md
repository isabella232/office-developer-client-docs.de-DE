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
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348076"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="a0c6a-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="a0c6a-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="a0c6a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0c6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0c6a-105">Vergleicht zwei Adressbuch **entryIDs** sicher in einem Exchange-Profil.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="a0c6a-106">Diese Funktion ist eine Ersatzfunktion für [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="a0c6a-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0c6a-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a0c6a-107">Header file:</span></span>  <br/> |<span data-ttu-id="a0c6a-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="a0c6a-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a0c6a-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a0c6a-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="a0c6a-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="a0c6a-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="a0c6a-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a0c6a-111">Called by:</span></span>  <br/> |<span data-ttu-id="a0c6a-112">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a0c6a-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a0c6a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0c6a-113">Parameters</span></span>

 <span data-ttu-id="a0c6a-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="a0c6a-114">_pmsess_</span></span>
  
> <span data-ttu-id="a0c6a-115">in Der angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="a0c6a-116">Er darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a0c6a-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="a0c6a-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="a0c6a-118">in Ein Zeiger auf ein **emsmdbUID** , das den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, den diese Funktion verwenden sollte, um Details zur Eintrags-ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="a0c6a-119">Wenn die ID des eingehenden Eintrags kein Exchange-Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D ails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="a0c6a-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="a0c6a-120">Wenn dieser Parameter NULL oder eine NULL-MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D ails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="a0c6a-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="a0c6a-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="a0c6a-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="a0c6a-122">in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="a0c6a-123">Er darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a0c6a-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="a0c6a-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="a0c6a-125">in Die Bytezahl des ersten Eintrags-Bezeichners, der durch den _lpEntryID1_ -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="a0c6a-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="a0c6a-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="a0c6a-127">in Ein Zeiger auf die erste Eintrags-ID, die den zu vergleichenden Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="a0c6a-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="a0c6a-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="a0c6a-129">in Die Bytezahl der zweiten Eintrags-ID, die durch den _lpEntryID2_ -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="a0c6a-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="a0c6a-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="a0c6a-131">in Ein Zeiger auf die zweite Eintrags-ID im Vergleich, die den zu vergleichenden Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="a0c6a-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0c6a-132">_ulFlags_</span></span>
  
> <span data-ttu-id="a0c6a-133">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a0c6a-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="a0c6a-134">_lpulResult_</span></span>
  
> <span data-ttu-id="a0c6a-135">Out Ein Zeiger auf den Speicherort, der die Ergebnisse des Vergleichs enthält.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

