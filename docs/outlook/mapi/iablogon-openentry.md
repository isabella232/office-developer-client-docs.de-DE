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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409230"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="6fac3-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6fac3-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="6fac3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fac3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fac3-105">Öffnet einen Container, einen Messagingbenutzer oder eine Verteilerliste und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, um weiteren Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="6fac3-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="6fac3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fac3-106">Parameters</span></span>

 <span data-ttu-id="6fac3-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6fac3-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="6fac3-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="6fac3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6fac3-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6fac3-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="6fac3-110">[in] Ein Zeiger auf die Eintrags-ID des zu öffnende Containers, Messagingbenutzers oder Verteilerlistens.</span><span class="sxs-lookup"><span data-stu-id="6fac3-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="6fac3-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6fac3-111">_lpInterface_</span></span>
  
> <span data-ttu-id="6fac3-112">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fac3-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="6fac3-113">Durch Übergeben von NULL wird der Bezeichner für die Standardschnittstelle des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fac3-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="6fac3-114">Für Container ist die Standardschnittstelle [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="6fac3-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="6fac3-115">Die Standardschnittstellen für Adressbuchobjekte sind [IDistList : IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser : IMAPIProp](imailuserimapiprop.md) für einen Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="6fac3-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="6fac3-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6fac3-116">_ulFlags_</span></span>
  
> <span data-ttu-id="6fac3-117">[in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="6fac3-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="6fac3-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6fac3-118">The following flags can be set:</span></span>
    
<span data-ttu-id="6fac3-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6fac3-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="6fac3-120">Fordert an, dass das Objekt mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und dem maximalen Clientanwendungszugriff geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="6fac3-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="6fac3-121">Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützte Berechtigungen verfügt, sollte das Objekt mit schreibgeschützter Berechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6fac3-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="6fac3-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6fac3-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6fac3-123">Ermöglicht der **OpenEntry-Methode,** erfolgreich zurückzukehren, möglicherweise bevor der aufrufende Client vollständig auf das Objekt zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="6fac3-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="6fac3-124">Wenn nicht auf das Objekt zugegriffen wird, kann durch einen nachfolgenden Objektaufruf ein Fehler verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="6fac3-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="6fac3-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6fac3-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="6fac3-126">Fordert Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="6fac3-126">Requests read/write permission.</span></span> <span data-ttu-id="6fac3-127">Standardmäßig werden Objekte mit schreibgeschützten Zugriff geöffnet, und Clients sollten nicht davon ausgehen, dass Lese-/Schreibberechtigungen erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="6fac3-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="6fac3-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="6fac3-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="6fac3-129">[out] Ein Zeiger auf den Typ des geöffneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="6fac3-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="6fac3-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="6fac3-130">_lppUnk_</span></span>
  
> <span data-ttu-id="6fac3-131">[out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="6fac3-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fac3-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6fac3-132">Remarks</span></span>

<span data-ttu-id="6fac3-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fac3-133">S_OK</span></span> 
  
> <span data-ttu-id="6fac3-134">Das Objekt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="6fac3-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="6fac3-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6fac3-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6fac3-136">Entweder verfügt der Benutzer nicht über ausreichende Berechtigungen zum Öffnen des Objekts, oder es wurde versucht, ein schreibgeschütztes Objekt mit Lese-/Schreibberechtigung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6fac3-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="6fac3-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6fac3-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6fac3-138">Der von  _lpEntryID_ angegebene Eintragsbezeichner stellt kein Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="6fac3-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="6fac3-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6fac3-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="6fac3-140">Der Eintragsbezeichner im  _lpEntryID-Parameter_ hat kein vom Adressbuchanbieter erkanntes Format.</span><span class="sxs-lookup"><span data-stu-id="6fac3-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6fac3-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6fac3-141">Remarks</span></span>

<span data-ttu-id="6fac3-142">MAPI ruft die **OpenEntry-Methode** auf, um einen Container, einen Messagingbenutzer oder eine Verteilerliste zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6fac3-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6fac3-143">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="6fac3-143">Notes to implementers</span></span>

<span data-ttu-id="6fac3-144">Bevor MAPI Ihre **OpenEntry-Methode** aufruft, bestimmt sie, dass der Eintragsbezeichner im  _lpEntryID-Parameter_ zu Ihnen und nicht zu einem anderen Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="6fac3-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="6fac3-145">MAPI führt dies durch Abgleichen der [MAPIUID-Struktur](mapiuid.md) in der Eintrags-ID mit der **MAPIUID** aus, die Sie beim Start durch Aufrufen der [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) registriert haben.</span><span class="sxs-lookup"><span data-stu-id="6fac3-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="6fac3-146">Öffnen Sie das Objekt als schreibgeschützt, es sei denn, MAPI_MODIFY oder MAPI_BEST_ACCESS im  _ulFlags-Parameter festgelegt_ ist.</span><span class="sxs-lookup"><span data-stu-id="6fac3-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="6fac3-147">Wenn Sie keine Änderung für das angeforderte Objekt zulassen, öffnen Sie das Objekt überhaupt nicht, und geben Sie MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="6fac3-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="6fac3-148">Wenn MAPI NULL für  _lpEntryID übergibt,_ öffnen Sie den Stammcontainer in der Containerhierarchie.</span><span class="sxs-lookup"><span data-stu-id="6fac3-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="6fac3-149">Das Objekt, das Sie öffnen möchten, kann ein Objekt sein, das von einem anderen Anbieter kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6fac3-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="6fac3-150">In diesem Fall wird die PR_TEMPLATEID **(** [PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fac3-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="6fac3-151">Wenn das Objekt diese Eigenschaft unterstützt, rufen Sie die [IMAPISupport::OpenTemplateID-Methode](imapisupport-opentemplateid.md) auf, um eine Bindung an Code für diesen Eintrag im fremden Anbieter zu erstellen. Übergeben Sie **PR_TEMPLATEID** im _lpTemplateID-Parameter_ und 0 im _ulTemplateFlags-Parameter._</span><span class="sxs-lookup"><span data-stu-id="6fac3-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="6fac3-152">**IMAPISupport::OpenTemplateID** übergibt diese Informationen an den fremden Anbieter in einem Aufruf der [IABLogon::OpenTemplateID-Methode](iablogon-opentemplateid.md) des fremden Anbieters.</span><span class="sxs-lookup"><span data-stu-id="6fac3-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="6fac3-153">Wenn **IMAPISupport::OpenTemplateID** einen Fehler verursacht, in der Regel, da der fremde Anbieter nicht verfügbar ist oder nicht im Profil enthalten ist, versuchen Sie, den Ungebundenen Eintrag als schreibgeschützt zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="6fac3-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="6fac3-154">Weitere Informationen zum Öffnen von fremden Adressbucheinträgen finden Sie unter [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6fac3-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6fac3-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fac3-155">See also</span></span>



[<span data-ttu-id="6fac3-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6fac3-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

