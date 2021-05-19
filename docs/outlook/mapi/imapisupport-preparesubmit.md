---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425736"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="89144-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="89144-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="89144-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89144-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89144-105">Bereitet eine Nachricht für die Übermittlung an den MAPI-Spooler vor.</span><span class="sxs-lookup"><span data-stu-id="89144-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="89144-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="89144-106">Parameters</span></span>

 <span data-ttu-id="89144-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="89144-107">_lpMessage_</span></span>
  
> <span data-ttu-id="89144-108">[in] Ein Zeiger auf die zu bereitende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="89144-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="89144-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="89144-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="89144-110">[in, out] Bei der Eingabe ist  _der lpulFlags-Parameter_ reserviert und muss null sein.</span><span class="sxs-lookup"><span data-stu-id="89144-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="89144-111">Bei der Ausgabe  _muss lpulFlags_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="89144-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="89144-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89144-112">Return value</span></span>

<span data-ttu-id="89144-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="89144-113">S_OK</span></span> 
  
> <span data-ttu-id="89144-114">Die Nachricht wurde erfolgreich vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="89144-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89144-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89144-115">Remarks</span></span>

<span data-ttu-id="89144-116">Die **IMAPISupport::P repareSubmit-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="89144-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="89144-117">Nachrichtenspeicheranbieter rufen **PrepareSubmit** in ihrer Implementierung der [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf, um eine Nachricht für die Übermittlung an den MAPI-Spooler vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="89144-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="89144-118">**PrepareSubmit wird** verwendet, um Nachrichten zu behandeln, deren MSGFLAG_RESEND -Flag in ihrer **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="89144-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="89144-119">MSGFLAG_RESEND wird für Nachrichten festgelegt, die eine Anforderung enthalten, die bei einem Fehler bei der ersten Übertragung erneut gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89144-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="89144-120">**PrepareSubmit** bestimmt, welcher der Empfänger in der Empfängerliste die Nachricht erfolgreich empfangen hat und welche nicht.</span><span class="sxs-lookup"><span data-stu-id="89144-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="89144-121">Um auf die Empfängerliste zu zugreifen, **ruft PrepareSubmit** die [IMessage::GetRecipientTable-Methode der Nachricht](imessage-getrecipienttable.md) auf.</span><span class="sxs-lookup"><span data-stu-id="89144-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="89144-122">Zum Abrufen der Empfängerdaten ruft **PrepareSubmit** die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) der Empfängertabelle auf.</span><span class="sxs-lookup"><span data-stu-id="89144-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="89144-123">Für jede Zeile in der Tabelle überprüft **PrepareSubmit** die **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) -Eigenschaft und führt eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="89144-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="89144-124">Wenn das MAPI_SUBMITTED festgelegt ist, wird das Flag von **PrepareSubmit** entfernt und die **eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89144-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="89144-125">Wenn das MAPI_SUBMITTED nicht festgelegt ist, wird  **PrepareSubmit** PR_RECIPIENT_TYPE in MAPI_P1 geändert und **PR_RESPONSIBILITY** TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89144-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="89144-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="89144-126">Notes to callers</span></span>

<span data-ttu-id="89144-127">Stellen Sie vor dem Aufrufen von **PrepareSubmit** sicher, dass Sie die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) aufgerufen haben, und legen Sie das NOTIFY_READYTOSEND im  _ulFlags-Parameter_ fest.</span><span class="sxs-lookup"><span data-stu-id="89144-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="89144-128">Der **SpoolerNotify-Aufruf** muss einmal pro Sitzung vor dem Aufruf von **PrepareSubmit vorgenommen werden.**</span><span class="sxs-lookup"><span data-stu-id="89144-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="89144-129">**SpoolerNotify** synchronisiert den MAPI-Spooler und stellt sicher, dass alle erforderlichen Transportanbieter angemeldet sind und ihre Adresstypen registriert werden.</span><span class="sxs-lookup"><span data-stu-id="89144-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89144-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89144-130">See also</span></span>



[<span data-ttu-id="89144-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="89144-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="89144-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="89144-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="89144-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="89144-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

