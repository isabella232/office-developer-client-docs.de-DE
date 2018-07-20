---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1d325c67c836e727d8285bd2dceecf88bf68327c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792523"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="55953-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="55953-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="55953-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55953-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55953-105">Speichert alle Eigenschaften der Nachricht und markiert die Nachricht als gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="55953-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="55953-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55953-106">Parameters</span></span>

 <span data-ttu-id="55953-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="55953-107">_ulFlags_</span></span>
  
> <span data-ttu-id="55953-108">[in] Bitmaske der Flags, die steuern, wie eine Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="55953-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="55953-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="55953-109">The following flag can be set:</span></span>
    
<span data-ttu-id="55953-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="55953-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="55953-111">MAPI sollten die Nachricht sofort zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="55953-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="55953-112">Dieses Kennzeichen werden derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="55953-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="55953-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55953-113">Return value</span></span>

<span data-ttu-id="55953-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="55953-114">S_OK</span></span> 
  
> <span data-ttu-id="55953-115">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="55953-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="55953-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="55953-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="55953-117">Empfänger der Nachricht-Tabelle ist leer.</span><span class="sxs-lookup"><span data-stu-id="55953-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="55953-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55953-118">Remarks</span></span>

<span data-ttu-id="55953-119">Die **IMessage::SubmitMessage** -Methode markiert die Nachricht als übertragen werden bereit.</span><span class="sxs-lookup"><span data-stu-id="55953-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="55953-120">MAPI übergibt Nachrichten an die zugrunde liegenden messaging-System in der Reihenfolge, in der sie zum Senden von markiert sind.</span><span class="sxs-lookup"><span data-stu-id="55953-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="55953-121">Aufgrund dieser Funktionalität möglicherweise eine Meldung in einem Nachrichtenspeicher bleiben Sie für eine Weile, bevor das zugrunde liegende messaging-System Verantwortung für sie entgegennehmen kann.</span><span class="sxs-lookup"><span data-stu-id="55953-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="55953-122">Die Reihenfolge des Eingangs im Zielverzeichnis befindet sich in der zugrunde liegenden messaging-System-Steuerelement und entspricht nicht unbedingt die Reihenfolge, in der Nachrichten gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="55953-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="55953-123">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="55953-123">Notes to implementers</span></span>

<span data-ttu-id="55953-124">Rufen Sie die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode zum Speichern und überprüfen Sie dann die Nachricht **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="55953-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="55953-125">Wenn das Flag MSGFLAG_RESEND festgelegt ist, rufen Sie [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span><span class="sxs-lookup"><span data-stu-id="55953-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="55953-126">**PrepareSubmit** aktualisiert die Empfängertyp und **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft für alle Empfänger in der Nachricht erneut senden.</span><span class="sxs-lookup"><span data-stu-id="55953-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="55953-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="55953-127">Notes to callers</span></span>

<span data-ttu-id="55953-128">**SubmitMessage** , gibt alle Zeiger auf die Meldung und die zugehörigen Unterobjekte Nachrichten sind Ordner, Anlagen, Datenströme, Tabellen und So weiter nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="55953-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="55953-129">MAPI erlaubt keine weiteren Vorgänge für diese Zeiger, außer für die **IUnknown** -Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="55953-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="55953-130">MAPI ist darauf ausgelegt, dass nach dem Aufruf von **SubmitMessage** Sie die Nachricht und alle zugehörigen Unterobjekte freigegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55953-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="55953-131">Wenn **SubmitMessage** einen Fehler zurück, der angibt, fehlende oder ungültige Informationen zurückgegeben wird, bleibt geöffnet, die Nachricht und die Zeiger noch gültig.</span><span class="sxs-lookup"><span data-stu-id="55953-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="55953-132">Um ein Sendevorgang abzubrechen, abrufen und einen Zeiger auf die Nachricht **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft gespeichert werden, bevor die Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="55953-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="55953-133">Da er die Eintrags-ID eine Nachricht ungültig ist, nachdem die Nachricht gesendet wurde, ist es erforderlich, vor dem Aufruf von **SubmitMessage**zu speichern.</span><span class="sxs-lookup"><span data-stu-id="55953-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="55953-134">Um das Senden abzubrechen, zeigen Sie den Parameter _LpEntryId_ auf dieses Eintrags-ID, und rufen Sie [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span><span class="sxs-lookup"><span data-stu-id="55953-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="55953-135">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="55953-135">MFCMAPI reference</span></span>

<span data-ttu-id="55953-136">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="55953-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="55953-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="55953-137">**File**</span></span>|<span data-ttu-id="55953-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="55953-138">**Function**</span></span>|<span data-ttu-id="55953-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="55953-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="55953-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="55953-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="55953-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="55953-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="55953-142">MFCMAPI (engl.) wird die **IMessage::SubmitMessage** -Methode verwendet, um die ausgewählte Nachricht zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="55953-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55953-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55953-143">See also</span></span>



[<span data-ttu-id="55953-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="55953-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="55953-145">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="55953-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="55953-146">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="55953-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

