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
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424455"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="90116-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="90116-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="90116-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90116-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90116-105">Kopiert oder verschiebt eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="90116-105">Copies or moves one or more messages.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="90116-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="90116-106">Parameters</span></span>

 <span data-ttu-id="90116-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="90116-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="90116-108">[in] Ein Zeiger auf ein Array von [ENTRYLIST-Strukturen,](entrylist.md) die die zu kopierende oder verschiebende Nachricht oder Nachrichten identifizieren.</span><span class="sxs-lookup"><span data-stu-id="90116-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="90116-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="90116-109">_lpInterface_</span></span>
  
> <span data-ttu-id="90116-110">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Zielordner verwendet werden soll, auf den der  _lpDestFolder-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="90116-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="90116-111">Das Übergeben von NULL führt dazu, dass der Dienstanbieter die Standardordnerschnittstelle [IMAPIFolder : IMAPIContainer zurück gibt.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="90116-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="90116-112">Clients müssen NULL übergeben.</span><span class="sxs-lookup"><span data-stu-id="90116-112">Clients must pass NULL.</span></span> <span data-ttu-id="90116-113">Andere Aufrufer können den  _lpInterface-Parameter_ auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="90116-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="90116-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="90116-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="90116-115">[in] Ein Zeiger auf den geöffneten Ordner, um die kopierten oder verschobenen Nachrichten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="90116-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="90116-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="90116-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="90116-117">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="90116-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="90116-118">Der _ulUIParam-Parameter_ wird ignoriert, es sei denn, der Client legt das MESSAGE_DIALOG im _ulFlags-Parameter_ fest und übergibt NULL im _lpProgress-Parameter._</span><span class="sxs-lookup"><span data-stu-id="90116-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="90116-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="90116-119">_lpProgress_</span></span>
  
