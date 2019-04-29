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
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="af4f9-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="af4f9-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="af4f9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af4f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af4f9-105">Bereitet eine Nachricht für die Übermittlung an den MAPI-Spooler vor.</span><span class="sxs-lookup"><span data-stu-id="af4f9-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="af4f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="af4f9-106">Parameters</span></span>

 <span data-ttu-id="af4f9-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="af4f9-107">_lpMessage_</span></span>
  
> <span data-ttu-id="af4f9-108">in Ein Zeiger auf die Nachricht, die vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="af4f9-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="af4f9-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="af4f9-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="af4f9-110">[in, out] Bei der Eingabe ist der _lpulFlags_ -Parameter reserviert und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="af4f9-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="af4f9-111">Bei der Ausgabe muss _LPULFLAGS_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="af4f9-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="af4f9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af4f9-112">Return value</span></span>

<span data-ttu-id="af4f9-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="af4f9-113">S_OK</span></span> 
  
> <span data-ttu-id="af4f9-114">Die Nachricht wurde erfolgreich vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="af4f9-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af4f9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af4f9-115">Remarks</span></span>

<span data-ttu-id="af4f9-116">Die **IMAPISupport::P reparesubmit** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="af4f9-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="af4f9-117">Nachrichtenspeicher Anbieter rufen **PrepareSubmit** in ihrer Implementierung der [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf, um eine Nachricht für die Übermittlung an den MAPI-Spooler vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="af4f9-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="af4f9-118">**PrepareSubmit** wird verwendet, um Nachrichten zu verarbeiten, für die das MSGFLAG_RESEND-Flag in Ihrer **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="af4f9-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="af4f9-119">MSGFLAG_RESEND wird für Nachrichten festgelegt, die eine Anforderung zum erneuten Senden einer anfänglichen Übertragung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="af4f9-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="af4f9-120">**PrepareSubmit** bestimmt, welche Empfänger in der Empfängerliste die Nachricht erfolgreich empfangen haben und welche nicht.</span><span class="sxs-lookup"><span data-stu-id="af4f9-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="af4f9-121">Um auf die Empfängerliste zuzugreifen, ruft **PrepareSubmit** die [IMessage::](imessage-getrecipienttable.md) getrecipientable-Methode der Nachricht auf.</span><span class="sxs-lookup"><span data-stu-id="af4f9-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="af4f9-122">Zum Abrufen der Empfängerdaten ruft **PrepareSubmit** die [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode der Empfängertabelle auf.</span><span class="sxs-lookup"><span data-stu-id="af4f9-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="af4f9-123">Für jede Zeile in der Tabelle prüft **PrepareSubmit** die **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))-Eigenschaft und führt eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="af4f9-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="af4f9-124">Wenn das MAPI_SUBMITTED-Flag festgelegt ist, löscht **PrepareSubmit** das Flag und legt die **PR_RESPONSIBILITY** ([PIDTAGRESPONSIBILITY (](pidtagresponsibility-canonical-property.md))-Eigenschaft auf false fest.</span><span class="sxs-lookup"><span data-stu-id="af4f9-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="af4f9-125">Wenn das MAPI_SUBMITTED-Flag nicht festgelegt ist, ändert **PrepareSubmit** **PR_RECIPIENT_TYPE** zu MAPI_P1 und legt **PR_RESPONSIBILITY** auf true fest.</span><span class="sxs-lookup"><span data-stu-id="af4f9-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="af4f9-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="af4f9-126">Notes to callers</span></span>

<span data-ttu-id="af4f9-127">Stellen Sie vor dem Aufrufen von **PrepareSubmit**sicher, dass Sie die [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode aufgerufen und das NOTIFY_READYTOSEND-Flag im Parameter _ulFlags_ festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="af4f9-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="af4f9-128">Der **SpoolerNotify** -Aufruf muss einmal pro Sitzung vor dem Aufruf von **PrepareSubmit**durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af4f9-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="af4f9-129">**SpoolerNotify** synchronisiert den MAPI-Spooler und stellt sicher, dass alle erforderlichen Transportanbieter angemeldet sind und ihre Adresstypen registriert sind.</span><span class="sxs-lookup"><span data-stu-id="af4f9-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af4f9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af4f9-130">See also</span></span>



[<span data-ttu-id="af4f9-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="af4f9-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="af4f9-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="af4f9-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="af4f9-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="af4f9-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

