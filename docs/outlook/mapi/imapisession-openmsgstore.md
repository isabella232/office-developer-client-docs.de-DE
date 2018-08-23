---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fdf75787153f9a85e6a7bcddff44cf2c468a7975
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595034"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="3fec3-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="3fec3-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="3fec3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fec3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fec3-105">Öffnet einen Nachrichtenspeicher und gibt einen Zeiger [IMsgStore](imsgstoreimapiprop.md) für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="3fec3-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a><span data-ttu-id="3fec3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fec3-106">Parameters</span></span>

<span data-ttu-id="3fec3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3fec3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="3fec3-108">[in] Ein Handle für das übergeordnete Fenster der Adresse Standarddialogfeld und anderer weiterführende zeigt.</span><span class="sxs-lookup"><span data-stu-id="3fec3-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="3fec3-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3fec3-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="3fec3-110">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="3fec3-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="3fec3-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="3fec3-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="3fec3-112">[in] Ein Zeiger auf die Eintrags-ID des Nachrichtenspeichers geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3fec3-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="3fec3-113">Der Parameter _LpEntryID_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="3fec3-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="3fec3-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="3fec3-114">_lpInterface_</span></span>
  
> <span data-ttu-id="3fec3-115">[in] Ein Zeiger auf die Schnittstellenbezeichner (IID), der die Schnittstelle für verwendet werden, um die Nachrichtenspeicher zugreifen darstellt.</span><span class="sxs-lookup"><span data-stu-id="3fec3-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="3fec3-116">Übergeben von NULL bewirkt, dass den _LppMDB_ -Parameter, um einen Zeiger auf die Standardschnittstelle für einen Nachrichtenspeicher (**IMsgStore**) zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3fec3-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="3fec3-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3fec3-117">_ulFlags_</span></span>
  
