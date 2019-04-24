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
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280178"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="000f8-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="000f8-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="000f8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="000f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="000f8-105">Kopiert oder verschiebt einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="000f8-105">Copies or moves a subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="000f8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="000f8-106">Parameters</span></span>

 <span data-ttu-id="000f8-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="000f8-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="000f8-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="000f8-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="000f8-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="000f8-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="000f8-110">in Ein Zeiger auf die Eintrags-ID des zu Kopier-oder verschobenen Unterordners.</span><span class="sxs-lookup"><span data-stu-id="000f8-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="000f8-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="000f8-111">_lpInterface_</span></span>
  
> <span data-ttu-id="000f8-112">in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf den Ordner verwendet werden soll, auf den der _lpDestFolder_ -Parameter zeigt.</span><span class="sxs-lookup"><span data-stu-id="000f8-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="000f8-113">Das übergeben von NULL bewirkt, dass der Dienstanbieter die Standardordner Schnittstelle [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="000f8-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="000f8-114">Gültige Werte für _lpInterface_ sind IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="000f8-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="000f8-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="000f8-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="000f8-116">in Ein Zeiger auf den geöffneten Ordner, um den kopierten oder verschobenen Unterordner zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="000f8-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="000f8-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="000f8-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="000f8-118">in Ein Zeiger auf den Namen des kopierten oder verschobenen Ordners in seinem neuen Ziel.</span><span class="sxs-lookup"><span data-stu-id="000f8-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="000f8-119">Wenn _lpszNewFolderName_ auf NULL festgelegt ist, wird der Name des Quell-Unterordners für den Namen des Zielordners verwendet.</span><span class="sxs-lookup"><span data-stu-id="000f8-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="000f8-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="000f8-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="000f8-121">in Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="000f8-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="000f8-122">Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag im _ulFlags_ -Parameter ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="000f8-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="000f8-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="000f8-123">_lpProgress_</span></span>
  
> <span data-ttu-id="000f8-124">in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="000f8-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="000f8-125">Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="000f8-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="000f8-126">Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird in _ulFlags_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="000f8-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="000f8-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="000f8-127">_ulFlags_</span></span>
  
> <span data-ttu-id="000f8-128">in Eine Bitmaske von Flags, die den Kopier-oder Verschiebungsvorgang steuert.</span><span class="sxs-lookup"><span data-stu-id="000f8-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="000f8-129">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="000f8-129">The following flags can be set:</span></span>
    
<span data-ttu-id="000f8-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="000f8-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="000f8-131">Alle Unterordner des zu kopierenden Unterordners sollten ebenfalls kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="000f8-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="000f8-132">Wenn COPY_SUBFOLDERS nicht für einen Kopiervorgang festgelegt ist, wird nur der durch _lpEntryID_ angegebene Unterordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="000f8-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="000f8-133">Bei einem Verschiebungsvorgang ist das COPY_SUBFOLDERS-Verhalten die Standardeinstellung, unabhängig davon, ob das Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="000f8-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="000f8-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="000f8-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="000f8-135">Fordert die Anzeige einer Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="000f8-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="000f8-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="000f8-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="000f8-137">Der Unterordner soll statt kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="000f8-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="000f8-138">Wenn FOLDER_MOVE nicht festgelegt ist, wird der Unterordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="000f8-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="000f8-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="000f8-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="000f8-140">Informiert den Nachrichtenspeicher Anbieter, dass bei der Implementierung von **CopyFolder** durch Aufrufen des [IMAPISupport::D ocopyto](imapisupport-docopyto.md) oder [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md) -Methode CopyFolder stattdessen sofort \*\*\*\* MAPI_E_ DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="000f8-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="000f8-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="000f8-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="000f8-142">Der Name des Zielordners ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="000f8-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="000f8-143">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist der Ordnername im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="000f8-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="000f8-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="000f8-144">Return value</span></span>

<span data-ttu-id="000f8-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="000f8-145">S_OK</span></span> 
  
> <span data-ttu-id="000f8-146">Der angegebene Ordner wurde erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="000f8-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="000f8-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="000f8-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="000f8-148">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und der Nachrichtenspeicher Anbieter unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und der Nachrichtenspeicher Anbieter unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="000f8-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="000f8-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="000f8-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="000f8-150">Der Name des Ordners, der verschoben oder kopiert wird, entspricht dem eines Unterordners im Zielordner.</span><span class="sxs-lookup"><span data-stu-id="000f8-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="000f8-151">Der Nachrichtenspeicher Anbieter benötigt eindeutige Ordnernamen.</span><span class="sxs-lookup"><span data-stu-id="000f8-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="000f8-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="000f8-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="000f8-153">Der Anbieter implementiert diese Methode durch Aufrufen einer Support Objektmethode, und der Aufrufer hat das MAPI_DECLINE_OK-Flag übergeben.</span><span class="sxs-lookup"><span data-stu-id="000f8-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="000f8-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="000f8-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="000f8-155">Der Quellordner enthält direkt oder indirekt den Zielordner.</span><span class="sxs-lookup"><span data-stu-id="000f8-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="000f8-156">Möglicherweise wurde vor dem erkennen dieser Bedingung eine beträchtliche Arbeit ausgeführt, sodass der Quell-und der Zielordner teilweise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="000f8-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="000f8-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="000f8-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="000f8-158">Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="000f8-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="000f8-159">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="000f8-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="000f8-160">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="000f8-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="000f8-161">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="000f8-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="000f8-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="000f8-162">Remarks</span></span>

