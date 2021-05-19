---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420885"
---
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="8d7ad-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="8d7ad-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="8d7ad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d7ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d7ad-105">Kopiert oder verschiebt einen Ordner aus dem aktuellen übergeordneten Ordner in einen anderen übergeordneten Ordner.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
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

## <a name="parameters"></a><span data-ttu-id="8d7ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d7ad-106">Parameters</span></span>

 <span data-ttu-id="8d7ad-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="8d7ad-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="8d7ad-108">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den übergeordneten Ordner des Ordners verwendet werden soll, der kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="8d7ad-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="8d7ad-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="8d7ad-110">[in] Ein Zeiger auf den übergeordneten Ordner des Ordners, der kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="8d7ad-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8d7ad-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="8d7ad-112">[in] Die Byteanzahl in der Eintrags-ID, auf die _von lpEntryID verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="8d7ad-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="8d7ad-113">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8d7ad-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="8d7ad-114">[in] Ein Zeiger auf die Eintrags-ID des Ordners, der kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="8d7ad-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8d7ad-115">_lpInterface_</span></span>
  
> <span data-ttu-id="8d7ad-116">[in] Reserviert; muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="8d7ad-117">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="8d7ad-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="8d7ad-118">[in] Ein Zeiger auf den Ordner, der den zu kopierende oder zu verschiebende Ordner empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="8d7ad-119">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="8d7ad-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="8d7ad-120">[in] Ein Zeiger auf den Namen des kopierten oder verschobenen Ordners; Andernfalls NULL, was angibt, dass der kopierte oder verschobene Ordner denselben Namen wie der Quellordner haben soll (der Ordner, auf den _lpEntryID verweist)._</span><span class="sxs-lookup"><span data-stu-id="8d7ad-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="8d7ad-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8d7ad-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="8d7ad-122">[in] Ein Handle des Fensters für das Dialogfeld Statusanzeige und zugehörige Fenster.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="8d7ad-123">Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8d7ad-124">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="8d7ad-124">_lpProgress_</span></span>
  
> <span data-ttu-id="8d7ad-125">[in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="8d7ad-126">Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="8d7ad-127">Der _lpProgress-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG ist in _ulFlags festgelegt._</span><span class="sxs-lookup"><span data-stu-id="8d7ad-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="8d7ad-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d7ad-128">_ulFlags_</span></span>
  
> <span data-ttu-id="8d7ad-129">[in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebevorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="8d7ad-130">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8d7ad-130">The following flags can be set:</span></span>
    
<span data-ttu-id="8d7ad-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="8d7ad-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="8d7ad-132">Alle Unterordner des Ordners sollten kopiert oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="8d7ad-133">Wenn COPY_SUBFOLDERS für einen Kopiervorgang nicht festgelegt ist, wird nur der durch  _lpEntryID identifizierte_ Ordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="8d7ad-134">Bei einem Verschiebevorgang ist COPY_SUBFOLDERS das Standardverhalten, unabhängig davon, ob das Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="8d7ad-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8d7ad-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="8d7ad-136">Fordert die Anzeige eines Statusindikators an.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="8d7ad-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="8d7ad-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="8d7ad-138">Der Ordner sollte verschoben werden, anstatt zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="8d7ad-139">Wenn FOLDER_MOVE nicht festgelegt ist, wird der Ordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="8d7ad-140">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8d7ad-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8d7ad-141">Der Name des Ordners ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="8d7ad-142">Wenn das MAPI_UNICODE nicht festgelegt ist, hat der Name des Ordners das ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d7ad-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d7ad-143">Return value</span></span>

<span data-ttu-id="8d7ad-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d7ad-144">S_OK</span></span> 
  
> <span data-ttu-id="8d7ad-145">Der Ordner wurde erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="8d7ad-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="8d7ad-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="8d7ad-147">Der Name des verschobenen oder kopierten Ordners ist identisch mit dem eines Unterordners im Zielordner.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="8d7ad-148">Der Nachrichtenspeicheranbieter erfordert, dass Ordnernamen eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="8d7ad-149">Der Vorgang wird beendet, ohne abgeschlossen zu werden.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="8d7ad-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="8d7ad-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="8d7ad-151">Der Aufruf ist erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="8d7ad-152">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="8d7ad-153">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="8d7ad-154">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="8d7ad-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d7ad-155">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d7ad-155">Remarks</span></span>

<span data-ttu-id="8d7ad-156">Die **IMAPISupport::CopyFolder-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="8d7ad-157">Nachrichtenspeicheranbieter können **IMAPISupport::CopyFolder** in ihrer Implementierung von [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) aufrufen, um einen einzelnen Ordner aus einem übergeordneten Ordner in einen anderen zu kopieren oder zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="8d7ad-158">**IMAPISupport::CopyFolder** fügt den kopierten oder verschobenen Ordner als Unterordner des Zielordners hinzu.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8d7ad-159">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8d7ad-159">Notes to callers</span></span>

 <span data-ttu-id="8d7ad-160">**IMAPISupport::CopyFolder** ermöglicht das gleichzeitige Umbenennen und Verschieben von Ordnern sowie das Kopieren oder Verschieben von Unterordnern des betroffenen Ordners.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="8d7ad-161">Um alle im kopierten oder verschobenen Ordner geschachtelten Unterordner zu kopieren oder zu verschieben, übergeben Sie das COPY_SUBFOLDERS in  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="8d7ad-162">Erwarten Sie die folgenden Rückgabewerte unter den folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="8d7ad-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="8d7ad-163">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="8d7ad-163">**Condition**</span></span>|<span data-ttu-id="8d7ad-164">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="8d7ad-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d7ad-165">**CopyFolder** hat den Ordner und alle unterordner erfolgreich kopiert oder verschoben, sofern zutreffend.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="8d7ad-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d7ad-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="8d7ad-167">**CopyFolder** konnte nicht alle Ordner erfolgreich kopieren oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="8d7ad-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="8d7ad-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="8d7ad-169">**CopyFolder** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="8d7ad-170">Beliebiger Fehlerwert</span><span class="sxs-lookup"><span data-stu-id="8d7ad-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="8d7ad-171">Wenn **CopyFolder** einen Fehlerwert zurückgibt, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="8d7ad-172">Ein oder mehrere Ordner hätten kopiert oder verschoben werden können, bevor **CopyFolder** den Fehler erlebte.</span><span class="sxs-lookup"><span data-stu-id="8d7ad-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d7ad-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d7ad-173">See also</span></span>



[<span data-ttu-id="8d7ad-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d7ad-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

