---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421970"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="d7692-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="d7692-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="d7692-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7692-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7692-105">Fordert an, dass der Transportanbieter sofort alle ausstehenden eingehenden oder ausgehenden Nachrichten zuliefert.</span><span class="sxs-lookup"><span data-stu-id="d7692-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d7692-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7692-106">Parameters</span></span>

 <span data-ttu-id="d7692-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d7692-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d7692-108">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d7692-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="d7692-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="d7692-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="d7692-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="d7692-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d7692-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="d7692-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="d7692-112">[in] Reserviert; muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d7692-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="d7692-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7692-113">_ulFlags_</span></span>
  
> <span data-ttu-id="d7692-114">[in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenwarteschlange geleert wird.</span><span class="sxs-lookup"><span data-stu-id="d7692-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="d7692-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d7692-115">The following flags can be set:</span></span>
    
<span data-ttu-id="d7692-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="d7692-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="d7692-117">Die Eingehende Nachrichtenwarteschlange oder Warteschlangen sollten geleert werden.</span><span class="sxs-lookup"><span data-stu-id="d7692-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="d7692-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="d7692-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="d7692-119">Der Transportanbieter sollte diese Anforderung nach Möglichkeit verarbeiten, auch wenn dies zeitaufwändig ist.</span><span class="sxs-lookup"><span data-stu-id="d7692-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="d7692-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="d7692-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="d7692-121">Der Transportanbieter sollte keine Benutzeroberfläche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7692-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="d7692-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="d7692-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="d7692-123">Die Warteschlange für ausgehende Nachrichten oder Warteschlangen sollte geleert werden.</span><span class="sxs-lookup"><span data-stu-id="d7692-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7692-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7692-124">Return value</span></span>

<span data-ttu-id="d7692-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7692-125">S_OK</span></span> 
  
> <span data-ttu-id="d7692-126">Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7692-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7692-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7692-127">Remarks</span></span>

<span data-ttu-id="d7692-128">Der MAPI-Spooler ruft die **IXPLogon::FlushQueues-Methode** auf, um den Transportanbieter zu informieren, dass der MAPI-Spooler mit der Verarbeitung von Nachrichten beginnt.</span><span class="sxs-lookup"><span data-stu-id="d7692-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="d7692-129">Der Transportanbieter sollte die [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) aufrufen, um ein geeignetes Bit für den Status in der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))-Eigenschaft der Statuszeile festlegen.</span><span class="sxs-lookup"><span data-stu-id="d7692-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="d7692-130">Nach dem Aktualisieren der Statuszeile sollte der Transportanbieter S_OK **FlushQueues-Aufruf zurückgeben.**</span><span class="sxs-lookup"><span data-stu-id="d7692-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="d7692-131">Der MAPI-Spooler beginnt dann mit dem Senden von Nachrichten, und der Vorgang ist synchron mit dem MAPI-Spooler.</span><span class="sxs-lookup"><span data-stu-id="d7692-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="d7692-132">Zur Unterstützung der Implementierung der [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) ruft der MAPI-Spooler **IXPLogon::FlushQueues** für alle Anmeldeobjekte für aktive Transportanbieter auf, die in einer Profilsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d7692-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="d7692-133">Wenn die **FlushQueues-Methode** eines Transportanbieters als Ergebnis eines Clientanwendungsaufrufs von **IMAPIStatus::FlushQueues** aufgerufen wird, erfolgt die Nachrichtenverarbeitung asynchron für den Client.</span><span class="sxs-lookup"><span data-stu-id="d7692-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7692-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7692-134">See also</span></span>



[<span data-ttu-id="d7692-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="d7692-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="d7692-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7692-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

