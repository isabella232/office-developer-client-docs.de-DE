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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 04bf7f2ddda7377df72417df2472246a2cf329bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792403"
---
# <a name="imapisupportopenentry"></a><span data-ttu-id="0dae1-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0dae1-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="0dae1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0dae1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0dae1-105">Öffnet ein Objekt und gibt einen Schnittstellenzeiger für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="0dae1-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="0dae1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dae1-106">Parameters</span></span>

 <span data-ttu-id="0dae1-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0dae1-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="0dae1-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="0dae1-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0dae1-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0dae1-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="0dae1-110">[in] Ein Zeiger auf die Eintrags-ID des Objekts zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0dae1-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="0dae1-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0dae1-111">_lpInterface_</span></span>
  
> <span data-ttu-id="0dae1-112">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, Zugriff auf das Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0dae1-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="0dae1-113">Bei Übergabe von NULL führt das Objekt Standardschnittstelle zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0dae1-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="0dae1-114">Wenn das Objekt geöffnet werden soll, eine Nachricht ist, ist der standard-Benutzeroberfläche beispielsweise [IMessage](imessageimapiprop.md); Ordner ist es [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0dae1-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="0dae1-115">Die standard-Schnittstellen für Address Book-Objekten sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für ein messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0dae1-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="0dae1-116">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="0dae1-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="0dae1-117">[in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="0dae1-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="0dae1-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0dae1-118">The following flags can be set:</span></span>
    
<span data-ttu-id="0dae1-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0dae1-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="0dae1-120">Fordert an, dass das Objekt mit den maximale Netzwerkberechtigungen für den Anrufer zulässig geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="0dae1-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="0dae1-121">Wenn der Aufrufer Lese-/Schreibberechtigung verfügt, sollte das Objekt beispielsweise mit Lese-/Schreibzugriff geöffnet werden; Wenn der Aufrufer nur-Lese-Berechtigung verfügt, sollte das Objekt als schreibgeschützt geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="0dae1-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="0dae1-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0dae1-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0dae1-123">**OpenEntry** erfolgreich, möglicherweise beendet, bevor das Objekt an den Anrufer vollständig zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0dae1-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="0dae1-124">Wenn das Objekt nicht möglich ist, kann nachfolgende Objekt Anrufen ein Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="0dae1-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="0dae1-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0dae1-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0dae1-126">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="0dae1-126">Requests read/write permission.</span></span> <span data-ttu-id="0dae1-127">In der Standardeinstellung Objekte werden als schreibgeschützt geöffnet, und Anrufer sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="0dae1-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="0dae1-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="0dae1-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="0dae1-129">[out] Ein Zeiger auf den Typ des Objekts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0dae1-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="0dae1-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="0dae1-130">_lppUnk_</span></span>
  
> <span data-ttu-id="0dae1-131">[out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="0dae1-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0dae1-132">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0dae1-132">Return value</span></span>

<span data-ttu-id="0dae1-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="0dae1-133">S_OK</span></span> 
  
> <span data-ttu-id="0dae1-134">Das Objekt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0dae1-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="0dae1-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0dae1-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0dae1-136">Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, ein Objekt zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="0dae1-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="0dae1-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0dae1-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0dae1-138">Es ist kein Objekt zugeordneten die Eintrags-ID in der _LpEntryID_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="0dae1-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="0dae1-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0dae1-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="0dae1-140">Die Eintrags-ID in der _LpEntryID_ -Parameter übergeben wird in einem Format nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="0dae1-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="0dae1-141">Dieser Wert wird in der Regel zurückgegeben, wenn die Adressbuchanbieter, die das Objekt enthält nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="0dae1-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0dae1-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0dae1-142">Remarks</span></span>

<span data-ttu-id="0dae1-143">Die **IMAPISupport::OpenEntry** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert.</span><span class="sxs-lookup"><span data-stu-id="0dae1-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="0dae1-144">Dienstanbieter anrufen **IMAPISupport::OpenEntry** um einen Zeiger auf eine Schnittstelle abzurufen, die verwendet werden kann, um auf ein bestimmtes Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="0dae1-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0dae1-145">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0dae1-145">Notes to callers</span></span>

<span data-ttu-id="0dae1-146">Rufen Sie **IMAPISupport::OpenEntry** nur, wenn Sie nicht wissen, welche Art Objekt Sie öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="0dae1-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="0dae1-147">Wenn Sie, dass Sie einen Ordner oder eine Nachricht öffnen wissen, rufen Sie stattdessen [IMsgStore::OpenEntry](imsgstore-openentry.md) .</span><span class="sxs-lookup"><span data-stu-id="0dae1-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="0dae1-148">Wenn Sie, dass Sie ein Adressbuchcontainer, ein messaging-Benutzer oder eine Verteilerliste öffnen wissen, rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="0dae1-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="0dae1-149">Diese bestimmten Methoden sind schneller als **IMAPISupport::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="0dae1-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="0dae1-150">**IMAPISupport::OpenEntry** öffnet alle Objekte als schreibgeschützt, es sei denn, Sie legen Sie das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im _UlFlags_ -Parameter und Ihre Berechtigungen ausreichend sind.</span><span class="sxs-lookup"><span data-stu-id="0dae1-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="0dae1-151">Festlegen einer dieser Flags garantiert keine bestimmte Art von Zugriff. die Berechtigungen, die Sie erteilt werden abhängig von Ihrer Zugriffsebene, die-Objekts und der Dienstanbieter, der das Objekt besitzt.</span><span class="sxs-lookup"><span data-stu-id="0dae1-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="0dae1-152">Rufen Sie zum Bestimmen der Zugriffsebene des geöffneten-Objekts, dessen **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="0dae1-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="0dae1-153">Überprüfen Sie den Wert in der _LpulObjType_ -Parameter, um zu bestimmen, dass der Objekttyp zurückgegeben wird, was Sie erwartet zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0dae1-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="0dae1-154">Wenn der Objekttyp ist wie erwartet, wandeln Sie den Zeiger auf einen Zeiger des entsprechenden Typs aus dem _LppUnk_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="0dae1-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="0dae1-155">Angenommen, wenn Sie einen Ordner öffnen, _LppUnk_ auf einen Zeiger vom Typ LPMAPIFOLDER umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="0dae1-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0dae1-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dae1-156">See also</span></span>



[<span data-ttu-id="0dae1-157">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0dae1-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

