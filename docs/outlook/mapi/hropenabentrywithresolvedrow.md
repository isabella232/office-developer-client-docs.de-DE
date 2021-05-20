---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2eb643e0002e2159e3197d66e021aba0bb8c126f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429908"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="78f83-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="78f83-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="78f83-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78f83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78f83-105">Führt die gleiche Funktion wie [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) aus, mit der Ausnahme, dass die **emsabpUID** automatisch aus der aufgelösten Zeile ruft und die **entryID geöffnet wird.**</span><span class="sxs-lookup"><span data-stu-id="78f83-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78f83-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="78f83-106">Header file:</span></span>  <br/> |<span data-ttu-id="78f83-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="78f83-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="78f83-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="78f83-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="78f83-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="78f83-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="78f83-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="78f83-110">Called by:</span></span>  <br/> |<span data-ttu-id="78f83-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="78f83-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithResolvedRow(
  LPSRow prwResolved,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="78f83-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="78f83-112">Parameters</span></span>

 <span data-ttu-id="78f83-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="78f83-113">_prwResolved_</span></span>
  
> <span data-ttu-id="78f83-114">[in] Ein Zeiger auf die aufgelöste Zeile, die verwendet wird, um **die emsabpUID** zu erhalten und die **entryID zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="78f83-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="78f83-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="78f83-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="78f83-116">[in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78f83-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="78f83-117">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="78f83-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="78f83-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="78f83-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="78f83-119">[in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="78f83-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="78f83-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="78f83-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="78f83-121">[in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="78f83-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="78f83-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="78f83-122">_lpInterface_</span></span>
  
> <span data-ttu-id="78f83-123">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78f83-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="78f83-124">Durch Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78f83-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="78f83-125">Für Messagingbenutzer ist die Standardschnittstelle [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="78f83-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="78f83-126">Für Verteilerlisten ist [IDistList : IMAPIContainer](idistlistimapicontainer.md)und für Container [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="78f83-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="78f83-127">Anrufer können  _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen.</span><span class="sxs-lookup"><span data-stu-id="78f83-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="78f83-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78f83-128">_ulFlags_</span></span>
  
> <span data-ttu-id="78f83-129">[in] Eine Bitmaske mit Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="78f83-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="78f83-130">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="78f83-130">The following flags can be set:</span></span>
    
<span data-ttu-id="78f83-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="78f83-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="78f83-132">Fordert an, dass der Eintrag mit den maximal zulässigen Netzwerk- und Clientberechtigungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="78f83-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="78f83-133">Wenn der Client beispielsweise über Lese- und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese- und Schreibberechtigung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="78f83-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="78f83-134">Der Client kann die Zugriffsebene abrufen, die gewährt wurde, indem die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des geöffneten Eintrags aufgerufen und die PR_ACCESS_LEVEL -Eigenschaft (PidTagAccessLevel) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="78f83-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="78f83-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="78f83-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="78f83-136">Verwendet nur das Offlineadressbuch, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="78f83-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="78f83-137">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und aus dem Cache auf einen Eintrag in diesem Adressbuch zu zugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="78f83-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="78f83-138">Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="78f83-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="78f83-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="78f83-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="78f83-140">Ermöglicht den Erfolgreichen Aufruf, möglicherweise bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="78f83-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="78f83-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="78f83-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="78f83-142">Verwendet nur die GAL, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="78f83-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="78f83-143">Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="78f83-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="78f83-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="78f83-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="78f83-145">Fordert an, dass der Eintrag mit Lese- und Schreibberechtigung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="78f83-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="78f83-146">Da Einträge standardmäßig mit schreibgeschützten Zugriffen geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese- und Schreibberechtigungen gewährt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="78f83-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="78f83-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="78f83-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="78f83-148">Verwendet das Offlineadressbuch nicht zum Ausführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="78f83-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="78f83-149">Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="78f83-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="78f83-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="78f83-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="78f83-151">[out] Ein Zeiger auf den Typ des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="78f83-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="78f83-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="78f83-152">_lppUnk_</span></span>
  
> <span data-ttu-id="78f83-153">[out] Ein Zeiger auf einen Zeiger des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="78f83-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

