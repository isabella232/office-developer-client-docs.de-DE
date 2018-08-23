---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e253aa6a701d565fbc61e8a0e0a6388f7199c000
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593263"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="982f5-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="982f5-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="982f5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="982f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="982f5-105">Kopiert oder verschiebt eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="982f5-105">Copies or moves one or more messages.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="982f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="982f5-106">Parameters</span></span>

 <span data-ttu-id="982f5-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="982f5-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="982f5-108">[in] Ein Zeiger auf ein Array von [ENTRYLIST](entrylist.md) -Strukturen, die identifizieren, zu kopieren oder Verschieben von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="982f5-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="982f5-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="982f5-109">_lpInterface_</span></span>
  
> <span data-ttu-id="982f5-110">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, um Zugriff auf den Zielordner darstellt, auf den durch den Parameter _LpDestFolder_ verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="982f5-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="982f5-111">Bei Übergabe von NULL führt den Dienstanbieter Zurückgeben der Schnittstelle Standardordner [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="982f5-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="982f5-112">Clients müssen NULL übergeben.</span><span class="sxs-lookup"><span data-stu-id="982f5-112">Clients must pass NULL.</span></span> <span data-ttu-id="982f5-113">Andere Aufrufer können den Parameter _LpInterface_ auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="982f5-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="982f5-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="982f5-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="982f5-115">[in] Ein Zeiger auf den Ordner öffnen, um die kopierte oder verschobenen Nachrichten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="982f5-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="982f5-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="982f5-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="982f5-117">[in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an.</span><span class="sxs-lookup"><span data-stu-id="982f5-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="982f5-118">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, der Client das Flag MESSAGE_DIALOG in der _UlFlags_ -Parameter wird und übergibt NULL im _LpProgress_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="982f5-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="982f5-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="982f5-119">_lpProgress_</span></span>
  
> <span data-ttu-id="982f5-120">[in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="982f5-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="982f5-121">Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="982f5-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="982f5-122">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG in _UlFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="982f5-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="982f5-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="982f5-123">_ulFlags_</span></span>
  
> <span data-ttu-id="982f5-124">[in] Eine Bitmaske aus Flags, die steuert, wie der kopieren oder verschieben-Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="982f5-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="982f5-125">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="982f5-125">The following flags can be set:</span></span>
    
<span data-ttu-id="982f5-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="982f5-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="982f5-127">Informiert den Nachricht-Speicher-Anbieter, um sofort MAPI_E_DECLINE_COPY zurückzugeben, wenn er **IMAPIFolder::CopyMessages** implementiert, durch die des Unterstützungsobjekts [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) oder [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="982f5-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="982f5-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="982f5-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="982f5-129">Eine Statusanzeige wird angezeigt, wie der-Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="982f5-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="982f5-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="982f5-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="982f5-131">Nachrichten werden anstelle von verschoben werden kopiert.</span><span class="sxs-lookup"><span data-stu-id="982f5-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="982f5-132">Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.</span><span class="sxs-lookup"><span data-stu-id="982f5-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="982f5-133">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="982f5-133">Return value</span></span>

<span data-ttu-id="982f5-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="982f5-134">S_OK</span></span> 
  
> <span data-ttu-id="982f5-135">Die Nachricht oder die Nachrichten wurden erfolgreich verschoben oder kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="982f5-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="982f5-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="982f5-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="982f5-137">Der Anbieter implementiert diese Methode durch den Aufruf einer Support, und der Aufrufer das Flag MAPI_DECLINE_OK verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="982f5-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="982f5-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="982f5-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="982f5-139">Der Aufruf war erfolgreich, aber nicht alle Einträge erfolgreich kopiert oder verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="982f5-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="982f5-140">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="982f5-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="982f5-141">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="982f5-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="982f5-142">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="982f5-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="982f5-143">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="982f5-143">Remarks</span></span>

<span data-ttu-id="982f5-144">Die **IMAPIFolder::CopyMessages** -Methode kopiert oder verschiebt Nachrichten in einen anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="982f5-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="982f5-145">Nachrichten, die mit Lese-/Schreibzugriff Berechtigung verschoben oder kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="982f5-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="982f5-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="982f5-146">Notes to implementers</span></span>

<span data-ttu-id="982f5-147">Wenn Sie Nachrichten an einen anderen Nachrichtenspeicher ohne Verwendung der Methode [IMAPISupport::CopyMessages](imapisupport-copymessages.md) kopieren möchten, müssen Sie zunächst [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) mit dem GENERATE_RECEIPT_ONLY-Flag aufrufen.</span><span class="sxs-lookup"><span data-stu-id="982f5-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="982f5-148">Der empfangenden Nachrichtenspeicher ist nicht verantwortlich für die kopierte oder verschobenen Nachrichten lesen Berichte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="982f5-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="982f5-149">Wenn Sie **IMAPISupport::CopyMessages** zum Implementieren der **IMAPIFolder::CopyMessages**aufrufen, rufen Sie **SetReadFlags**nicht. MAPI wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="982f5-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="982f5-150">Die Implementierung kann verschieben oder Kopieren von Nachrichten in beliebiger Reihenfolge und Lesen Statusberichte in beliebiger Reihenfolge zu generieren.</span><span class="sxs-lookup"><span data-stu-id="982f5-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="982f5-151">D. h., können Sie das Kopieren von Nachrichten vor dem Generieren eines Berichts gelesen-Status abgeschlossen oder die Berichte senden, bevor die Implementierung den Kopiervorgang beginnt.</span><span class="sxs-lookup"><span data-stu-id="982f5-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="982f5-152">Lesen Sie jedoch für alle Nachrichten kopiert werden sollen, unabhängig davon, ob der Kopiervorgang erfolgreich war, Berichte gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="982f5-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="982f5-153">Wenn der Vorgang kopieren oder Verschieben von mehr als eine Nachricht beteiligt sind, führen Sie den Vorgang vollständig wie möglich.</span><span class="sxs-lookup"><span data-stu-id="982f5-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="982f5-154">Beenden Sie den Vorgang nicht vorzeitig auf, es sei denn, ein Fehler, die außerhalb Ihrer Kontrolle auftritt, wie nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder der Beschädigung im Nachrichtenspeicher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="982f5-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="982f5-155">Versuchen Sie, Eintragsbezeichner Verschiebe-oder Kopie zu wahren.</span><span class="sxs-lookup"><span data-stu-id="982f5-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="982f5-156">Sie sollten auch Eintragsbezeichner, beibehalten, obwohl es nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="982f5-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="982f5-157">Senden Sie Benachrichtigung, wenn Sie verschieben oder Kopieren von Nachrichten, damit Clients passieren werden, dass ihre Anrufe an die Nachrichten [IMAPIProp::SaveChanges](imapiprop-savechanges.md) Methoden fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="982f5-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="982f5-158">Schließen Sie eine Nachricht den Status in die Kopie oder Verschiebevorgang nicht.</span><span class="sxs-lookup"><span data-stu-id="982f5-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="982f5-159">Verschieben oder Kopieren eines Nachrichtenstatus erheblich wirkt sich auf Leistung.</span><span class="sxs-lookup"><span data-stu-id="982f5-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="982f5-160">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="982f5-160">Notes to callers</span></span>

<span data-ttu-id="982f5-161">Verwenden Sie **IMAPIFolder::CopyMessages** , um Suchergebnisse Ordner, aufzufüllen, in dem Nachrichten häufig übergeordneten Ordner gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="982f5-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="982f5-162">Diese Rückgabewerte unter folgenden Umständen zu erwarten.</span><span class="sxs-lookup"><span data-stu-id="982f5-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="982f5-163">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="982f5-163">**Condition**</span></span>|<span data-ttu-id="982f5-164">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="982f5-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="982f5-165">**IMAPIFolder::CopyMessages** wurde erfolgreich kopiert oder jeder Nachricht verschoben.</span><span class="sxs-lookup"><span data-stu-id="982f5-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="982f5-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="982f5-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="982f5-167">**IMAPIFolder::CopyMessages** konnte nicht erfolgreich kopieren oder verschieben Sie jede Nachricht.</span><span class="sxs-lookup"><span data-stu-id="982f5-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="982f5-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="982f5-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="982f5-169">**IMAPIFolder::CopyMessages** konnte nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="982f5-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="982f5-170">Einen anderen Fehlerwert als</span><span class="sxs-lookup"><span data-stu-id="982f5-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="982f5-171">Wenn **IMAPIFolder::CopyMessages** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="982f5-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="982f5-172">**IMAPIFolder::CopyMessages** wurden möglicherweise kopieren oder verschieben Sie eine oder mehrere Nachrichten vor den Fehler auftreten können.</span><span class="sxs-lookup"><span data-stu-id="982f5-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="982f5-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="982f5-173">See also</span></span>



[<span data-ttu-id="982f5-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="982f5-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