> <span data-ttu-id="3fec3-118">[in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="3fec3-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="3fec3-119">Die folgenden Werte können verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="3fec3-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="3fec3-120">MAPI_BEST_ACCESS: Fordert, dass der Nachrichtenspeicher mit den Netzwerkberechtigungen maximale geöffnet werden zulässig für den Benutzer und die maximale Client Anwendungsberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="3fec3-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="3fec3-121">Beispielsweise sollte der Client Lese-/Schreibberechtigung verfügt, der Nachrichtenspeicher mit Lese-/Schreibzugriff geöffnet werden; Wenn der Client nur-Lese-Berechtigung verfügt, sollte der Nachrichtenspeicher mit Leseberechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3fec3-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="3fec3-122">MAPI_DEFERRED_ERRORS: Ermöglicht **OpenMsgStore** zurückgegeben wurde, ist möglicherweise vor der Meldung Store an den aufrufenden Client vollständig verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3fec3-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="3fec3-123">Wenn der Nachrichtenspeicher nicht verfügbar ist, kann die nachfolgende Objekt Anrufen ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="3fec3-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="3fec3-124">MDB\_NO_DIALOG: verhindert, dass die Anzeige von Dialogfeldern für die Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="3fec3-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="3fec3-125">Wenn dieses Flag festgelegt ist, und **OpenMsgStore** hat nicht genügend Konfigurationsinformationen des Nachrichtenspeichers ohne die Benutzer Hilfe öffnen, wird die MAPI_E_LOGON_FAILED zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3fec3-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="3fec3-126">Wenn dieses Flag nicht festgelegt ist, kann der Nachricht Speicheranbieter auffordern, um einen Namen oder das Kennwort zu korrigieren oder andere Aktionen auszuführen, die zum Herstellen einer Verbindung mit dem Nachrichtenspeicher benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="3fec3-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="3fec3-127">MDB\_NO_MAIL: Nachrichtenspeicher sollte nicht für das Senden oder Empfangen von e-Mail verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3fec3-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="3fec3-128">Wenn dieses Flag festgelegt ist, benachrichtigt MAPI nicht der MAPI-Warteschlange, dass dieses Nachrichtenspeichers geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="3fec3-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="3fec3-129">MDB\_ONLINE: In Cached Exchange Mode ein Client oder Dienstanbieter kann diese Methode mit MDB_ONLINE Überschreiben der Verbindungs mit den lokalen Nachrichtenspeicher und öffnen Sie den Speicher auf dem Remoteserver aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3fec3-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="3fec3-130">Sie können keinen Exchange-Speicher gleichzeitig in derselben MAPI-Sitzung im Cache-Modus und im nicht-Cache-Modus öffnen.</span><span class="sxs-lookup"><span data-stu-id="3fec3-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="3fec3-131">Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie dieses Flag zu öffnen, oder öffnen eine neue MAPI-Sitzung, in dem Sie den Exchange-Speicher auf dem Remoteserver mithilfe dieses Flag öffnen können.</span><span class="sxs-lookup"><span data-stu-id="3fec3-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="3fec3-132">MDB_TEMPORARY: Weist MAPI an, dass der Nachrichtenspeicher ist jedoch nicht dauerhaft und nicht die Nachricht Store-Tabelle hinzugefügt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="3fec3-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="3fec3-133">Dieses Kennzeichen werden verwendet, um den Nachrichtenspeicher anmelden, damit Informationen aus dem Profilabschnitt programmgesteuert abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3fec3-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="3fec3-134">MDB_WRITE: Anforderungen Lese-/Schreibberechtigung auf den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="3fec3-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="3fec3-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="3fec3-135">_lppMDB_</span></span>
  
> <span data-ttu-id="3fec3-136">[out] Zeiger auf einen Zeiger des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="3fec3-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3fec3-137">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3fec3-137">Return value</span></span>

<span data-ttu-id="3fec3-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="3fec3-138">S_OK</span></span> 
  
> <span data-ttu-id="3fec3-139">Der Nachrichtenspeicher wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3fec3-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="3fec3-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="3fec3-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="3fec3-141">Es wurde versucht, auf einen Nachrichtenspeicher zugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="3fec3-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="3fec3-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3fec3-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3fec3-143">Der Nachrichtenspeicher angegeben durch _LpEntryID_ ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3fec3-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="3fec3-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="3fec3-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="3fec3-145">Der Server ist nicht zur Unterstützung der Codeseite für den Client konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3fec3-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="3fec3-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="3fec3-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="3fec3-147">Der Server ist nicht konfiguriert, um Gebietsschemainformationen des Clients zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3fec3-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="3fec3-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="3fec3-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="3fec3-149">Der Aufruf war erfolgreich, aber der Nachricht Speicheranbieter hat Fehlerinformationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3fec3-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="3fec3-150">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="3fec3-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="3fec3-151">Wenn Sie die Fehlerinformationen vom Anbieter erhalten möchten, rufen Sie die [IMAPISession::GetLastError](imapisession-getlasterror.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3fec3-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="3fec3-152">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="3fec3-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="3fec3-153">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="3fec3-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3fec3-154">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="3fec3-154">Remarks</span></span>

<span data-ttu-id="3fec3-155">Die **IMAPISession::OpenMsgStore** -Methode wird die einen bestimmten Nachrichtenspeicher geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3fec3-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3fec3-156">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3fec3-156">Notes to callers</span></span>

<span data-ttu-id="3fec3-157">Die Standardberechtigungsstufe für Nachrichtenspeicher ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3fec3-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="3fec3-158">Wenn Sie das MDB_WRITE-Flag festlegen, können Sie noch nicht Lese-/Schreibberechtigung erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="3fec3-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="3fec3-159">Die endgültige Zugriffsebene, die MAPI-weist mit dem Nachrichtenspeicher hängt von Ihrer Berechtigungsstufe, die Nachricht selbst und die Nachricht Speicheranbieter gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3fec3-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="3fec3-160">Wenn Sie **OpenMsgStore** zum Öffnen eines Nachrichtenspeichers mit Leseberechtigung aufrufen, geschieht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3fec3-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="3fec3-161">Des Speichers **PR\_STORE_SUPPORT_MASK** -Eigenschaft ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) haben keinen dessen Speicher\_MODIFY_OK und STORE\_CREATE_OK bits festlegen.</span><span class="sxs-lookup"><span data-stu-id="3fec3-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="3fec3-162">Anrufe an des Nachrichtenspeicher Nachrichten oder Ordner öffnen, indem Sie [IMAPISession::OpenEntry](imapisession-openentry.md) mit dem Flag MAPI_MODIFY schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="3fec3-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="3fec3-163">Anrufe an eine der Eigenschaften des Nachrichtenspeicher Nachrichten oder Ordner öffnen, indem Sie das Kennzeichen MAPI_MODIFY [IMAPIProp::OpenProperty](imapiprop-openproperty.md) mit schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="3fec3-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="3fec3-164">Aufrufe an eine der folgenden Methoden schlagen fehl:</span><span class="sxs-lookup"><span data-stu-id="3fec3-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="3fec3-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="3fec3-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="3fec3-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="3fec3-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="3fec3-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="3fec3-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="3fec3-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="3fec3-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="3fec3-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="3fec3-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="3fec3-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="3fec3-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="3fec3-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="3fec3-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="3fec3-172">Aufrufe der folgenden Methoden schlägt fehl, wenn das Ziel für die kopierte Nachricht schreibgeschützt ist, ob das Ziel identisch mit der Quelle Nachrichtenspeicher ist oder einen anderen nur-Lese-Speicher.</span><span class="sxs-lookup"><span data-stu-id="3fec3-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="3fec3-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="3fec3-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="3fec3-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="3fec3-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="3fec3-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="3fec3-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3fec3-176">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="3fec3-176">MFCMAPI reference</span></span>

<span data-ttu-id="3fec3-177">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3fec3-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3fec3-178">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3fec3-178">**File**</span></span>|<span data-ttu-id="3fec3-179">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3fec3-179">**Function**</span></span>|<span data-ttu-id="3fec3-180">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3fec3-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3fec3-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="3fec3-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="3fec3-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="3fec3-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="3fec3-183">MFCMAPI (engl.) verwendet die **IMAPISession::OpenMsgStore** -Methode, um einen Nachrichtenspeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3fec3-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3fec3-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fec3-184">See also</span></span>

- [<span data-ttu-id="3fec3-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3fec3-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="3fec3-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3fec3-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="3fec3-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3fec3-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="3fec3-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="3fec3-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="3fec3-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3fec3-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="3fec3-190">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="3fec3-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="3fec3-191">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="3fec3-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

