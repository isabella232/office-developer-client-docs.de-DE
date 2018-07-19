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
ms.openlocfilehash: 15cf8ff7e282035ddff53565aa92e81e3886729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792093"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="1915f-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="1915f-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="1915f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1915f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1915f-105">Löscht einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="1915f-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1915f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1915f-106">Parameters</span></span>

 <span data-ttu-id="1915f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1915f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="1915f-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="1915f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1915f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1915f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="1915f-110">[in] Ein Zeiger auf die Eintrags-ID des Unterordners zu löschen.</span><span class="sxs-lookup"><span data-stu-id="1915f-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="1915f-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1915f-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="1915f-112">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="1915f-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="1915f-113">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1915f-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1915f-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="1915f-114">_lpProgress_</span></span>
  
> <span data-ttu-id="1915f-115">[in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1915f-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="1915f-116">Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1915f-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="1915f-117">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG in _UlFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1915f-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="1915f-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1915f-118">_ulFlags_</span></span>
  
> <span data-ttu-id="1915f-119">[in] Eine Bitmaske aus Flags, die das Löschen des Unterordners steuert.</span><span class="sxs-lookup"><span data-stu-id="1915f-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="1915f-120">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1915f-120">The following flags can be set:</span></span>
    
<span data-ttu-id="1915f-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="1915f-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="1915f-122">Alle Unterordner des Unterordners auf den _LpEntryID_ sollte gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1915f-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="1915f-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="1915f-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="1915f-124">Alle Nachrichten in den Unterordner auf den _LpEntryID_ sollte gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1915f-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="1915f-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1915f-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="1915f-126">Eine Statusanzeige sollte angezeigt werden, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1915f-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1915f-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1915f-127">Return value</span></span>

<span data-ttu-id="1915f-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="1915f-128">S_OK</span></span> 
  
> <span data-ttu-id="1915f-129">Der angegebene Ordner wurde erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1915f-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="1915f-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="1915f-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="1915f-131">Der zu löschende Unterordner enthält Unterordner, und das Flag DEL_FOLDERS wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1915f-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="1915f-132">Die Unterordner wurden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1915f-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="1915f-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="1915f-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="1915f-134">Der zu löschende Unterordner enthält Nachrichten, und das Flag DEL_MESSAGES wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1915f-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="1915f-135">Der Unterordner wurde nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1915f-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="1915f-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="1915f-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="1915f-137">Der Aufruf war erfolgreich, aber nicht alle Einträge erfolgreich gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="1915f-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="1915f-138">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="1915f-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1915f-139">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="1915f-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1915f-140">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="1915f-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1915f-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1915f-141">Remarks</span></span>

<span data-ttu-id="1915f-142">Die **IMAPIFolder::DeleteFolder** -Methode löscht einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="1915f-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="1915f-143">In der Standardeinstellung **DeleteFolder** funktioniert nur bei leeren Ordnern, jedoch können Sie sie erfolgreich für nicht leeren Ordner durch zwei Werte festlegen: DEL_FOLDERS und DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="1915f-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="1915f-144">Nur leere Ordner oder die Ordner, in denen die DEL_FOLDERS und die DEL_MESSAGES Kennzeichen für den Aufruf **DeleteFolder** festlegen können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1915f-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="1915f-145">DEL_FOLDERS können alle Unterordner des Ordners entfernt werden soll. DEL_MESSAGES können alle Nachrichten von den Ordner entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1915f-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1915f-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="1915f-146">Notes to implementers</span></span>

<span data-ttu-id="1915f-147">Wenn der Löschvorgang mehrere Ordner umfasst, führen Sie den Vorgang für jeden Ordner möglichst vollständig.</span><span class="sxs-lookup"><span data-stu-id="1915f-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="1915f-148">Manchmal einen der zu löschenden Ordner wurde ist nicht vorhanden oder verschoben oder kopiert wurde an anderer Stelle.</span><span class="sxs-lookup"><span data-stu-id="1915f-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="1915f-149">Beenden Sie den Vorgang nicht vorzeitig auf, es sei denn, ein Fehler, die außerhalb Ihrer Kontrolle auftritt, wie nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder der Beschädigung im Nachrichtenspeicher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1915f-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1915f-150">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1915f-150">Notes to callers</span></span>

<span data-ttu-id="1915f-151">Diese Rückgabewerte unter folgenden Umständen zu erwarten.</span><span class="sxs-lookup"><span data-stu-id="1915f-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="1915f-152">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="1915f-152">**Condition**</span></span>|<span data-ttu-id="1915f-153">**Rückgabewert**</span><span class="sxs-lookup"><span data-stu-id="1915f-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1915f-154">Jede Nachricht und Unterordner **DeleteFolder** wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1915f-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="1915f-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="1915f-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="1915f-156">**DeleteFolder** konnte jede Nachricht und Unterordner erfolgreich zu löschen.</span><span class="sxs-lookup"><span data-stu-id="1915f-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="1915f-157">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1915f-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="1915f-158">**DeleteFolder** konnte nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1915f-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="1915f-159">Einen Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1915f-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="1915f-160">Wenn **DeleteFolder** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1915f-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="1915f-161">**DeleteFolder** wurden möglicherweise eine oder mehrere Nachrichten und Unterordner löschen, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1915f-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="1915f-162">Wenn eine oder mehrere Unterordner können nicht gelöscht werden, gibt **DeleteFolder** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, je nach der Implementierung der Nachricht Informationsdienst zurück.</span><span class="sxs-lookup"><span data-stu-id="1915f-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1915f-163">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="1915f-163">MFCMAPI reference</span></span>

<span data-ttu-id="1915f-164">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1915f-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1915f-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1915f-165">**File**</span></span>|<span data-ttu-id="1915f-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1915f-166">**Function**</span></span>|<span data-ttu-id="1915f-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1915f-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1915f-168">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1915f-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="1915f-169">CMsgStoreDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="1915f-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="1915f-170">MFCMAPI (engl.) verwendet die **IMAPIFolder::DeleteFolder** -Methode zum Löschen von Ordnern.</span><span class="sxs-lookup"><span data-stu-id="1915f-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1915f-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1915f-171">See also</span></span>



[<span data-ttu-id="1915f-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="1915f-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="1915f-173">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1915f-173">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

