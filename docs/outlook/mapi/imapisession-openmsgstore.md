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
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418022"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="8970e-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="8970e-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="8970e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8970e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8970e-105">Öffnet einen Nachrichtenspeicher und gibt einen [IMsgStore](imsgstoreimapiprop.md) -Zeiger für den weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="8970e-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="8970e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8970e-106">Parameters</span></span>

<span data-ttu-id="8970e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8970e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="8970e-108">in Ein Handle für das übergeordnete Fenster des Dialogfelds "allgemeine Adresse" und andere zugehörige anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8970e-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="8970e-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8970e-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="8970e-110">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8970e-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="8970e-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8970e-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="8970e-112">in Ein Zeiger auf die Eintrags-ID des zu öffnenden Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="8970e-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="8970e-113">Der _lpEntryID_ -Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8970e-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="8970e-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8970e-114">_lpInterface_</span></span>
  
> <span data-ttu-id="8970e-115">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den Nachrichtenspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8970e-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="8970e-116">Übergeben von NULL bewirkt, dass der Parameter _lppMDB_ einen Zeiger auf die Standardschnittstelle für einen Nachrichtenspeicher (**IMsgStore**) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8970e-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="8970e-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8970e-117">_ulFlags_</span></span>
  
> <span data-ttu-id="8970e-118">in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8970e-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="8970e-119">Die folgenden Flags können verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="8970e-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="8970e-120">MAPI_BEST_ACCESS: fordert, dass der Nachrichtenspeicher mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und den maximalen Client Anwendungsberechtigungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8970e-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="8970e-121">Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte der Nachrichtenspeicher mit Lese-/Schreibzugriff geöffnet werden. Wenn der Client schreibgeschützte Berechtigung hat, sollte der Nachrichtenspeicher mit Leseberechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="8970e-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="8970e-122">MAPI_DEFERRED_ERRORS: ermöglicht es **OpenMsgStore** , erfolgreich zurückzugeben, möglicherweise, bevor der Nachrichtenspeicher für den aufrufenden Client vollständig verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8970e-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="8970e-123">Wenn der Nachrichtenspeicher nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="8970e-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="8970e-124">MDB\_-NO_DIALOG: verhindert die Anzeige von Anmelde Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="8970e-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="8970e-125">Wenn dieses Flag festgelegt ist und **OpenMsgStore** nicht über genügend Konfigurationsinformationen zum Öffnen des Nachrichtenspeichers ohne die Hilfe des Benutzers verfügt, wird MAPI_E_LOGON_FAILED zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8970e-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="8970e-126">Wenn dieses Flag nicht festgelegt ist, kann der Nachrichtenspeicher Anbieter den Benutzer auffordern, einen Namen oder ein Kennwort zu korrigieren oder andere Aktionen auszuführen, die zum Herstellen einer Verbindung mit dem Nachrichtenspeicher erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8970e-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="8970e-127">MDB\_-NO_MAIL: der Nachrichtenspeicher sollte nicht zum Senden oder empfangen von e-Mails verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8970e-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="8970e-128">Wenn dieses Flag festgelegt ist, wird die MAPI-Spooler nicht benachrichtigt, dass dieser Nachrichtenspeicher geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8970e-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="8970e-129">MDB\_online: im Exchange-Cache-Modus kann ein Client oder Dienstanbieter diese Methode mit MDB_ONLINE aufrufen, um die Verbindung mit dem lokalen Nachrichtenspeicher zu überschreiben und den Speicher auf dem Remoteserver zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8970e-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="8970e-130">Sie können einen Exchange-Speicher nicht im Cache-Modus und gleichzeitig im nicht-Cache-Modus in derselben MAPI-Sitzung öffnen.</span><span class="sxs-lookup"><span data-stu-id="8970e-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="8970e-131">Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie ihn mit dieser Kennzeichnung öffnen, oder eine neue MAPI-Sitzung öffnen, in der Sie den Exchange-Speicher auf dem Remoteserver mit dieser Kennzeichnung öffnen können.</span><span class="sxs-lookup"><span data-stu-id="8970e-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="8970e-132">MDB_TEMPORARY: gibt MAPI an, dass der Nachrichtenspeicher nicht permanent ist und nicht der Nachrichtenspeichertabelle hinzugefügt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="8970e-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="8970e-133">Dieses Flag wird verwendet, um sich beim Nachrichtenspeicher anzumelden, damit Informationen programmgesteuert aus dem Abschnitt profile abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="8970e-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="8970e-134">MDB_WRITE: fordert Lese-/Schreibzugriff für den Nachrichtenspeicher an.</span><span class="sxs-lookup"><span data-stu-id="8970e-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="8970e-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="8970e-135">_lppMDB_</span></span>
  
> <span data-ttu-id="8970e-136">Out Zeiger auf einen Zeiger des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="8970e-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8970e-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8970e-137">Return value</span></span>

