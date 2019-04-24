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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349266"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="dfc88-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="dfc88-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="dfc88-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfc88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfc88-105">Das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht wird festgelegt oder gelöscht, und das Senden von Lese Berichten wird verwaltet.</span><span class="sxs-lookup"><span data-stu-id="dfc88-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="dfc88-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfc88-106">Parameters</span></span>

<span data-ttu-id="dfc88-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dfc88-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dfc88-108">in Bitmaske von Flags, die die Einstellung des Lese Kennzeichens einer Nachricht steuert, das MSGFLAG_READ-flag der Nachricht in der **PR_MESSAGE_FLAGS** -Eigenschaft und die Verarbeitung von Lese Berichten.</span><span class="sxs-lookup"><span data-stu-id="dfc88-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="dfc88-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="dfc88-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="dfc88-110">CLEAR_READ_FLAG: das MSGFLAG_READ-flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und es sollte kein Lesebericht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfc88-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="dfc88-111">CLEAR_NRN_PENDING: das MSGFLAG_NRN_PENDING-Flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und ein nicht gelesener Bericht sollte nicht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfc88-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="dfc88-112">CLEAR_RN_PENDING: das MSGFLAG_RN_PENDING-Flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und es sollte kein Lesebericht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfc88-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="dfc88-113">GENERATE_RECEIPT_ONLY: ein Lesebericht sollte gesendet werden, wenn ein ausstehender ist, aber es sollte keine Änderung des Status des MSGFLAG_READ-Flags geben.</span><span class="sxs-lookup"><span data-stu-id="dfc88-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="dfc88-114">MAPI_DEFERRED_ERRORS: ermöglicht es **SetReadFlag** , erfolgreich zurückzugeben, möglicherweise bevor der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="dfc88-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="dfc88-115">SUPPRESS_RECEIPT: ein ausstehender Lesebericht sollte abgebrochen werden, wenn ein Lesebericht angefordert wurde und dieser Aufruf den Status der Nachricht von ungelesen in lesen ändert.</span><span class="sxs-lookup"><span data-stu-id="dfc88-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="dfc88-116">Wenn durch diesen Anruf der Status der Nachricht nicht geändert wird, kann der Nachrichtenspeicher Anbieter dieses Flag ignorieren.</span><span class="sxs-lookup"><span data-stu-id="dfc88-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dfc88-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfc88-117">Return value</span></span>

<span data-ttu-id="dfc88-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfc88-118">S_OK</span></span> 
  
> <span data-ttu-id="dfc88-119">Die Read-Kennzeichnung der Nachricht wurde erfolgreich festgelegt oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dfc88-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="dfc88-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="dfc88-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="dfc88-121">Der Nachrichtenspeicher Anbieter unterstützt die Unterdrückung von Lese Berichten nicht.</span><span class="sxs-lookup"><span data-stu-id="dfc88-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="dfc88-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dfc88-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="dfc88-123">Eine der folgenden Kombinationen von Flags wird im Parameter _ulFlags_ festgelegt:</span><span class="sxs-lookup"><span data-stu-id="dfc88-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="dfc88-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="dfc88-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="dfc88-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="dfc88-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="dfc88-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="dfc88-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dfc88-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfc88-127">Remarks</span></span>

<span data-ttu-id="dfc88-128">Mit der **IMessage:: SetReadFlag** -Methode wird das MSGFLAG_READ-flag der Nachricht in der **PR_MESSAGE_FLAGS** -Eigenschaft festgelegt oder gelöscht, und [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) wird aufgerufen, um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="dfc88-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="dfc88-129">Durch Festlegen des MSGFLAG_READ-Flags wird eine Nachricht als gelesen markiert, was nicht unbedingt darauf hinweist, dass der vorgesehene Empfänger die Nachricht tatsächlich gelesen hat.</span><span class="sxs-lookup"><span data-stu-id="dfc88-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="dfc88-130">**SetReadFlags** verwaltet auch das Senden von Lese Berichten.</span><span class="sxs-lookup"><span data-stu-id="dfc88-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="dfc88-131">Ein Lesebericht wird nur gesendet, wenn der Absender einen angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="dfc88-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="dfc88-132">Die Read-Kennzeichnung kann nicht geändert werden für:</span><span class="sxs-lookup"><span data-stu-id="dfc88-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="dfc88-133">Nachrichten, die nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dfc88-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="dfc88-134">Nachrichten, die an anderer Stelle verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="dfc88-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="dfc88-135">Mit Lese-/Schreibzugriff geöffnete Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="dfc88-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="dfc88-136">Nachrichten, die derzeit übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="dfc88-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="dfc88-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="dfc88-137">Notes to callers</span></span>

