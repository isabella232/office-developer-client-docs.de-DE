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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280120"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="33da1-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="33da1-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="33da1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33da1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33da1-105">Löscht eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="33da1-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="33da1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33da1-106">Parameters</span></span>

 <span data-ttu-id="33da1-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="33da1-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="33da1-108">in Ein Zeiger auf eine [entrylist](entrylist.md) -Struktur, die die Anzahl der zu löschenden Nachrichten und ein Array von [Eintrags](entryid.md) -ID-Strukturen enthält, die die Nachrichten identifizieren.</span><span class="sxs-lookup"><span data-stu-id="33da1-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="33da1-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="33da1-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="33da1-110">in Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="33da1-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="33da1-111">Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="33da1-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="33da1-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="33da1-112">_lpProgress_</span></span>
  
> <span data-ttu-id="33da1-113">in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="33da1-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="33da1-114">Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="33da1-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="33da1-115">Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="33da1-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="33da1-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="33da1-116">_ulFlags_</span></span>
  
> <span data-ttu-id="33da1-117">in Eine Bitmaske von Flags, die steuert, wie die Nachrichten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="33da1-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="33da1-118">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="33da1-118">The following flags can be set:</span></span>
    
<span data-ttu-id="33da1-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="33da1-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="33da1-120">Entfernt alle Nachrichten, einschließlich der gelöschten, dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="33da1-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="33da1-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="33da1-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="33da1-122">Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="33da1-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="33da1-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33da1-123">Return value</span></span>

<span data-ttu-id="33da1-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="33da1-124">S_OK</span></span> 
  
> <span data-ttu-id="33da1-125">Die angegebenen Nachrichten wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="33da1-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="33da1-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="33da1-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="33da1-127">Der Aufruf wurde erfolgreich ausgeführt, aber nicht alle Nachrichten wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="33da1-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="33da1-128">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="33da1-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="33da1-129">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="33da1-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="33da1-130">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="33da1-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33da1-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33da1-131">Remarks</span></span>

<span data-ttu-id="33da1-132">Mit der **IMAPIFolder::D eletemessages** -Methode werden Nachrichten aus einem Ordner gelöscht.</span><span class="sxs-lookup"><span data-stu-id="33da1-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="33da1-133">Nachrichten, die nicht vorhanden sind, die an anderer Stelle verschoben wurden, die mit Lese-/Schreibzugriff-Berechtigung geöffnet oder derzeit übermittelt wurden, können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="33da1-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="33da1-134">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="33da1-134">Notes to implementers</span></span>

<span data-ttu-id="33da1-135">Wenn der Löschvorgang mehr als eine Nachricht umfasst, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus, selbst wenn eine oder mehrere der Nachrichten nicht gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="33da1-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="33da1-136">Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihres Steuerelements liegt, beispielsweise ausgehender Arbeitsspeicher, unzureichender Festplattenspeicherplatz oder Beschädigung im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="33da1-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="33da1-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="33da1-137">Notes to callers</span></span>

<span data-ttu-id="33da1-138">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="33da1-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="33da1-139">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="33da1-139">**Condition**</span></span>|<span data-ttu-id="33da1-140">**Rückgabewert**</span><span class="sxs-lookup"><span data-stu-id="33da1-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33da1-141">**DeleteMessages** hat jede Nachricht erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="33da1-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="33da1-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="33da1-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="33da1-143">**DeleteMessages** konnte nicht alle Nachrichten und Unterordner erfolgreich löschen.</span><span class="sxs-lookup"><span data-stu-id="33da1-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="33da1-144">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="33da1-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="33da1-145">**DeleteMessages** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="33da1-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="33da1-146">Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="33da1-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="33da1-147">Wenn **DeleteMessages** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="33da1-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="33da1-148">**DeleteMessages** kann möglicherweise eine oder mehrere der Nachrichten löschen, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="33da1-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="33da1-149">**DeleteMessages** gibt MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND in Abhängigkeit von der Implementierung des Nachrichtenspeichers zurück.</span><span class="sxs-lookup"><span data-stu-id="33da1-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="33da1-150">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="33da1-150">MFCMAPI reference</span></span>

<span data-ttu-id="33da1-151">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="33da1-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="33da1-152">**Datei**</span><span class="sxs-lookup"><span data-stu-id="33da1-152">**File**</span></span>|<span data-ttu-id="33da1-153">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="33da1-153">**Function**</span></span>|<span data-ttu-id="33da1-154">**Comment**</span><span class="sxs-lookup"><span data-stu-id="33da1-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="33da1-155">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="33da1-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="33da1-156">CFolderDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="33da1-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="33da1-157">MFCMAPI verwendet die **IMAPIFolder::D-eletemessages** -Methode, um die angegebenen Nachrichten zu löschen.</span><span class="sxs-lookup"><span data-stu-id="33da1-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33da1-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33da1-158">See also</span></span>



[<span data-ttu-id="33da1-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="33da1-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="33da1-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="33da1-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="33da1-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="33da1-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="33da1-162">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="33da1-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="33da1-163">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="33da1-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

