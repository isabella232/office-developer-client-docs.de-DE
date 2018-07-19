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
ms.openlocfilehash: a52c0501040d77ddb8172b212bf341a08704dcc3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792118"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="c3ab0-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="c3ab0-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="c3ab0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c3ab0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c3ab0-105">Legt fest oder löscht das Flag MSGFLAG_READ in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) von einem oder mehreren der Nachrichten, die den Ordner und das Senden von lesen Berichte verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c3ab0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3ab0-106">Parameters</span></span>

<span data-ttu-id="c3ab0-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="c3ab0-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="c3ab0-108">[in] Ein Zeiger auf ein Array von [ENTRYLIST](entrylist.md) -Strukturen, die identifizieren, die Nachricht oder Nachrichten, die Flags festzulegen oder zu deaktivieren, um gelesen haben.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="c3ab0-109">Wenn _LpMsgList_ auf NULL festgelegt ist, kennzeichnet das Lesen für alle, die Nachrichten aus den Ordnern festgelegt oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="c3ab0-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c3ab0-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="c3ab0-111">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="c3ab0-112">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="c3ab0-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="c3ab0-113">_lpProgress_</span></span>
  
> <span data-ttu-id="c3ab0-114">[in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="c3ab0-115">Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe des MAPI-Implementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="c3ab0-116">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG in _UlFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="c3ab0-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c3ab0-117">_ulFlags_</span></span>
  
> <span data-ttu-id="c3ab0-118">[in] Eine Bitmaske aus Flags, die die Einstellung des Volumens Flags eine Nachricht und die Verarbeitung steuert Lesen von Berichten.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="c3ab0-119">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c3ab0-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="c3ab0-120">CLEAR_READ_FLAG: Das Flag MSGFLAG_READ sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und ein Bericht lesen nicht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="c3ab0-121">CLEAR_NRN_PENDING: Das Flag MSGFLAG_NRN_PENDING sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und ein Bericht ungelesener nicht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="c3ab0-122">CLEAR_RN_PENDING: Das Flag MSGFLAG_RN_PENDING sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und ein Bericht lesen nicht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="c3ab0-123">GENERATE_RECEIPT_ONLY: Lese-Bericht gesendet werden soll, wenn eine steht noch aus, aber keine Änderung im Zustand des MSGFLAG_READ Flags werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="c3ab0-124">MAPI_DEFERRED_ERRORS: Ermöglicht **SetReadFlags** erfolgreich, möglicherweise beendet, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="c3ab0-125">MESSAGE_DIALOG: Eine Statusanzeige angezeigt, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="c3ab0-126">SUPPRESS_RECEIPT: Ein ausstehender lesen Bericht sollte abgebrochen werden, wenn ein Bericht lesen angefordert und dieses Anrufs den Status der Nachricht vom ungelesene zum Lesen von ändert.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="c3ab0-127">Wenn dieses Anrufs nicht den Status der Nachricht ändert, kann der Nachricht Speicheranbieter dieses Flag ignorieren.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c3ab0-128">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c3ab0-128">Return values</span></span>

<span data-ttu-id="c3ab0-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3ab0-129">S_OK</span></span> 
  
> <span data-ttu-id="c3ab0-130">Das Lesen-Flag für die angegebene Nachricht(en) wurde erfolgreich festgelegt oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="c3ab0-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="c3ab0-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="c3ab0-132">Der Nachricht Speicheranbieter unterstützt nicht die Unterdrückung der Lese-Berichte.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="c3ab0-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c3ab0-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c3ab0-134">Eine der folgenden inkompatiblen Kombinationen von Flags wird in der _UlFlags_ -Parameter festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c3ab0-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="c3ab0-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="c3ab0-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="c3ab0-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="c3ab0-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="c3ab0-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="c3ab0-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="c3ab0-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="c3ab0-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="c3ab0-139">Der Aufruf war erfolgreich, jedoch nicht alle Nachrichten erfolgreich verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="c3ab0-140">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c3ab0-141">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c3ab0-142">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="c3ab0-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3ab0-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3ab0-143">Remarks</span></span>

<span data-ttu-id="c3ab0-144">Die **IMAPIFolder::SetReadFlags** -Methode aktiviert oder deaktiviert das Flag MSGFLAG_READ in der **PR_MESSAGE_FLAGS** -Eigenschaft von einem oder mehreren der Nachrichten, die den Ordner.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="c3ab0-145">Markiert die Nachricht als gelesen, die nicht unbedingt darauf hinweist, dass der Empfänger die Nachricht tatsächlich gelesen hat das MSGFLAG_READ-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="c3ab0-146">**SetReadFlags** verwaltet auch das Senden von Berichten lesen.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="c3ab0-147">Das Flag lesen kann nicht für die folgenden geändert werden:</span><span class="sxs-lookup"><span data-stu-id="c3ab0-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="c3ab0-148">Nachrichten, die nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="c3ab0-149">Nachrichten, die wurden verschoben eingehen.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="c3ab0-150">Nachrichten, die mit Lese-/Schreibzugriff geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="c3ab0-151">Nachrichten, die derzeit übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c3ab0-152">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c3ab0-152">Notes to implementers</span></span>

<span data-ttu-id="c3ab0-153">Sie können nicht für das Senden von Lese-Berichten und die Anforderung an die schreibgeschützte Reports unterdrücken unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="c3ab0-154">Zum Vermeiden von unterdrücken lesen-Bericht zurückgeben Sie MAPI_E_NO_SUPPRESS **SetReadFlags** mit SUPPRESS_RECEIPT festlegen in der _UlFlags_ -Parameter aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="c3ab0-155">Wenn der Parameter _LpMsgList_ auf mehr als eine Nachricht zeigt, führen Sie den Vorgang für jede Nachricht möglichst vollständig.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="c3ab0-156">Beenden Sie den Vorgang nicht vorzeitig auf, es sei denn, ein Fehler, die außerhalb Ihrer Kontrolle auftritt, wie nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder der Beschädigung im Nachrichtenspeicher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="c3ab0-157">Wenn keiner der Werte in der _UlFlags_ -Parameter festgelegt ist, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="c3ab0-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="c3ab0-158">Wenn MSGFLAG_READ bereits festgelegt ist, wird keine Aktion durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="c3ab0-159">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es sofort und senden Sie alle ausstehenden lesen Berichte, wenn die Eigenschaft **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="c3ab0-160">Wenn das Flag SUPPRESS_RECEIPT festgelegt ist, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="c3ab0-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="c3ab0-161">Wenn MSGFLAG_READ bereits festgelegt ist, wird keine Aktion durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="c3ab0-162">Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es und Abbrechen an alle ausstehenden lesen Berichte.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="c3ab0-163">Wenn das Flag CLEAR_READ_FLAG festgelegt ist, deaktivieren Sie die Kennzeichen MSGFLAG_READ in jede Nachricht **PR_MESSAGE_FLAGS** -Eigenschaft und senden Sie keine lesen Berichte.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="c3ab0-164">Wenn das Flag GENERATE_RECEIPT_ONLY festgelegt ist, senden Sie alle ausstehenden Lese-Berichte.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="c3ab0-165">Führen Sie MSGFLAG_READ nicht festgelegt oder löschen.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="c3ab0-166">Wenn die SUPPRESS_RECEIPT und die GENERATE_RECEIPT_ONLY Flags festgelegt werden, **PR_READ_RECEIPT_REQUESTED** auf FALSE festgelegt, wenn sie festgelegt ist, und senden Sie einen read Bericht nicht.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c3ab0-167">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c3ab0-167">Notes to callers</span></span>

<span data-ttu-id="c3ab0-168">Diese Rückgabewerte unter folgenden Umständen zu erwarten.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="c3ab0-169">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="c3ab0-169">**Condition**</span></span>|<span data-ttu-id="c3ab0-170">**Rückgabewert**</span><span class="sxs-lookup"><span data-stu-id="c3ab0-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c3ab0-171">**SetReadFlags** hat jede Nachricht erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="c3ab0-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3ab0-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="c3ab0-173">**SetReadFlags** konnte nicht erfolgreich jede Nachricht zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="c3ab0-174">MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c3ab0-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="c3ab0-175">**SetReadFlags** konnte nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="c3ab0-176">Einen Fehlerwert außer MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c3ab0-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="c3ab0-177">Wenn **SetReadFlags** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="c3ab0-178">**SetReadFlags** wurden möglicherweise Lage festzulegen oder das Flag MSGFLAG_READ für eine oder mehrere Nachrichten zu löschen, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c3ab0-179">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="c3ab0-179">MFCMAPI reference</span></span>

<span data-ttu-id="c3ab0-180">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c3ab0-181">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c3ab0-181">**File**</span></span>|<span data-ttu-id="c3ab0-182">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c3ab0-182">**Function**</span></span>|<span data-ttu-id="c3ab0-183">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c3ab0-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c3ab0-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c3ab0-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="c3ab0-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="c3ab0-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="c3ab0-186">MFCMAPI (engl.) verwendet die **IMAPIFolder::SetReadFlags** -Methode, manuell gelesen-Status für die angegebenen Nachrichten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c3ab0-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3ab0-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3ab0-187">See also</span></span>

- [<span data-ttu-id="c3ab0-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="c3ab0-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="c3ab0-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="c3ab0-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="c3ab0-190">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c3ab0-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="c3ab0-191">PidTagReadReceiptRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c3ab0-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="c3ab0-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c3ab0-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="c3ab0-193">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c3ab0-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="c3ab0-194">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="c3ab0-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

