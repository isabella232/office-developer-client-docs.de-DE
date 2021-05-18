---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406913"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="64d07-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="64d07-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="64d07-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64d07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64d07-105">Legt das flag MSGFLAG_READ in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer oder mehreren Nachrichten des Ordners fest oder entfernt es und verwaltet das Senden von Leseberichten.</span><span class="sxs-lookup"><span data-stu-id="64d07-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="64d07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64d07-106">Parameters</span></span>

<span data-ttu-id="64d07-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="64d07-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="64d07-108">[in] Ein Zeiger auf ein Array von [ENTRYLIST-Strukturen,](entrylist.md) die die Nachricht oder Nachrichten identifizieren, deren Lesekennzeichen festgelegt oder löschen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64d07-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="64d07-109">Wenn  _lpMsgList_ auf NULL festgelegt ist, werden die Leseflags für alle Nachrichten des Ordners festgelegt oder geräumt.</span><span class="sxs-lookup"><span data-stu-id="64d07-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="64d07-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="64d07-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="64d07-111">[in] Ein Handle zum übergeordneten Fenster des Statusindikators.</span><span class="sxs-lookup"><span data-stu-id="64d07-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="64d07-112">Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MESSAGE_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64d07-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="64d07-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="64d07-113">_lpProgress_</span></span>
  
> <span data-ttu-id="64d07-114">[in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="64d07-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="64d07-115">Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der IMPLEMENTIERUNG von MAPI eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="64d07-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="64d07-116">Der _lpProgress-Parameter_ wird ignoriert, es sei denn, MESSAGE_DIALOG in _ulFlags festgelegt ist._</span><span class="sxs-lookup"><span data-stu-id="64d07-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="64d07-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="64d07-117">_ulFlags_</span></span>
  
> <span data-ttu-id="64d07-118">[in] Eine Bitmaske mit Flags, die die Einstellung des Lesekennzeichens einer Nachricht und die Verarbeitung von Leseberichten steuert.</span><span class="sxs-lookup"><span data-stu-id="64d07-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="64d07-119">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="64d07-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="64d07-120">CLEAR_READ_FLAG: Das MSGFLAG_READ sollte **in** der PR_MESSAGE_FLAGS und ein Lesebericht nicht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="64d07-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="64d07-121">CLEAR_NRN_PENDING: Das MSGFLAG_NRN_PENDING-Flag sollte **in** der PR_MESSAGE_FLAGS und kein ungelesener Bericht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="64d07-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="64d07-122">CLEAR_RN_PENDING: Das MSGFLAG_RN_PENDING sollte **in** der PR_MESSAGE_FLAGS und ein Lesebericht nicht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="64d07-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="64d07-123">GENERATE_RECEIPT_ONLY: Ein Lesebericht sollte gesendet werden, wenn ein Ausstehend ist, aber es sollte keine Änderung im Status des MSGFLAG_READ werden.</span><span class="sxs-lookup"><span data-stu-id="64d07-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="64d07-124">MAPI_DEFERRED_ERRORS: Ermöglicht die erfolgreiche Rückgabe von **SetReadFlags,** möglicherweise vor Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="64d07-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="64d07-125">MESSAGE_DIALOG: Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="64d07-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="64d07-126">SUPPRESS_RECEIPT: Ein ausstehender Lesebericht sollte abgebrochen werden, wenn ein Lesebericht angefordert wurde und dieser Aufruf den Status der Nachricht von ungelesen zu lesen ändert.</span><span class="sxs-lookup"><span data-stu-id="64d07-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="64d07-127">Wenn dieser Aufruf den Status der Nachricht nicht ändert, kann der Nachrichtenspeicheranbieter dieses Kennzeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="64d07-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="64d07-128">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="64d07-128">Return values</span></span>

<span data-ttu-id="64d07-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="64d07-129">S_OK</span></span> 
  
> <span data-ttu-id="64d07-130">Das Leseflag für die angegebene Nachricht oder Nachrichten wurde erfolgreich festgelegt oder geräumt.</span><span class="sxs-lookup"><span data-stu-id="64d07-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="64d07-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="64d07-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="64d07-132">Der Nachrichtenspeicheranbieter unterstützt die Unterdrückung von Leseberichten nicht.</span><span class="sxs-lookup"><span data-stu-id="64d07-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="64d07-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="64d07-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="64d07-134">Eine der folgenden inkompatiblen Kombinationen von Flags wird im  _ulFlags-Parameter_ festgelegt:</span><span class="sxs-lookup"><span data-stu-id="64d07-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="64d07-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="64d07-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="64d07-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="64d07-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="64d07-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="64d07-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="64d07-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="64d07-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="64d07-139">Der Aufruf ist erfolgreich, aber nicht alle Nachrichten wurden erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="64d07-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="64d07-140">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="64d07-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="64d07-141">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="64d07-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="64d07-142">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="64d07-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64d07-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="64d07-143">Remarks</span></span>

<span data-ttu-id="64d07-144">Mit **der IMAPIFolder::SetReadFlags-Methode** wird das MSGFLAG_READ-Flag in der **PR_MESSAGE_FLAGS-Eigenschaft** einer oder mehreren Nachrichten des Ordners festgelegt oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="64d07-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="64d07-145">Das Festlegen MSGFLAG_READ markiert eine Nachricht als gelesen, was nicht unbedingt darauf hinweist, dass der beabsichtigte Empfänger die Nachricht tatsächlich gelesen hat.</span><span class="sxs-lookup"><span data-stu-id="64d07-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="64d07-146">**SetReadFlags** verwaltet auch das Senden von Leseberichten.</span><span class="sxs-lookup"><span data-stu-id="64d07-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="64d07-147">Das Leseflag kann für Folgendes nicht geändert werden:</span><span class="sxs-lookup"><span data-stu-id="64d07-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="64d07-148">Nachrichten, die nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="64d07-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="64d07-149">Nachrichten, die an anderer Stelle verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="64d07-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="64d07-150">Nachrichten, die mit Lese-/Schreibberechtigung geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="64d07-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="64d07-151">Nachrichten, die derzeit übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="64d07-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="64d07-152">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="64d07-152">Notes to implementers</span></span>

<span data-ttu-id="64d07-153">Sie können entscheiden, das Senden von Leseberichten und die Anforderung zum Unterdrücken von Leseberichten nicht zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="64d07-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="64d07-154">Um das Unterdrücken eines Leseberichts zu vermeiden, geben Sie MAPI_E_NO_SUPPRESS zurück, wenn **SetReadFlags** mit SUPPRESS_RECEIPT  _ulFlags-Parameter aufgerufen_ wird.</span><span class="sxs-lookup"><span data-stu-id="64d07-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="64d07-155">Wenn der  _lpMsgList-Parameter_ auf mehrere Nachrichten zeigt, führen Sie den Vorgang für jede Nachricht so vollständig wie möglich aus.</span><span class="sxs-lookup"><span data-stu-id="64d07-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="64d07-156">Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der sich außerhalb Ihres Steuerelements befindet, z. B. nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="64d07-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="64d07-157">Wenn keines der Flags im  _ulFlags-Parameter_ festgelegt ist, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="64d07-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="64d07-158">Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.</span><span class="sxs-lookup"><span data-stu-id="64d07-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="64d07-159">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es sofort fest, und senden Sie alle ausstehenden Leseberichte, wenn die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) -Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="64d07-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="64d07-160">Wenn das SUPPRESS_RECEIPT festgelegt ist, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="64d07-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="64d07-161">Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.</span><span class="sxs-lookup"><span data-stu-id="64d07-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="64d07-162">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie sie fest, und brechen Sie alle ausstehenden Leseberichte ab.</span><span class="sxs-lookup"><span data-stu-id="64d07-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="64d07-163">Wenn das CLEAR_READ_FLAG festgelegt ist, löschen Sie das MSGFLAG_READ in der  PR_MESSAGE_FLAGS-Eigenschaft jeder Nachricht, und senden Sie keine Leseberichte.</span><span class="sxs-lookup"><span data-stu-id="64d07-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="64d07-164">Wenn das GENERATE_RECEIPT_ONLY festgelegt ist, senden Sie alle ausstehenden Leseberichte.</span><span class="sxs-lookup"><span data-stu-id="64d07-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="64d07-165">Legen Sie keine MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="64d07-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="64d07-166">Wenn sowohl die SUPPRESS_RECEIPT als auch GENERATE_RECEIPT_ONLY festgelegt sind, legen Sie **PR_READ_RECEIPT_REQUESTED** auf FALSE festgelegt, wenn sie festgelegt ist, und senden Sie keinen Lesebericht.</span><span class="sxs-lookup"><span data-stu-id="64d07-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="64d07-167">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="64d07-167">Notes to callers</span></span>

