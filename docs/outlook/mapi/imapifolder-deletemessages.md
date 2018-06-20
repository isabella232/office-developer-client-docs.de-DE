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
ms.openlocfilehash: 7845abc4f3010daf8e13d56ac4b13d0333bad07e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792114"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="51b86-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="51b86-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="51b86-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51b86-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51b86-105">Löscht eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="51b86-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="51b86-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51b86-106">Parameters</span></span>

 <span data-ttu-id="51b86-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="51b86-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="51b86-108">[in] Ein Zeiger auf eine [ENTRYLIST](entrylist.md) -Struktur, die enthält die Anzahl der Nachrichten löschen und ein Array von [ENTRYID](entryid.md) -Strukturen, die die Nachrichten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="51b86-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="51b86-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="51b86-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="51b86-110">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="51b86-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="51b86-111">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="51b86-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="51b86-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="51b86-112">_lpProgress_</span></span>
  
> <span data-ttu-id="51b86-113">[in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51b86-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="51b86-114">Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51b86-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="51b86-115">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="51b86-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="51b86-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="51b86-116">_ulFlags_</span></span>
  
> <span data-ttu-id="51b86-117">[in] Eine Bitmaske aus Flags, die steuert, wie die Nachrichten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="51b86-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="51b86-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="51b86-118">The following flags can be set:</span></span>
    
<span data-ttu-id="51b86-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="51b86-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="51b86-120">Entfernt alle Nachrichten, einschließlich vorläufig Gelöschte Objekte.</span><span class="sxs-lookup"><span data-stu-id="51b86-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="51b86-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="51b86-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="51b86-122">Eine Statusanzeige wird angezeigt, wie der-Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="51b86-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51b86-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="51b86-123">Return value</span></span>

<span data-ttu-id="51b86-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="51b86-124">S_OK</span></span> 
  
> <span data-ttu-id="51b86-125">Die angegebene Nachricht(en) wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="51b86-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="51b86-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="51b86-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="51b86-127">Der Aufruf war erfolgreich, aber nicht alle Nachrichten erfolgreich gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="51b86-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="51b86-128">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="51b86-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="51b86-129">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="51b86-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="51b86-130">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="51b86-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51b86-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51b86-131">Remarks</span></span>

<span data-ttu-id="51b86-132">Die **IMAPIFolder::DeleteMessages** -Methode löscht Nachrichten aus einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="51b86-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="51b86-133">Nachrichten, die nicht vorhanden sind, an anderer Stelle verschoben wurden, die mit Lese-/Schreibzugriff geöffnet sind oder, die derzeit übermittelt hat, können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="51b86-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="51b86-134">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="51b86-134">Notes to implementers</span></span>

<span data-ttu-id="51b86-135">Wenn der Löschvorgang mehr als eine Nachricht umfasst, führen Sie den Vorgang möglichst vollständig für jeden Ordner, auch wenn eine oder mehrere Nachrichten nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="51b86-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="51b86-136">Beenden Sie den Vorgang nicht vorzeitig auf, es sei denn, ein Fehler, die außerhalb Ihrer Kontrolle auftritt, wie nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder der Beschädigung im Nachrichtenspeicher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51b86-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="51b86-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="51b86-137">Notes to callers</span></span>

<span data-ttu-id="51b86-138">Diese Rückgabewerte unter folgenden Umständen zu erwarten.</span><span class="sxs-lookup"><span data-stu-id="51b86-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="51b86-139">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="51b86-139">**Condition**</span></span>|<span data-ttu-id="51b86-140">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="51b86-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="51b86-141">Jede Nachricht **DeleteMessages** wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="51b86-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="51b86-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="51b86-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="51b86-143">**DeleteMessages** konnte nicht erfolgreich jede Nachricht und Unterordner löschen.</span><span class="sxs-lookup"><span data-stu-id="51b86-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="51b86-144">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="51b86-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="51b86-145">**DeleteMessages** konnte nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="51b86-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="51b86-146">Einen Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="51b86-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="51b86-147">Wenn **DeleteMessages** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="51b86-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="51b86-148">Möglicherweise wurden **DeleteMessages** können eine oder mehrere Nachrichten löschen, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="51b86-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="51b86-149">**DeleteMessages** gibt MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, je nach den Nachrichtenspeicher Implementierung zurück.</span><span class="sxs-lookup"><span data-stu-id="51b86-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="51b86-150">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="51b86-150">MFCMAPI reference</span></span>

<span data-ttu-id="51b86-151">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="51b86-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="51b86-152">**Datei**</span><span class="sxs-lookup"><span data-stu-id="51b86-152">**File**</span></span>|<span data-ttu-id="51b86-153">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="51b86-153">**Function**</span></span>|<span data-ttu-id="51b86-154">**Comment**</span><span class="sxs-lookup"><span data-stu-id="51b86-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="51b86-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="51b86-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="51b86-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="51b86-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="51b86-157">MFCMAPI (engl.) wird die **IMAPIFolder::DeleteMessages** -Methode zum Löschen der angegebenen Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="51b86-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51b86-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51b86-158">See also</span></span>



[<span data-ttu-id="51b86-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="51b86-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="51b86-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="51b86-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="51b86-161">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="51b86-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="51b86-162">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="51b86-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="51b86-163">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="51b86-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
