---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Letzte �nderung: Freitag, 1. Februar 2013'
ms.openlocfilehash: fa279962043f6f7cb7a134b624000c9c7e65369f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19792017"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="7a11b-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7a11b-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="7a11b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a11b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a11b-105">Öffnet ein Adressbuch Adresseintrag, und gibt einen Zeiger auf eine Schnittstelle, die den Eintrag Zugriff auf verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a11b-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="7a11b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a11b-106">Parameters</span></span>

<span data-ttu-id="7a11b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7a11b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7a11b-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="7a11b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="7a11b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7a11b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7a11b-110">[in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.</span><span class="sxs-lookup"><span data-stu-id="7a11b-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="7a11b-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7a11b-111">_lpInterface_</span></span>
  
> <span data-ttu-id="7a11b-112">[in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, greifen Sie auf den Eintrag open verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a11b-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="7a11b-113">Übergeben von NULL gibt Standardschnittstelle für das Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="7a11b-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="7a11b-114">Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="7a11b-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="7a11b-115">Verteilerlisten, ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md) und Containern, ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="7a11b-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="7a11b-116">Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen.</span><span class="sxs-lookup"><span data-stu-id="7a11b-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="7a11b-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a11b-117">_ulFlags_</span></span>
  
> <span data-ttu-id="7a11b-118">[in] Eine Bitmaske aus Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7a11b-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="7a11b-119">Die folgenden Kennzeichen können festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7a11b-119">The following flags can be set.</span></span>
    
<span data-ttu-id="7a11b-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7a11b-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="7a11b-121">Fordert, dass der Eintrag mit den maximalen zulässigen Netzwerk- und Client Berechtigungen geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7a11b-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="7a11b-122">Wenn der Client über Lese-/Schreibberechtigung verfügt, sollten beispielsweise die Adressbuchanbieter versuchen, um den Eintrag mit Lese-/Schreibzugriff zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7a11b-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="7a11b-123">Der Client kann die Zugriffsebene abzurufen, die durch Aufrufen der open Eintrag [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode und Abrufen der Eigenschaft **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="7a11b-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="7a11b-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="7a11b-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="7a11b-125">Öffnet ein Adressbuch Adresseintrag und greift er nur aus dem Cache.</span><span class="sxs-lookup"><span data-stu-id="7a11b-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="7a11b-126">Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7a11b-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="7a11b-127">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11b-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="7a11b-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7a11b-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7a11b-129">Ermöglicht den Anruf, potenziell erfolgreich ausgeführt werden kann, bevor der Eintrag vollständig geöffnet und kann, sagen, dass später aufruft, um den Eintrag einen Fehler zurück, möglicherweise ist.</span><span class="sxs-lookup"><span data-stu-id="7a11b-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="7a11b-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="7a11b-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="7a11b-131">Verwenden Sie nur die globale Adressliste, um namensauflösung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7a11b-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="7a11b-132">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11b-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="7a11b-133">_UlFlags_ MAPI_GAL_ONLY möglicherweise nicht in der herunterladbaren Headerdatei derzeit definiert werden, in diesem Fall können Sie es dem Code mit dem folgenden Wert hinzufügen: >`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="7a11b-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="7a11b-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7a11b-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7a11b-135">Anforderungen, denen der Eintrag geöffnet werden, mit Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="7a11b-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="7a11b-136">Da Einträge standardmäßig mit schreibgeschützten Zugriff geöffnet sind, sollte Clients nicht wird vorausgesetzt, dass Lese-/Schreibberechtigung erteilt wurde, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7a11b-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="7a11b-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="7a11b-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="7a11b-138">Verwenden Sie das Offlineadressbuch nicht namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a11b-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="7a11b-139">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11b-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="7a11b-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="7a11b-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="7a11b-141">[out] Ein Zeiger auf den Typ des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7a11b-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="7a11b-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="7a11b-142">_lppUnk_</span></span>
  
> <span data-ttu-id="7a11b-143">[out] Ein Zeiger auf einen Zeiger auf den Eintrag geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7a11b-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a11b-144">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7a11b-144">Return value</span></span>

<span data-ttu-id="7a11b-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a11b-145">S_OK</span></span> 
  
> <span data-ttu-id="7a11b-146">Der Eintrag wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7a11b-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="7a11b-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7a11b-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7a11b-148">Es wurde versucht, einen Eintrag zu öffnen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="7a11b-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="7a11b-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7a11b-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7a11b-150">Der Eintrag durch _LpEntryID_ dargestellt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7a11b-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="7a11b-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7a11b-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="7a11b-152">Die in _LpEntryID_ angegebene Eintrags-ID wird nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="7a11b-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="7a11b-153">Dieser Wert wird in der Regel zurückgegeben, wenn die Adressbuchanbieter verantwortlich für den entsprechenden Eintrag nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="7a11b-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7a11b-154">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a11b-154">Remarks</span></span>

<span data-ttu-id="7a11b-155">Clients und -Dienstanbieter rufen Sie die **IAddrBook::OpenEntry** -Methode, um ein Adressbuch Adresseintrag zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7a11b-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="7a11b-156">MAPI leitet den Anruf an die entsprechenden Adressbuchanbieter basierend auf der [MAPIUID](mapiuid.md) -Struktur in die Eintrags-ID in der _LpEntryID_ -Parameter übergeben enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a11b-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="7a11b-157">Der Adressbuchanbieter öffnet den Eintrag im schreibgeschützten Modus, es sei denn, das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7a11b-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="7a11b-158">Allerdings werden diese Flags Vorschläge.</span><span class="sxs-lookup"><span data-stu-id="7a11b-158">However, these flags are suggestions.</span></span> <span data-ttu-id="7a11b-159">Wenn die Adressbuchanbieter keine Änderung für den Eintrag angefordert zulässt, wird MAPI_E_NO_ACCESS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a11b-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="7a11b-160">Der Parameter _LpInterface_ gibt an, welche Schnittstelle zum Zugriff auf die geöffnete Eintrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a11b-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="7a11b-161">Übergeben von NULL in _LpInterface_ gibt an, dass die standard-MAPI-Schnittstelle für diesen Eintrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a11b-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="7a11b-162">Da die Adressbuchanbieter eine andere Schnittstelle als die durch den Parameter _LpInterface_ vorgeschlagene zurückgegeben werden, sollte der Aufrufer überprüfen Sie den Wert zurückgegeben, die in der _LpulObjType_ -Parameter, um festzustellen, ob der Objekttyp zurückgegeben wird Was wurde erwartet.</span><span class="sxs-lookup"><span data-stu-id="7a11b-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="7a11b-163">Wenn der Objekttyp nicht mit dem erwarteten Typ ist, kann der Aufrufer den _LppUnk_ -Parameter auf einen Typ umgewandelt, die besser geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="7a11b-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a11b-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a11b-164">See also</span></span>

- [<span data-ttu-id="7a11b-165">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7a11b-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

