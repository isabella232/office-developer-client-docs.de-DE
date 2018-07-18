---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5e56fd8c053ff32bdeb7b243701c0330b378cdc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792423"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="1e0af-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="1e0af-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="1e0af-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e0af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e0af-105">Generiert einen Lese- oder nonread Bericht für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1e0af-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="1e0af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e0af-106">Parameters</span></span>

 <span data-ttu-id="1e0af-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1e0af-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1e0af-108">[in] Eine Bitmaske aus Flags, die steuert, wie das Lesen oder den nonread Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1e0af-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="1e0af-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1e0af-109">The following flag can be set:</span></span>
    
<span data-ttu-id="1e0af-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="1e0af-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="1e0af-111">Ein nonread Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1e0af-111">A nonread report is generated.</span></span> <span data-ttu-id="1e0af-112">Wenn MAPI_NON_READ nicht festgelegt ist, wird ein schreibgeschützte Bericht generiert.</span><span class="sxs-lookup"><span data-stu-id="1e0af-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="1e0af-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="1e0af-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="1e0af-114">[in] Ein Zeiger auf die Nachricht, die der Bericht generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e0af-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="1e0af-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="1e0af-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="1e0af-116">[in, out] Eingabe _LppEmptyMessage_ zeigt auf einen Zeiger auf eine leere Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1e0af-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="1e0af-117">Ausgabe _LppEmptyMessage_ zeigt auf einen Zeiger auf den Berichtnachricht.</span><span class="sxs-lookup"><span data-stu-id="1e0af-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1e0af-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1e0af-118">Return value</span></span>

<span data-ttu-id="1e0af-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e0af-119">S_OK</span></span> 
  
> <span data-ttu-id="1e0af-120">Der Bericht wurde erfolgreich generiert.</span><span class="sxs-lookup"><span data-stu-id="1e0af-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e0af-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e0af-121">Remarks</span></span>

<span data-ttu-id="1e0af-122">Die **IMAPISupport::ReadReceipt** -Methode ist nur für Nachricht Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="1e0af-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="1e0af-123">Nachricht-Anbieter anrufen **ReadReceipt** um anzuweisen, MAPI, um eine Lese- oder nonread Bericht für die Meldung über den Parameter _LpReadMessage_ generieren.</span><span class="sxs-lookup"><span data-stu-id="1e0af-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1e0af-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1e0af-124">Notes to callers</span></span>

<span data-ttu-id="1e0af-125">Rufen Sie **ReadReceipt** , wenn die Eigenschaft **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) festgelegt ist und eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="1e0af-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="1e0af-126">Die Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="1e0af-126">The message has been read.</span></span>
    
- <span data-ttu-id="1e0af-127">Die Nachricht wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="1e0af-127">The message has been moved.</span></span>
    
- <span data-ttu-id="1e0af-128">Die Nachricht wurde kopiert.</span><span class="sxs-lookup"><span data-stu-id="1e0af-128">The message has been copied.</span></span>
    
- <span data-ttu-id="1e0af-129">Die Nachricht [IMessage::SetReadFlag](imessage-setreadflag.md) -Methode wurde aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e0af-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="1e0af-130">Rufen Sie **ReadReceipt** nicht auf, wenn eine Nachricht gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1e0af-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="1e0af-131">Ein Lese- oder nonread Bericht soll nur einmal für eine Nachricht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e0af-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="1e0af-132">Verfolgen einer Nachricht gelesen-Status und nicht senden Sie mehrere Berichte für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1e0af-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="1e0af-133">Wenn der Parameter _LppEmptyMessage_ mit einer gültigen Bericht Meldung zeigt MAPI aus **ReadReceipt**gibt, rufen Sie die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode zum Senden der Nachricht und klicken Sie dann den Zeiger durch Aufrufen der **IUnknown:s:Release-Version **Methode.</span><span class="sxs-lookup"><span data-stu-id="1e0af-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="1e0af-134">Wenn **ReadReceipt** ein Fehler auftritt, sollten die Nachricht freigegeben werden, ohne gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e0af-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="1e0af-135">Wenn Sie die Nachricht gelesen-Status gespeichert werden sollen, können Sie versuchen, den Lese- oder nonread Bericht zu einem späteren Zeitpunkt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1e0af-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="1e0af-136">Sie können entweder aus- oder Einblenden von Lese- und nonread Berichte vom Speicher in Ihrem Ordner generiert.</span><span class="sxs-lookup"><span data-stu-id="1e0af-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="1e0af-137">Speichern von Lese- und nonread Berichten in verborgenen Ordnern können Sie eine engere Sicherheit zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="1e0af-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1e0af-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e0af-138">See also</span></span>



[<span data-ttu-id="1e0af-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="1e0af-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="1e0af-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="1e0af-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="1e0af-141">PidTagReadReceiptRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1e0af-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="1e0af-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e0af-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

