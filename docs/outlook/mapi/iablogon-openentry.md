---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 53dfb62bb33a4941e2b5627e729763101e24319d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791965"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="b66a2-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b66a2-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="b66a2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b66a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b66a2-105">Öffnet einen Container, messaging-Benutzer oder eine Verteilerliste, und gibt einen Zeiger auf eine Implementierung Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b66a2-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b66a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b66a2-106">Parameters</span></span>

 <span data-ttu-id="b66a2-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b66a2-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b66a2-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="b66a2-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b66a2-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b66a2-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b66a2-110">[in] Ein Zeiger auf die Eintrags-ID des Containers, messaging-Benutzer oder Verteilerliste zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b66a2-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="b66a2-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b66a2-111">_lpInterface_</span></span>
  
> <span data-ttu-id="b66a2-112">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle für den Zugriff auf die open-Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b66a2-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="b66a2-113">Übergeben von NULL gibt den Bezeichner für das Objekt standard-Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="b66a2-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="b66a2-114">Für Container, ist der standard-Benutzeroberfläche [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="b66a2-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="b66a2-115">Der Standard-Schnittstellen für Address Book-Objekten sind [IDistList: IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser: IMAPIProp](imailuserimapiprop.md) für ein messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b66a2-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="b66a2-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b66a2-116">_ulFlags_</span></span>
  
> <span data-ttu-id="b66a2-117">[in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b66a2-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="b66a2-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b66a2-118">The following flags can be set:</span></span>
    
<span data-ttu-id="b66a2-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b66a2-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="b66a2-120">Fordert an, dass das Objekt mit den maximale Netzwerkberechtigungen für den Benutzer und die maximale Anwendung Clientzugriff zulässig geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="b66a2-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="b66a2-121">Beispielsweise sollte der Client Lese-/Schreibberechtigung verfügt, das Objekt mit Lese-/Schreibzugriff geöffnet werden; Wenn der Client nur-Lese-Berechtigung verfügt, sollte das Objekt mit Leseberechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="b66a2-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="b66a2-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b66a2-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="b66a2-123">Ermöglicht die **OpenEntry** -Methode erfolgreich, möglicherweise zurückgegeben werden, bevor der aufrufende Client vollständig Zugriff auf das Objekt hat.</span><span class="sxs-lookup"><span data-stu-id="b66a2-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="b66a2-124">Wenn das Objekt nicht zugegriffen werden kann, kann die nachfolgenden Objekt Anrufen ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b66a2-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="b66a2-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b66a2-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b66a2-126">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="b66a2-126">Requests read/write permission.</span></span> <span data-ttu-id="b66a2-127">Standardmäßig werden Objekte mit schreibgeschützten Zugriff geöffnet, und Clients sollte nicht davon ausgehen, dass die Lese-Schreib-Berechtigung gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="b66a2-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="b66a2-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="b66a2-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="b66a2-129">[out] Ein Zeiger auf den Typ des Objekts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b66a2-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="b66a2-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="b66a2-130">_lppUnk_</span></span>
  
> <span data-ttu-id="b66a2-131">[out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="b66a2-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b66a2-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b66a2-132">Remarks</span></span>

<span data-ttu-id="b66a2-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="b66a2-133">S_OK</span></span> 
  
> <span data-ttu-id="b66a2-134">Das Objekt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b66a2-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="b66a2-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b66a2-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b66a2-136">Entweder der Benutzer verfügt nicht über ausreichende Berechtigungen zum Öffnen des Objekts oder es wurde versucht, ein nur-Lese-Objekt mit Lese-/Schreibzugriff zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b66a2-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="b66a2-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b66a2-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b66a2-138">Die _LpEntryID_ angegebene Eintrags-ID stellt kein Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="b66a2-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="b66a2-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b66a2-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b66a2-140">Die Eintrags-ID in der _LpEntryID_ -Parameter ist nicht vom durch die Adressbuchanbieter erkanntes Format.</span><span class="sxs-lookup"><span data-stu-id="b66a2-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b66a2-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b66a2-141">Remarks</span></span>

<span data-ttu-id="b66a2-142">MAPI-Aufrufen die **OpenEntry** -Methode, um einen Container öffnen messaging-Benutzer oder eine Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="b66a2-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b66a2-143">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="b66a2-143">Notes to implementers</span></span>

<span data-ttu-id="b66a2-144">Bevor Sie MAPI Ihrer **OpenEntry** -Methode aufruft, wird festgelegt, dass die Eintrags-ID in der _LpEntryID_ -Parameter für den Benutzer und nicht für einen anderen Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="b66a2-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="b66a2-145">MAPI wird durch entsprechende [MAPIUID](mapiuid.md) Strukturänderung in die Eintrags-ID mit der **MAPIUID** , die Sie durch Aufrufen der [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode beim Start registriert.</span><span class="sxs-lookup"><span data-stu-id="b66a2-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="b66a2-146">Öffnen Sie das Objekt als schreibgeschützt, es sei denn, das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b66a2-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b66a2-147">Wenn Sie die Änderung für das angeforderte Objekt nicht zulässig ist, keine überhaupt öffnen Sie das Objekt und zurückzugeben Sie MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="b66a2-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="b66a2-148">Wenn MAPI NULL für _LpEntryID_übergibt, öffnen Sie den Stammcontainer in der Containerhierarchie.</span><span class="sxs-lookup"><span data-stu-id="b66a2-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="b66a2-149">Das Objekt, das Sie aufgefordert werden, öffnen Sie möglicherweise ein Objekt aus einem anderen Anbieter kopiert.</span><span class="sxs-lookup"><span data-stu-id="b66a2-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="b66a2-150">In diesem Fall wird die Eigenschaft **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b66a2-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="b66a2-151">Wenn diese Eigenschaft auf das Objekt unterstützt, rufen Sie die [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) -Methode zum Binden von Code für diesen Eintrag in der fremden Anbieter auf und übergibt **PR_TEMPLATEID** in der _LpTemplateID_ -Parameter und den Wert 0 in die _ulTemplateFlags _Parameter.</span><span class="sxs-lookup"><span data-stu-id="b66a2-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="b66a2-152">**IMAPISupport::OpenTemplateID** übergibt diese Informationen an den foreign Anbieter in einem Aufruf der fremde Anbieter [OpenTemplateID](iablogon-opentemplateid.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b66a2-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="b66a2-153">Wenn **IMAPISupport::OpenTemplateID** löst einen Fehler aus, in der Regel, da der fremde Anbieter nicht verfügbar ist oder nicht in das Profil enthalten ist versuchen Sie fortfahren, indem Sie den Eintrag ungebundenen als schreibgeschützt behandeln.</span><span class="sxs-lookup"><span data-stu-id="b66a2-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="b66a2-154">Weitere Informationen zum Öffnen von Adressbucheinträgen fremden finden Sie unter [als ein Host-Adressbuchanbieter fungiert](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b66a2-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b66a2-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b66a2-155">See also</span></span>



[<span data-ttu-id="b66a2-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b66a2-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

