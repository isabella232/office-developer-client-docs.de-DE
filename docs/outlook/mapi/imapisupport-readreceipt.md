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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326306"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="7afdc-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="7afdc-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="7afdc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7afdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7afdc-105">Generiert einen Lese-oder nicht gelesenen Bericht für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7afdc-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="7afdc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7afdc-106">Parameters</span></span>

 <span data-ttu-id="7afdc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7afdc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7afdc-108">in Eine Bitmaske von Flags, die die Generierung des Lese-oder nonread-Berichts steuert.</span><span class="sxs-lookup"><span data-stu-id="7afdc-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="7afdc-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7afdc-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7afdc-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="7afdc-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="7afdc-111">Ein ungelesener Bericht wird generiert.</span><span class="sxs-lookup"><span data-stu-id="7afdc-111">A nonread report is generated.</span></span> <span data-ttu-id="7afdc-112">Wenn MAPI_NON_READ nicht festgelegt ist, wird ein Lesebericht generiert.</span><span class="sxs-lookup"><span data-stu-id="7afdc-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="7afdc-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="7afdc-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="7afdc-114">in Ein Zeiger auf die Nachricht, über die der Bericht generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7afdc-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="7afdc-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="7afdc-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="7afdc-116">[in, out] Bei der Eingabe zeigt _lppEmptyMessage_ auf einen Zeiger auf eine leere Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7afdc-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="7afdc-117">Bei der Ausgabe zeigt _lppEmptyMessage_ auf einen Zeiger auf die Bericht Meldung.</span><span class="sxs-lookup"><span data-stu-id="7afdc-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7afdc-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7afdc-118">Return value</span></span>

<span data-ttu-id="7afdc-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7afdc-119">S_OK</span></span> 
  
> <span data-ttu-id="7afdc-120">Der Bericht wurde erfolgreich generiert.</span><span class="sxs-lookup"><span data-stu-id="7afdc-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7afdc-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7afdc-121">Remarks</span></span>

<span data-ttu-id="7afdc-122">Die **IMAPISupport:: ReadReceipt** -Methode wird nur für Support Objekte des Nachrichtenspeicher Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="7afdc-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="7afdc-123">Nachrichtenspeicher Anbieter rufen **ReadReceipt** auf, um MAPI anzuweisen, einen Lese-oder nicht gelesenen Bericht für die Nachricht zu generieren, auf die durch den _lpReadMessage_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7afdc-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7afdc-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7afdc-124">Notes to callers</span></span>

<span data-ttu-id="7afdc-125">Rufen Sie **ReadReceipt** auf, wenn die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft festgelegt ist und eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7afdc-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="7afdc-126">Die Nachricht wurde gelesen.</span><span class="sxs-lookup"><span data-stu-id="7afdc-126">The message has been read.</span></span>
    
- <span data-ttu-id="7afdc-127">Die Nachricht wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="7afdc-127">The message has been moved.</span></span>
    
- <span data-ttu-id="7afdc-128">Die Nachricht wurde kopiert.</span><span class="sxs-lookup"><span data-stu-id="7afdc-128">The message has been copied.</span></span>
    
- <span data-ttu-id="7afdc-129">Die [IMessage:: SetReadFlag](imessage-setreadflag.md) -Methode der Nachricht wurde aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7afdc-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="7afdc-130">Rufen Sie **ReadReceipt** nicht auf, wenn eine Nachricht gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7afdc-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="7afdc-131">Ein Lese-oder ungelesener Bericht sollte nur einmal für eine Nachricht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7afdc-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="7afdc-132">Verfolgen Sie den Lesestatus einer Nachricht, und senden Sie nicht mehrere Berichte für eine einzelne Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7afdc-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="7afdc-133">Wenn der _lppEmptyMessage_ -Parameter auf eine gültige Bericht Meldung zeigt, wenn MAPI von **ReadReceipt**zurückgegeben wird, rufen Sie die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf, um die Nachricht zu senden, und lassen Sie den Zeiger dann durch Aufrufen des \*\*IUnknown: s: Release \*\*-Methode.</span><span class="sxs-lookup"><span data-stu-id="7afdc-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="7afdc-134">Wenn **ReadReceipt** fehlschlägt, sollte die Nachricht ohne übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="7afdc-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="7afdc-135">Wenn Sie den Lesestatus der Nachricht speichern, können Sie versuchen, den Lese-oder nonread-Bericht zu einem späteren Zeitpunkt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7afdc-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="7afdc-136">Sie können Lese-und nonread-Berichte, die von Speichern in Ihren Ordnern generiert wurden, entweder ausblenden oder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7afdc-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="7afdc-137">Durch das Speichern von Lese-und nonread-Berichten in ausgeblendeten Ordnern können Sie eine engere Sicherheit implementieren.</span><span class="sxs-lookup"><span data-stu-id="7afdc-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7afdc-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7afdc-138">See also</span></span>



[<span data-ttu-id="7afdc-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="7afdc-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="7afdc-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="7afdc-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="7afdc-141">Kanonische Pidtagreadreceiptrequested (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7afdc-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="7afdc-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7afdc-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

