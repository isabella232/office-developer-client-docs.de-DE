---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5961e7a2118a46bdc9c0e66138363976ae2f7154
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792100"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="5e799-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="5e799-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="5e799-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e799-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e799-105">Kopiert oder Verschiebt einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="5e799-105">Copies or moves a subfolder.</span></span>
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5e799-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e799-106">Parameters</span></span>

 <span data-ttu-id="5e799-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5e799-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="5e799-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="5e799-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5e799-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5e799-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="5e799-110">[in] Ein Zeiger auf die Eintrags-ID des Unterordners kopieren oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="5e799-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="5e799-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5e799-111">_lpInterface_</span></span>
  
> <span data-ttu-id="5e799-112">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden soll, dem auf der _LpDestFolder_ -Parameter verweist auf den Ordner zugreifen darstellt.</span><span class="sxs-lookup"><span data-stu-id="5e799-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="5e799-113">Übergeben von NULL bewirkt, dass die Standardordner-Schnittstelle zurück, die den Dienstanbieter [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="5e799-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="5e799-114">Gültige Werte für _LpInterface_ sind IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="5e799-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="5e799-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="5e799-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="5e799-116">[in] Ein Zeiger auf den Ordner öffnen, um den Unterordner kopiert oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="5e799-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="5e799-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="5e799-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="5e799-118">[in] Ein Zeiger auf den Namen des Ordners kopiert oder verschoben in ihr neues Ziel.</span><span class="sxs-lookup"><span data-stu-id="5e799-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="5e799-119">Wenn _LpszNewFolderName_ auf NULL festgelegt ist, wird der Name des Unterordners Quelle für den Namen des Zielordners verwendet.</span><span class="sxs-lookup"><span data-stu-id="5e799-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="5e799-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5e799-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="5e799-121">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="5e799-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="5e799-122">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5e799-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="5e799-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="5e799-123">_lpProgress_</span></span>
  
