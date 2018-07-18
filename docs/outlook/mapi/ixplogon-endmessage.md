---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f81a0c3c9a9ad0a9bcef5c5685aa5b343237f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792868"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="7225b-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="7225b-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="7225b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7225b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7225b-105">Der Transportdienst informiert werden, dass die MAPI-Warteschlange die Verarbeitung für eine ausgehende Nachricht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7225b-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7225b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7225b-106">Parameters</span></span>

 <span data-ttu-id="7225b-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="7225b-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="7225b-108">[in] Ein Message-spezifische-Verweiswert, der in einem früheren Aufruf der [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) -Methode abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7225b-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="7225b-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="7225b-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="7225b-110">[out] Eine Bitmaske aus Flags, die an die Warteschlange MAPI gibt an, was mit der Nachricht Verfahren werden soll.</span><span class="sxs-lookup"><span data-stu-id="7225b-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="7225b-111">Wenn keine Flags festgelegt sind, hat die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7225b-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="7225b-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7225b-112">The following flags can be set:</span></span>
    
<span data-ttu-id="7225b-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="7225b-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="7225b-114">Der Transportdienst verfügt über alle Informationen, die über diese Meldung für jetzt benötigt.</span><span class="sxs-lookup"><span data-stu-id="7225b-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="7225b-115">Wenn der Adressbuchhierarchie Weitere Informationen erforderlich sind, oder wenn sie die Nachricht gesendet hat, benachrichtigt die MAPI-Warteschlange, die [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode mit dem NOTIFY_SENTDEFERRED-Flag und durch Übergeben der Eintrags-ID der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7225b-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="7225b-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="7225b-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="7225b-117">Der Transportdienst sendet die Nachricht nicht an der aktuellen Zeit Gründen, die nicht fehlerbedingungen sind.</span><span class="sxs-lookup"><span data-stu-id="7225b-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="7225b-118">Der Transportdienst sollte erneut zum Senden der Nachricht höher aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7225b-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="7225b-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="7225b-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="7225b-120">Der Transportdienst muss neu gestartet werden die Nachricht in einem Aufruf der [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="7225b-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7225b-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7225b-121">Return value</span></span>

<span data-ttu-id="7225b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="7225b-122">S_OK</span></span> 
  
> <span data-ttu-id="7225b-123">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7225b-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7225b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7225b-124">Remarks</span></span>

<span data-ttu-id="7225b-125">Die MAPI-Warteschlange Ruft die **IXPLogon::EndMessage** -Methode nach dem Abschluss der Verarbeitung von erweiterten Übermittlung oder Nondelivery Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7225b-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="7225b-126">Nachdem dieser Aufruf zurückgegeben wird, ist der Wert in der _UlMsgRef_ -Parameter nicht mehr gültig für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7225b-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="7225b-127">Der Transportdienst kann den gleichen Wert auf eine zukünftige Nachricht wiederverwenden.</span><span class="sxs-lookup"><span data-stu-id="7225b-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="7225b-128">Alle Objekte, die der Adressbuchhierarchie während der Übertragung einer Nachricht öffnet sollten vor der **EndMessage** Rückgabe, mit Ausnahme von Message-Objekts freigegeben werden, die die MAPI-Warteschlange an der Adressbuchhierarchie übergibt.</span><span class="sxs-lookup"><span data-stu-id="7225b-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="7225b-129">Die MAPI-Warteschlange übergebener Message-Objekts ist nach dem Aufruf der **EndMessage** ungültig.</span><span class="sxs-lookup"><span data-stu-id="7225b-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7225b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7225b-130">See also</span></span>



[<span data-ttu-id="7225b-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="7225b-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="7225b-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="7225b-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="7225b-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="7225b-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="7225b-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7225b-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

