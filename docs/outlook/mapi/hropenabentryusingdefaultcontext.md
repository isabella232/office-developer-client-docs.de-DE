---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 74660de551d43c589cb903b5c3852136f2f18269
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791930"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="20a60-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="20a60-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="20a60-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20a60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20a60-105">Führt die gleiche Funktion wie [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , mit der Ausnahme, dass es der Vorgängerversion **EmsmdbUID** als _pEmsmdbUID_ -Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="20a60-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="20a60-106">Verwenden Sie diese Funktion nicht, es sei denn, Sie nicht die richtige **EmsmdbUID** für den Aufruf von [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)beziehen können.</span><span class="sxs-lookup"><span data-stu-id="20a60-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20a60-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="20a60-107">Header file:</span></span>  <br/> |<span data-ttu-id="20a60-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="20a60-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="20a60-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="20a60-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="20a60-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="20a60-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="20a60-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="20a60-111">Called by:</span></span>  <br/> |<span data-ttu-id="20a60-112">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="20a60-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="20a60-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="20a60-113">Parameters</span></span>

 <span data-ttu-id="20a60-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="20a60-114">_pmsess_</span></span>
  
> <span data-ttu-id="20a60-115">[in] Die angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="20a60-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="20a60-116">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="20a60-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="20a60-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="20a60-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="20a60-118">[in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="20a60-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="20a60-119">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="20a60-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="20a60-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="20a60-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="20a60-121">[in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="20a60-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="20a60-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="20a60-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="20a60-123">[in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.</span><span class="sxs-lookup"><span data-stu-id="20a60-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="20a60-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="20a60-124">_lpInterface_</span></span>
  
> <span data-ttu-id="20a60-125">[in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, die den Eintrag open Zugriff auf verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20a60-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="20a60-126">Übergeben von NULL gibt die standard-Schnittstelle des Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="20a60-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="20a60-127">Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="20a60-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="20a60-128">Wird für es Verteilerlisten [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container ist [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="20a60-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="20a60-129">Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen.</span><span class="sxs-lookup"><span data-stu-id="20a60-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="20a60-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20a60-130">_ulFlags_</span></span>
  
> <span data-ttu-id="20a60-131">[in] Eine Bitmaske aus Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="20a60-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="20a60-132">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="20a60-132">The following flags can be set:</span></span>
    
<span data-ttu-id="20a60-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="20a60-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="20a60-134">Fordert, dass der Eintrag mit den maximalen zulässigen Netzwerk- und Client Berechtigungen geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="20a60-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="20a60-135">Wenn der Client über Lese- und Schreibberechtigungen, versucht der Adressbuchanbieter beispielsweise, öffnen Sie den Eintrag mit Lese- und Schreibberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="20a60-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="20a60-136">Der Client kann die Zugriffsebene abzurufen, die durch Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode des Eintrags öffnen und das Abrufen der Eigenschaft PR_ACCESS_LEVEL (PidTagAccessLevel) gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="20a60-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="20a60-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="20a60-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="20a60-138">Verwendet nur das Offlineadressbuch namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="20a60-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="20a60-139">Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="20a60-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="20a60-140">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="20a60-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="20a60-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="20a60-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="20a60-142">Ermöglicht den Anruf, potenziell erfolgreich ausgeführt werden kann, bevor der Eintrag vollständig geöffnet und verfügbar ist, dass dies, dass nachfolgende Aufrufe von den Eintrag möglicherweise einen Fehler zurück, ist.</span><span class="sxs-lookup"><span data-stu-id="20a60-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="20a60-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="20a60-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="20a60-144">Verwendet nur die globale Adressliste namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="20a60-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="20a60-145">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="20a60-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="20a60-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="20a60-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="20a60-147">Anforderungen, denen mit der Eintrag geöffnet werden Lese- und Schreibberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="20a60-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="20a60-148">Da die Einträge in der Standardeinstellung mit schreibgeschützten Zugriff geöffnet sind, sollte Clients nicht davon ausgehen, das Lesen und schreiben, dass die Berechtigung erteilt wurde, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="20a60-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="20a60-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="20a60-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="20a60-150">Das Offlineadressbuch wird nicht zum Ausführen von namensauflösung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20a60-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="20a60-151">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="20a60-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="20a60-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="20a60-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="20a60-153">[out] Ein Zeiger auf den Typ des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="20a60-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="20a60-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="20a60-154">_lppUnk_</span></span>
  
> <span data-ttu-id="20a60-155">[out] Ein Zeiger auf einen Zeiger des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="20a60-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

