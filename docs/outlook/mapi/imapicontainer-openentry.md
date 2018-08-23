---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cd93866ae8823eb5897318fc2dda4e8432d974b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578465"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="aac96-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="aac96-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="aac96-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aac96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aac96-105">Öffnet ein Objekt im Container einen Schnittstellenzeiger für den weiteren Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="aac96-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="aac96-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aac96-106">Parameters</span></span>

 <span data-ttu-id="aac96-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="aac96-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="aac96-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="aac96-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="aac96-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="aac96-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="aac96-110">[in] Ein Zeiger auf die Eintrags-ID des Objekts zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aac96-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="aac96-111">Wenn _LpEntryID_ auf NULL festgelegt ist, wird der Container der obersten Ebene in der Hierarchie des Containers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="aac96-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="aac96-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="aac96-112">_lpInterface_</span></span>
  
> <span data-ttu-id="aac96-113">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, Zugriff auf das Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="aac96-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="aac96-114">Bei Übergabe von NULL führt den Bezeichner für das Objekt Standardschnittstelle zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aac96-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="aac96-115">Für Nachrichten, die standard-Schnittstelle ist [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); für Ordner, es ist [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="aac96-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="aac96-116">Der Standard-Schnittstellen für Address Book-Objekten sind [IDistList: IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser: IMAPIProp](imailuserimapiprop.md) für ein messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="aac96-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="aac96-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aac96-117">_ulFlags_</span></span>
  
> <span data-ttu-id="aac96-118">[in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="aac96-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="aac96-119">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="aac96-119">The following flags can be set:</span></span>
    
<span data-ttu-id="aac96-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="aac96-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="aac96-121">Fordert an, dass das Objekt mit den maximale Netzwerkberechtigungen für den Benutzer und die maximale Anwendung Clientzugriff zulässig geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="aac96-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="aac96-122">Beispielsweise sollte der Client Lese-/Schreibberechtigung verfügt, das Objekt mit Lese-/Schreibzugriff geöffnet werden; Wenn der Client schreibgeschützten Zugriff hat, sollte das Objekt mit schreibgeschützten Zugriff geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="aac96-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="aac96-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="aac96-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="aac96-124">Ermöglicht **OpenEntry** erfolgreich, möglicherweise beendet, bevor das Objekt an den aufrufenden Client vollständig verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aac96-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="aac96-125">Wenn das Objekt nicht verfügbar ist, kann die nachfolgenden Objekt Anrufen ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="aac96-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="aac96-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="aac96-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="aac96-127">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="aac96-127">Requests read/write permission.</span></span> <span data-ttu-id="aac96-128">Standardmäßig werden Objekte mit schreibgeschützten Zugriff geöffnet, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="aac96-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="aac96-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="aac96-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="aac96-130">Zeigt Elemente, die derzeit als soft gekennzeichnet sind gelöscht – d. h., sie sind in der Aufbewahrungszeit für gelöschte Elemente Zeit Phase.</span><span class="sxs-lookup"><span data-stu-id="aac96-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="aac96-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="aac96-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="aac96-132">[out] Ein Zeiger auf die geöffnete Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="aac96-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="aac96-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="aac96-133">_lppUnk_</span></span>
  
> <span data-ttu-id="aac96-134">[out] Ein Zeiger auf einen Zeiger auf die Implementierung eines verwenden, um das geöffnete Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="aac96-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aac96-135">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="aac96-135">Return value</span></span>

<span data-ttu-id="aac96-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="aac96-136">S_OK</span></span> 
  
> <span data-ttu-id="aac96-137">Das Objekt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="aac96-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="aac96-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="aac96-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="aac96-139">Der Benutzer verfügt nicht über ausreichende Berechtigungen zum Öffnen des Objekts oder es wurde versucht, ein nur-Lese-Objekt mit Lese-/Schreibzugriff zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aac96-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="aac96-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aac96-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="aac96-141">Die _LpEntryID_ angegebene Eintrags-ID stellt kein Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="aac96-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="aac96-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="aac96-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="aac96-143">Die Eintrags-ID in der _LpEntryID_ -Parameter ist nicht vom durch das Container erkanntes Format.</span><span class="sxs-lookup"><span data-stu-id="aac96-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aac96-144">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="aac96-144">Remarks</span></span>

<span data-ttu-id="aac96-145">Die **IMAPIContainer::OpenEntry** -Methode öffnet ein Objekt in der gesamten ein Container und gibt einen Zeiger auf eine Implementierung für weitere Access verwenden.</span><span class="sxs-lookup"><span data-stu-id="aac96-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aac96-146">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="aac96-146">Notes to callers</span></span>

<span data-ttu-id="aac96-147">Da Dienstanbieter nicht erforderlich sind, um eine Implementierung der von der Schnittstelle-ID in der _LpInterface_ -Parameter angegebenen Typs zurückzugeben, überprüfen Sie den Wert, der auf den durch den Parameter _LpulObjType_ .</span><span class="sxs-lookup"><span data-stu-id="aac96-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="aac96-148">Wandeln Sie den Zeiger auf einen Zeiger des entsprechenden Typs in _LppUnk_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aac96-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="aac96-149">Standardmäßig öffnen Dienstanbieter Objekte mit schreibgeschützten Zugriff, es sei denn, Sie entweder die MAPI_MODIFY oder MAPI_BEST_ACCESS-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="aac96-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="aac96-150">Wenn eine der folgenden Werte festgelegt ist, versuchen Dienstanbieter, ein änderbare-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="aac96-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="aac96-151">Allerdings nehmen Sie nicht an, die, da Sie ein Objekt geändert werden, dass das geöffnete Objekt Lese-/Schreibberechtigung hat angefordert haben.</span><span class="sxs-lookup"><span data-stu-id="aac96-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="aac96-152">Entweder die Möglichkeit der Änderung einer nachfolgenden fehl, oder rufen Sie das Objekt **PR_ACCESS_LEVEL** -Eigenschaft, gewährt durch **OpenEntry**Zugriffsstufe planen.</span><span class="sxs-lookup"><span data-stu-id="aac96-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aac96-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aac96-153">See also</span></span>



[<span data-ttu-id="aac96-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aac96-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

