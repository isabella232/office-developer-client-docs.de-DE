---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439870"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="9571c-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="9571c-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="9571c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9571c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9571c-105">Legt das MSGFLAG_READ in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft der Nachricht fest oder entfernt es und verwaltet das Senden von Leseberichten.</span><span class="sxs-lookup"><span data-stu-id="9571c-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9571c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9571c-106">Parameters</span></span>

<span data-ttu-id="9571c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9571c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9571c-108">[in] Bitmaske von Flags, die die Einstellung des Lesekennzeichens einer Nachricht steuert, d. h. das MSGFLAG_READ-Flag der Nachricht in ihrer **PR_MESSAGE_FLAGS-Eigenschaft** und die Verarbeitung von Leseberichten.</span><span class="sxs-lookup"><span data-stu-id="9571c-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="9571c-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9571c-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="9571c-110">CLEAR_READ_FLAG: Das MSGFLAG_READ sollte **in** der PR_MESSAGE_FLAGS und kein Lesebericht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9571c-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="9571c-111">CLEAR_NRN_PENDING: Das MSGFLAG_NRN_PENDING-Flag sollte **in** der PR_MESSAGE_FLAGS und ein nicht gelesener Bericht sollte nicht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9571c-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="9571c-112">CLEAR_RN_PENDING: Das MSGFLAG_RN_PENDING-Flag sollte **in** der PR_MESSAGE_FLAGS und kein Lesebericht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9571c-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="9571c-113">GENERATE_RECEIPT_ONLY: Ein Lesebericht sollte gesendet werden, wenn ein Ausstehend ist, aber es sollte keine Änderung im Status des MSGFLAG_READ werden.</span><span class="sxs-lookup"><span data-stu-id="9571c-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="9571c-114">MAPI_DEFERRED_ERRORS: Ermöglicht die erfolgreiche Rückgabe von **SetReadFlag,** möglicherweise vor Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="9571c-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="9571c-115">SUPPRESS_RECEIPT: Ein ausstehender Lesebericht sollte abgebrochen werden, wenn ein Lesebericht angefordert wurde und dieser Aufruf den Status der Nachricht von ungelesen zu lesen ändert.</span><span class="sxs-lookup"><span data-stu-id="9571c-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="9571c-116">Wenn dieser Aufruf den Status der Nachricht nicht ändert, kann der Nachrichtenspeicheranbieter dieses Kennzeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="9571c-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9571c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9571c-117">Return value</span></span>

<span data-ttu-id="9571c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9571c-118">S_OK</span></span> 
  
> <span data-ttu-id="9571c-119">Das Leseflag der Nachricht wurde erfolgreich festgelegt oder geräumt.</span><span class="sxs-lookup"><span data-stu-id="9571c-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="9571c-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="9571c-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="9571c-121">Der Nachrichtenspeicheranbieter unterstützt die Unterdrückung von Leseberichten nicht.</span><span class="sxs-lookup"><span data-stu-id="9571c-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="9571c-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9571c-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="9571c-123">Eine der folgenden Kombinationen von Flags wird im  _ulFlags-Parameter_ festgelegt:</span><span class="sxs-lookup"><span data-stu-id="9571c-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="9571c-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="9571c-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="9571c-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="9571c-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="9571c-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="9571c-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9571c-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9571c-127">Remarks</span></span>

