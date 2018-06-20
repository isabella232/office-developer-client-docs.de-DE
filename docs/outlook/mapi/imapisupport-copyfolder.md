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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0b079b311a68459a43b0a7659ddfbe94d96d7f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792344"
---
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="7e49f-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="7e49f-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="7e49f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e49f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e49f-105">Kopiert oder Verschiebt einen Ordner von seinem aktuellen übergeordneten Ordner in einer anderen übergeordneten Ordner.</span><span class="sxs-lookup"><span data-stu-id="7e49f-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7e49f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e49f-106">Parameters</span></span>

 <span data-ttu-id="7e49f-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="7e49f-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="7e49f-108">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die stellt die Schnittstelle des übergeordneten Ordners des Ordners kopiert oder verschoben werden Zugriff auf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e49f-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="7e49f-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="7e49f-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="7e49f-110">[in] Ein Zeiger auf den übergeordneten Ordner des Ordners, kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e49f-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="7e49f-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7e49f-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="7e49f-112">[in] Die Byteanzahl von in die Eintrags-ID auf _LpEntryID_zeigt.</span><span class="sxs-lookup"><span data-stu-id="7e49f-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="7e49f-113">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7e49f-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="7e49f-114">[in] Ein Zeiger auf die Eintrags-ID des Ordners, kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e49f-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="7e49f-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7e49f-115">_lpInterface_</span></span>
  
> <span data-ttu-id="7e49f-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="7e49f-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="7e49f-117">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="7e49f-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="7e49f-118">[in] Ein Zeiger auf den Ordner, der den Empfangsordner kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e49f-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="7e49f-119">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="7e49f-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="7e49f-120">[in] Ein Zeiger auf den Namen des Ordners kopiert oder verschoben werden soll andernfalls NULL, die angibt, dass der Ordner kopierte oder verschobene als Quellordners (in den Ordner auf den _LpEntryID_) den gleichen Namen verfügen soll.</span><span class="sxs-lookup"><span data-stu-id="7e49f-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="7e49f-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7e49f-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="7e49f-122">[in] Ein Handle für das Fenster für das Dialogfeld Symbol Status und zugehörige Fenster.</span><span class="sxs-lookup"><span data-stu-id="7e49f-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="7e49f-123">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7e49f-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="7e49f-124">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="7e49f-124">_lpProgress_</span></span>
  
> <span data-ttu-id="7e49f-125">[in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e49f-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="7e49f-126">Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e49f-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="7e49f-127">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG in _UlFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7e49f-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="7e49f-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e49f-128">_ulFlags_</span></span>
  
> <span data-ttu-id="7e49f-129">[in] Eine Bitmaske aus Flags, die steuert, wie der kopieren oder verschieben-Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e49f-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="7e49f-130">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7e49f-130">The following flags can be set:</span></span>
    
<span data-ttu-id="7e49f-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="7e49f-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="7e49f-132">Alle Unterordner des Ordners sollte kopiert oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="7e49f-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="7e49f-133">Wenn COPY_SUBFOLDERS für einen Kopiervorgang nicht festgelegt ist, wird nur der Ordner, die vom _LpEntryID_ kopiert.</span><span class="sxs-lookup"><span data-stu-id="7e49f-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="7e49f-134">Mit einem Verschiebevorgang wird das Verhalten COPY_SUBFOLDERS standardmäßig unabhängig davon, ob das Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7e49f-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="7e49f-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="7e49f-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="7e49f-136">Fordert die Anzeige einer Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="7e49f-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="7e49f-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="7e49f-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="7e49f-138">Der Ordner verschoben werden soll anstelle von kopiert.</span><span class="sxs-lookup"><span data-stu-id="7e49f-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="7e49f-139">Wenn FOLDER_MOVE nicht festgelegt ist, wird der Ordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="7e49f-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="7e49f-140">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7e49f-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7e49f-141">Der Name des Ordners ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="7e49f-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="7e49f-142">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Name des Ordners im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="7e49f-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7e49f-143">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7e49f-143">Return value</span></span>

<span data-ttu-id="7e49f-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e49f-144">S_OK</span></span> 
  
> <span data-ttu-id="7e49f-145">Der Ordner wurde erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="7e49f-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="7e49f-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="7e49f-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="7e49f-147">Der Name des Ordners, die verschoben oder kopiert ist identisch mit der von einem Unterordner im Zielordner.</span><span class="sxs-lookup"><span data-stu-id="7e49f-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="7e49f-148">Der Nachricht Speicheranbieter erfordert, dass Ordnernamen eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7e49f-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="7e49f-149">Der Vorgang wird beendet, ohne abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7e49f-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="7e49f-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="7e49f-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="7e49f-151">Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="7e49f-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="7e49f-152">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7e49f-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7e49f-153">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="7e49f-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7e49f-154">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7e49f-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e49f-155">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7e49f-155">Remarks</span></span>

<span data-ttu-id="7e49f-156">Die **IMAPISupport::CopyFolder** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="7e49f-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="7e49f-157">Nachricht-Anbieter können in ihrer Durchführung des [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) zu kopieren oder verschieben ein einzelnes Ordners aus einem übergeordneten Ordner in einen anderen **IMAPISupport::CopyFolder** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7e49f-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="7e49f-158">**IMAPISupport::CopyFolder** fügt den kopierte oder verschobenen Ordner als Unterordner des Zielordners.</span><span class="sxs-lookup"><span data-stu-id="7e49f-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7e49f-159">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7e49f-159">Notes to callers</span></span>

 <span data-ttu-id="7e49f-160">**IMAPISupport::CopyFolder** ermöglicht das gleichzeitige umbenennen und Verschieben von Ordnern und das Kopieren oder Verschieben von Unterordner des betroffenen.</span><span class="sxs-lookup"><span data-stu-id="7e49f-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="7e49f-161">Zum Kopieren oder verschieben alle Unterordner im Ordner kopiert oder verschoben geschachtelt, übergeben Sie die Kennzeichen COPY_SUBFOLDERS _UlFlags_.</span><span class="sxs-lookup"><span data-stu-id="7e49f-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="7e49f-162">Davon ausgehen Sie, dass die folgenden Rückgabewerte in den folgenden Situationen:</span><span class="sxs-lookup"><span data-stu-id="7e49f-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="7e49f-163">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="7e49f-163">**Condition**</span></span>|<span data-ttu-id="7e49f-164">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="7e49f-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e49f-165">**CopyFolder** erfolgreich kopieren oder verschieben den Ordner und alle Unterordner ein, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="7e49f-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="7e49f-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e49f-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="7e49f-167">**CopyFolder** konnte erfolgreich kopieren oder verschieben Sie alle Ordner.</span><span class="sxs-lookup"><span data-stu-id="7e49f-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="7e49f-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="7e49f-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="7e49f-169">**CopyFolder** konnte nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7e49f-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="7e49f-170">Einen anderen Fehlerwert als</span><span class="sxs-lookup"><span data-stu-id="7e49f-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="7e49f-171">Wenn **CopyFolder** einen Fehlerwert zurückgibt, fahren Sie unter der Voraussetzung, die keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7e49f-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="7e49f-172">Einen oder mehrere Ordner konnte kopiert oder verschoben wurden vor dem **CopyFolder** den Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7e49f-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e49f-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e49f-173">See also</span></span>



[<span data-ttu-id="7e49f-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e49f-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

