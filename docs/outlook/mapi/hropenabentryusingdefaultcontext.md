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
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="1da4b-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="1da4b-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="1da4b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1da4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1da4b-105">Führt die gleiche Funktion wie [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) aus, außer dass der Legacy- **emsmdbUID** als _pEmsmdbUID_ -Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1da4b-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="1da4b-106">Verwenden Sie diese Funktion nur, wenn Sie nicht die richtige **emsmdbUID** für den Aufruf von [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)abrufen können.</span><span class="sxs-lookup"><span data-stu-id="1da4b-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1da4b-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1da4b-107">Header file:</span></span>  <br/> |<span data-ttu-id="1da4b-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="1da4b-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="1da4b-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1da4b-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="1da4b-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="1da4b-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="1da4b-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1da4b-111">Called by:</span></span>  <br/> |<span data-ttu-id="1da4b-112">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1da4b-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="1da4b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1da4b-113">Parameters</span></span>

 <span data-ttu-id="1da4b-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="1da4b-114">_pmsess_</span></span>
  
> <span data-ttu-id="1da4b-115">in Der angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="1da4b-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="1da4b-116">Er darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1da4b-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="1da4b-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="1da4b-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="1da4b-118">in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="1da4b-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="1da4b-119">Er darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1da4b-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="1da4b-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1da4b-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="1da4b-121">in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="1da4b-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1da4b-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1da4b-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="1da4b-123">in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="1da4b-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="1da4b-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1da4b-124">_lpInterface_</span></span>
  
> <span data-ttu-id="1da4b-125">in Ein Zeiger auf die Schnittstellen-ID (IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1da4b-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="1da4b-126">Beim Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1da4b-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="1da4b-127">Für Messagingbenutzer ist die Standardschnittstelle [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="1da4b-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="1da4b-128">Für Verteilerlisten ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="1da4b-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="1da4b-129">Anrufer können _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen.</span><span class="sxs-lookup"><span data-stu-id="1da4b-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="1da4b-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1da4b-130">_ulFlags_</span></span>
  
> <span data-ttu-id="1da4b-131">in Eine Bitmaske von Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1da4b-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="1da4b-132">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1da4b-132">The following flags can be set:</span></span>
    
<span data-ttu-id="1da4b-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1da4b-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="1da4b-134">Fordert, dass der Eintrag mit den maximal zulässigen Netzwerk-und Clientberechtigungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1da4b-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="1da4b-135">Wenn der Client beispielsweise über Lese-und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese-und Schreibberechtigung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1da4b-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="1da4b-136">Der Client kann die Zugriffsebene abrufen, die durch Aufrufen der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des geöffneten Eintrags und Abrufen der PR_ACCESS_LEVEL (pidtagaccesslevel ()-Eigenschaft erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="1da4b-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="1da4b-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="1da4b-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="1da4b-138">Verwendet nur das Offlineadressbuch zum Durchführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="1da4b-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="1da4b-139">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1da4b-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="1da4b-140">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1da4b-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="1da4b-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1da4b-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="1da4b-142">Der Aufruf kann erfolgreich ausgeführt werden, bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1da4b-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="1da4b-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="1da4b-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="1da4b-144">Verwendet nur die GAL zur Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="1da4b-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="1da4b-145">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1da4b-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="1da4b-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="1da4b-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="1da4b-147">Fordert, dass der Eintrag mit Lese-und Schreibberechtigung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1da4b-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="1da4b-148">Da Einträge standardmäßig mit schreibgeschütztem Zugriff geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese-und Schreibberechtigungen erteilt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1da4b-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="1da4b-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="1da4b-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="1da4b-150">Das Offlineadressbuch wird nicht zum Durchführen der Namensauflösung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1da4b-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="1da4b-151">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1da4b-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="1da4b-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="1da4b-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="1da4b-153">Out Ein Zeiger auf den Typ des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="1da4b-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="1da4b-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="1da4b-154">_lppUnk_</span></span>
  
> <span data-ttu-id="1da4b-155">Out Ein Zeiger auf einen Zeiger des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="1da4b-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

