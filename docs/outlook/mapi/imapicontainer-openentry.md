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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286932"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="2f428-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="2f428-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="2f428-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f428-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f428-105">Öffnet ein Objekt im Container und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="2f428-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2f428-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f428-106">Parameters</span></span>

 <span data-ttu-id="2f428-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2f428-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="2f428-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2f428-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2f428-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2f428-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="2f428-110">in Ein Zeiger auf die Eintrags-ID des zu öffnenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="2f428-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="2f428-111">Wenn _lpEntryID_ auf NULL festgelegt ist, wird der Container der obersten Ebene in der Hierarchie des Containers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2f428-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="2f428-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="2f428-112">_lpInterface_</span></span>
  
> <span data-ttu-id="2f428-113">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f428-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="2f428-114">Das übergeben von NULL führt zu dem Bezeichner für die zurückgegebene Standardschnittstelle des Objekts.</span><span class="sxs-lookup"><span data-stu-id="2f428-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="2f428-115">Bei Nachrichten lautet die Standardschnittstelle [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); für Ordner ist es [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="2f428-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="2f428-116">Die Standardschnittstellen für Adressbuch Objekte sind [IDistList: IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser: IMAPIProp](imailuserimapiprop.md) für einen Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="2f428-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="2f428-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2f428-117">_ulFlags_</span></span>
  
> <span data-ttu-id="2f428-118">in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2f428-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="2f428-119">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2f428-119">The following flags can be set:</span></span>
    
<span data-ttu-id="2f428-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2f428-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="2f428-121">Fordert, dass das Objekt mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und dem maximalen Zugriff auf Clientanwendungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2f428-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="2f428-122">Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte das Objekt mit Lese-/Schreibzugriff geöffnet werden. Wenn der Client schreibgeschützten Zugriff hat, sollte das Objekt mit Schreibschutz geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="2f428-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="2f428-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="2f428-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="2f428-124">Ermöglicht \*\*\*\* das erfolgreiche zurückgeben von OpenEntry, bevor das Objekt vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2f428-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="2f428-125">Wenn das Objekt nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2f428-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="2f428-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="2f428-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="2f428-127">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="2f428-127">Requests read/write permission.</span></span> <span data-ttu-id="2f428-128">Standardmäßig werden Objekte mit Schreibschutz geöffnet, und Clients sollten nicht unter der Annahme arbeiten, dass die Berechtigung zum Lesen/Schreiben erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="2f428-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="2f428-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="2f428-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="2f428-130">Zeigt Elemente an, die derzeit als weich gelöscht markiert sind, d. h., Sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente.</span><span class="sxs-lookup"><span data-stu-id="2f428-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="2f428-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="2f428-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="2f428-132">Out Ein Zeiger auf den Typ des geöffneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="2f428-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="2f428-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="2f428-133">_lppUnk_</span></span>
  
> <span data-ttu-id="2f428-134">Out Ein Zeiger auf einen Zeiger auf die Schnittstellenimplementierung, die für den Zugriff auf das Open-Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f428-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2f428-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f428-135">Return value</span></span>

<span data-ttu-id="2f428-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="2f428-136">S_OK</span></span> 
  
> <span data-ttu-id="2f428-137">Das Objekt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2f428-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="2f428-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2f428-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="2f428-139">Entweder hat der Benutzer unzureichende Berechtigungen zum Öffnen des Objekts oder es wurde versucht, ein schreibgeschütztes Objekt mit Lese-/Schreibzugriff zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2f428-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="2f428-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2f428-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2f428-141">Die durch _lpEntryID_ angegebene Eintrags-ID stellt kein Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="2f428-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="2f428-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2f428-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="2f428-143">Die Eintrags-ID im _lpEntryID_ -Parameter weist kein Format auf, das vom Container erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="2f428-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2f428-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f428-144">Remarks</span></span>

<span data-ttu-id="2f428-145">Die **IMAPIContainer:: OpenEntry** -Methode öffnet ein Objekt in einem Container und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, die für weiteren Zugriff verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f428-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2f428-146">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="2f428-146">Notes to callers</span></span>

<span data-ttu-id="2f428-147">Da es für Dienstanbieter nicht erforderlich ist, eine Schnittstellenimplementierung des durch den Schnittstellenbezeichner im _lpInterface_ -Parameter angegebenen Typs zurückzugeben, überprüfen Sie den Wert, der durch den _lpulObjType_ -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="2f428-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="2f428-148">Falls erforderlich, wandeln Sie den in _lppUnk_ zurückgegebenen Zeiger in einen Zeiger des entsprechenden Typs um.</span><span class="sxs-lookup"><span data-stu-id="2f428-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="2f428-149">Standardmäßig öffnen Dienstanbieter Objekte mit schreibgeschütztem Zugriff, es sei denn, Sie legen das MAPI_MODIFY-oder MAPI_BEST_ACCESS-Flag fest.</span><span class="sxs-lookup"><span data-stu-id="2f428-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="2f428-150">Wenn eines dieser Flags festgelegt ist, versuchen Dienstanbieter, ein änderbares Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="2f428-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="2f428-151">Sie sollten jedoch nicht davon ausgehen, dass Sie ein änderbares Objekt angefordert haben, dass das geöffnete Objekt Lese-/Schreibzugriff hat.</span><span class="sxs-lookup"><span data-stu-id="2f428-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="2f428-152">Planen Sie entweder, ob eine spätere Änderung fehlschlagen soll, oder rufen Sie die **PR_ACCESS_LEVEL** -Eigenschaft des Objekts ab, um die \*\*\*\* von OpenEntry erteilte Zugriffsebene zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2f428-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f428-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f428-153">See also</span></span>



[<span data-ttu-id="2f428-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2f428-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