> <span data-ttu-id="90116-120">[in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="90116-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="90116-121">Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="90116-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="90116-122">Der _lpProgress-Parameter_ wird ignoriert, es sei denn, MESSAGE_DIALOG in _ulFlags festgelegt ist._</span><span class="sxs-lookup"><span data-stu-id="90116-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="90116-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="90116-123">_ulFlags_</span></span>
  
> <span data-ttu-id="90116-124">[in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebevorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90116-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="90116-125">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="90116-125">The following flags can be set:</span></span>
    
<span data-ttu-id="90116-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="90116-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="90116-127">Informiert den Nachrichtenspeicheranbieter, MAPI_E_DECLINE_COPY sofort zurückzukehren, wenn **er IMAPIFolder::CopyMessages** implementiert, indem die [IMAPISupport::D oCopyTo-](imapisupport-docopyto.md) oder [IMAPISupport::D oCopyProps-Methode](imapisupport-docopyprops.md) des Supportobjekts aufruft.</span><span class="sxs-lookup"><span data-stu-id="90116-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="90116-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="90116-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="90116-129">Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="90116-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="90116-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="90116-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="90116-131">Die Nachricht oder Nachrichten sollen verschoben werden, anstatt sie zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="90116-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="90116-132">Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.</span><span class="sxs-lookup"><span data-stu-id="90116-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90116-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90116-133">Return value</span></span>

<span data-ttu-id="90116-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="90116-134">S_OK</span></span> 
  
> <span data-ttu-id="90116-135">Die Nachricht oder Nachrichten wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="90116-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="90116-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="90116-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="90116-137">Der Anbieter implementiert diese Methode durch Aufrufen einer Supportobjektmethode, und der Aufrufer hat das MAPI_DECLINE_OK übergeben.</span><span class="sxs-lookup"><span data-stu-id="90116-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="90116-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="90116-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="90116-139">Der Aufruf ist erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="90116-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="90116-140">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="90116-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="90116-141">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="90116-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="90116-142">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="90116-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90116-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="90116-143">Remarks</span></span>

<span data-ttu-id="90116-144">Die **IMAPIFolder::CopyMessages-Methode** kopiert oder verschiebt Nachrichten in einen anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="90116-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="90116-145">Nachrichten, die mit Lese-/Schreibberechtigung geöffnet werden, können verschoben oder kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="90116-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="90116-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="90116-146">Notes to implementers</span></span>

<span data-ttu-id="90116-147">Wenn Sie Nachrichten in einen anderen Nachrichtenspeicher kopieren, ohne die [IMAPISupport::CopyMessages-Methode](imapisupport-copymessages.md) zu verwenden, müssen Sie zunächst [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) mit dem GENERATE_RECEIPT_ONLY aufrufen.</span><span class="sxs-lookup"><span data-stu-id="90116-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="90116-148">Der empfangende Nachrichtenspeicher ist nicht für das Generieren von Leseberichten für die kopierten oder verschobenen Nachrichten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="90116-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="90116-149">Wenn Sie **IMAPISupport::CopyMessages** aufrufen, um **IMAPIFolder::CopyMessages** zu implementieren, rufen Sie **SetReadFlags** nicht auf. MAPI wird es aufrufen.</span><span class="sxs-lookup"><span data-stu-id="90116-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="90116-150">Ihre Implementierung kann die Nachrichten in beliebiger Reihenfolge verschieben oder kopieren und Lesestatusberichte in beliebiger Reihenfolge generieren.</span><span class="sxs-lookup"><span data-stu-id="90116-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="90116-151">Das heißt, Sie können das Kopieren von Nachrichten beenden, bevor Sie einen der Lesestatusberichte generieren oder die Berichte senden, bevor Die Implementierung den Kopiervorgang startet.</span><span class="sxs-lookup"><span data-stu-id="90116-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="90116-152">Leseberichte sollten jedoch gesendet werden, damit alle Nachrichten kopiert werden, unabhängig davon, ob die Kopie erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="90116-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="90116-153">Wenn der Kopier- oder Verschiebevorgang mehrere Nachrichten umfasst, führen Sie den Vorgang so vollständig wie möglich aus.</span><span class="sxs-lookup"><span data-stu-id="90116-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="90116-154">Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der sich außerhalb Ihres Steuerelements befindet, z. B. nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="90116-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="90116-155">Versuchen Sie, Eintragsbezeichner für alle Verschieben- oder Kopiervorgänge zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="90116-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="90116-156">Sie sollten auch Eintragsbezeichner beibehalten, obwohl sie nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="90116-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="90116-157">Senden Sie Benachrichtigungen, wenn Sie Nachrichten verschieben oder kopieren, damit Clients darauf warnt werden, dass ihre Aufrufe der [IMAPIProp::SaveChanges-Methoden](imapiprop-savechanges.md) der Nachrichten fehlschlagen können.</span><span class="sxs-lookup"><span data-stu-id="90116-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="90116-158">Schließen Sie den Status einer Nachricht nicht in den Kopier- oder Verschiebevorgang ein.</span><span class="sxs-lookup"><span data-stu-id="90116-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="90116-159">Das Verschieben oder Kopieren eines Nachrichtenstatus wirkt sich stark auf die Leistung aus.</span><span class="sxs-lookup"><span data-stu-id="90116-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="90116-160">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="90116-160">Notes to callers</span></span>

<span data-ttu-id="90116-161">Verwenden **Sie IMAPIFolder::CopyMessages** zum Auffüllen von Suchergebnissenordnern, in denen Nachrichten häufig nach übergeordneten Ordnern gruppieren.</span><span class="sxs-lookup"><span data-stu-id="90116-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="90116-162">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="90116-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="90116-163">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="90116-163">**Condition**</span></span>|<span data-ttu-id="90116-164">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="90116-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90116-165">**IMAPIFolder::CopyMessages** hat jede Nachricht erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="90116-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="90116-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="90116-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="90116-167">**IMAPIFolder::CopyMessages** konnte nicht jede Nachricht erfolgreich kopieren oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="90116-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="90116-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="90116-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="90116-169">**IMAPIFolder::CopyMessages** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="90116-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="90116-170">Beliebiger Fehlerwert</span><span class="sxs-lookup"><span data-stu-id="90116-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="90116-171">Wenn **IMAPIFolder::CopyMessages** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="90116-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="90116-172">**IMAPIFolder::CopyMessages** konnte möglicherweise eine oder mehrere Nachrichten kopieren oder verschieben, bevor der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="90116-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90116-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90116-173">See also</span></span>



[<span data-ttu-id="90116-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="90116-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

