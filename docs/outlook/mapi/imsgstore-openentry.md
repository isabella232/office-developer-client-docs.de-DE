---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409335"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="51193-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="51193-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="51193-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51193-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51193-105">Öffnet einen Ordner oder eine Nachricht und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="51193-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="51193-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51193-106">Parameters</span></span>

 <span data-ttu-id="51193-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="51193-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="51193-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird _._</span><span class="sxs-lookup"><span data-stu-id="51193-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="51193-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="51193-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="51193-110">in Ein Zeiger auf die Eintrags-ID des zu öffnenden Objekts oder NULL.</span><span class="sxs-lookup"><span data-stu-id="51193-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="51193-111">Wenn _lpEntryID_ auf NULL festgelegt ist \*\*\*\* , öffnet OpenEntry den Stammordner für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="51193-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="51193-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="51193-112">_lpInterface_</span></span>
  
> <span data-ttu-id="51193-113">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51193-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="51193-114">Das übergeben von NULL-Ergebnissen in der Standardschnittstelle des Objekts ([IMAPIFolder](imapifolderimapicontainer.md) für Ordner und [IMessage](imessageimapiprop.md) für Nachrichten) wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51193-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="51193-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="51193-115">_ulFlags_</span></span>
  
> <span data-ttu-id="51193-116">in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="51193-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="51193-117">Die folgenden Flags können verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="51193-117">The following flags can be used:</span></span>
    
<span data-ttu-id="51193-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="51193-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="51193-119">Fordert, dass das Objekt unter Verwendung der maximal für den Benutzer zulässigen Netzwerkberechtigungen und des maximalen Client Anwendungszugriffs geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="51193-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="51193-120">Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte das Objekt mithilfe der Lese-/Schreibzugriff-Berechtigung geöffnet werden. Wenn der Client schreibgeschützte Berechtigung hat, sollte das Objekt mithilfe der Read-Only-Berechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="51193-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="51193-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="51193-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="51193-122">Ermöglicht \*\*\*\* das erfolgreiche zurückgeben von OpenEntry, bevor das Objekt vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="51193-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="51193-123">Wenn das Objekt nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="51193-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="51193-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="51193-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="51193-125">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="51193-125">Requests read/write permission.</span></span> <span data-ttu-id="51193-126">Standardmäßig werden Objekte mit Schreibschutz Berechtigung geöffnet, und Clients sollten nicht mit der Annahme arbeiten, dass Lese-/Schreibzugriff erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="51193-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="51193-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="51193-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="51193-128">Out Ein Zeiger auf den Typ des geöffneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="51193-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="51193-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="51193-129">_lppUnk_</span></span>
  
> <span data-ttu-id="51193-130">Out Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="51193-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51193-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51193-131">Return value</span></span>

<span data-ttu-id="51193-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="51193-132">S_OK</span></span> 
  
> <span data-ttu-id="51193-133">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="51193-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="51193-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="51193-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="51193-135">Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="51193-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="51193-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="51193-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="51193-137">Wenn ein Speicher im Cache-Modus geöffnet wird, kann ein Client oder Dienstanbieter **IMsgStore:: OpenEntry**aufrufen und das MAPI_NO_CACHE-Flag festlegen, um ein Element oder einen Ordner im Remotespeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="51193-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="51193-138">Wenn Sie den Nachrichtenspeicher mit dem MDB_ONLINE-Flag auf dem Remoteserver öffnen, müssen Sie das MAPI_NO_CACHE-Flag nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="51193-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51193-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51193-139">Remarks</span></span>

<span data-ttu-id="51193-140">Die **IMsgStore:: OpenEntry** -Methode öffnet einen Ordner oder eine Nachricht und gibt einen Zeiger auf eine Schnittstelle zurück, die für weiteren Zugriff verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="51193-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="51193-141">Beim Öffnen von Ordnereinträgen in einem öffentlichen Informationsspeicher wie Ordner und Nachrichten verwenden Sie **IMsgStore:: OpenEntry** anstelle von [IMAPISession:: OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="51193-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="51193-142">Dadurch wird sichergestellt, dass öffentliche Ordner ordnungsgemäß funktionieren, wenn mehrere Exchange-Konten in einem Profil definiert sind.</span><span class="sxs-lookup"><span data-stu-id="51193-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="51193-143">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="51193-143">Notes to callers</span></span>

<span data-ttu-id="51193-144">Ordner und Nachrichten werden automatisch mit Schreibschutz Berechtigung geöffnet, es sei denn, Sie legen das MAPI_MODIFY-oder MAPI_BEST_ACCESS-Flag im _ulFlags_ -Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="51193-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="51193-145">Durch Festlegen eines dieser Flags kann kein bestimmter Berechtigungstyp garantiert werden. die Berechtigungen, die Ihnen erteilt werden, hängen vom Nachrichtenspeicher Anbieter, der Zugriffsebene und dem Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="51193-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="51193-146">Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie die **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="51193-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="51193-147">Obwohl **IMsgStore:: OpenEntry** zum Öffnen von Ordnern oder Nachrichten verwendet werden kann, ist es in der Regel schneller, die [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) -Methode zu verwenden, wenn Sie Zugriff auf den übergeordneten Ordner des Ordners oder der Nachricht haben, der geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51193-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="51193-148">Überprüfen Sie den Wert, der im _lpulObjType_ -Parameter zurückgegeben wird, um zu bestimmen, ob der zurückgegebene Objekttyp Ihren Erwartungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="51193-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="51193-149">Wenn der Objekttyp nicht der erwartete Typ ist, wandeln Sie den Zeiger vom _lppUnk_ -Parameter in einen Zeiger des entsprechenden Typs um.</span><span class="sxs-lookup"><span data-stu-id="51193-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="51193-150">Wenn Sie beispielsweise einen Ordner öffnen, werfen Sie _lppUnk_ in einen Zeiger vom Typ **LPMAPIFOLDER**.</span><span class="sxs-lookup"><span data-stu-id="51193-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="51193-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="51193-151">MFCMAPI reference</span></span>

<span data-ttu-id="51193-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="51193-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="51193-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="51193-153">**File**</span></span>|<span data-ttu-id="51193-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="51193-154">**Function**</span></span>|<span data-ttu-id="51193-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="51193-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="51193-156">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="51193-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="51193-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="51193-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="51193-158">MFCMAPI verwendet die **IMsgStore:: OpenEntry** -Methode, um das Objekt zu öffnen, das einer EINTRAGS-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="51193-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51193-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51193-159">See also</span></span>



[<span data-ttu-id="51193-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="51193-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="51193-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="51193-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="51193-162">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="51193-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

