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
ms.openlocfilehash: 0ae35166f01f597c2c3ab399a1b66e5760ab0dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792519"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="c1800-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="c1800-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="c1800-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1800-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1800-105">Festgelegt oder löscht das Flag MSGFLAG_READ in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht und das Senden von lesen Berichte verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c1800-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c1800-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1800-106">Parameters</span></span>

<span data-ttu-id="c1800-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1800-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c1800-108">[in] Bitmaske aus Flags, die die Einstellung der eine Nachricht lesen steuert kennzeichnen d. h., die Nachricht MSGFLAG_READ Flag in seiner **PR_MESSAGE_FLAGS** -Eigenschaft und die Verarbeitung von Berichten lesen.</span><span class="sxs-lookup"><span data-stu-id="c1800-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="c1800-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c1800-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="c1800-110">CLEAR_READ_FLAG: Das Flag MSGFLAG_READ sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und kein Lese Bericht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1800-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="c1800-111">CLEAR_NRN_PENDING: Das Flag MSGFLAG_NRN_PENDING sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und ein Bericht nicht gelesen nicht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1800-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="c1800-112">CLEAR_RN_PENDING: Das Flag MSGFLAG_RN_PENDING sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und kein Lese Bericht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1800-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="c1800-113">GENERATE_RECEIPT_ONLY: Lese-Bericht gesendet werden soll, wenn eine steht noch aus, aber keine Änderung im Zustand des MSGFLAG_READ Flags werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1800-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="c1800-114">MAPI_DEFERRED_ERRORS: Ermöglicht **SetReadFlag** erfolgreich, möglicherweise beendet, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c1800-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="c1800-115">SUPPRESS_RECEIPT: Ein ausstehender lesen Bericht sollte abgebrochen werden, wenn ein Bericht lesen angefordert und dieses Anrufs den Status der Nachricht vom ungelesene zum Lesen von ändert.</span><span class="sxs-lookup"><span data-stu-id="c1800-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="c1800-116">Wenn dieses Anrufs nicht den Status der Nachricht ändert, kann der Nachricht Speicheranbieter dieses Flag ignorieren.</span><span class="sxs-lookup"><span data-stu-id="c1800-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1800-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c1800-117">Return value</span></span>

<span data-ttu-id="c1800-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1800-118">S_OK</span></span> 
  
> <span data-ttu-id="c1800-119">Lesen Nachrichtenkennzeichnung wurde erfolgreich festgelegt oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c1800-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="c1800-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="c1800-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="c1800-121">Der Nachricht Speicheranbieter unterstützt nicht die Unterdrückung der Lese-Berichte.</span><span class="sxs-lookup"><span data-stu-id="c1800-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="c1800-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c1800-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c1800-123">Eine der folgenden Kombinationen von Flags wird in der _UlFlags_ -Parameter festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c1800-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="c1800-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="c1800-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="c1800-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="c1800-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="c1800-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="c1800-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1800-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1800-127">Remarks</span></span>

<span data-ttu-id="c1800-128">Die **IMessage::SetReadFlag** -Methode legt oder löscht die Nachricht MSGFLAG_READ Flag in der **PR_MESSAGE_FLAGS** -Eigenschaft und ruft [IMAPIProp::SaveChanges](imapiprop-savechanges.md) die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c1800-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="c1800-129">Festlegen des MSGFLAG_READ-Flags markiert eine Nachricht als gelesen, die nicht unbedingt darauf hinweist, dass der Empfänger die Nachricht tatsächlich gelesen hat.</span><span class="sxs-lookup"><span data-stu-id="c1800-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="c1800-130">**SetReadFlags** verwaltet auch das Senden von Berichten lesen.</span><span class="sxs-lookup"><span data-stu-id="c1800-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="c1800-131">Ein Bericht gelesen wird gesendet, nur, wenn der Absender eine angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="c1800-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="c1800-132">Das Flag lesen können für nicht geändert werden:</span><span class="sxs-lookup"><span data-stu-id="c1800-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="c1800-133">Nachrichten, die nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c1800-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="c1800-134">Nachrichten, die wurden verschoben eingehen.</span><span class="sxs-lookup"><span data-stu-id="c1800-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="c1800-135">Nachrichten, die mit Lese-/Schreibzugriff geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="c1800-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="c1800-136">Nachrichten, die derzeit übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="c1800-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="c1800-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c1800-137">Notes to callers</span></span>

