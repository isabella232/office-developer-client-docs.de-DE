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
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="7817e-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="7817e-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="7817e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7817e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7817e-105">Legt das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer oder mehrerer der Nachrichten des Ordners fest oder löscht das Senden von Lese Berichten.</span><span class="sxs-lookup"><span data-stu-id="7817e-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7817e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7817e-106">Parameters</span></span>

<span data-ttu-id="7817e-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="7817e-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="7817e-108">in Ein Zeiger auf ein Array von [entrylist](entrylist.md) -Strukturen, die die Nachricht oder Nachrichten identifizieren, die Read Flags haben, um festzulegen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7817e-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="7817e-109">Wenn _lpMsgList_ auf NULL festgelegt ist, werden die Lese Kennzeichen für alle Nachrichten des Ordners festgelegt oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7817e-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="7817e-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7817e-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="7817e-111">in Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="7817e-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="7817e-112">Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7817e-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="7817e-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="7817e-113">_lpProgress_</span></span>
  
> <span data-ttu-id="7817e-114">in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="7817e-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="7817e-115">Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Implementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="7817e-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="7817e-116">Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag wird in _ulFlags_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7817e-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="7817e-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7817e-117">_ulFlags_</span></span>
  
> <span data-ttu-id="7817e-118">in Eine Bitmaske von Flags, die die Einstellung der Read-Kennzeichnung einer Nachricht und die Verarbeitung von Lese Berichten steuert.</span><span class="sxs-lookup"><span data-stu-id="7817e-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="7817e-119">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7817e-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="7817e-120">CLEAR_READ_FLAG: das MSGFLAG_READ-flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und ein Lesebericht sollte nicht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7817e-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="7817e-121">CLEAR_NRN_PENDING: das MSGFLAG_NRN_PENDING-Flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und ein ungelesener Bericht sollte nicht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7817e-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="7817e-122">CLEAR_RN_PENDING: das MSGFLAG_RN_PENDING-Flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und ein Lesebericht sollte nicht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7817e-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="7817e-123">GENERATE_RECEIPT_ONLY: ein Lesebericht sollte gesendet werden, wenn ein ausstehender ist, aber es sollte keine Änderung des Status des MSGFLAG_READ-Flags geben.</span><span class="sxs-lookup"><span data-stu-id="7817e-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="7817e-124">MAPI_DEFERRED_ERRORS: ermöglicht es **SetReadFlags** , erfolgreich zurückzugeben, möglicherweise bevor der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7817e-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="7817e-125">MESSAGE_DIALOG: zeigt während des Vorgangs eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="7817e-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="7817e-126">SUPPRESS_RECEIPT: ein ausstehender Lesebericht sollte abgebrochen werden, wenn ein Lesebericht angefordert wurde und dieser Aufruf den Status der Nachricht von ungelesen in lesen ändert.</span><span class="sxs-lookup"><span data-stu-id="7817e-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="7817e-127">Wenn durch diesen Anruf der Status der Nachricht nicht geändert wird, kann der Nachrichtenspeicher Anbieter dieses Flag ignorieren.</span><span class="sxs-lookup"><span data-stu-id="7817e-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7817e-128">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7817e-128">Return values</span></span>

<span data-ttu-id="7817e-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="7817e-129">S_OK</span></span> 
  
> <span data-ttu-id="7817e-130">Die Read-Kennzeichnung für die angegebenen Nachrichten wurde erfolgreich festgelegt oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7817e-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="7817e-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="7817e-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="7817e-132">Der Nachrichtenspeicher Anbieter unterstützt die Unterdrückung von Lese Berichten nicht.</span><span class="sxs-lookup"><span data-stu-id="7817e-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="7817e-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7817e-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="7817e-134">Eine der folgenden inkompatiblen Kombinationen von Flags wird im _ulFlags_ -Parameter festgelegt:</span><span class="sxs-lookup"><span data-stu-id="7817e-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="7817e-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="7817e-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="7817e-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="7817e-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="7817e-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="7817e-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="7817e-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="7817e-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="7817e-139">Der Aufruf war erfolgreich, aber nicht alle Nachrichten wurden erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7817e-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="7817e-140">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="7817e-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7817e-141">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="7817e-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7817e-142">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7817e-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7817e-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7817e-143">Remarks</span></span>

<span data-ttu-id="7817e-144">Mit der **IMAPIFolder:: SetReadFlags** -Methode wird das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** -Eigenschaft eines oder mehrerer der Nachrichten des Ordners festgelegt oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7817e-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="7817e-145">Durch Festlegen des MSGFLAG_READ-Flags wird eine Nachricht als gelesen markiert, was nicht unbedingt darauf hinweist, dass der vorgesehene Empfänger die Nachricht tatsächlich gelesen hat.</span><span class="sxs-lookup"><span data-stu-id="7817e-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="7817e-146">**SetReadFlags** verwaltet auch das Senden von Lese Berichten.</span><span class="sxs-lookup"><span data-stu-id="7817e-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="7817e-147">Die Read-Kennzeichnung kann für Folgendes nicht geändert werden:</span><span class="sxs-lookup"><span data-stu-id="7817e-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="7817e-148">Nachrichten, die nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7817e-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="7817e-149">Nachrichten, die an anderer Stelle verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="7817e-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="7817e-150">Mit Lese-/Schreibzugriff geöffnete Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="7817e-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="7817e-151">Nachrichten, die derzeit übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="7817e-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="7817e-152">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7817e-152">Notes to implementers</span></span>

