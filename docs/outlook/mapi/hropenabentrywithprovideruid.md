---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e33e656e70802437ab8b8717c5e175e2a13e384e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791926"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="7653d-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="7653d-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="7653d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7653d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7653d-105">Öffnet die **Eintrags-ID** mithilfe der Exchange-Adressbuch durch _pEmsabpUID_identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7653d-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="7653d-106">Diese Funktion arbeitet ähnlich wie [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit der Ausnahme, dass mit dieser Funktion wird sichergestellt, dass [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit dem erwarteten Exchange-Adressbuch Anbieter geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7653d-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7653d-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7653d-107">Header file:</span></span>  <br/> |<span data-ttu-id="7653d-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="7653d-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="7653d-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7653d-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="7653d-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="7653d-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="7653d-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7653d-111">Called by:</span></span>  <br/> |<span data-ttu-id="7653d-112">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7653d-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="7653d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7653d-113">Parameters</span></span>

 <span data-ttu-id="7653d-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="7653d-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="7653d-115">[in] Ein Zeiger auf eine **EmsmdbUID** , die den Exchange-Dienst identifiziert, die die Exchange-Adressbuchanbieter enthält, die diese Funktion zum Anzeigen von Details auf die Eintrags-ID verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7653d-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="7653d-116">Wenn eingehende Eintrags-ID nicht um ein Exchange-Adressbuchanbieter Eintrags-ID ist, dieser Parameter wird ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="7653d-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="7653d-117">Wenn dieser Parameter auf NULL oder eine MAPIUID NULL ist, verhält sich diese Funktion wie [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="7653d-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="7653d-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="7653d-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="7653d-119">[in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7653d-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="7653d-120">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7653d-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="7653d-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7653d-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="7653d-122">[in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="7653d-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7653d-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7653d-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="7653d-124">[in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.</span><span class="sxs-lookup"><span data-stu-id="7653d-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="7653d-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7653d-125">_lpInterface_</span></span>
  
> <span data-ttu-id="7653d-126">[in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, die den Eintrag open Zugriff auf verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7653d-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="7653d-127">Übergeben von NULL gibt die standard-Schnittstelle des Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="7653d-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="7653d-128">Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="7653d-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="7653d-129">Verteilerlisten, ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md)und Containern, ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="7653d-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="7653d-130">Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen.</span><span class="sxs-lookup"><span data-stu-id="7653d-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="7653d-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7653d-131">_ulFlags_</span></span>
  
> <span data-ttu-id="7653d-132">[in] Eine Bitmaske aus Flags, die die wie steuert der Eintrag geöffnet wird, können die folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7653d-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="7653d-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7653d-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="7653d-134">Fordert, dass der Eintrag mit den maximalen zulässigen Netzwerk- und Client Berechtigungen geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7653d-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="7653d-135">Wenn der Client über Lese- und Schreibberechtigungen, versucht der Adressbuchanbieter beispielsweise, öffnen Sie den Eintrag mit Lese- und Schreibberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="7653d-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="7653d-136">Der Client kann die Zugriffsebene abzurufen, die durch Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode des Eintrags öffnen und das Abrufen der Eigenschaft PR_ACCESS_LEVEL (PidTagAccessLevel) gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="7653d-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="7653d-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="7653d-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="7653d-138">Verwenden Sie nur das Offlineadressbuch, um namensauflösung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7653d-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="7653d-139">Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7653d-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="7653d-140">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7653d-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="7653d-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7653d-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="7653d-142">Ermöglicht den Anruf, potenziell erfolgreich ausgeführt werden kann, bevor der Eintrag vollständig geöffnet und verfügbar ist, dass dies, dass nachfolgende Aufrufe von den Eintrag möglicherweise einen Fehler zurück, ist.</span><span class="sxs-lookup"><span data-stu-id="7653d-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="7653d-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="7653d-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="7653d-144">Verwenden Sie nur die globale Adressliste, um namensauflösung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7653d-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="7653d-145">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7653d-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="7653d-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7653d-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="7653d-147">Anforderungen, denen mit der Eintrag geöffnet werden Lese- und Schreibberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="7653d-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="7653d-148">Da die Einträge in der Standardeinstellung mit schreibgeschützten Zugriff geöffnet sind, sollte Clients nicht davon ausgehen, das Lesen und schreiben, dass die Berechtigung erteilt wurde, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7653d-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="7653d-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="7653d-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="7653d-150">Verwenden Sie das Offlineadressbuch nicht namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="7653d-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="7653d-151">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7653d-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="7653d-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="7653d-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="7653d-153">[out] Ein Zeiger auf den Typ des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7653d-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="7653d-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="7653d-154">_lppUnk_</span></span>
  
> <span data-ttu-id="7653d-155">[out] Ein Zeiger auf einen Zeiger des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7653d-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

