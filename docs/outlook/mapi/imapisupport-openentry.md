---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409615"
---
# <a name="imapisupportopenentry"></a><span data-ttu-id="a1664-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="a1664-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="a1664-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1664-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1664-105">Öffnet ein Objekt und gibt einen Schnittstellenzeiger für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="a1664-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
ULONG FAR * lpulObjType,
LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="a1664-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1664-106">Parameters</span></span>

 <span data-ttu-id="a1664-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1664-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="a1664-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="a1664-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a1664-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1664-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="a1664-110">[in] Ein Zeiger auf den Eintragsbezeichner des zu öffnende Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1664-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="a1664-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a1664-111">_lpInterface_</span></span>
  
> <span data-ttu-id="a1664-112">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1664-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="a1664-113">Das Übergeben von NULL führt dazu, dass die Standardschnittstelle des Objekts zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a1664-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="a1664-114">Wenn das zu öffnende Objekt z. B. eine Nachricht ist, lautet die Standardschnittstelle [IMessage](imessageimapiprop.md); für Ordner ist es [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="a1664-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="a1664-115">Die Standardschnittstellen für Adressbuchobjekte sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für einen Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="a1664-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="a1664-116">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="a1664-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="a1664-117">[in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a1664-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="a1664-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a1664-118">The following flags can be set:</span></span>
    
<span data-ttu-id="a1664-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a1664-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="a1664-120">Fordert an, dass das Objekt mit den maximalen Netzwerkberechtigungen geöffnet wird, die für den Aufrufer zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a1664-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="a1664-121">Wenn der Aufrufer beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt als Lese-/Schreibzugriff geöffnet werden. Wenn der Aufrufer über schreibgeschützte Berechtigungen verfügt, sollte das Objekt als schreibgeschützt geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="a1664-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="a1664-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a1664-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a1664-123">Ermöglicht **openEntry** die erfolgreiche Rückgabe, möglicherweise bevor auf das Objekt vollständig für den Aufrufer zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1664-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="a1664-124">Wenn auf das Objekt nicht zugegriffen werden kann, kann ein nachfolgender Objektaufruf zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="a1664-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="a1664-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a1664-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a1664-126">Fordert Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="a1664-126">Requests read/write permission.</span></span> <span data-ttu-id="a1664-127">Standardmäßig werden Objekte als schreibgeschützt geöffnet, und Anrufer sollten nicht unter der Annahme arbeiten, dass Lese-/Schreibberechtigungen erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="a1664-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="a1664-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a1664-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="a1664-129">[out] Ein Zeiger auf den Typ des geöffneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1664-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="a1664-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="a1664-130">_lppUnk_</span></span>
  
> <span data-ttu-id="a1664-131">[out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="a1664-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1664-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1664-132">Return value</span></span>

<span data-ttu-id="a1664-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1664-133">S_OK</span></span> 
  
> <span data-ttu-id="a1664-134">Das Objekt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a1664-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="a1664-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a1664-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="a1664-136">Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, auf ein Objekt zu zugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="a1664-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="a1664-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a1664-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a1664-138">Dem Eintragsbezeichner, der im  _lpEntryID-Parameter_ übergeben wird, ist kein Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a1664-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="a1664-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a1664-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="a1664-140">Der im  _lpEntryID-Parameter_ übergebene Eintragsbezeichner hat ein nicht wiedererkennbares Format.</span><span class="sxs-lookup"><span data-stu-id="a1664-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="a1664-141">Dieser Wert wird in der Regel zurückgegeben, wenn der Adressbuchanbieter, der das Objekt enthält, nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="a1664-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a1664-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1664-142">Remarks</span></span>

<span data-ttu-id="a1664-143">Die **IMAPISupport::OpenEntry-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="a1664-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="a1664-144">Dienstanbieter rufen **IMAPISupport::OpenEntry auf,** um einen Zeiger auf eine Schnittstelle abzurufen, die für den Zugriff auf ein bestimmtes Objekt verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1664-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a1664-145">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a1664-145">Notes to callers</span></span>

<span data-ttu-id="a1664-146">Rufen **Sie IMAPISupport::OpenEntry** nur auf, wenn Sie nicht wissen, welche Art von Objekt Sie öffnen.</span><span class="sxs-lookup"><span data-stu-id="a1664-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="a1664-147">Wenn Sie wissen, dass Sie einen Ordner oder eine Nachricht öffnen, rufen Sie [stattdessen IMsgStore::OpenEntry](imsgstore-openentry.md) auf.</span><span class="sxs-lookup"><span data-stu-id="a1664-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="a1664-148">Wenn Sie wissen, dass Sie einen Adressbuchcontainer, einen Messagingbenutzer oder eine Verteilerliste öffnen, rufen Sie [IAddrBook::OpenEntry auf.](iaddrbook-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="a1664-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="a1664-149">Diese spezifischere Methoden sind schneller als **IMAPISupport::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="a1664-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="a1664-150">**IMAPISupport::OpenEntry** öffnet alle Objekte als schreibgeschützt, es sei denn, Sie legen das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im  _ulFlags-Parameter_ ein, und Ihre Berechtigungen sind ausreichend.</span><span class="sxs-lookup"><span data-stu-id="a1664-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="a1664-151">Das Festlegen eines dieser Kennzeichen garantiert keine bestimmte Art von Zugriff. Die Ihnen erteilten Berechtigungen hängen von Ihrer Zugriffsebene, dem Objekt und dem Dienstanbieter ab, der das Objekt besitzt.</span><span class="sxs-lookup"><span data-stu-id="a1664-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="a1664-152">Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie die **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) -Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="a1664-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a1664-153">Überprüfen Sie den im  _lpulObjType-Parameter_ zurückgegebenen Wert, um zu ermitteln, ob der zurückgegebene Objekttyp den erwarteten Wert hat.</span><span class="sxs-lookup"><span data-stu-id="a1664-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="a1664-154">Wenn der Objekttyp wie erwartet ist, wird der Zeiger vom  _lppUnk-Parameter_ in einen Zeiger des entsprechenden Typs umgekippt.</span><span class="sxs-lookup"><span data-stu-id="a1664-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="a1664-155">Wenn Sie z. B. einen Ordner öffnen, wird  _lppUnk_ in einen Zeiger vom Typ LPMAPIFOLDER verschoben.</span><span class="sxs-lookup"><span data-stu-id="a1664-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1664-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1664-156">See also</span></span>



[<span data-ttu-id="a1664-157">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1664-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