<span data-ttu-id="000f8-163">Die **IMAPIFolder:: CopyFolder** -Methode kopiert oder verschiebt einen Unterordner von einem Speicherort an einen anderen.</span><span class="sxs-lookup"><span data-stu-id="000f8-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="000f8-164">Der Unterordner, der kopiert oder verschoben wird, wird dem Zielordner als Unterordner hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="000f8-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="000f8-165">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="000f8-165">Notes to implementers</span></span>

<span data-ttu-id="000f8-166">Wenn der Kopier-oder Verschiebungsvorgang mehr als einen Ordner umfasst, wie durch Festlegen des COPY_SUBFOLDERS-Flags angegeben, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus.</span><span class="sxs-lookup"><span data-stu-id="000f8-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="000f8-167">Manchmal ist der Ordner, der verschoben oder kopiert werden soll, nicht vorhanden oder wurde bereits an anderer Stelle verschoben oder kopiert.</span><span class="sxs-lookup"><span data-stu-id="000f8-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="000f8-168">Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihres Steuerelements liegt, beispielsweise ausgehender Arbeitsspeicher, unzureichender Festplattenspeicherplatz oder Beschädigung im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="000f8-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="000f8-169">Versuchen Sie, alle Nachrichteneingabe-IDs in den kopierten Nachrichten beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="000f8-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="000f8-170">Sie sollten auch versuchen, Eintrags-IDs beizubehalten, aber es ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="000f8-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="000f8-171">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="000f8-171">Notes to callers</span></span>

<span data-ttu-id="000f8-172">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="000f8-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="000f8-173">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="000f8-173">**Condition**</span></span>|<span data-ttu-id="000f8-174">**Rückgabewert**</span><span class="sxs-lookup"><span data-stu-id="000f8-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="000f8-175">**CopyFolder** hat alle Nachrichten und Unterordner erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="000f8-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="000f8-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="000f8-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="000f8-177">**CopyFolder** konnte alle Nachrichten und Unterordner nicht erfolgreich kopieren oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="000f8-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="000f8-178">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="000f8-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="000f8-179">**CopyFolder** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="000f8-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="000f8-180">Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="000f8-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="000f8-181">Wenn **CopyFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="000f8-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="000f8-182">**CopyFolder** kann möglicherweise eine oder mehrere der Nachrichten und Unterordner kopiert oder verschoben haben, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="000f8-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="000f8-183">Wenn ein Eintragsbezeichner für einen Ordner, der nicht vorhanden ist, in _lpEntryID_übergeben wird, gibt **COPYFOLDER** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND zurück, je nach der Implementierung des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="000f8-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="000f8-184">Je nach Nachrichtenspeicher Anbieter kann die Eintrags-ID der ursprünglichen Nachricht in der kopierten Nachricht beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="000f8-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="000f8-185">Sie sollten Eintrags-IDs nach Möglichkeit beibehalten, aber es ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="000f8-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="000f8-186">Sie können in der Regel von den folgenden Szenarien abhängen:</span><span class="sxs-lookup"><span data-stu-id="000f8-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="000f8-187">Wenn Sie einen Ordner zwischen zwei verschiedenen Nachrichtenspeicher Typen verschieben, wird der Eintragsbezeichner sicher geändert.</span><span class="sxs-lookup"><span data-stu-id="000f8-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="000f8-188">Wenn Sie einen Ordner zwischen zwei Nachrichtenspeicher des gleichen Typs verschieben, ändert sich die Eintrags-ID fast immer.</span><span class="sxs-lookup"><span data-stu-id="000f8-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="000f8-189">Wenn Sie einen Ordner an einen anderen Speicherort im gleichen Nachrichtenspeicher verschieben, kann sich die Eintrags-ID je nach Nachrichtenspeicher Anbieter ändern.</span><span class="sxs-lookup"><span data-stu-id="000f8-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="000f8-190">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="000f8-190">MFCMAPI reference</span></span>

<span data-ttu-id="000f8-191">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="000f8-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="000f8-192">**Datei**</span><span class="sxs-lookup"><span data-stu-id="000f8-192">**File**</span></span>|<span data-ttu-id="000f8-193">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="000f8-193">**Function**</span></span>|<span data-ttu-id="000f8-194">**Comment**</span><span class="sxs-lookup"><span data-stu-id="000f8-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="000f8-195">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="000f8-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="000f8-196">CMsgStoreDlg:: OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="000f8-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="000f8-197">MFCMAPI verwendet die **IMAPIFolder:: CopyFolder** -Methode, um Ordner von einem Speicherort an einen anderen zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="000f8-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="000f8-198">MFCMAPI merkt sich während des Kopiervorgangs den Quellordner und führt die Kopie tatsächlich während des Einfügevorgangs aus.</span><span class="sxs-lookup"><span data-stu-id="000f8-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="000f8-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="000f8-199">See also</span></span>



[<span data-ttu-id="000f8-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="000f8-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="000f8-201">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="000f8-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

