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
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423636"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="3ea4a-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3ea4a-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="3ea4a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ea4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ea4a-105">Öffnet ein Objekt im Container und gibt einen Schnittstellenzeiger für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="3ea4a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ea4a-106">Parameters</span></span>

 <span data-ttu-id="3ea4a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3ea4a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="3ea4a-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3ea4a-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="3ea4a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="3ea4a-110">[in] Ein Zeiger auf den Eintragsbezeichner des zu öffnende Objekts.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="3ea4a-111">Wenn  _lpEntryID_ auf NULL festgelegt ist, wird der Container auf oberster Ebene in der Containerhierarchie geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="3ea4a-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="3ea4a-112">_lpInterface_</span></span>
  
> <span data-ttu-id="3ea4a-113">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="3ea4a-114">Das Übergeben von NULL führt dazu, dass der Bezeichner für die Standardschnittstelle des Objekts zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="3ea4a-115">Für Nachrichten ist die Standardschnittstelle [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); für Ordner ist es [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="3ea4a-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="3ea4a-116">Die Standardschnittstellen für Adressbuchobjekte sind [IDistList : IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser : IMAPIProp](imailuserimapiprop.md) für einen Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="3ea4a-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ea4a-117">_ulFlags_</span></span>
  
> <span data-ttu-id="3ea4a-118">[in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="3ea4a-119">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3ea4a-119">The following flags can be set:</span></span>
    
<span data-ttu-id="3ea4a-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="3ea4a-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="3ea4a-121">Fordert an, dass das Objekt mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und dem maximalen Clientanwendungszugriff geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="3ea4a-122">Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützten Zugriff verfügt, sollte das Objekt mit schreibgeschützten Zugriff geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="3ea4a-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="3ea4a-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="3ea4a-124">Ermöglicht **openEntry** die erfolgreiche Rückgabe, möglicherweise bevor das Objekt vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="3ea4a-125">Wenn das Objekt nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="3ea4a-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="3ea4a-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="3ea4a-127">Fordert Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-127">Requests read/write permission.</span></span> <span data-ttu-id="3ea4a-128">Standardmäßig werden Objekte mit schreibgeschützten Zugriff geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="3ea4a-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="3ea4a-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="3ea4a-130">Zeigt Elemente an, die derzeit als "soft deleted" gekennzeichnet sind, d. h. sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="3ea4a-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="3ea4a-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="3ea4a-132">[out] Ein Zeiger auf den Typ des geöffneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="3ea4a-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="3ea4a-133">_lppUnk_</span></span>
  
> <span data-ttu-id="3ea4a-134">[out] Ein Zeiger auf einen Zeiger auf die Schnittstellenimplementierung, die für den Zugriff auf das geöffnete Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ea4a-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ea4a-135">Return value</span></span>

<span data-ttu-id="3ea4a-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ea4a-136">S_OK</span></span> 
  
> <span data-ttu-id="3ea4a-137">Das Objekt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="3ea4a-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="3ea4a-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="3ea4a-139">Entweder verfügt der Benutzer nicht über ausreichende Berechtigungen zum Öffnen des Objekts, oder es wurde versucht, ein schreibgeschütztes Objekt mit Lese-/Schreibberechtigung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="3ea4a-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3ea4a-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3ea4a-141">Der von  _lpEntryID_ angegebene Eintragsbezeichner stellt kein Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="3ea4a-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3ea4a-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="3ea4a-143">Der Eintragsbezeichner im  _lpEntryID-Parameter_ hat kein vom Container erkanntes Format.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3ea4a-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3ea4a-144">Remarks</span></span>

<span data-ttu-id="3ea4a-145">Die **IMAPIContainer::OpenEntry-Methode** öffnet ein Objekt in einem Container und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, die für weiteren Zugriff verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3ea4a-146">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3ea4a-146">Notes to callers</span></span>

<span data-ttu-id="3ea4a-147">Da Dienstanbieter keine Schnittstellenimplementierung des typs zurückgeben müssen, der durch den Schnittstellenbezeichner im  _lpInterface-Parameter_ angegeben wird, überprüfen Sie den Wert, auf den der  _lpulObjType-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="3ea4a-148">Bei Bedarf wird der in  _lppUnk_ zurückgegebene Zeiger in einen Zeiger des entsprechenden Typs umgekippt.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="3ea4a-149">Standardmäßig öffnen Dienstanbieter Objekte mit schreibgeschützten Zugriffen, es sei denn, Sie legen MAPI_MODIFY oder MAPI_BEST_ACCESS ein.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="3ea4a-150">Wenn eines dieser Kennzeichen festgelegt ist, versuchen Dienstanbieter, ein veränderbares Objekt zurückzusenken.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="3ea4a-151">Gehen Sie jedoch nicht davon aus, dass das geöffnete Objekt über Lese-/Schreibberechtigungen verfügt, da Sie ein veränderbares Objekt angefordert haben.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="3ea4a-152">Planen Sie entweder, dass eine nachfolgende Änderung fehlschlägt, oder rufen Sie die **PR_ACCESS_LEVEL-Eigenschaft** des Objekts ab, um die von **OpenEntry** gewährte Zugriffsebene zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3ea4a-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ea4a-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ea4a-153">See also</span></span>



[<span data-ttu-id="3ea4a-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3ea4a-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