<span data-ttu-id="9571c-128">Die **IMessage::SetReadFlag-Methode** legt das MSGFLAG_READ-Flag der Nachricht in der **PR_MESSAGE_FLAGS-Eigenschaft** fest oder entfernt sie und ruft [IMAPIProp::SaveChanges](imapiprop-savechanges.md) auf, um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9571c-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="9571c-129">Das Festlegen MSGFLAG_READ markiert eine Nachricht als gelesen, was nicht unbedingt bedeutet, dass der beabsichtigte Empfänger die Nachricht gelesen hat.</span><span class="sxs-lookup"><span data-stu-id="9571c-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="9571c-130">**SetReadFlags** verwaltet auch das Senden von Leseberichten.</span><span class="sxs-lookup"><span data-stu-id="9571c-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="9571c-131">Ein Lesebericht wird nur gesendet, wenn der Absender einen angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="9571c-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="9571c-132">Das Leseflag kann nicht geändert werden für:</span><span class="sxs-lookup"><span data-stu-id="9571c-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="9571c-133">Nachrichten, die nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9571c-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="9571c-134">Nachrichten, die an anderer Stelle verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="9571c-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="9571c-135">Nachrichten, die mit Lese-/Schreibberechtigung geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="9571c-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="9571c-136">Nachrichten, die derzeit übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9571c-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="9571c-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9571c-137">Notes to callers</span></span>

<span data-ttu-id="9571c-138">Wenn keines der Flags im  _ulFlags-Parameter_ festgelegt ist, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="9571c-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="9571c-139">Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.</span><span class="sxs-lookup"><span data-stu-id="9571c-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="9571c-140">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie sie fest, und senden Sie alle ausstehenden Leseberichte, wenn die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) -Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9571c-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="9571c-141">Wenn sowohl die SUPPRESS_RECEIPT als auch GENERATE_RECEIPT_ONLY festgelegt sind, sollte das PR_READ_RECEIPT_REQUESTED-Bit, falls festgelegt, geräumt werden, und es sollte kein Lesebericht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9571c-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="9571c-142">Wenn das SUPPRESS_RECEIPT festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="9571c-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="9571c-143">Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.</span><span class="sxs-lookup"><span data-stu-id="9571c-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="9571c-144">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie sie fest, und brechen Sie alle ausstehenden Leseberichte ab.</span><span class="sxs-lookup"><span data-stu-id="9571c-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="9571c-145">Wenn das CLEAR_READ_FLAG festgelegt ist, löschen Sie das MSGFLAG_READ in der  PR_MESSAGE_FLAGS-Eigenschaft jeder Nachricht, und senden Sie keine Leseberichte.</span><span class="sxs-lookup"><span data-stu-id="9571c-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="9571c-146">Wenn das GENERATE_RECEIPT_ONLY festgelegt ist, senden Sie alle ausstehenden Leseberichte.</span><span class="sxs-lookup"><span data-stu-id="9571c-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="9571c-147">Legen Sie keine MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="9571c-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="9571c-148">Wenn sowohl SUPPRESS_RECEIPT als auch GENERATE_RECEIPT_ONLY festgelegt sind, legen Sie die PR_READ_RECEIPT_REQUESTED-Eigenschaft auf FALSE, wenn sie festgelegt ist, und senden Sie keinen Lesebericht.</span><span class="sxs-lookup"><span data-stu-id="9571c-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="9571c-149">Sie können das Berichtsverhalten optimieren, indem Sie die Generierung von Leseberichten unter bestimmten Bedingungen unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="9571c-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="9571c-150">Wenn Sie jedoch die Unterdrückung von Berichten nicht unterstützen und ein Client **SetReadFlag** mit dem SUPPRESS_RECEIPT aufruft, geben Sie MAPI_E_NO_SUPPRESS.</span><span class="sxs-lookup"><span data-stu-id="9571c-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9571c-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="9571c-151">MFCMAPI reference</span></span>

<span data-ttu-id="9571c-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9571c-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9571c-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="9571c-153">**File**</span></span>|<span data-ttu-id="9571c-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="9571c-154">**Function**</span></span>|<span data-ttu-id="9571c-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="9571c-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9571c-156">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9571c-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="9571c-157">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="9571c-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="9571c-158">MFCMAPI verwendet die **IMessage::SetReadFlag-Methode** zum Festlegen von Lesekennzeichen für ausgewählte Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="9571c-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9571c-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9571c-159">See also</span></span>

- [<span data-ttu-id="9571c-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="9571c-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="9571c-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="9571c-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="9571c-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="9571c-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="9571c-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9571c-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="9571c-164">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9571c-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="9571c-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9571c-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="9571c-166">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="9571c-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