<span data-ttu-id="7817e-153">Sie können sich entscheiden, das Senden von Lese Berichten und die Anforderung zur Unterdrückung von Lese Berichten nicht zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7817e-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="7817e-154">Um zu verhindern, dass ein Lesebericht unterdrückt wird, geben Sie MAPI_E_NO_SUPPRESS zurück, wenn **SetReadFlags** mit SUPPRESS_RECEIPT im _ulFlags_ -Parameter festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7817e-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="7817e-155">Wenn der Parameter _lpMsgList_ auf mehr als eine Nachricht zeigt, führen Sie den Vorgang für jede Nachricht so vollständig wie möglich aus.</span><span class="sxs-lookup"><span data-stu-id="7817e-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="7817e-156">Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihres Steuerelements liegt, beispielsweise ausgehender Arbeitsspeicher, unzureichender Festplattenspeicherplatz oder Beschädigung im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="7817e-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="7817e-157">Wenn keines der Flags im Parameter _ulFlags_ festgelegt wird, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="7817e-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="7817e-158">Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.</span><span class="sxs-lookup"><span data-stu-id="7817e-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="7817e-159">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie Sie sofort fest, und senden Sie ausstehende Lese Berichte, wenn die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7817e-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="7817e-160">Wenn das SUPPRESS_RECEIPT-Flag festgelegt ist, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="7817e-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="7817e-161">Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.</span><span class="sxs-lookup"><span data-stu-id="7817e-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="7817e-162">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es fest und brechen alle ausstehenden Lese Berichte ab.</span><span class="sxs-lookup"><span data-stu-id="7817e-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="7817e-163">Wenn das CLEAR_READ_FLAG-Flag festgelegt ist, deaktivieren Sie das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** -Eigenschaft jeder Nachricht, und senden Sie keine Lese Berichte.</span><span class="sxs-lookup"><span data-stu-id="7817e-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="7817e-164">Wenn das GENERATE_RECEIPT_ONLY-Flag festgelegt ist, senden Sie ausstehende Lese Berichte.</span><span class="sxs-lookup"><span data-stu-id="7817e-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="7817e-165">MSGFLAG_READ nicht festlegen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="7817e-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="7817e-166">Wenn sowohl die SUPPRESS_RECEIPT-als auch die GENERATE_RECEIPT_ONLY-Flags festgelegt sind, legen Sie **PR_READ_RECEIPT_REQUESTED** auf false fest, wenn es festgelegt ist, und senden Sie keinen Lesebericht.</span><span class="sxs-lookup"><span data-stu-id="7817e-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7817e-167">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7817e-167">Notes to callers</span></span>

<span data-ttu-id="7817e-168">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="7817e-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="7817e-169">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="7817e-169">**Condition**</span></span>|<span data-ttu-id="7817e-170">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="7817e-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7817e-171">**SetReadFlags** hat jede Nachricht erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7817e-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="7817e-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="7817e-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="7817e-173">**SetReadFlags** konnte jede Nachricht nicht erfolgreich verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7817e-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="7817e-174">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7817e-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="7817e-175">**SetReadFlags** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7817e-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="7817e-176">Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7817e-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="7817e-177">Wenn **SetReadFlags** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7817e-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="7817e-178">**SetReadFlags** kann möglicherweise das MSGFLAG_READ-flag für eine oder mehrere der Nachrichten festlegen oder löschen, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="7817e-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7817e-179">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="7817e-179">MFCMAPI reference</span></span>

<span data-ttu-id="7817e-180">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7817e-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7817e-181">**Datei**</span><span class="sxs-lookup"><span data-stu-id="7817e-181">**File**</span></span>|<span data-ttu-id="7817e-182">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="7817e-182">**Function**</span></span>|<span data-ttu-id="7817e-183">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7817e-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7817e-184">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="7817e-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="7817e-185">CFolderDlg:: OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="7817e-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="7817e-186">MFCMAPI verwendet die **IMAPIFolder:: SetReadFlags** -Methode, um den Lesestatus für die angegebenen Nachrichten manuell festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7817e-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7817e-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7817e-187">See also</span></span>

- [<span data-ttu-id="7817e-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="7817e-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="7817e-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="7817e-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="7817e-190">Kanonische PidTagMessageFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7817e-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="7817e-191">Kanonische Pidtagreadreceiptrequested (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7817e-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="7817e-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7817e-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="7817e-193">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="7817e-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="7817e-194">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="7817e-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