<span data-ttu-id="dfc88-138">Wenn keines der Flags im Parameter _ulFlags_ festgelegt wird, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="dfc88-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="dfc88-139">Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.</span><span class="sxs-lookup"><span data-stu-id="dfc88-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="dfc88-140">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es fest, und senden Sie ausstehende Lese Berichte, wenn die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dfc88-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="dfc88-141">Wenn sowohl die SUPPRESS_RECEIPT-als auch die GENERATE_RECEIPT_ONLY-Flags festgelegt sind, sollte das PR_READ_RECEIPT_REQUESTED-Bit, falls festgelegt, gelöscht werden, und ein Lesebericht sollte nicht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfc88-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="dfc88-142">Wenn das SUPPRESS_RECEIPT-Flag festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="dfc88-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="dfc88-143">Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.</span><span class="sxs-lookup"><span data-stu-id="dfc88-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="dfc88-144">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es fest und brechen alle ausstehenden Lese Berichte ab.</span><span class="sxs-lookup"><span data-stu-id="dfc88-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="dfc88-145">Wenn das CLEAR_READ_FLAG-Flag festgelegt ist, deaktivieren Sie das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** -Eigenschaft jeder Nachricht, und senden Sie keine Lese Berichte.</span><span class="sxs-lookup"><span data-stu-id="dfc88-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="dfc88-146">Wenn das GENERATE_RECEIPT_ONLY-Flag festgelegt ist, senden Sie ausstehende Lese Berichte.</span><span class="sxs-lookup"><span data-stu-id="dfc88-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="dfc88-147">MSGFLAG_READ nicht festlegen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="dfc88-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="dfc88-148">Wenn sowohl die SUPPRESS_RECEIPT-als auch die GENERATE_RECEIPT_ONLY-Flags festgelegt sind, legen Sie die PR_READ_RECEIPT_REQUESTED-Eigenschaft auf FALSE fest, wenn Sie festgelegt ist, und senden Sie keinen Lesebericht.</span><span class="sxs-lookup"><span data-stu-id="dfc88-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="dfc88-149">Sie können das Verhalten des Berichts optimieren, indem Sie die Generierung von Lese Berichten unter bestimmten Bedingungen verhindern.</span><span class="sxs-lookup"><span data-stu-id="dfc88-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="dfc88-150">Wenn Sie jedoch die Unterdrückung von Berichten nicht unterstützen und ein Client **SetReadFlag** mit der SUPPRESS_RECEIPT-flaggruppe aufruft, geben Sie MAPI_E_NO_SUPPRESS zurück.</span><span class="sxs-lookup"><span data-stu-id="dfc88-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dfc88-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="dfc88-151">MFCMAPI reference</span></span>

<span data-ttu-id="dfc88-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dfc88-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dfc88-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="dfc88-153">**File**</span></span>|<span data-ttu-id="dfc88-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="dfc88-154">**Function**</span></span>|<span data-ttu-id="dfc88-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="dfc88-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dfc88-156">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="dfc88-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="dfc88-157">CFolderDlg:: OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="dfc88-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="dfc88-158">MFCMAPI verwendet die **IMessage:: SetReadFlag** -Methode, um Lese Kennzeichen für ausgewählte Nachrichten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="dfc88-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dfc88-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfc88-159">See also</span></span>

- [<span data-ttu-id="dfc88-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="dfc88-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="dfc88-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="dfc88-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="dfc88-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="dfc88-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="dfc88-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="dfc88-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="dfc88-164">Kanonische PidTagMessageFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dfc88-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="dfc88-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dfc88-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="dfc88-166">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="dfc88-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

