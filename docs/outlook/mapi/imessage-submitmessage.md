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
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437364"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="d26f2-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d26f2-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="d26f2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d26f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d26f2-105">Speichert alle Eigenschaften der Nachricht und markiert die Nachricht als bereit zum Senden.</span><span class="sxs-lookup"><span data-stu-id="d26f2-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d26f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d26f2-106">Parameters</span></span>

 <span data-ttu-id="d26f2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d26f2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d26f2-108">[in] Bitmaske von Flags, die verwendet werden, um zu steuern, wie eine Nachricht übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="d26f2-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="d26f2-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d26f2-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d26f2-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="d26f2-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="d26f2-111">MAPI sollte die Nachricht sofort übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d26f2-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="d26f2-112">Dieses Flag wird derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d26f2-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d26f2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d26f2-113">Return value</span></span>

<span data-ttu-id="d26f2-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d26f2-114">S_OK</span></span> 
  
> <span data-ttu-id="d26f2-115">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d26f2-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d26f2-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="d26f2-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="d26f2-117">Die Empfängertabelle der Nachricht ist leer.</span><span class="sxs-lookup"><span data-stu-id="d26f2-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d26f2-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d26f2-118">Remarks</span></span>

<span data-ttu-id="d26f2-119">Die **IMessage::SubmitMessage-Methode** markiert eine Nachricht als bereit für die Übertragung.</span><span class="sxs-lookup"><span data-stu-id="d26f2-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="d26f2-120">MAPI übergibt Nachrichten an das zugrunde liegende Messagingsystem in der Reihenfolge, in der sie für das Senden markiert sind.</span><span class="sxs-lookup"><span data-stu-id="d26f2-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="d26f2-121">Aufgrund dieser Funktionalität bleibt eine Nachricht möglicherweise einige Zeit in einem Nachrichtenspeicher, bevor das zugrunde liegende Messagingsystem die Verantwortung dafür übernehmen kann.</span><span class="sxs-lookup"><span data-stu-id="d26f2-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="d26f2-122">Die Reihenfolge des Empfangs am Ziel befindet sich im Steuerelement des zugrunde liegenden Messagingsystems und nicht unbedingt mit der Reihenfolge, in der Nachrichten gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d26f2-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d26f2-123">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d26f2-123">Notes to implementers</span></span>

<span data-ttu-id="d26f2-124">Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht auf, um sie zu speichern, und überprüfen Sie dann die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d26f2-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="d26f2-125">Wenn das MSGFLAG_RESEND festgelegt ist, rufen [Sie IMAPISupport::P repareSubmit auf.](imapisupport-preparesubmit.md)</span><span class="sxs-lookup"><span data-stu-id="d26f2-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="d26f2-126">**PrepareSubmit** aktualisiert den Empfängertyp **und PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft für alle Empfänger in der erneut gesendeten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d26f2-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d26f2-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d26f2-127">Notes to callers</span></span>

<span data-ttu-id="d26f2-128">Wenn **SubmitMessage** zurückgegeben wird, sind alle Zeiger auf die Nachricht und die zugehörigen Unterobjekte Nachrichten, Ordner, Anlagen, Datenströme, Tabellen und so weiter nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="d26f2-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="d26f2-129">MAPI lässt keine weiteren Vorgänge für diese Zeiger zu, mit Ausnahme des Aufrufens ihrer **IUnknown::Release-Methoden.**</span><span class="sxs-lookup"><span data-stu-id="d26f2-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="d26f2-130">MAPI ist so konzipiert, dass Sie nach dem Aufgerufen von **SubmitMessage** die Nachricht und alle zugehörigen Unterobjekte los lassen sollten.</span><span class="sxs-lookup"><span data-stu-id="d26f2-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="d26f2-131">Wenn **SubmitMessage** jedoch einen Fehlerwert zurückgibt, der fehlende oder ungültige Informationen angibt, bleibt die Nachricht geöffnet, und die Zeiger bleiben gültig.</span><span class="sxs-lookup"><span data-stu-id="d26f2-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="d26f2-132">Um einen Sendevorgang abbricht, erhalten und speichern Sie einen Zeiger auf die **PR_ENTRYID** -[PidTagEntryId](pidtagentryid-canonical-property.md)-Eigenschaft der Nachricht, bevor die Nachricht übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="d26f2-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="d26f2-133">Da der Eintragsbezeichner einer Nachricht ungültig ist, nachdem die Nachricht übermittelt wurde, muss sie gespeichert werden, bevor **Sie SubmitMessage aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="d26f2-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="d26f2-134">Wenn Sie das Senden abbrechen möchten, zeigen Sie den _lpEntryId-Parameter_ auf diesen Eintragsbezeichner, und rufen Sie [IMsgStore::AbortSubmit auf.](imsgstore-abortsubmit.md)</span><span class="sxs-lookup"><span data-stu-id="d26f2-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d26f2-135">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="d26f2-135">MFCMAPI reference</span></span>

<span data-ttu-id="d26f2-136">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d26f2-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d26f2-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d26f2-137">**File**</span></span>|<span data-ttu-id="d26f2-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d26f2-138">**Function**</span></span>|<span data-ttu-id="d26f2-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d26f2-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d26f2-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d26f2-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="d26f2-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="d26f2-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="d26f2-142">MFCMAPI verwendet die **IMessage::SubmitMessage-Methode,** um die ausgewählte Nachricht zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d26f2-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d26f2-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d26f2-143">See also</span></span>



[<span data-ttu-id="d26f2-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="d26f2-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="d26f2-145">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d26f2-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="d26f2-146">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d26f2-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

