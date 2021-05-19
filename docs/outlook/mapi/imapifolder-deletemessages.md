---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426072"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="48f8a-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="48f8a-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="48f8a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48f8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48f8a-105">Löscht eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="48f8a-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="48f8a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48f8a-106">Parameters</span></span>

 <span data-ttu-id="48f8a-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="48f8a-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="48f8a-108">[in] Ein Zeiger auf eine [ENTRYLIST-Struktur,](entrylist.md) die die Anzahl der zu löschenden Nachrichten und ein Array von [ENTRYID-Strukturen](entryid.md) enthält, die die Nachrichten identifizieren.</span><span class="sxs-lookup"><span data-stu-id="48f8a-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="48f8a-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="48f8a-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="48f8a-110">[in] Ein Handle zum übergeordneten Fenster des Statusindikators.</span><span class="sxs-lookup"><span data-stu-id="48f8a-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="48f8a-111">Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MESSAGE_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="48f8a-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="48f8a-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="48f8a-112">_lpProgress_</span></span>
  
> <span data-ttu-id="48f8a-113">[in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="48f8a-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="48f8a-114">Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="48f8a-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="48f8a-115">Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das MESSAGE_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="48f8a-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="48f8a-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="48f8a-116">_ulFlags_</span></span>
  
> <span data-ttu-id="48f8a-117">[in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="48f8a-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="48f8a-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="48f8a-118">The following flags can be set:</span></span>
    
<span data-ttu-id="48f8a-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="48f8a-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="48f8a-120">Entfernt dauerhaft alle Nachrichten, einschließlich der gelöschten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="48f8a-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="48f8a-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="48f8a-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="48f8a-122">Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="48f8a-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="48f8a-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48f8a-123">Return value</span></span>

<span data-ttu-id="48f8a-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="48f8a-124">S_OK</span></span> 
  
> <span data-ttu-id="48f8a-125">Die angegebene Nachricht oder Nachrichten wurde erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="48f8a-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="48f8a-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="48f8a-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="48f8a-127">Der Aufruf ist erfolgreich, aber nicht alle Nachrichten wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="48f8a-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="48f8a-128">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="48f8a-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="48f8a-129">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="48f8a-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="48f8a-130">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="48f8a-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48f8a-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48f8a-131">Remarks</span></span>

<span data-ttu-id="48f8a-132">Die **IMAPIFolder::D eleteMessages-Methode** löscht Nachrichten aus einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="48f8a-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="48f8a-133">Nachrichten, die nicht vorhanden sind, an eine andere Stelle verschoben wurden, die mit Lese-/Schreibberechtigung geöffnet sind oder die derzeit übermittelt werden, können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="48f8a-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="48f8a-134">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="48f8a-134">Notes to implementers</span></span>

<span data-ttu-id="48f8a-135">Wenn der Löschvorgang mehrere Nachrichten umfasst, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus, auch wenn eine oder mehrere Nachrichten nicht gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="48f8a-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="48f8a-136">Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der sich außerhalb Ihres Steuerelements befindet, z. B. nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="48f8a-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="48f8a-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="48f8a-137">Notes to callers</span></span>

<span data-ttu-id="48f8a-138">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="48f8a-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="48f8a-139">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="48f8a-139">**Condition**</span></span>|<span data-ttu-id="48f8a-140">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="48f8a-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48f8a-141">**DeleteMessages** hat jede Nachricht erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="48f8a-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="48f8a-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="48f8a-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="48f8a-143">**DeleteMessages** konnte nicht alle Nachrichten und Unterordner erfolgreich löschen.</span><span class="sxs-lookup"><span data-stu-id="48f8a-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="48f8a-144">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="48f8a-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="48f8a-145">**DeleteMessages** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="48f8a-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="48f8a-146">Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="48f8a-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="48f8a-147">Wenn **DeleteMessages** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="48f8a-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="48f8a-148">**DeleteMessages** konnte möglicherweise eine oder mehrere der Nachrichten löschen, bevor der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="48f8a-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="48f8a-149">**DeleteMessages** gibt MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, abhängig von der Implementierung des Nachrichtenspeichers, zurück.</span><span class="sxs-lookup"><span data-stu-id="48f8a-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="48f8a-150">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="48f8a-150">MFCMAPI reference</span></span>

<span data-ttu-id="48f8a-151">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="48f8a-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="48f8a-152">**Datei**</span><span class="sxs-lookup"><span data-stu-id="48f8a-152">**File**</span></span>|<span data-ttu-id="48f8a-153">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="48f8a-153">**Function**</span></span>|<span data-ttu-id="48f8a-154">**Comment**</span><span class="sxs-lookup"><span data-stu-id="48f8a-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="48f8a-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="48f8a-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="48f8a-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="48f8a-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="48f8a-157">MFCMAPI verwendet die **IMAPIFolder::D eleteMessages-Methode,** um die angegebenen Nachrichten zu löschen.</span><span class="sxs-lookup"><span data-stu-id="48f8a-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48f8a-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48f8a-158">See also</span></span>



[<span data-ttu-id="48f8a-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="48f8a-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="48f8a-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="48f8a-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="48f8a-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="48f8a-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="48f8a-162">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="48f8a-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="48f8a-163">Verwenden von Makros für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="48f8a-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

