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
# <a name="ixplogonflushqueues"></a><span data-ttu-id="6c624-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="6c624-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="6c624-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c624-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c624-105">Fordert, dass der Transportanbieter alle ausstehenden eingehenden oder ausgehenden Nachrichten sofort bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6c624-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6c624-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c624-106">Parameters</span></span>

 <span data-ttu-id="6c624-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6c624-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="6c624-108">in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.</span><span class="sxs-lookup"><span data-stu-id="6c624-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="6c624-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="6c624-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="6c624-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="6c624-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6c624-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="6c624-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="6c624-112">in Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6c624-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="6c624-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c624-113">_ulFlags_</span></span>
  
> <span data-ttu-id="6c624-114">in Eine Bitmaske von Flags, die steuert, wie die Nachrichten Warteschlangen Spülung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c624-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="6c624-115">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6c624-115">The following flags can be set:</span></span>
    
<span data-ttu-id="6c624-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="6c624-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="6c624-117">Die Warteschlange für eingehende Nachrichten oder Warteschlangen sollte geleert werden.</span><span class="sxs-lookup"><span data-stu-id="6c624-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="6c624-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="6c624-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="6c624-119">Der Transportanbieter sollte diese Anforderung, wenn möglich, verarbeiten, auch wenn dies zeitaufwändig ist.</span><span class="sxs-lookup"><span data-stu-id="6c624-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="6c624-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="6c624-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="6c624-121">Der Transportanbieter sollte keine Benutzeroberfläche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6c624-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="6c624-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="6c624-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="6c624-123">Die Warteschlange für ausgehende Nachrichten oder Warteschlangen sollte geleert werden.</span><span class="sxs-lookup"><span data-stu-id="6c624-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c624-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c624-124">Return value</span></span>

<span data-ttu-id="6c624-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c624-125">S_OK</span></span> 
  
> <span data-ttu-id="6c624-126">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c624-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c624-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c624-127">Remarks</span></span>

<span data-ttu-id="6c624-128">Der MAPI-Spooler Ruft die **IXPLogon:: FlushQueues** -Methode auf, um dem Transportanbieter zu raten, dass der MAPI-Spooler mit der Verarbeitung von Nachrichten beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="6c624-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="6c624-129">Der Transportanbieter sollte die [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode aufrufen, um ein entsprechendes Bit für seinen Status in der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft der Status Zeile festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6c624-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="6c624-130">Nach dem Aktualisieren der Statuszeile sollte der Transportanbieter S_OK für den **FlushQueues** -Aufruf zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6c624-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="6c624-131">Der MAPI-Spooler startet dann das Senden von Nachrichten, wobei der Vorgang synchron mit dem MAPI-Spooler ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c624-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="6c624-132">Zur Unterstützung der Implementierung der [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) -Methode ruft der MAPI-Spooler **IXPLogon:: FlushQueues** für alle Anmeldeobjekte für aktive Transportanbieter auf, die in einer Profil Sitzung laufen.</span><span class="sxs-lookup"><span data-stu-id="6c624-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="6c624-133">Wenn die **FlushQueues** -Methode eines Transportanbieters als Ergebnis eines Client Anwendungsaufrufs an **IMAPIStatus:: FlushQueues**aufgerufen wird, wird die Nachrichtenverarbeitung asynchron für den Client ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c624-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6c624-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c624-134">See also</span></span>



[<span data-ttu-id="6c624-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="6c624-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="6c624-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c624-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