<span data-ttu-id="c1800-138">Wenn keiner der Werte in der _UlFlags_ -Parameter festgelegt ist, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="c1800-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="c1800-139">Wenn MSGFLAG_READ bereits festgelegt ist, wird keine Aktion durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1800-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="c1800-140">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es, und senden Sie alle ausstehenden lesen Berichte, wenn die Eigenschaft **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c1800-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="c1800-141">Wenn die SUPPRESS_RECEIPT und die GENERATE_RECEIPT_ONLY Flags festgelegt sind, die PR_READ_RECEIPT_REQUESTED bit, wenn festgelegt, gelöscht werden sollen und ein Bericht lesen nicht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1800-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="c1800-142">Wenn das Flag SUPPRESS_RECEIPT festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="c1800-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="c1800-143">Wenn MSGFLAG_READ bereits festgelegt ist, wird keine Aktion durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1800-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="c1800-144">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es und Abbrechen an alle ausstehenden lesen Berichte.</span><span class="sxs-lookup"><span data-stu-id="c1800-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="c1800-145">Wenn das Flag CLEAR_READ_FLAG festgelegt ist, deaktivieren Sie die Kennzeichen MSGFLAG_READ in jede Nachricht **PR_MESSAGE_FLAGS** -Eigenschaft und senden Sie keine lesen Berichte.</span><span class="sxs-lookup"><span data-stu-id="c1800-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="c1800-146">Wenn das Flag GENERATE_RECEIPT_ONLY festgelegt ist, senden Sie alle ausstehenden Lese-Berichte.</span><span class="sxs-lookup"><span data-stu-id="c1800-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="c1800-147">Führen Sie MSGFLAG_READ nicht festgelegt oder löschen.</span><span class="sxs-lookup"><span data-stu-id="c1800-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="c1800-148">Wenn die SUPPRESS_RECEIPT und die GENERATE_RECEIPT_ONLY Flags festgelegt werden, die PR_READ_RECEIPT_REQUESTED-Eigenschaft auf FALSE festgelegt, wenn sie festgelegt ist, und senden Sie einen read Bericht nicht.</span><span class="sxs-lookup"><span data-stu-id="c1800-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="c1800-149">Sie können Bericht Verhalten optimieren, indem Sie die Generierung von lesen Berichte unter bestimmten Umständen unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="c1800-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="c1800-150">Jedoch, wenn Sie die Unterdrückung von Berichten nicht unterstützt und **SetReadFlag** von einem Client mit dem Flag SUPPRESS_RECEIPT aufgerufen, MAPI_E_NO_SUPPRESS zurück.</span><span class="sxs-lookup"><span data-stu-id="c1800-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c1800-151">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="c1800-151">MFCMAPI reference</span></span>

<span data-ttu-id="c1800-152">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c1800-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c1800-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c1800-153">**File**</span></span>|<span data-ttu-id="c1800-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c1800-154">**Function**</span></span>|<span data-ttu-id="c1800-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c1800-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1800-156">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c1800-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="c1800-157">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="c1800-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="c1800-158">MFCMAPI (engl.) verwendet die **IMessage::SetReadFlag** -Methode, lesen Flags für ausgewählte Nachrichten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c1800-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1800-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1800-159">See also</span></span>

- [<span data-ttu-id="c1800-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c1800-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="c1800-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="c1800-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="c1800-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c1800-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="c1800-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c1800-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="c1800-164">Kanonische PidTagMessageFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c1800-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="c1800-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c1800-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="c1800-166">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c1800-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

