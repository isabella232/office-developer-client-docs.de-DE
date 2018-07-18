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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 116e3cfaace9c0965001021575b76ec371667877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792877"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="7ffc8-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="7ffc8-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="7ffc8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ffc8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ffc8-105">Fordert, dass der Adressbuchhierarchie sofort alle ausstehende eingehende oder ausgehende Nachrichten übermitteln.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7ffc8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ffc8-106">Parameters</span></span>

 <span data-ttu-id="7ffc8-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7ffc8-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="7ffc8-108">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="7ffc8-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="7ffc8-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="7ffc8-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7ffc8-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="7ffc8-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="7ffc8-112">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="7ffc8-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ffc8-113">_ulFlags_</span></span>
  
> <span data-ttu-id="7ffc8-114">[in] Eine Bitmaske aus Flags, die steuert, wie Nachrichten die Warteschlange das leeren erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="7ffc8-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7ffc8-115">The following flags can be set:</span></span>
    
<span data-ttu-id="7ffc8-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="7ffc8-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="7ffc8-117">Die Warteschlange für eingehende Nachrichten oder Warteschlangen geleert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="7ffc8-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="7ffc8-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="7ffc8-119">Der Adressbuchhierarchie sollte Verarbeiten dieser Anforderung, wenn möglich, auch wenn dies also Zeit in Anspruch nehmen ist.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="7ffc8-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="7ffc8-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="7ffc8-121">Der Transportdienst keine Benutzeroberfläche angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="7ffc8-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="7ffc8-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="7ffc8-123">Die Warteschlange für ausgehende Nachrichten oder Warteschlangen geleert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ffc8-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7ffc8-124">Return value</span></span>

<span data-ttu-id="7ffc8-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ffc8-125">S_OK</span></span> 
  
> <span data-ttu-id="7ffc8-126">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ffc8-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ffc8-127">Remarks</span></span>

<span data-ttu-id="7ffc8-128">Die MAPI-Warteschlange Ruft die **IXPLogon::FlushQueues** -Methode, um der Adressbuchhierarchie darauf hinzuweisen, dass die MAPI-Warteschlange ist dabei, die Verarbeitung von Nachrichten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="7ffc8-129">Der Transportdienst sollte die [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode zum Festlegen einer entsprechenden Bit für den Zustand in die **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))-Eigenschaft des seine Statuszeile aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="7ffc8-130">Nach dem Aktualisieren der Statuszeile, sollte der Adressbuchhierarchie für den Anruf **FlushQueues** S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="7ffc8-131">Die MAPI-Warteschlange startet das Senden von Nachrichten, mit dem Vorgang synchron an die Warteschlange MAPI.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="7ffc8-132">Unterstützung der Implementierung der [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) -Methode ruft die MAPI-Warteschlange **IXPLogon::FlushQueues** für alle Objekte, Anmeldung für aktiven Transport-Anbieter, die in einer Sitzung Profil ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="7ffc8-133">Wenn als Ergebnis einer Client-Anwendung **IMAPIStatus::FlushQueues**Aufruf eines Transportdienstes **FlushQueues** -Methode aufgerufen wird, tritt die Verarbeitung von Nachrichten asynchron an den Client.</span><span class="sxs-lookup"><span data-stu-id="7ffc8-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ffc8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ffc8-134">See also</span></span>



[<span data-ttu-id="7ffc8-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="7ffc8-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="7ffc8-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ffc8-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

