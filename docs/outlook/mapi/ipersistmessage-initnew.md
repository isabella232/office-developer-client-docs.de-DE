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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317150"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="30a15-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="30a15-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="30a15-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30a15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30a15-105">Initialisiert eine neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="30a15-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="30a15-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30a15-106">Parameters</span></span>

 <span data-ttu-id="30a15-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="30a15-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="30a15-108">in Ein Zeiger auf die Nachrichtenwebsite, die das Formular für die Arbeit mit der Nachricht im Viewer verwendet.</span><span class="sxs-lookup"><span data-stu-id="30a15-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="30a15-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="30a15-109">_pMessage_</span></span>
  
> <span data-ttu-id="30a15-110">in Ein Zeiger auf die neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="30a15-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="30a15-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30a15-111">Return value</span></span>

<span data-ttu-id="30a15-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="30a15-112">S_OK</span></span> 
  
> <span data-ttu-id="30a15-113">Die neue Nachricht wurde erfolgreich initialisiert.</span><span class="sxs-lookup"><span data-stu-id="30a15-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30a15-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30a15-114">Remarks</span></span>

<span data-ttu-id="30a15-115">Formular Betrachter rufen die **IPersistMessage:: InitNew** -Methode auf, wenn der Benutzer eine neue Nachricht schreibt, die zu einer Nachrichtenklasse gehört, die vom Formular verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="30a15-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="30a15-116">Wenn das Form-Objekt einen gültigen Benutzeroberflächen Zeiger aufweist, sollte die Benutzeroberfläche für das Message-Objekt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="30a15-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="30a15-117">**InitNew** sollte nicht aufgerufen werden, wenn sich das Formular in einem beliebigen Zustand [](uninitialized-state.md) mit Ausnahme des nicht initialisierten Zustands befindet.</span><span class="sxs-lookup"><span data-stu-id="30a15-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="30a15-118">Wenn sich das Formular in einem der anderen Zustände befindet, wenn **InitNew** aufgerufen wird, geben Sie E_UNEXPECTED zurück.</span><span class="sxs-lookup"><span data-stu-id="30a15-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="30a15-119">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="30a15-119">Notes to implementers</span></span>

<span data-ttu-id="30a15-120">In der Regel werden Nachrichten mit nicht gespeicherten Eigenschaften als geändert gekennzeichnet, sodass der Client ein Dialogfeld anzeigen kann, in dem der Benutzer gefragt wird, ob diese Eigenschaften gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30a15-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="30a15-121">Wenn der Benutzer angibt, dass eine Nachricht gespeichert werden soll, speichern Sie die Daten, markieren Sie die Nachricht als sauber, und beenden Sie sie normal.</span><span class="sxs-lookup"><span data-stu-id="30a15-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="30a15-122">Wenn die Verarbeitung für Ihre neu initialisierten Nachrichten jedoch eine oder mehrere berechnete Eigenschaften festlegt und es wichtig ist, diese Eigenschaften zu speichern, markieren Sie die Nachrichten nicht als geändert.</span><span class="sxs-lookup"><span data-stu-id="30a15-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="30a15-123">Da berechnete Eigenschaften für Benutzer unsichtbar sein sollen, sollte kein Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="30a15-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="30a15-124">Wenn das Formular einen Verweis auf eine aktive Nachrichtenwebsite hat, die nicht an **InitNew**übergeben wird, geben Sie die ursprüngliche Website frei, da Sie nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="30a15-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="30a15-125">Speichern Sie die Zeiger auf den Nachrichten Standort und die Nachricht aus den Parametern _pMessageSite_ und _pMessage_ , und rufen Sie die Methoden [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) der Objekte auf, um Ihre Verweisanzahl zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="30a15-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="30a15-126">Legen Sie die Eigenschaften **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) und **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md)) für die neue Nachricht auf einen für Ihre Nachrichtenklasse geeigneten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="30a15-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="30a15-127">Viele Nachrichtenklassen legen **PR_MESSAGE_FLAGS** für neue Nachrichten auf MSGFLAG_UNSENT fest.</span><span class="sxs-lookup"><span data-stu-id="30a15-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="30a15-128">Wechseln Sie vor dem zurückgeben das Formular in den [Normal](normal-state.md) Zustand, wenn keine Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="30a15-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="30a15-129">Senden Sie eine neue Nachrichten Benachrichtigung an alle registrierten Viewer, indem Sie Ihre [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methoden aufrufen und S_OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="30a15-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="30a15-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="30a15-130">Notes to callers</span></span>

<span data-ttu-id="30a15-131">Nachdem Sie einen erfolgreichen Aufruf an **InitNew**durchgeführt haben, können Sie davon ausgehen, dass die folgenden erforderlichen Eigenschaften und keine anderen für das Formular festgelegt wurden:</span><span class="sxs-lookup"><span data-stu-id="30a15-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="30a15-132">**PR_DELETE_AFTER_SUBMIT** ([Pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30a15-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="30a15-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30a15-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="30a15-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30a15-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="30a15-135">**PR_PRIORITY** ([Pidtagpriority (](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30a15-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="30a15-136">**PR_READ_RECEIPT_REQUESTED** ([Pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30a15-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="30a15-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30a15-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="30a15-138">**PR_SENTMAIL_ENTRYID** ([Pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30a15-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="30a15-139">Weitere Informationen zu den Status von Formularen finden Sie unter [Formular Status](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="30a15-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="30a15-140">Weitere Informationen zur Initialisierung von Speicherobjekten finden Sie unter der [IPersistStorage:: InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="30a15-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30a15-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30a15-141">See also</span></span>



[<span data-ttu-id="30a15-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30a15-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

