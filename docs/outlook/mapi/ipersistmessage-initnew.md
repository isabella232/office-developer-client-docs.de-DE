---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e237e73f59fa691821dcb55b59f5d17518451797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792723"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="bde6d-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="bde6d-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="bde6d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bde6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bde6d-105">Initialisiert eine neue Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="bde6d-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="bde6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bde6d-106">Parameters</span></span>

 <span data-ttu-id="bde6d-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="bde6d-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="bde6d-108">[in] Ein Zeiger auf die Nachricht-Website, die das Formular verwendet wird, um die Nachricht im Viewer entwickelt.</span><span class="sxs-lookup"><span data-stu-id="bde6d-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="bde6d-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="bde6d-109">_pMessage_</span></span>
  
> <span data-ttu-id="bde6d-110">[in] Ein Zeiger auf die neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bde6d-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bde6d-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="bde6d-111">Return value</span></span>

<span data-ttu-id="bde6d-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="bde6d-112">S_OK</span></span> 
  
> <span data-ttu-id="bde6d-113">Die neue Nachricht wurde erfolgreich initialisiert.</span><span class="sxs-lookup"><span data-stu-id="bde6d-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bde6d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bde6d-114">Remarks</span></span>

<span data-ttu-id="bde6d-115">Formular Viewer rufen die **IPersistMessage::InitNew** -Methode auf, wenn der Benutzer eine neue Nachricht verfasst, zu der eine Nachrichtenklasse gehört, der das Formular behandelt.</span><span class="sxs-lookup"><span data-stu-id="bde6d-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="bde6d-116">Wenn das Form-Objekt einen gültigen Benutzernamen Schnittstellenzeiger aufweist, sollte die Benutzeroberfläche für das Objekt "Message" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bde6d-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="bde6d-117">**InitNew** sollte nicht aufgerufen werden, wenn das Formular in einen beliebigen Zustand außer den Status [nicht initialisiert](uninitialized-state.md) wird.</span><span class="sxs-lookup"><span data-stu-id="bde6d-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="bde6d-118">Wenn das Formular eines der anderen Status ist **InitNew** aufgerufen wird, zurückgeben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="bde6d-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bde6d-119">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="bde6d-119">Notes to implementers</span></span>

<span data-ttu-id="bde6d-120">In der Regel werden Nachrichten, die Eigenschaften nicht gespeicherte haben als geändert markiert, sodass der Client ein Dialogfeld angezeigt werden kann, die der Benutzer aufgefordert wird, ob diese Eigenschaften gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bde6d-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="bde6d-121">Wenn der Benutzer gibt an, dass eine Nachricht gespeichert werden soll, speichern Sie die Daten, markieren der Nachricht als clean und normal beenden.</span><span class="sxs-lookup"><span data-stu-id="bde6d-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="bde6d-122">Jedoch wenn Verarbeitung für Ihre neu initialisierten Nachrichten umfasst eine festlegen oder Eigenschaften berechnete, und es ist wichtig für diese Eigenschaften gespeichert werden soll, führen Sie nicht die Nachrichten als geändert zu markieren.</span><span class="sxs-lookup"><span data-stu-id="bde6d-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="bde6d-123">Da berechnete Eigenschaften für Benutzer nicht sichtbar sein soll, sollte das Dialogfeld nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bde6d-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="bde6d-124">Wenn Ihr Formular einen Verweis auf eine aktive Nachricht Website als derjenigen, die in **InitNew**übergeben wird, lassen Sie die ursprüngliche Website, da sie nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bde6d-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="bde6d-125">Der Zeiger auf die Nachricht-Website und die Nachricht der Parameter _pMessageSite_ und _pMessage_ gespeichert, und rufen beide Objekte [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) Methoden, um ihre Referenzzähler erhöhen.</span><span class="sxs-lookup"><span data-stu-id="bde6d-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="bde6d-126">Legen Sie die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) und **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaften für die neue Nachricht in einen passenden für Ihre Nachrichtenklasse ein.</span><span class="sxs-lookup"><span data-stu-id="bde6d-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="bde6d-127">Viele Nachrichtenklassen, legen Sie beispielsweise **PR_MESSAGE_FLAGS** auf MSGFLAG_UNSENT für neue Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="bde6d-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="bde6d-128">Vor der Rückgabe, Übergang des Formulars auf den [normalen](normal-state.md) Status, wenn keine Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bde6d-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="bde6d-129">Senden Sie eine neue Benachrichtigung an alle registrierten Viewer durch ihre [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methoden aufrufen, und geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="bde6d-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bde6d-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="bde6d-130">Notes to callers</span></span>

<span data-ttu-id="bde6d-131">Nachdem Sie einen erfolgreichen Aufruf von **InitNew**vorgenommen haben, können Sie davon ausgehen, dass die folgenden erforderlichen Eigenschaften und keine andere, für das Formular festgelegt wurden:</span><span class="sxs-lookup"><span data-stu-id="bde6d-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="bde6d-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bde6d-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="bde6d-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bde6d-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="bde6d-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bde6d-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="bde6d-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bde6d-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="bde6d-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bde6d-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="bde6d-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bde6d-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="bde6d-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bde6d-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="bde6d-139">Weitere Informationen über die Zustände von Formularen finden Sie unter [Formular Zustände](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="bde6d-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="bde6d-140">Weitere Informationen dazu, wie Speicherobjekte initialisiert werden finden Sie unter der [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bde6d-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bde6d-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bde6d-141">See also</span></span>



[<span data-ttu-id="bde6d-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bde6d-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