<span data-ttu-id="64d07-168">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="64d07-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="64d07-169">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="64d07-169">**Condition**</span></span>|<span data-ttu-id="64d07-170">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="64d07-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64d07-171">**SetReadFlags** hat jede Nachricht erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="64d07-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="64d07-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="64d07-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="64d07-173">**SetReadFlags** konnte nicht jede Nachricht erfolgreich verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="64d07-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="64d07-174">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="64d07-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="64d07-175">**SetReadFlags** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="64d07-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="64d07-176">Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="64d07-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="64d07-177">Wenn **SetReadFlags** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="64d07-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="64d07-178">**SetReadFlags** konnte möglicherweise das MSGFLAG_READ für eine oder mehrere Nachrichten festlegen oder löschen, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="64d07-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="64d07-179">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="64d07-179">MFCMAPI reference</span></span>

<span data-ttu-id="64d07-180">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="64d07-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="64d07-181">**Datei**</span><span class="sxs-lookup"><span data-stu-id="64d07-181">**File**</span></span>|<span data-ttu-id="64d07-182">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="64d07-182">**Function**</span></span>|<span data-ttu-id="64d07-183">**Comment**</span><span class="sxs-lookup"><span data-stu-id="64d07-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="64d07-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="64d07-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="64d07-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="64d07-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="64d07-186">MFCMAPI verwendet die **IMAPIFolder::SetReadFlags-Methode,** um den Lesestatus für die angegebenen Nachrichten manuell fest.</span><span class="sxs-lookup"><span data-stu-id="64d07-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64d07-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64d07-187">See also</span></span>

- [<span data-ttu-id="64d07-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="64d07-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="64d07-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="64d07-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="64d07-190">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="64d07-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="64d07-191">PidTagReadReceiptRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="64d07-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="64d07-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="64d07-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="64d07-193">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="64d07-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="64d07-194">Verwenden von Makros für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="64d07-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

