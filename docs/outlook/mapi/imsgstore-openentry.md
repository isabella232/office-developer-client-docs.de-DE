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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 124208a3f5c6bb300aca3699a04b15e842c46cd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792646"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="10c98-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="10c98-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="10c98-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10c98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10c98-105">Öffnet einen Ordner oder eine Nachricht, und gibt einen Schnittstellenzeiger für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="10c98-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="10c98-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10c98-106">Parameters</span></span>

 <span data-ttu-id="10c98-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="10c98-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="10c98-108">[in] Die Byteanzahl von in die Eintrags-ID auf das durch den Parameter _LpEntryID_ _._</span><span class="sxs-lookup"><span data-stu-id="10c98-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="10c98-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="10c98-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="10c98-110">[in] Ein Zeiger auf die Eintrags-ID des-Objekts zum Öffnen oder NULL.</span><span class="sxs-lookup"><span data-stu-id="10c98-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="10c98-111">Wenn _LpEntryID_ auf NULL festgelegt ist, wird **OpenEntry** Stammordner für den Nachrichtenspeicher geöffnet.</span><span class="sxs-lookup"><span data-stu-id="10c98-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="10c98-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="10c98-112">_lpInterface_</span></span>
  
> <span data-ttu-id="10c98-113">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, den Zugriff auf die geöffnete Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="10c98-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="10c98-114">Bei Übergabe von NULL führt das Objekt des standard-Schnittstelle ([IMAPIFolder](imapifolderimapicontainer.md) für Ordner) und [IMessage](imessageimapiprop.md) für Nachrichten zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10c98-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="10c98-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="10c98-115">_ulFlags_</span></span>
  
> <span data-ttu-id="10c98-116">[in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="10c98-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="10c98-117">Die folgenden Werte können verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="10c98-117">The following flags can be used:</span></span>
    
<span data-ttu-id="10c98-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="10c98-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="10c98-119">Fordert an, dass das Objekt geöffnet werden, mithilfe der maximale Netzwerkberechtigungen für den Benutzer und die maximale Clientzugriff Anwendung zulässig.</span><span class="sxs-lookup"><span data-stu-id="10c98-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="10c98-120">Wenn der Client über Lese-/Schreibberechtigung verfügt, sollte beispielsweise das Objekt geöffnet werden mithilfe von Lese-/Schreibberechtigung für; Wenn der Client nur-Lese-Berechtigung verfügt, sollte das Objekt mithilfe von schreibgeschützt geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="10c98-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="10c98-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="10c98-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="10c98-122">Ermöglicht **OpenEntry** erfolgreich, möglicherweise beendet, bevor das Objekt an den aufrufenden Client vollständig verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="10c98-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="10c98-123">Wenn das Objekt nicht verfügbar ist, kann die nachfolgenden Objekt Anrufen ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="10c98-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="10c98-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="10c98-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="10c98-125">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="10c98-125">Requests read/write permission.</span></span> <span data-ttu-id="10c98-126">Standardmäßig werden Objekte mit Leseberechtigung geöffnet, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="10c98-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="10c98-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="10c98-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="10c98-128">[out] Ein Zeiger auf den Typ des Objekts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="10c98-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="10c98-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="10c98-129">_lppUnk_</span></span>
  
> <span data-ttu-id="10c98-130">[out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="10c98-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10c98-131">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="10c98-131">Return value</span></span>

<span data-ttu-id="10c98-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="10c98-132">S_OK</span></span> 
  
> <span data-ttu-id="10c98-133">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="10c98-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="10c98-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="10c98-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="10c98-135">Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="10c98-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="10c98-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="10c98-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="10c98-137">Wenn ein Speichers im Cache-Modus geöffnet wird, kann ein Client oder Dienstanbieter **IMsgStore::OpenEntry**, das MAPI_NO_CACHE-Flag zum Öffnen eines Elements oder einen Ordner auf dem remote-Speicher aufrufen.</span><span class="sxs-lookup"><span data-stu-id="10c98-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="10c98-138">Wenn Sie den Nachrichtenspeicher mit dem MDB_ONLINE-Flag auf dem Remoteserver öffnen, müssen Sie nicht das Flag MAPI_NO_CACHE verwenden.</span><span class="sxs-lookup"><span data-stu-id="10c98-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10c98-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="10c98-139">Remarks</span></span>

<span data-ttu-id="10c98-140">Die **IMsgStore::OpenEntry** -Methode öffnet ein Ordner oder eine Nachricht und gibt einen Zeiger auf eine Schnittstelle, die für eine zusätzliche Access verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="10c98-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="10c98-141">Beim Öffnen der Einträge im Ordner in einem öffentlichen Speicher, wie Ordner und Nachrichten, verwenden Sie anstelle von [IMAPISession::OpenEntry](imapisession-openentry.md) **IMsgStore::OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="10c98-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="10c98-142">Dadurch wird die Funktion für Öffentliche Ordner ordnungsgemäß sichergestellt, wenn in einem Profil mehrere Exchange-Konten definiert sind.</span><span class="sxs-lookup"><span data-stu-id="10c98-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="10c98-143">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="10c98-143">Notes to callers</span></span>

<span data-ttu-id="10c98-144">Ordner und Nachrichten werden automatisch mit Leseberechtigung, geöffnet, es sei denn, Sie die Kennzeichen MAPI_MODIFY oder MAPI_BEST_ACCESS in der _UlFlags_ -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="10c98-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="10c98-145">Festlegen einer dieser Flags garantiert keine bestimmte Art von Berechtigung. die Berechtigungen, die Sie erteilt werden, abhängig von der Nachricht Informationsdienst, Ihre Zugriffsebene und das Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="10c98-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="10c98-146">Rufen Sie zum Bestimmen der Zugriffsebene des geöffneten-Objekts, dessen **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="10c98-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="10c98-147">Obwohl **IMsgStore::OpenEntry** zum Öffnen eines beliebigen Ordners oder einer Nachricht verwendet werden können, ist es in der Regel schneller die [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) -Methode verwenden, wenn Sie haben Zugriff auf den übergeordneten Ordner des Ordners oder Nachricht geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="10c98-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="10c98-148">Überprüfen Sie den Wert im _LpulObjType_ -Parameter bestimmt, ob der zurückgegebene Objekttyp ist, was Sie erwartet zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="10c98-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="10c98-149">Wenn der Objekttyp nicht dem erwarteten Typ ist, wandeln Sie den Zeiger auf einen Zeiger des entsprechenden Typs aus dem _LppUnk_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="10c98-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="10c98-150">Angenommen, wenn Sie einen Ordner öffnen, _LppUnk_ auf einen Zeiger vom Typ **LPMAPIFOLDER**umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="10c98-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="10c98-151">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="10c98-151">MFCMAPI reference</span></span>

<span data-ttu-id="10c98-152">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="10c98-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="10c98-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="10c98-153">**File**</span></span>|<span data-ttu-id="10c98-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="10c98-154">**Function**</span></span>|<span data-ttu-id="10c98-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="10c98-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="10c98-156">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="10c98-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="10c98-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="10c98-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="10c98-158">MFCMAPI (engl.) verwendet die **IMsgStore::OpenEntry** -Methode zum Öffnen des Objekts eines Eintrags-ID zugeordnet</span><span class="sxs-lookup"><span data-stu-id="10c98-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10c98-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10c98-159">See also</span></span>



[<span data-ttu-id="10c98-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="10c98-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="10c98-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="10c98-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="10c98-162">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="10c98-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

