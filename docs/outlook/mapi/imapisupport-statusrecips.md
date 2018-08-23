---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cda629cf78d3f7915b64c130867ed4f8ebbd6f8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563842"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="9ea7d-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="9ea7d-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="9ea7d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ea7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ea7d-105">Bereitstellung und Nondelivery Berichte generiert.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="9ea7d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ea7d-106">Parameters</span></span>

 <span data-ttu-id="9ea7d-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="9ea7d-107">_lpMessage_</span></span>
  
> <span data-ttu-id="9ea7d-108">[in] Ein Zeiger auf die Meldung für die der Bericht generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="9ea7d-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="9ea7d-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="9ea7d-110">[in] Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die Empfänger der Nachricht beschreibt, auf _LpMessage_zeigt.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9ea7d-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9ea7d-111">Return value</span></span>

<span data-ttu-id="9ea7d-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ea7d-112">S_OK</span></span> 
  
> <span data-ttu-id="9ea7d-113">Der Bericht wurde erfolgreich generiert.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="9ea7d-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="9ea7d-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="9ea7d-115">Der Aufruf war insgesamt erfolgreich, aber es sind keine Empfänger Optionen für diese Art des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="9ea7d-116">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="9ea7d-117">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="9ea7d-118">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="9ea7d-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ea7d-119">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9ea7d-119">Remarks</span></span>

<span data-ttu-id="9ea7d-120">Die **IMAPISupport::StatusRecips** -Methode wird für Transport Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="9ea7d-121">Transportanbieter Aufrufen **StatusRecips** um anzufordern, MAPI Senden eines Berichts Übermittlung oder Nondelivery einen Satz von mindestens eines der Empfänger einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9ea7d-122">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9ea7d-122">Notes to callers</span></span>

<span data-ttu-id="9ea7d-123">Sie können **StatusRecips** mehrmals während der Verarbeitung einer Nachricht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="9ea7d-124">Jedoch, wenn Sie **StatusRecips** für einer geöffneten Nachricht aufrufen, sollten Sie sammeln alle Übermittlung und Nondelivery Informationen für die Empfänger der Nachricht, und rufen Sie **StatusRecips** für diese Empfängerliste.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="9ea7d-125">Eine zentrale Stelle Auflistung ist wichtig, da mehrere **StatusRecips** Anrufe für einen Empfänger in mehreren identische Berichten gesendete führen können.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="9ea7d-126">Speichern von Eigenschaften, die auf die Nachrichtenübermittlung oder Nondelivery in der **ADRLIST** -Struktur, die durch den _LpRecipList_ -Parameter angegebenen beziehen.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="9ea7d-127">Eine vollständige Liste der erforderlichen und optionalen Eigenschaften für Übermittlungsberichte und Unzustellbarkeitsberichten finden Sie unter [Erforderliche Bericht Nachrichteneigenschaften](required-report-message-properties.md) und [Optional Bericht Nachrichteneigenschaften](optional-report-message-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9ea7d-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="9ea7d-128">Speicher für die **ADRLIST** -Struktur im _LpRecipList_ mithilfe der Funktionen [MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="9ea7d-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="9ea7d-129">MAPI-Freigaben für den Speicher durch Aufrufen der Funktion [MAPIFreeBuffer](mapifreebuffer.md) nur, wenn **StatusRecips** erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="9ea7d-130">Eine Übersicht über die Bereitstellung und Nondelivery Berichte finden Sie unter [MAPI-Berichtnachrichten](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="9ea7d-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ea7d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ea7d-131">See also</span></span>



[<span data-ttu-id="9ea7d-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="9ea7d-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="9ea7d-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="9ea7d-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="9ea7d-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="9ea7d-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="9ea7d-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="9ea7d-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="9ea7d-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9ea7d-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="9ea7d-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="9ea7d-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="9ea7d-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9ea7d-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9ea7d-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ea7d-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

