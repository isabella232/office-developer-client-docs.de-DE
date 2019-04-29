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
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="90c11-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="90c11-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="90c11-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90c11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90c11-105">Löscht einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="90c11-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="90c11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="90c11-106">Parameters</span></span>

 <span data-ttu-id="90c11-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="90c11-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="90c11-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="90c11-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="90c11-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="90c11-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="90c11-110">in Ein Zeiger auf die Eintrags-ID des zu löschenden Unterordners.</span><span class="sxs-lookup"><span data-stu-id="90c11-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="90c11-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="90c11-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="90c11-112">in Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="90c11-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="90c11-113">Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90c11-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="90c11-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="90c11-114">_lpProgress_</span></span>
  
> <span data-ttu-id="90c11-115">in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="90c11-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="90c11-116">Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="90c11-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="90c11-117">Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird in _ulFlags_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90c11-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="90c11-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="90c11-118">_ulFlags_</span></span>
  
> <span data-ttu-id="90c11-119">in Eine Bitmaske von Flags, die das Löschen des Unterordners steuert.</span><span class="sxs-lookup"><span data-stu-id="90c11-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="90c11-120">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="90c11-120">The following flags can be set:</span></span>
    
<span data-ttu-id="90c11-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="90c11-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="90c11-122">Alle Unterordner des Unterordners, auf die durch _lpEntryID_ verwiesen wird, sollten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="90c11-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="90c11-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="90c11-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="90c11-124">Alle Nachrichten im Unterordner, auf die von _lpEntryID_ verwiesen wird, sollten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="90c11-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="90c11-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="90c11-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="90c11-126">Während des Vorgangs wird eine Statusanzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90c11-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90c11-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90c11-127">Return value</span></span>

<span data-ttu-id="90c11-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="90c11-128">S_OK</span></span> 
  
> <span data-ttu-id="90c11-129">Der angegebene Ordner wurde erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90c11-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="90c11-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="90c11-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="90c11-131">Der gelöschte Ordner enthält Unterordner, und das DEL_FOLDERS-Flag wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90c11-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="90c11-132">Die Unterordner wurden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90c11-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="90c11-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="90c11-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="90c11-134">Der gelöschte Ordner enthält Nachrichten, und das DEL_MESSAGES-Flag wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90c11-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="90c11-135">Der Unterordner wurde nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90c11-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="90c11-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="90c11-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="90c11-137">Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90c11-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="90c11-138">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="90c11-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="90c11-139">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="90c11-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="90c11-140">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="90c11-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90c11-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90c11-141">Remarks</span></span>

<span data-ttu-id="90c11-142">Die **IMAPIFolder::D eletefolder** -Methode löscht einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="90c11-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="90c11-143">Standardmäßig wird **DeleteFolder** nur in leeren Ordnern ausgeführt, aber Sie können es erfolgreich in nicht leeren Ordnern verwenden, indem Sie zwei Flags festlegen: DEL_FOLDERS und DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="90c11-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="90c11-144">Nur leere Ordner oder Ordner, die sowohl die DEL_FOLDERS-als auch die DEL_MESSAGES-Flags für den **DeleteFolder** -Aufruf festlegen, können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="90c11-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="90c11-145">DEL_FOLDERS ermöglicht das Entfernen aller Unterordner des Ordners; DEL_MESSAGES ermöglicht das Entfernen aller Nachrichten des Ordners.</span><span class="sxs-lookup"><span data-stu-id="90c11-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="90c11-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="90c11-146">Notes to implementers</span></span>

<span data-ttu-id="90c11-147">Wenn der Löschvorgang mehr als einen Ordner umfasst, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus.</span><span class="sxs-lookup"><span data-stu-id="90c11-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="90c11-148">Manchmal ist einer der zu löschenden Ordner nicht vorhanden oder wurde an anderer Stelle verschoben oder kopiert.</span><span class="sxs-lookup"><span data-stu-id="90c11-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="90c11-149">Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihres Steuerelements liegt, beispielsweise ausgehender Arbeitsspeicher, unzureichender Festplattenspeicherplatz oder Beschädigung im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="90c11-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="90c11-150">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="90c11-150">Notes to callers</span></span>

<span data-ttu-id="90c11-151">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="90c11-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="90c11-152">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="90c11-152">**Condition**</span></span>|<span data-ttu-id="90c11-153">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="90c11-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90c11-154">**DeleteFolder** hat alle Nachrichten und Unterordner erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90c11-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="90c11-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="90c11-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="90c11-156">**DeleteFolder** konnte nicht alle Nachrichten und Unterordner erfolgreich löschen.</span><span class="sxs-lookup"><span data-stu-id="90c11-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="90c11-157">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="90c11-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="90c11-158">**DeleteFolder** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="90c11-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="90c11-159">Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="90c11-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="90c11-160">Wenn **DeleteFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="90c11-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="90c11-161">**DeleteFolder** kann möglicherweise eine oder mehrere der Nachrichten und Unterordner gelöscht haben, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="90c11-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="90c11-162">Wenn ein oder mehrere Unterordner nicht gelöscht werden können, gibt **DELETEFOLDER** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND zurück, je nach der Implementierung des Nachrichtenspeicher Anbieters.</span><span class="sxs-lookup"><span data-stu-id="90c11-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="90c11-163">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="90c11-163">MFCMAPI reference</span></span>

<span data-ttu-id="90c11-164">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="90c11-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="90c11-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="90c11-165">**File**</span></span>|<span data-ttu-id="90c11-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="90c11-166">**Function**</span></span>|<span data-ttu-id="90c11-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="90c11-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="90c11-168">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="90c11-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="90c11-169">CMsgStoreDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="90c11-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="90c11-170">MFCMAPI verwendet die **IMAPIFolder::D eletefolder** -Methode, um Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="90c11-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90c11-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90c11-171">See also</span></span>



[<span data-ttu-id="90c11-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="90c11-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="90c11-173">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="90c11-173">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

