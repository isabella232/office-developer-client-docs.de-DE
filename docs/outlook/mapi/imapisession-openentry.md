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
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329414"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="22c55-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="22c55-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="22c55-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22c55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22c55-105">Öffnet ein Objekt und gibt einen Schnittstellenzeiger für zusätzlichen Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="22c55-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="22c55-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22c55-106">Parameters</span></span>

 <span data-ttu-id="22c55-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="22c55-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="22c55-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="22c55-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="22c55-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="22c55-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="22c55-110">in Ein Zeiger auf die Eintrags-ID des zu öffnenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="22c55-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="22c55-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="22c55-111">_lpInterface_</span></span>
  
> <span data-ttu-id="22c55-112">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22c55-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="22c55-113">Durch das Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22c55-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="22c55-114">Wenn das zu öffnende Objekt beispielsweise eine Nachricht ist, ist die Standardschnittstelle [IMessage](imessageimapiprop.md); für Ordner ist es [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="22c55-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="22c55-115">Die Standardschnittstellen für Adressbuch Objekte sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für einen Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="22c55-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="22c55-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22c55-116">_ulFlags_</span></span>
  
> <span data-ttu-id="22c55-117">in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="22c55-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="22c55-118">Die folgenden Flags können verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="22c55-118">The following flags can be used:</span></span>
    
<span data-ttu-id="22c55-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="22c55-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="22c55-120">Fordert, dass das Objekt unter Verwendung der maximal für den Benutzer zulässigen Netzwerkberechtigungen und des maximalen Client Anwendungszugriffs geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="22c55-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="22c55-121">Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte das Objekt mit Lese-/Schreibzugriff geöffnet werden. Wenn der Client schreibgeschützte Berechtigung hat, sollte das Objekt mit Leseberechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="22c55-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="22c55-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="22c55-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="22c55-123">Verwenden Sie alle Mittel, einschließlich Offlineadressbüchern, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="22c55-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="22c55-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="22c55-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="22c55-125">Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="22c55-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="22c55-126">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="22c55-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="22c55-127">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22c55-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="22c55-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="22c55-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="22c55-129">Ermöglicht \*\*\*\* das erfolgreiche zurückgeben von OpenEntry, bevor das Objekt vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="22c55-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="22c55-130">Wenn das Objekt nicht verfügbar ist, kann das Ausführen eines nachfolgenden Objekt Aufrufs einen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="22c55-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="22c55-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="22c55-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="22c55-132">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="22c55-132">Requests read/write permission.</span></span> <span data-ttu-id="22c55-133">Standardmäßig werden Objekte mit Schreibschutz Berechtigung geöffnet, und Clients sollten nicht mit der Annahme arbeiten, dass Lese-/Schreibzugriff erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="22c55-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="22c55-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="22c55-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="22c55-135">Verwenden Sie das Offlineadressbuch nicht zum Ausführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="22c55-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="22c55-136">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22c55-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="22c55-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="22c55-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="22c55-138">Elemente anzeigen, die derzeit als "Soft Deleted" markiert sind (also in der Aufbewahrungszeit für gelöschte Elemente).</span><span class="sxs-lookup"><span data-stu-id="22c55-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="22c55-139">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="22c55-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="22c55-140">Out Ein Zeiger auf den Typ des geöffneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="22c55-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="22c55-141">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="22c55-141">_lppUnk_</span></span>
  
> <span data-ttu-id="22c55-142">Out Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="22c55-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="22c55-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22c55-143">Return value</span></span>

<span data-ttu-id="22c55-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="22c55-144">S_OK</span></span> 
  
> <span data-ttu-id="22c55-145">Das Objekt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="22c55-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="22c55-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="22c55-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="22c55-147">Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="22c55-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="22c55-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="22c55-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="22c55-149">Es ist kein Objekt mit der im _lpEntryID_ -Parameter übergebenen Eintrags-ID verknüpft.</span><span class="sxs-lookup"><span data-stu-id="22c55-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="22c55-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="22c55-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="22c55-151">Die im _lpEntryID_ -Parameter übergebene Eintrags-ID weist ein unbekanntes Format auf.</span><span class="sxs-lookup"><span data-stu-id="22c55-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="22c55-152">Dieser Wert wird in der Regel zurückgegeben, wenn der Dienstanbieter, der das Objekt enthält, nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="22c55-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="22c55-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22c55-153">Remarks</span></span>

<span data-ttu-id="22c55-154">Mit der **IMAPISession:: OpenEntry** -Methode wird ein Nachrichtenspeicher-oder Adressbuchobjekt geöffnet, und es wird ein Zeiger auf eine Schnittstelle zurückgegeben, die für den Zugriff auf das Objekt verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="22c55-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="22c55-155">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="22c55-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22c55-156">Beim Öffnen von Ordnereinträgen in einem öffentlichen Informationsspeicher wie Ordner und Nachrichten verwenden Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) anstelle von **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="22c55-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="22c55-157">Dadurch wird sichergestellt, dass öffentliche Ordner ordnungsgemäß funktionieren, wenn mehrere Exchange-Konten in einem Profil definiert sind.</span><span class="sxs-lookup"><span data-stu-id="22c55-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="22c55-158">Rufen Sie **IMAPISession:: OpenEntry** nur auf, wenn Sie nicht wissen, welche Art von Objekt Sie öffnen.</span><span class="sxs-lookup"><span data-stu-id="22c55-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="22c55-159">Wenn Sie wissen, dass Sie einen Ordner oder eine Nachricht öffnen, rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md)auf.</span><span class="sxs-lookup"><span data-stu-id="22c55-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="22c55-160">Wenn Sie wissen, dass Sie einen Adressbuchcontainer, einen Messagingbenutzer oder eine Verteilerliste öffnen, rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md)auf.</span><span class="sxs-lookup"><span data-stu-id="22c55-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="22c55-161">Diese spezifischeren Methoden sind schneller als **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="22c55-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="22c55-162">MAPI öffnet alle Objekte mit Schreibschutz Berechtigung, es sei denn, Sie legen das MAPI_MODIFY-oder MAPI_BEST_ACCESS-Flag im _ulFlags_ -Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="22c55-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="22c55-163">Das Festlegen eines dieser Flags garantiert keinen bestimmten Zugriffstyp. welche Berechtigungen erteilt werden, hängt vom Dienstanbieter, der Zugriffsebene und dem Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="22c55-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="22c55-164">Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie die **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="22c55-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="22c55-165">Das Aufrufen von **IMAPISession:: OpenEntry** und das Festlegen von _lpEntryID_ so, dass auf den Eintragsbezeichner eines Nachrichtenspeichers verwiesen wird, entspricht dem Aufrufen der [IMAPISession:: OPENMSGSTORE](imapisession-openmsgstore.md) -Methode mit dem MDB_NO_DIALOG-Flagsatz.</span><span class="sxs-lookup"><span data-stu-id="22c55-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="22c55-166">Die Flageinstellungen sind ebenfalls äquivalent, mit der Ausnahme, dass zum Anfordern der Berechtigung zum Lesen/Schreiben mit **OpenMsgStore**das MDB_WRITE-Flag anstelle von MAPI_MODIFY festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="22c55-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="22c55-167">Überprüfen Sie den Wert, der im _lpulObjType_ -Parameter zurückgegeben wird, um zu bestimmen, ob der zurückgegebene Objekttyp Ihren Erwartungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="22c55-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="22c55-168">Wenn der Objekttyp nicht der erwartete Typ ist, wandeln Sie den Zeiger vom _lppUnk_ -Parameter in einen Zeiger des entsprechenden Typs um.</span><span class="sxs-lookup"><span data-stu-id="22c55-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="22c55-169">Wenn Sie beispielsweise einen Ordner öffnen, werfen Sie _lppUnk_ in einen Zeiger vom Typ LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="22c55-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="22c55-170">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="22c55-170">MFCMAPI reference</span></span>

<span data-ttu-id="22c55-171">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="22c55-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="22c55-172">**Datei**</span><span class="sxs-lookup"><span data-stu-id="22c55-172">**File**</span></span>|<span data-ttu-id="22c55-173">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="22c55-173">**Function**</span></span>|<span data-ttu-id="22c55-174">**Comment**</span><span class="sxs-lookup"><span data-stu-id="22c55-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="22c55-175">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="22c55-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="22c55-176">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="22c55-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="22c55-177">MFCMAPI verwendet die **IMAPISession:: OpenEntry** -Methode, um ein Objekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="22c55-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22c55-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22c55-178">See also</span></span>



[<span data-ttu-id="22c55-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="22c55-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="22c55-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="22c55-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="22c55-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="22c55-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="22c55-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="22c55-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="22c55-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="22c55-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="22c55-184">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="22c55-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="22c55-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="22c55-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="22c55-186">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22c55-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="22c55-187">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="22c55-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

