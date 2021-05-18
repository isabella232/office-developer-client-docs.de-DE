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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408768"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="eb829-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="eb829-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="eb829-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb829-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb829-105">Generiert Übermittlungs- und Nicht-Lieferberichte.</span><span class="sxs-lookup"><span data-stu-id="eb829-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="eb829-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb829-106">Parameters</span></span>

 <span data-ttu-id="eb829-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="eb829-107">_lpMessage_</span></span>
  
> <span data-ttu-id="eb829-108">[in] Ein Zeiger auf die Nachricht, für die der Bericht generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb829-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="eb829-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="eb829-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="eb829-110">[in] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Empfänger der Nachricht beschreibt, auf die von _lpMessage verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="eb829-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eb829-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb829-111">Return value</span></span>

<span data-ttu-id="eb829-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb829-112">S_OK</span></span> 
  
> <span data-ttu-id="eb829-113">Der Bericht wurde erfolgreich generiert.</span><span class="sxs-lookup"><span data-stu-id="eb829-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="eb829-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="eb829-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="eb829-115">Der Anruf war insgesamt erfolgreich, es gibt jedoch keine Empfängeroptionen für diesen Empfängertyp.</span><span class="sxs-lookup"><span data-stu-id="eb829-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="eb829-116">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="eb829-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="eb829-117">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="eb829-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="eb829-118">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="eb829-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb829-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eb829-119">Remarks</span></span>

<span data-ttu-id="eb829-120">Die **IMAPISupport::StatusRecips-Methode** wird für Unterstützungsobjekte des Transportanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="eb829-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="eb829-121">Transportanbieter rufen **StatusRecips auf,** um zu fordern, dass MAPI einen Zustellungs- oder Unzustelldienstbericht an einen oder mehrere Empfänger einer Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="eb829-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eb829-122">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="eb829-122">Notes to callers</span></span>

<span data-ttu-id="eb829-123">Sie können **StatusRecips während** der Verarbeitung einer Nachricht mehrmals aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eb829-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="eb829-124">Wenn Sie **statusRecips** jedoch für eine geöffnete Nachricht aufrufen, tun Sie ihr Bestes, um alle Übermittlungs- und Nichtzustellinformationen für die Nachrichtenempfänger zu sammeln und **StatusRecips** für diese Empfängerliste anzurufen.</span><span class="sxs-lookup"><span data-stu-id="eb829-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="eb829-125">Ein einzelner Sammlungspunkt ist wichtig, da mehrere **StatusRecips-Aufrufe** für einen Empfänger dazu führen können, dass mehrere identische Berichte gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb829-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="eb829-126">Store eigenschaften, die sich auf die Nachrichtenzustellung oder Nichtzustellung in der **adrlist-Struktur** beziehen, die durch den _lpRecipList-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="eb829-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="eb829-127">Eine vollständige Liste der erforderlichen und optionalen Eigenschaften für Übermittlungsberichte und Nicht-Lieferberichte finden Sie unter [Required Report Message Properties](required-report-message-properties.md) und Optional Report Message [Properties](optional-report-message-properties.md).</span><span class="sxs-lookup"><span data-stu-id="eb829-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="eb829-128">Zuordnen von Arbeitsspeicher für die **ADRLIST-Struktur** in _lpRecipList_ mithilfe der [Funktionen MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIAllocateMore.](mapiallocatemore.md)</span><span class="sxs-lookup"><span data-stu-id="eb829-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="eb829-129">MAPI gibt den Speicher frei, indem die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) nur dann aufruft, wenn **StatusRecips erfolgreich** ist.</span><span class="sxs-lookup"><span data-stu-id="eb829-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="eb829-130">Eine Übersicht über Zustellungs- und Nicht-Lieferberichte finden Sie unter [MAPI Report Messages](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="eb829-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb829-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb829-131">See also</span></span>



[<span data-ttu-id="eb829-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="eb829-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="eb829-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="eb829-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="eb829-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="eb829-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="eb829-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="eb829-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="eb829-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="eb829-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="eb829-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="eb829-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="eb829-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="eb829-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="eb829-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb829-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