> <span data-ttu-id="5e799-124">[in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e799-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="5e799-125">Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e799-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="5e799-126">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG in _UlFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5e799-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="5e799-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e799-127">_ulFlags_</span></span>
  
> <span data-ttu-id="5e799-128">[in] Eine Bitmaske aus Flags, die den Vorgang kopieren oder verschieben steuert.</span><span class="sxs-lookup"><span data-stu-id="5e799-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="5e799-129">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5e799-129">The following flags can be set:</span></span>
    
<span data-ttu-id="5e799-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="5e799-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="5e799-131">Alle Unterordner im Unterordner kopiert werden sollte auch kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="5e799-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="5e799-132">Wenn COPY_SUBFOLDERS für einen Kopiervorgang nicht festgelegt ist, wird nur der identifizierten _LpEntryID_ Unterordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="5e799-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="5e799-133">Mit einem Verschiebevorgang wird das Verhalten COPY_SUBFOLDERS standardmäßig unabhängig davon, ob das Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5e799-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="5e799-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="5e799-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="5e799-135">Fordert die Anzeige einer Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="5e799-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="5e799-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="5e799-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="5e799-137">Der Unterordner ist anstelle von verschoben werden kopiert.</span><span class="sxs-lookup"><span data-stu-id="5e799-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="5e799-138">Wenn FOLDER_MOVE nicht festgelegt ist, wird der Unterordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="5e799-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="5e799-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="5e799-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="5e799-140">Dem Nachricht Speicheranbieter informiert werden, dass wenn diese **CopyFolder** implementiert, durch die des Unterstützungsobjekts [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) oder [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) -Methode aufrufen, **CopyFolder** stattdessen sofort MAPI_E_ zurückgegeben werden soll DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="5e799-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="5e799-141">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5e799-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5e799-142">Der Name des Zielordners ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="5e799-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="5e799-143">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Name des Ordners im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="5e799-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e799-144">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5e799-144">Return value</span></span>

<span data-ttu-id="5e799-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e799-145">S_OK</span></span> 
  
> <span data-ttu-id="5e799-146">Der angegebene Ordner wurde erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="5e799-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="5e799-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5e799-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5e799-148">Entweder die Option MAPI_UNICODE festgelegt wurde und die Nachrichtenanbieter unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und der Nachricht Speicher-Anbieter unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e799-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="5e799-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="5e799-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="5e799-150">Der Name des Ordners, die verschoben oder kopiert ist identisch mit der von einem Unterordner im Zielordner.</span><span class="sxs-lookup"><span data-stu-id="5e799-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="5e799-151">Der Nachricht Speicheranbieter erfordert eindeutige Ordnernamen.</span><span class="sxs-lookup"><span data-stu-id="5e799-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="5e799-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="5e799-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="5e799-153">Der Anbieter implementiert diese Methode durch den Aufruf einer Support, und der Aufrufer das Flag MAPI_DECLINE_OK verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="5e799-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="5e799-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="5e799-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="5e799-155">Der Source-Ordner enthält direkt oder indirekt den Zielordner.</span><span class="sxs-lookup"><span data-stu-id="5e799-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="5e799-156">Erhebliche Arbeit möglicherweise durchgeführt wurden, bevor diese Bedingung ermittelt wurde, damit der Quell- und Zielserver Ordner teilweise geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e799-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="5e799-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="5e799-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="5e799-158">Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="5e799-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="5e799-159">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5e799-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="5e799-160">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="5e799-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="5e799-161">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="5e799-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e799-162">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e799-162">Remarks</span></span>

<span data-ttu-id="5e799-163">Die **IMAPIFolder::CopyFolder** -Methode kopiert oder Verschiebt einen Unterordner von einem Speicherort an einen anderen.</span><span class="sxs-lookup"><span data-stu-id="5e799-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="5e799-164">Der Unterordner kopiert oder verschoben wird in den Zielordner als Unterordner hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5e799-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5e799-165">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="5e799-165">Notes to implementers</span></span>

<span data-ttu-id="5e799-166">Beim Kopieren oder verschieben-Vorgang mehrere Ordner umfasst, wie durch Festlegen der COPY_SUBFOLDERS-Flag angegeben, führen Sie den Vorgang für jeden Ordner möglichst vollständig.</span><span class="sxs-lookup"><span data-stu-id="5e799-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="5e799-167">In einigen Fällen einen der Ordner verschoben oder kopiert wurde ist nicht vorhanden oder bereits verschoben oder kopiert wurde an anderer Stelle.</span><span class="sxs-lookup"><span data-stu-id="5e799-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="5e799-168">Beenden Sie den Vorgang nicht vorzeitig auf, es sei denn, ein Fehler, die außerhalb Ihrer Kontrolle auftritt, wie nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder der Beschädigung im Nachrichtenspeicher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e799-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="5e799-169">Versuchen Sie, die alle Nachricht-Eintragsbezeichner in der kopierten Nachrichten beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="5e799-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="5e799-170">Sie sollten auch versuchen, Eintragsbezeichner beibehalten, aber es ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5e799-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5e799-171">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="5e799-171">Notes to callers</span></span>

<span data-ttu-id="5e799-172">Diese Rückgabewerte unter folgenden Umständen zu erwarten.</span><span class="sxs-lookup"><span data-stu-id="5e799-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="5e799-173">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="5e799-173">**Condition**</span></span>|<span data-ttu-id="5e799-174">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="5e799-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e799-175">**CopyFolder** wurde erfolgreich kopiert oder jede Nachricht und Unterordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="5e799-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="5e799-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e799-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="5e799-177">**CopyFolder** konnte erfolgreich kopieren oder verschieben Sie jede Nachricht und Unterordner.</span><span class="sxs-lookup"><span data-stu-id="5e799-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="5e799-178">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5e799-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="5e799-179">**CopyFolder** konnte nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5e799-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="5e799-180">Einen Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5e799-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="5e799-181">Wenn **CopyFolder** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="5e799-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="5e799-182">**CopyFolder** wurden möglicherweise kopieren oder verschieben Sie eine oder mehrere Nachrichten und Unterordner vor den Fehler auftreten können.</span><span class="sxs-lookup"><span data-stu-id="5e799-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="5e799-183">Wenn ein Eintrag Bezeichner für einen Ordner, der nicht vorhanden ist _LpEntryID_übergeben wird, gibt **CopyFolder** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, je nach den Nachrichtenspeicher Implementierung.</span><span class="sxs-lookup"><span data-stu-id="5e799-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="5e799-184">Je nach Anbieter die Nachricht die Eintrags-ID der ursprünglichen Nachricht oder nicht in der kopierten Nachricht beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="5e799-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="5e799-185">Sie sollten Eintragsbezeichner nach Möglichkeit beizubehalten, aber es ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5e799-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="5e799-186">Sie können die folgenden Szenarien in der Regel abhängig:</span><span class="sxs-lookup"><span data-stu-id="5e799-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="5e799-187">Wenn Sie einen Ordner zwischen zwei verschiedene Arten von Nachrichtenspeicher verschieben, wird die Eintrags-ID unbedingt ändern.</span><span class="sxs-lookup"><span data-stu-id="5e799-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="5e799-188">Wenn Sie einen Ordner zwischen zwei Nachrichtenspeicher des gleichen Typs, ändert sich die Eintrags-ID fast immer.</span><span class="sxs-lookup"><span data-stu-id="5e799-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="5e799-189">Wenn Sie einen Ordner an einen anderen Speicherort in der gleichen Nachrichtenspeicher verschieben, die Eintrags-ID kann oder möglicherweise nicht ändern, abhängig von der Nachricht Speicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="5e799-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="5e799-190">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="5e799-190">MFCMAPI reference</span></span>

<span data-ttu-id="5e799-191">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5e799-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5e799-192">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5e799-192">**File**</span></span>|<span data-ttu-id="5e799-193">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5e799-193">**Function**</span></span>|<span data-ttu-id="5e799-194">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5e799-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5e799-195">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5e799-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="5e799-196">CMsgStoreDlg::OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="5e799-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="5e799-197">MFCMAPI (engl.) verwendet die **IMAPIFolder::CopyFolder** -Methode, um Ordner von einem Speicherort in einen anderen zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="5e799-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="5e799-198">MFCMAPI (engl.) speichert Quellordners während des Kopiervorgangs und die Kopie tatsächlich während der Einfügevorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="5e799-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e799-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e799-199">See also</span></span>



[<span data-ttu-id="5e799-200">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5e799-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="5e799-201">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5e799-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

