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
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434340"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="338dd-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="338dd-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="338dd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="338dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="338dd-105">Führt dieselbe Funktion wie [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) aus, mit der Ausnahme, dass der ältere **emsmdbUID** als  _pEmsmdbUID-Parameter verwendet_ wird.</span><span class="sxs-lookup"><span data-stu-id="338dd-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="338dd-106">Verwenden Sie diese Funktion nur, wenn Sie die richtige **emsmdbUID** für den Aufruf von [HrOpenABEntryWithExchangeContext nicht abrufen können.](hropenabentrywithexchangecontext.md)</span><span class="sxs-lookup"><span data-stu-id="338dd-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="338dd-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="338dd-107">Header file:</span></span>  <br/> |<span data-ttu-id="338dd-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="338dd-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="338dd-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="338dd-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="338dd-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="338dd-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="338dd-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="338dd-111">Called by:</span></span>  <br/> |<span data-ttu-id="338dd-112">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="338dd-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="338dd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="338dd-113">Parameters</span></span>

 <span data-ttu-id="338dd-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="338dd-114">_pmsess_</span></span>
  
> <span data-ttu-id="338dd-115">[in] Die angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="338dd-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="338dd-116">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="338dd-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="338dd-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="338dd-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="338dd-118">[in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="338dd-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="338dd-119">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="338dd-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="338dd-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="338dd-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="338dd-121">[in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="338dd-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="338dd-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="338dd-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="338dd-123">[in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="338dd-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="338dd-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="338dd-124">_lpInterface_</span></span>
  
> <span data-ttu-id="338dd-125">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="338dd-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="338dd-126">Durch Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="338dd-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="338dd-127">Für Messagingbenutzer ist die Standardschnittstelle [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="338dd-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="338dd-128">Für Verteilerlisten ist [IDistList : IMAPIContainer](idistlistimapicontainer.md)und für Container [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="338dd-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="338dd-129">Anrufer können  _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen.</span><span class="sxs-lookup"><span data-stu-id="338dd-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="338dd-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="338dd-130">_ulFlags_</span></span>
  
> <span data-ttu-id="338dd-131">[in] Eine Bitmaske mit Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="338dd-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="338dd-132">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="338dd-132">The following flags can be set:</span></span>
    
<span data-ttu-id="338dd-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="338dd-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="338dd-134">Fordert an, dass der Eintrag mit den maximal zulässigen Netzwerk- und Clientberechtigungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="338dd-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="338dd-135">Wenn der Client beispielsweise über Lese- und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese- und Schreibberechtigung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="338dd-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="338dd-136">Der Client kann die Zugriffsebene abrufen, die gewährt wurde, indem die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des geöffneten Eintrags aufgerufen und die PR_ACCESS_LEVEL -Eigenschaft (PidTagAccessLevel) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="338dd-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="338dd-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="338dd-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="338dd-138">Verwendet nur das Offlineadressbuch, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="338dd-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="338dd-139">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und aus dem Cache auf einen Eintrag in diesem Adressbuch zu zugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="338dd-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="338dd-140">Dieses Flag wird nur vom Adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="338dd-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="338dd-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="338dd-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="338dd-142">Ermöglicht den Erfolgreichen Aufruf, möglicherweise bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="338dd-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="338dd-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="338dd-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="338dd-144">Verwendet nur die GAL, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="338dd-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="338dd-145">Dieses Flag wird nur vom Adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="338dd-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="338dd-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="338dd-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="338dd-147">Fordert an, dass der Eintrag mit Lese- und Schreibberechtigung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="338dd-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="338dd-148">Da Einträge standardmäßig mit schreibgeschützten Zugriffen geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese- und Schreibberechtigungen gewährt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="338dd-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="338dd-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="338dd-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="338dd-150">Verwendet das Offlineadressbuch nicht zum Ausführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="338dd-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="338dd-151">Dieses Flag wird nur vom Adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="338dd-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="338dd-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="338dd-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="338dd-153">[out] Ein Zeiger auf den Typ des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="338dd-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="338dd-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="338dd-154">_lppUnk_</span></span>
  
> <span data-ttu-id="338dd-155">[out] Ein Zeiger auf einen Zeiger des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="338dd-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

