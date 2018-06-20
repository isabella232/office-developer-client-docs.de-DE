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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f6902b45cde3e5349d69b6f35c3f8980deb031b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792424"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="1a5a1-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="1a5a1-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="1a5a1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a5a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a5a1-105">Bereitet eine Nachricht für die Übermittlung an die MAPI-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1a5a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a5a1-106">Parameters</span></span>

 <span data-ttu-id="1a5a1-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="1a5a1-107">_lpMessage_</span></span>
  
> <span data-ttu-id="1a5a1-108">[in] Ein Zeiger auf die Nachricht zum Vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="1a5a1-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a5a1-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="1a5a1-110">[in, out] Bei der Eingabe der Parameter _LpulFlags_ ist reserviert und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="1a5a1-111">_LpulFlags_ muss NULL sein, bei der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1a5a1-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1a5a1-112">Return value</span></span>

<span data-ttu-id="1a5a1-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a5a1-113">S_OK</span></span> 
  
> <span data-ttu-id="1a5a1-114">Die Nachricht wurde erfolgreich vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a5a1-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a5a1-115">Remarks</span></span>

<span data-ttu-id="1a5a1-116">Die **IMAPISupport::PrepareSubmit** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="1a5a1-117">Nachricht-Anbieter anrufen **PrepareSubmit** in ihrer Implementierung der [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode, um eine Nachricht für die Übermittlung an die Warteschlange MAPI vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="1a5a1-118">**PrepareSubmit** wird verwendet, um die Verarbeitung von Nachrichten, die die in ihrer **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft MSGFLAG_RESEND gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="1a5a1-119">MSGFLAG_RESEND wird für Nachrichten festgelegt, die eine Anforderung erneut gesendet werden, wenn eine anfängliche Übertragung fehlschlägt enthalten.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="1a5a1-120">**PrepareSubmit** bestimmt, dem der Empfänger in der Liste der Empfänger die Nachricht erfolgreich empfangen und die nicht der Fall.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="1a5a1-121">**PrepareSubmit** die Nachricht [IMessage::GetRecipientTable](imessage-getrecipienttable.md) Methode aufgerufen, um Zugriff auf die Empfängerliste.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="1a5a1-122">Zum Abrufen der Empfängerdaten ruft **PrepareSubmit** [QueryRows der Empfänger Tabelle](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="1a5a1-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="1a5a1-123">Für jede Zeile in der Tabelle **PrepareSubmit** die **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))-Eigenschaft überprüft und akzeptiert einen der folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="1a5a1-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="1a5a1-124">Wenn das Flag MAPI_SUBMITTED festgelegt ist, löscht das Flag **PrepareSubmit** , und die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="1a5a1-125">Wenn das Flag MAPI_SUBMITTED nicht festgelegt ist, wird **PrepareSubmit** **PR_RECIPIENT_TYPE** in MAPI_P1 geändert und **PR_RESPONSIBILITY** auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="1a5a1-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1a5a1-126">Notes to callers</span></span>

<span data-ttu-id="1a5a1-127">Bevor Sie **PrepareSubmit**aufrufen, müssen Sie unbedingt, haben die [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode aufgerufen und legen Sie die Kennzeichen NOTIFY_READYTOSEND im _UlFlags_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="1a5a1-128">Die **SpoolerNotify** muss einmal pro Sitzung vor dem Aufruf von **PrepareSubmit**aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="1a5a1-129">**SpoolerNotify** synchronisiert die MAPI-Warteschlange und wird sichergestellt, dass alle erforderlichen Transportanbieter angemeldet sind und ihre Adresstypen registriert sind.</span><span class="sxs-lookup"><span data-stu-id="1a5a1-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a5a1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a5a1-130">See also</span></span>



[<span data-ttu-id="1a5a1-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1a5a1-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="1a5a1-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="1a5a1-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="1a5a1-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a5a1-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
