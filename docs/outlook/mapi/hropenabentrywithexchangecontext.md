---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fcedaf689db8280b4649662ba61c8468d0f98305
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791929"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="437c4-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="437c4-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="437c4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="437c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="437c4-105">Öffnet die **Eintrags-ID** mithilfe der Exchange-Adressbuch durch **pEmsmdbUID**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="437c4-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="437c4-106">Diese Funktion arbeitet ähnlich wie [IAddrBook::Details](iaddrbook-details.md) mit der Ausnahme, dass mit dieser Funktion wird sichergestellt, dass die [IAddrBook::OpenEntry](iaddrbook-openentry.md) mithilfe der erwarteten Exchange-Adressbuchanbieter geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="437c4-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="437c4-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="437c4-107">Header file:</span></span>  <br/> |<span data-ttu-id="437c4-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="437c4-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="437c4-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="437c4-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="437c4-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="437c4-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="437c4-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="437c4-111">Called by:</span></span>  <br/> |<span data-ttu-id="437c4-112">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="437c4-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="437c4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="437c4-113">Parameters</span></span>

 <span data-ttu-id="437c4-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="437c4-114">_pmsess_</span></span>
  
> <span data-ttu-id="437c4-115">[in] Die angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="437c4-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="437c4-116">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="437c4-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="437c4-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="437c4-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="437c4-118">[in] Ein Zeiger auf eine **EmsmdbUID** , die den Exchange-Dienst identifiziert, die die Exchange-Adressbuchanbieter enthält, die diese Funktion zum Anzeigen von Details auf die Eintrags-ID verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="437c4-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="437c4-119">Wenn eingehende Eintrags-ID nicht um ein Exchange-Adressbuchanbieter Eintrags-ID ist, dieser Parameter wird ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="437c4-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="437c4-120">Wenn dieser Parameter auf NULL oder eine MAPIUID NULL ist, verhält sich diese Funktion wie [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="437c4-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="437c4-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="437c4-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="437c4-122">[in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="437c4-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="437c4-123">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="437c4-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="437c4-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="437c4-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="437c4-125">[in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="437c4-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="437c4-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="437c4-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="437c4-127">[in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.</span><span class="sxs-lookup"><span data-stu-id="437c4-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="437c4-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="437c4-128">_ulFlags_</span></span>
  
> <span data-ttu-id="437c4-129">[in] Eine Bitmaske aus Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="437c4-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="437c4-130">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="437c4-130">The following flags can be set:</span></span>
    
<span data-ttu-id="437c4-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="437c4-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="437c4-132">Fordert, dass der Eintrag mit den maximalen zulässigen Netzwerk- und Client Berechtigungen geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="437c4-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="437c4-133">Wenn der Client über Lese- und Schreibberechtigungen, versucht der Adressbuchanbieter beispielsweise, öffnen Sie den Eintrag mit Lese- und Schreibberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="437c4-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="437c4-134">Der Client kann die Zugriffsebene abzurufen, die durch Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode des Eintrags öffnen und das Abrufen der Eigenschaft PR_ACCESS_LEVEL (PidTagAccessLevel) gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="437c4-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="437c4-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="437c4-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="437c4-136">Verwendet nur das Offlineadressbuch namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="437c4-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="437c4-137">Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="437c4-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="437c4-138">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="437c4-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="437c4-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="437c4-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="437c4-140">Ermöglicht den Anruf, potenziell erfolgreich ausgeführt werden kann, bevor der Eintrag vollständig geöffnet und verfügbar ist, dass dies, dass nachfolgende Aufrufe von den Eintrag möglicherweise einen Fehler zurück, ist.</span><span class="sxs-lookup"><span data-stu-id="437c4-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="437c4-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="437c4-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="437c4-142">Verwendet nur die globale Adressliste namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="437c4-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="437c4-143">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="437c4-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="437c4-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="437c4-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="437c4-145">Anforderungen, denen mit der Eintrag geöffnet werden Lese- und Schreibberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="437c4-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="437c4-146">Da die Einträge in der Standardeinstellung mit schreibgeschützten Zugriff geöffnet sind, sollte Clients nicht davon ausgehen, das Lesen und schreiben, dass die Berechtigung erteilt wurde, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="437c4-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="437c4-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="437c4-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="437c4-148">Das Offlineadressbuch wird nicht zum Ausführen von namensauflösung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="437c4-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="437c4-149">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="437c4-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

