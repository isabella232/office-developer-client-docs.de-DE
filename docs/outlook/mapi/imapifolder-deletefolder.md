---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417406"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="cf9ee-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="cf9ee-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="cf9ee-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf9ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf9ee-105">Löscht einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cf9ee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf9ee-106">Parameters</span></span>

 <span data-ttu-id="cf9ee-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="cf9ee-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="cf9ee-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="cf9ee-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="cf9ee-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="cf9ee-110">[in] Ein Zeiger auf die Eintrags-ID des zu löschende Unterordners.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="cf9ee-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="cf9ee-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="cf9ee-112">[in] Ein Handle zum übergeordneten Fenster des Statusindikators.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="cf9ee-113">Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="cf9ee-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="cf9ee-114">_lpProgress_</span></span>
  
> <span data-ttu-id="cf9ee-115">[in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="cf9ee-116">Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="cf9ee-117">Der _lpProgress-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG ist in _ulFlags festgelegt._</span><span class="sxs-lookup"><span data-stu-id="cf9ee-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="cf9ee-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf9ee-118">_ulFlags_</span></span>
  
> <span data-ttu-id="cf9ee-119">[in] Eine Bitmaske mit Flags, die das Löschen des Unterordners steuert.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="cf9ee-120">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cf9ee-120">The following flags can be set:</span></span>
    
<span data-ttu-id="cf9ee-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="cf9ee-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="cf9ee-122">Alle Unterordner des Unterordners, auf die  _von lpEntryID_ verwiesen wird, sollten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="cf9ee-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="cf9ee-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="cf9ee-124">Alle Nachrichten im Unterordner, auf die  _von lpEntryID_ verwiesen wird, sollten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="cf9ee-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="cf9ee-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="cf9ee-126">Ein Statusindikator sollte angezeigt werden, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf9ee-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf9ee-127">Return value</span></span>

<span data-ttu-id="cf9ee-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf9ee-128">S_OK</span></span> 
  
> <span data-ttu-id="cf9ee-129">Der angegebene Ordner wurde erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="cf9ee-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="cf9ee-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="cf9ee-131">Der zu löschende Unterordner enthält Unterordner, und das DEL_FOLDERS wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="cf9ee-132">Die Unterordner wurden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="cf9ee-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="cf9ee-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="cf9ee-134">Der zu löschende Unterordner enthält Nachrichten, und das DEL_MESSAGES wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="cf9ee-135">Der Unterordner wurde nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="cf9ee-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="cf9ee-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="cf9ee-137">Der Aufruf ist erfolgreich, aber nicht alle Einträge wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="cf9ee-138">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="cf9ee-139">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="cf9ee-140">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ee-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf9ee-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cf9ee-141">Remarks</span></span>

<span data-ttu-id="cf9ee-142">Die **IMAPIFolder::D eleteFolder-Methode** löscht einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="cf9ee-143">**DeleteFolder** wird standardmäßig nur für leere Ordner verwendet, Sie können es jedoch erfolgreich für nicht leere Ordner verwenden, indem Sie zwei Flags festlegen: DEL_FOLDERS und DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="cf9ee-144">Es können nur leere Ordner oder Ordner gelöscht werden, die die DEL_FOLDERS und DEL_MESSAGES für den **DeleteFolder-Aufruf** festlegen.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="cf9ee-145">DEL_FOLDERS ermöglicht das Entfernen aller Unterordner des Ordners. DEL_MESSAGES können alle Nachrichten des Ordners entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cf9ee-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="cf9ee-146">Notes to implementers</span></span>

<span data-ttu-id="cf9ee-147">Wenn der Löschvorgang mehrere Ordner umfasst, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="cf9ee-148">Manchmal ist einer der zu löschenden Ordner nicht vorhanden oder wurde an anderer Stelle verschoben oder kopiert.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="cf9ee-149">Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der sich außerhalb Ihres Steuerelements befindet, z. B. nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="cf9ee-150">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="cf9ee-150">Notes to callers</span></span>

<span data-ttu-id="cf9ee-151">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="cf9ee-152">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="cf9ee-152">**Condition**</span></span>|<span data-ttu-id="cf9ee-153">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="cf9ee-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf9ee-154">**DeleteFolder** hat alle Nachrichten und Unterordner erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="cf9ee-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf9ee-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="cf9ee-156">**DeleteFolder** konnte nicht alle Nachrichten und Unterordner erfolgreich löschen.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="cf9ee-157">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cf9ee-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="cf9ee-158">**DeleteFolder** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="cf9ee-159">Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cf9ee-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="cf9ee-160">Wenn **DeleteFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="cf9ee-161">**DeleteFolder** konnte möglicherweise eine oder mehrere Nachrichten und Unterordner löschen, bevor der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="cf9ee-162">Wenn ein oder mehrere Unterordner nicht gelöscht werden können, gibt **DeleteFolder** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, abhängig von der Implementierung des Nachrichtenspeicheranbieters, zurück.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cf9ee-163">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="cf9ee-163">MFCMAPI reference</span></span>

<span data-ttu-id="cf9ee-164">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cf9ee-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="cf9ee-165">**File**</span></span>|<span data-ttu-id="cf9ee-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="cf9ee-166">**Function**</span></span>|<span data-ttu-id="cf9ee-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="cf9ee-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf9ee-168">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="cf9ee-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="cf9ee-169">CMsgStoreDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="cf9ee-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="cf9ee-170">MFCMAPI verwendet die **IMAPIFolder::D eleteFolder-Methode,** um Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf9ee-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf9ee-171">See also</span></span>



[<span data-ttu-id="cf9ee-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="cf9ee-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="cf9ee-173">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="cf9ee-173">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