<span data-ttu-id="8970e-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="8970e-138">S_OK</span></span> 
  
> <span data-ttu-id="8970e-139">Der Nachrichtenspeicher wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8970e-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="8970e-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8970e-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8970e-141">Es wurde versucht, auf einen Nachrichtenspeicher zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="8970e-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="8970e-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8970e-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8970e-143">Der von _lpEntryID_ angegebene Nachrichtenspeicher ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8970e-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="8970e-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="8970e-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="8970e-145">Der Server ist nicht für die Unterstützung der Codeseite des Clients konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8970e-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="8970e-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="8970e-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="8970e-147">Der Server ist nicht für die Unterstützung der Gebietsschemainformationen des Clients konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8970e-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="8970e-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="8970e-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="8970e-149">Der Aufruf war erfolgreich, aber der Nachrichtenspeicher Anbieter hat Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="8970e-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="8970e-150">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="8970e-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="8970e-151">Rufen Sie die [IMAPISession:: getlasterroraufzurufen](imapisession-getlasterror.md) -Methode auf, um die Fehlerinformationen vom Anbieter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8970e-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="8970e-152">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="8970e-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="8970e-153">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="8970e-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8970e-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8970e-154">Remarks</span></span>

<span data-ttu-id="8970e-155">Mit der **IMAPISession:: OpenMsgStore** -Methode wird ein bestimmter Nachrichtenspeicher geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8970e-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8970e-156">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8970e-156">Notes to callers</span></span>

<span data-ttu-id="8970e-157">Die Standardberechtigungsstufe für Nachrichtenspeicher ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8970e-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="8970e-158">Wenn Sie das MDB_WRITE-Flag festlegen, werden Ihnen möglicherweise weiterhin keine Lese-/Schreibzugriff erteilt.</span><span class="sxs-lookup"><span data-stu-id="8970e-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="8970e-159">Die letzte Zugriffsebene, die MAPI dem Nachrichtenspeicher zuweist, hängt von Ihrer Berechtigungsstufe, dem Nachrichtenspeicher selbst und dem Nachrichtenspeicher Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="8970e-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="8970e-160">Wenn Sie **OpenMsgStore** aufrufen, um einen Nachrichtenspeicher mit Schreibschutz Berechtigung zu öffnen, wird Folgendes ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="8970e-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="8970e-161">Die **PR\_-STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Stores hat nicht\_die Speicher MODIFY_OK\_und speichert CREATE_OK-Bits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8970e-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="8970e-162">Aufrufe zum Öffnen eines der Nachrichten oder Ordner des Nachrichtenspeichers mithilfe von [IMAPISession:: OpenEntry](imapisession-openentry.md) mit dem MAPI_MODIFY-Flagsatz schlagen fehl.</span><span class="sxs-lookup"><span data-stu-id="8970e-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="8970e-163">Aufrufe zum Öffnen einer der Eigenschaften der Nachrichten oder Ordner des Nachrichtenspeichers mithilfe von [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) mit dem MAPI_MODIFY-Flag schlagen fehl.</span><span class="sxs-lookup"><span data-stu-id="8970e-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="8970e-164">Bei Aufrufen einer der folgenden Methoden tritt ein Fehler auf:</span><span class="sxs-lookup"><span data-stu-id="8970e-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="8970e-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="8970e-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="8970e-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="8970e-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="8970e-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="8970e-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="8970e-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="8970e-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="8970e-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="8970e-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="8970e-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="8970e-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="8970e-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="8970e-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="8970e-172">Bei Aufrufen der folgenden Methoden tritt ein Fehler auf, wenn das Ziel für die kopierte Nachricht schreibgeschützt ist, unabhängig davon, ob das Ziel mit dem Quell Nachrichtenspeicher identisch ist oder wenn es sich um einen anderen schreibgeschützten Speicher handelt.</span><span class="sxs-lookup"><span data-stu-id="8970e-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="8970e-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="8970e-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="8970e-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="8970e-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="8970e-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="8970e-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8970e-176">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8970e-176">MFCMAPI reference</span></span>

<span data-ttu-id="8970e-177">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8970e-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8970e-178">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8970e-178">**File**</span></span>|<span data-ttu-id="8970e-179">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8970e-179">**Function**</span></span>|<span data-ttu-id="8970e-180">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8970e-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8970e-181">MAPIStoreFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="8970e-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="8970e-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="8970e-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="8970e-183">MFCMAPI verwendet die **IMAPISession:: OpenMsgStore** -Methode, um einen Nachrichtenspeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8970e-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8970e-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8970e-184">See also</span></span>

- [<span data-ttu-id="8970e-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8970e-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="8970e-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8970e-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="8970e-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8970e-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="8970e-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="8970e-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="8970e-189">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8970e-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="8970e-190">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8970e-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="8970e-191">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="8970e-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

