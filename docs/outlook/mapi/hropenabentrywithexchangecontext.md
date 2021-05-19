---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434053"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="5a355-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="5a355-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="5a355-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a355-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a355-105">Öffnet die **entryID** mit dem Exchange, das von **pEmsmdbUID identifiziert wurde.**</span><span class="sxs-lookup"><span data-stu-id="5a355-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="5a355-106">Diese Funktion funktioniert ähnlich wie [IAddrBook::D etails,](iaddrbook-details.md) mit der Ausnahme, dass die Verwendung dieser Funktion sicherstellt, dass das [IAddrBook::OpenEntry](iaddrbook-openentry.md) mithilfe des erwarteten Exchange-Adressbuchanbieters geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5a355-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a355-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5a355-107">Header file:</span></span>  <br/> |<span data-ttu-id="5a355-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="5a355-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="5a355-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5a355-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="5a355-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="5a355-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="5a355-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5a355-111">Called by:</span></span>  <br/> |<span data-ttu-id="5a355-112">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5a355-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="5a355-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a355-113">Parameters</span></span>

 <span data-ttu-id="5a355-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="5a355-114">_pmsess_</span></span>
  
> <span data-ttu-id="5a355-115">[in] Die angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="5a355-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="5a355-116">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="5a355-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="5a355-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="5a355-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="5a355-118">[in] Ein Zeiger auf eine **emsmdbUID,** die den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, den diese Funktion verwenden soll, um Details zur Eintrags-ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5a355-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="5a355-119">Wenn der Bezeichner für eingehende Eingaben kein eintragsbezeichner Exchange Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="5a355-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="5a355-120">Wenn dieser Parameter NULL oder null MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="5a355-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="5a355-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="5a355-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="5a355-122">[in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a355-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="5a355-123">Es kann nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="5a355-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="5a355-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5a355-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="5a355-125">[in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="5a355-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5a355-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5a355-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="5a355-127">[in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a355-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="5a355-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a355-128">_ulFlags_</span></span>
  
> <span data-ttu-id="5a355-129">[in] Eine Bitmaske mit Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5a355-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="5a355-130">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5a355-130">The following flags can be set:</span></span>
    
<span data-ttu-id="5a355-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5a355-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="5a355-132">Fordert an, dass der Eintrag mit den maximal zulässigen Netzwerk- und Clientberechtigungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5a355-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="5a355-133">Wenn der Client beispielsweise über Lese- und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese- und Schreibberechtigung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5a355-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="5a355-134">Der Client kann die Zugriffsebene abrufen, die gewährt wurde, indem die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des geöffneten Eintrags aufgerufen und die PR_ACCESS_LEVEL -Eigenschaft (PidTagAccessLevel) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5a355-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="5a355-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="5a355-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="5a355-136">Verwendet nur das Offlineadressbuch, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="5a355-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="5a355-137">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und aus dem Cache auf einen Eintrag in diesem Adressbuch zu zugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a355-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="5a355-138">Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a355-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="5a355-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5a355-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="5a355-140">Ermöglicht den Erfolgreichen Aufruf, möglicherweise bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5a355-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="5a355-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="5a355-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="5a355-142">Verwendet nur die GAL, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="5a355-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="5a355-143">Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a355-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="5a355-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5a355-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="5a355-145">Fordert an, dass der Eintrag mit Lese- und Schreibberechtigung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5a355-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="5a355-146">Da Einträge standardmäßig mit schreibgeschützten Zugriffen geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese- und Schreibberechtigungen gewährt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5a355-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="5a355-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="5a355-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="5a355-148">Verwendet das Offlineadressbuch nicht zum Ausführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="5a355-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="5a355-149">Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a355-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

