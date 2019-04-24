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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280127"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="1cbc7-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="1cbc7-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="1cbc7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cbc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cbc7-105">Kopiert oder verschiebt eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-105">Copies or moves one or more messages.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1cbc7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cbc7-106">Parameters</span></span>

 <span data-ttu-id="1cbc7-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="1cbc7-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="1cbc7-108">in Ein Zeiger auf ein Array von [entrylist](entrylist.md) -Strukturen, die die zu kopierende oder zu verschiebende Nachricht oder Nachrichten identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="1cbc7-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1cbc7-109">_lpInterface_</span></span>
  
> <span data-ttu-id="1cbc7-110">in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf den Zielordner verwendet wird, auf den durch den _lpDestFolder_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="1cbc7-111">Übergeben von NULL-Ergebnissen im Dienstanbieter zurückgeben der Standardordner Schnittstelle [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="1cbc7-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="1cbc7-112">Clients müssen NULL überschreiten.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-112">Clients must pass NULL.</span></span> <span data-ttu-id="1cbc7-113">Andere Aufrufer können den _lpInterface_ -Parameter auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder festlegen.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="1cbc7-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="1cbc7-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="1cbc7-115">in Ein Zeiger auf den geöffneten Ordner, um die kopierten oder verschobenen Nachrichten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="1cbc7-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1cbc7-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="1cbc7-117">in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="1cbc7-118">Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, der Client legt das MESSAGE_DIALOG-Flag im _ulFlags_ -Parameter fest und übergibt im _LPPROGRESS_ -Parameter den Wert NULL.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="1cbc7-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="1cbc7-119">_lpProgress_</span></span>
  
> <span data-ttu-id="1cbc7-120">in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="1cbc7-121">Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="1cbc7-122">Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag wird in _ulFlags_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="1cbc7-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1cbc7-123">_ulFlags_</span></span>
  
> <span data-ttu-id="1cbc7-124">in Eine Bitmaske von Flags, die steuert, wie der Kopier-oder Verschiebungsvorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="1cbc7-125">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1cbc7-125">The following flags can be set:</span></span>
    
<span data-ttu-id="1cbc7-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="1cbc7-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="1cbc7-127">Informiert den Nachrichtenspeicher Anbieter, dass MAPI_E_DECLINE_COPY sofort zurückgegeben wird, wenn er **IMAPIFolder:: CopyMessages** implementiert, indem er das [IMAPISupport::D ocopyto](imapisupport-docopyto.md) oder [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md) -Methode des Support-Objekts aufruft.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="1cbc7-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1cbc7-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="1cbc7-129">Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="1cbc7-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="1cbc7-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="1cbc7-131">Die Nachrichten werden nicht kopiert, sondern verschoben.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="1cbc7-132">Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1cbc7-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1cbc7-133">Return value</span></span>

<span data-ttu-id="1cbc7-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cbc7-134">S_OK</span></span> 
  
> <span data-ttu-id="1cbc7-135">Die Nachricht oder Nachrichten wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="1cbc7-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="1cbc7-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="1cbc7-137">Der Anbieter implementiert diese Methode durch Aufrufen einer Support Objektmethode, und der Aufrufer hat das MAPI_DECLINE_OK-Flag übergeben.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="1cbc7-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="1cbc7-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="1cbc7-139">Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="1cbc7-140">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1cbc7-141">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1cbc7-142">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="1cbc7-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cbc7-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cbc7-143">Remarks</span></span>

<span data-ttu-id="1cbc7-144">Die **IMAPIFolder:: CopyMessages** -Methode kopiert oder verschiebt Nachrichten in einen anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="1cbc7-145">Mit Lese-/Schreibzugriff geöffnete Nachrichten können verschoben oder kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1cbc7-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="1cbc7-146">Notes to implementers</span></span>

<span data-ttu-id="1cbc7-147">Wenn Sie Nachrichten in einen anderen Nachrichtenspeicher kopieren, ohne die [IMAPISupport:: CopyMessages](imapisupport-copymessages.md) -Methode zu verwenden, müssen Sie zunächst [IMAPIFolder:: SETREADFLAGS](imapifolder-setreadflags.md) mit dem GENERATE_RECEIPT_ONLY-Flagsatz aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="1cbc7-148">Der empfangende Nachrichtenspeicher ist nicht für das Generieren von Lese Berichten für die kopierten oder verschobenen Nachrichten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="1cbc7-149">Wenn Sie **IMAPISupport:: CopyMessages** zum Implementieren von **IMAPIFolder:: CopyMessages**aufrufen, rufen Sie **SetReadFlags**nicht auf; MAPI wird es aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="1cbc7-150">Ihre Implementierung kann die Nachrichten in beliebiger Reihenfolge verschieben oder kopieren und Lesestatus Berichte in beliebiger Reihenfolge generieren.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="1cbc7-151">Das heißt, Sie können das Kopieren von Nachrichten abschließen, bevor Sie einen der Lesestatus Berichte generieren, oder die Berichte senden, bevor die Implementierung den Kopiervorgang startet.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="1cbc7-152">Allerdings sollten Lese Berichte gesendet werden, damit alle Nachrichten kopiert werden, unabhängig davon, ob die Kopie erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="1cbc7-153">Wenn der Kopier-oder Verschiebungsvorgang mehr als eine Nachricht umfasst, führen Sie den Vorgang so vollständig wie möglich aus.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="1cbc7-154">Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihres Steuerelements liegt, beispielsweise ausgehender Arbeitsspeicher, unzureichender Festplattenspeicherplatz oder Beschädigung im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="1cbc7-155">Versuchen Sie, Eintrags-IDs über Verschiebungs-oder Kopiervorgänge hinweg zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="1cbc7-156">Sie sollten auch Eintrags-IDs beibehalten, obwohl dies nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="1cbc7-157">Senden von Benachrichtigungen beim Verschieben oder Kopieren von Nachrichten, sodass Clients gewarnt werden, dass die Aufrufe der Nachrichten ' [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methoden fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="1cbc7-158">Schließen Sie den Status einer Nachricht nicht in den Kopier-oder Verschiebungsvorgang ein.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="1cbc7-159">Das bewegen oder Kopieren eines Nachrichtenstatus wirkt sich erheblich auf die Leistung aus.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1cbc7-160">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1cbc7-160">Notes to callers</span></span>

<span data-ttu-id="1cbc7-161">Verwenden Sie **IMAPIFolder:: CopyMessages** , um Suchergebnisordner aufzufüllen, in denen Nachrichten häufig nach übergeordneten Ordnern gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="1cbc7-162">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="1cbc7-163">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="1cbc7-163">**Condition**</span></span>|<span data-ttu-id="1cbc7-164">**Rückgabewert**</span><span class="sxs-lookup"><span data-stu-id="1cbc7-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1cbc7-165">**IMAPIFolder:: CopyMessages** hat jede Nachricht erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="1cbc7-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cbc7-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="1cbc7-167">**IMAPIFolder:: CopyMessages** konnte jede Nachricht nicht erfolgreich kopieren oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="1cbc7-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="1cbc7-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="1cbc7-169">**IMAPIFolder:: CopyMessages** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="1cbc7-170">Beliebiger Fehlerwert</span><span class="sxs-lookup"><span data-stu-id="1cbc7-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="1cbc7-171">Wenn **IMAPIFolder:: CopyMessages** nicht abgeschlossen werden kann, sollten Sie nicht davon ausgehen, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="1cbc7-172">**IMAPIFolder:: CopyMessages** kann möglicherweise eine oder mehrere Nachrichten kopieren oder verschieben, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1cbc7-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cbc7-173">See also</span></span>



[<span data-ttu-id="1cbc7-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="1cbc7-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

