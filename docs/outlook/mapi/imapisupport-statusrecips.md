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
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341769"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="ef96c-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="ef96c-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="ef96c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef96c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef96c-105">Generiert Unzustellbarkeitsberichte.</span><span class="sxs-lookup"><span data-stu-id="ef96c-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="ef96c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef96c-106">Parameters</span></span>

 <span data-ttu-id="ef96c-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="ef96c-107">_lpMessage_</span></span>
  
> <span data-ttu-id="ef96c-108">in Ein Zeiger auf die Nachricht, für die der Bericht generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef96c-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="ef96c-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="ef96c-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="ef96c-110">in Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Empfänger der Nachricht beschreibt, auf die von _lpMessage_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ef96c-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ef96c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef96c-111">Return value</span></span>

<span data-ttu-id="ef96c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef96c-112">S_OK</span></span> 
  
> <span data-ttu-id="ef96c-113">Der Bericht wurde erfolgreich generiert.</span><span class="sxs-lookup"><span data-stu-id="ef96c-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="ef96c-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="ef96c-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="ef96c-115">Der Anruf war insgesamt erfolgreich, aber es gibt keine Empfängeroptionen für diesen Empfängertyp.</span><span class="sxs-lookup"><span data-stu-id="ef96c-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="ef96c-116">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="ef96c-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ef96c-117">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="ef96c-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ef96c-118">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="ef96c-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef96c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef96c-119">Remarks</span></span>

<span data-ttu-id="ef96c-120">Die **IMAPISupport:: StatusRecips** -Methode wird für Support Objekte des Transportanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="ef96c-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="ef96c-121">Transport Anbieter rufen **StatusRecips** auf, um anzufordern, dass MAPI einen Zustellungs-oder Unzustellbarkeitsbericht an eine Gruppe von einem oder mehreren Empfängern einer Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="ef96c-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ef96c-122">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ef96c-122">Notes to callers</span></span>

<span data-ttu-id="ef96c-123">Sie können **StatusRecips** während der Verarbeitung einer Nachricht mehrmals aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ef96c-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="ef96c-124">Wenn Sie jedoch **StatusRecips** für eine offene Nachricht aufrufen, sollten Sie alle zugestellten und nicht zugestellten Informationen für die Nachrichtenempfänger erfassen und **StatusRecips** für diese Empfängerliste aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ef96c-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="ef96c-125">Ein einzelner Sammlungspunkt ist wichtig, da mehrere **StatusRecips** -Aufrufe für einen Empfänger dazu führen können, dass mehrere identische Berichte gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef96c-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="ef96c-126">Speichern von Eigenschaften, die sich auf die Nachrichtenübermittlung oder Nichtübermittlung beziehen, in der **ADRLIST** -Struktur, die durch den _lpRecipList_ -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef96c-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="ef96c-127">Eine vollständige Liste der erforderlichen und optionalen Eigenschaften für Zustellungsberichte und Unzustellbarkeitsberichte finden Sie unter erforderliche Eigenschaften für [Berichtsnachrichten](required-report-message-properties.md) und [optionale Berichtnachrichten Eigenschaften](optional-report-message-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ef96c-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="ef96c-128">Zuweisen von Arbeitsspeicher für die **ADRLIST** -Struktur in _LpRecipList_ mithilfe der [MAPIAllocateBuffer](mapiallocatebuffer.md) -und [MAPIAllocateMore](mapiallocatemore.md) -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ef96c-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="ef96c-129">MAPI gibt den Arbeitsspeicher frei, indem die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion nur aufgerufen wird, wenn **StatusRecips** erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef96c-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="ef96c-130">Eine Übersicht über Zusteller-und Unzustellbarkeitsberichte finden Sie unter [MAPI Report Messages](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="ef96c-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef96c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef96c-131">See also</span></span>



[<span data-ttu-id="ef96c-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="ef96c-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="ef96c-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="ef96c-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="ef96c-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="ef96c-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="ef96c-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="ef96c-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="ef96c-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ef96c-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ef96c-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="ef96c-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="ef96c-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ef96c-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ef96c-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef96c-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

