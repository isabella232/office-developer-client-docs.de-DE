---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f23b4855b7e2faeb599868f8c2db52ae9cbfbfd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792310"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="04fe0-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="04fe0-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="04fe0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04fe0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04fe0-105">Öffnet ein Objekt und gibt einen Schnittstellenzeiger für zusätzliche Zugriff.</span><span class="sxs-lookup"><span data-stu-id="04fe0-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="04fe0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04fe0-106">Parameters</span></span>

 <span data-ttu-id="04fe0-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="04fe0-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="04fe0-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="04fe0-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="04fe0-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="04fe0-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="04fe0-110">[in] Ein Zeiger auf die Eintrags-ID des Objekts zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="04fe0-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="04fe0-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="04fe0-111">_lpInterface_</span></span>
  
> <span data-ttu-id="04fe0-112">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, den Zugriff auf die geöffnete Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="04fe0-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="04fe0-113">Übergeben von NULL gibt Standardschnittstelle für das Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="04fe0-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="04fe0-114">Wenn das Objekt geöffnet werden soll, eine Nachricht ist, ist der standard-Benutzeroberfläche beispielsweise [IMessage](imessageimapiprop.md); Ordner ist es [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="04fe0-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="04fe0-115">Die standard-Schnittstellen für Address Book-Objekten sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für ein messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="04fe0-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="04fe0-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="04fe0-116">_ulFlags_</span></span>
  
> <span data-ttu-id="04fe0-117">[in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="04fe0-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="04fe0-118">Die folgenden Werte können verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="04fe0-118">The following flags can be used:</span></span>
    
<span data-ttu-id="04fe0-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="04fe0-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="04fe0-120">Fordert an, dass das Objekt geöffnet werden, mithilfe der maximale Netzwerkberechtigungen für den Benutzer und die maximale Clientzugriff Anwendung zulässig.</span><span class="sxs-lookup"><span data-stu-id="04fe0-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="04fe0-121">Beispielsweise sollte der Client Lese-/Schreibberechtigung verfügt, das Objekt mit Lese-/Schreibzugriff geöffnet werden; Wenn der Client nur-Lese-Berechtigung verfügt, sollte das Objekt mit Leseberechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="04fe0-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="04fe0-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="04fe0-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="04fe0-123">Verwenden Sie alle Mittel, einschließlich Offlineadressbücher, um namensauflösung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="04fe0-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="04fe0-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="04fe0-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="04fe0-125">Verwenden Sie nur das Offlineadressbuch, um namensauflösung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="04fe0-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="04fe0-126">Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="04fe0-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="04fe0-127">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="04fe0-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="04fe0-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="04fe0-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="04fe0-129">Ermöglicht **OpenEntry** erfolgreich, möglicherweise beendet, bevor das Objekt an den aufrufenden Client vollständig verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="04fe0-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="04fe0-130">Wenn das Objekt nicht verfügbar ist, kann nachfolgende Objekt anrufen verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="04fe0-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="04fe0-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="04fe0-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="04fe0-132">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="04fe0-132">Requests read/write permission.</span></span> <span data-ttu-id="04fe0-133">Standardmäßig werden Objekte mit Leseberechtigung geöffnet, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="04fe0-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="04fe0-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="04fe0-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="04fe0-135">Verwenden Sie das Offlineadressbuch nicht namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="04fe0-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="04fe0-136">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="04fe0-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="04fe0-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="04fe0-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="04fe0-138">Anzeigen der Elemente, die aktuell als soft markiert werden gelöscht (d. h., sie sind in der Aufbewahrungszeit für gelöschte Elemente Zeit Phase).</span><span class="sxs-lookup"><span data-stu-id="04fe0-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="04fe0-139">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="04fe0-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="04fe0-140">[out] Ein Zeiger auf den Typ des Objekts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="04fe0-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="04fe0-141">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="04fe0-141">_lppUnk_</span></span>
  
> <span data-ttu-id="04fe0-142">[out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="04fe0-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="04fe0-143">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="04fe0-143">Return value</span></span>

<span data-ttu-id="04fe0-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="04fe0-144">S_OK</span></span> 
  
> <span data-ttu-id="04fe0-145">Das Objekt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="04fe0-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="04fe0-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="04fe0-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="04fe0-147">Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, ein Objekt zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="04fe0-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="04fe0-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="04fe0-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="04fe0-149">Es ist kein Objekt zugeordneten die Eintrags-ID in der _LpEntryID_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="04fe0-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="04fe0-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="04fe0-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="04fe0-151">Die Eintrags-ID in der _LpEntryID_ -Parameter übergeben wird in einem Format nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="04fe0-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="04fe0-152">Dieser Wert wird in der Regel zurückgegeben, wenn der Dienstanbieter, der das Objekt enthält nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="04fe0-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="04fe0-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04fe0-153">Remarks</span></span>

<span data-ttu-id="04fe0-154">Zugriff auf das Objekt, können die **IMAPISession::OpenEntry** -Methode wird geöffnet, eine Nachricht speichern oder address Book-Objekt zurückgeben einem Zeiger auf eine Schnittstelle, die, verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04fe0-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="04fe0-155">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="04fe0-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04fe0-156">Beim Öffnen der Einträge im Ordner in einem öffentlichen Speicher, wie Ordner und Nachrichten, verwenden Sie anstelle von **IMAPISession::OpenEntry** [IMsgStore::OpenEntry](imsgstore-openentry.md) .</span><span class="sxs-lookup"><span data-stu-id="04fe0-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="04fe0-157">Dadurch wird die Funktion für Öffentliche Ordner ordnungsgemäß sichergestellt, wenn in einem Profil mehrere Exchange-Konten definiert sind.</span><span class="sxs-lookup"><span data-stu-id="04fe0-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="04fe0-158">Rufen Sie **IMAPISession::OpenEntry** nur, wenn Sie nicht über welche Art Objekt kennen, die Sie öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="04fe0-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="04fe0-159">Wenn Sie wissen, dass Sie einen Ordner oder eine Nachricht öffnen möchten, rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="04fe0-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="04fe0-160">Wenn Sie wissen, dass Sie ein Adressbuchcontainer öffnen möchten, rufen Sie ein messaging-Benutzer oder eine Verteilerliste, [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="04fe0-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="04fe0-161">Diese bestimmten Methoden sind schneller als **IMAPISession::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="04fe0-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="04fe0-162">MAPI öffnet alle Objekte mit Leseberechtigung, es sei denn, Sie das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im _UlFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04fe0-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="04fe0-163">Festlegen einer dieser Flags garantiert keine bestimmte Art von Zugriff. die Berechtigungen, die erteilt werden, hängt von der Dienstanbieter, die Zugriffsebene und das Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="04fe0-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="04fe0-164">Rufen Sie zum Bestimmen der Zugriffsebene des geöffneten-Objekts, dessen **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="04fe0-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="04fe0-165">Aufrufen von **IMAPISession::OpenEntry** und Einstellung _LpEntryID_ So zeigen Sie auf die Eintrags-ID des einen Nachrichtenspeicher ist identisch mit Aufrufen der [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode mit dem MDB_NO_DIALOG-Flag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04fe0-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="04fe0-166">Die Kennzeichnung Einstellungen sind auch entspricht, es sei denn, die Berechtigung Lese-/Schreibzugriff mit **OpenMsgStore**, muss das Flag MDB_WRITE anstelle von MAPI_MODIFY festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="04fe0-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="04fe0-167">Überprüfen Sie den Wert in der _LpulObjType_ -Parameter, um festzustellen, ob der Objekttyp zurückgegeben wird, was Sie erwartet zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="04fe0-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="04fe0-168">Wenn der Objekttyp nicht den Typ, den Sie erwartet ist, wandeln Sie den Zeiger auf einen Zeiger des entsprechenden Typs aus dem _LppUnk_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="04fe0-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="04fe0-169">Angenommen, wenn Sie einen Ordner öffnen, _LppUnk_ auf einen Zeiger vom Typ LPMAPIFOLDER umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="04fe0-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="04fe0-170">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="04fe0-170">MFCMAPI reference</span></span>

<span data-ttu-id="04fe0-171">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="04fe0-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="04fe0-172">**Datei**</span><span class="sxs-lookup"><span data-stu-id="04fe0-172">**File**</span></span>|<span data-ttu-id="04fe0-173">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="04fe0-173">**Function**</span></span>|<span data-ttu-id="04fe0-174">**Comment**</span><span class="sxs-lookup"><span data-stu-id="04fe0-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="04fe0-175">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="04fe0-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="04fe0-176">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="04fe0-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="04fe0-177">MFCMAPI (engl.) verwendet die **IMAPISession::OpenEntry** -Methode zum Öffnen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="04fe0-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04fe0-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04fe0-178">See also</span></span>



[<span data-ttu-id="04fe0-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="04fe0-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="04fe0-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="04fe0-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="04fe0-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="04fe0-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="04fe0-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="04fe0-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="04fe0-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="04fe0-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="04fe0-184">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="04fe0-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="04fe0-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="04fe0-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="04fe0-186">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="04fe0-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="04fe0-187">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="04fe0-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

