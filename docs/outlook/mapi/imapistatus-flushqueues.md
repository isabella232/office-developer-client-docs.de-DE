---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432604"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="05e4f-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="05e4f-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="05e4f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05e4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05e4f-105">Erzwingt, dass alle Nachrichten, die auf das Senden oder Empfangen warten, sofort hochgeladen oder heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="05e4f-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="05e4f-106">Das MAPI-Spoolerstatusobjekt und die Statusobjekte, die von Transportanbietern implementiert werden, unterstützen diese Methode.</span><span class="sxs-lookup"><span data-stu-id="05e4f-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="05e4f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="05e4f-107">Parameters</span></span>

 <span data-ttu-id="05e4f-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="05e4f-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="05e4f-109">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="05e4f-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="05e4f-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="05e4f-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="05e4f-111">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpTargetTransport-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="05e4f-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="05e4f-112">Der  _cbTargetTransport-Parameter_ wird nur für Aufrufe des Statusobjekts des MAPI-Spoolers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="05e4f-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="05e4f-113">Für Anrufe an einen Transportanbieter ist  _der cbTargetTransport-Parameter_ auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="05e4f-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="05e4f-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="05e4f-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="05e4f-115">[in] Ein Zeiger auf die Eintrags-ID des Transportanbieters, der seine Nachrichtenwarteschlangen leeren soll.</span><span class="sxs-lookup"><span data-stu-id="05e4f-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="05e4f-116">Der  _lpTargetTransport-Parameter_ wird nur für Aufrufe des Statusobjekts des MAPI-Spoolers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="05e4f-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="05e4f-117">Für Anrufe an einen Transportanbieter ist  _der lpTargetTransport-Parameter_ auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="05e4f-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="05e4f-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05e4f-118">_ulFlags_</span></span>
  
> <span data-ttu-id="05e4f-119">[in] Eine Bitmaske mit Flags, die den Leerungsvorgang steuert.</span><span class="sxs-lookup"><span data-stu-id="05e4f-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="05e4f-120">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="05e4f-120">The following flags can be set:</span></span>
    
<span data-ttu-id="05e4f-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="05e4f-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="05e4f-122">Der Leerungsvorgang kann asynchron erfolgen.</span><span class="sxs-lookup"><span data-stu-id="05e4f-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="05e4f-123">Dieses Flag gilt nur für das Statusobjekt des MAPI-Spoolers.</span><span class="sxs-lookup"><span data-stu-id="05e4f-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="05e4f-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="05e4f-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="05e4f-125">Die Warteschlangen für eingehende Nachrichten sollten geleert werden.</span><span class="sxs-lookup"><span data-stu-id="05e4f-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="05e4f-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="05e4f-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="05e4f-127">Der Leerungsvorgang sollte unabhängig von der Wahrscheinlichkeit eines Leistungsrückgangs erfolgen.</span><span class="sxs-lookup"><span data-stu-id="05e4f-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="05e4f-128">Dieses Flag muss festgelegt werden, wenn ein asynchroner Transportanbieter als Ziel festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="05e4f-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="05e4f-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="05e4f-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="05e4f-130">Das Statusobjekt sollte keine Statusanzeige anzeigen.</span><span class="sxs-lookup"><span data-stu-id="05e4f-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="05e4f-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="05e4f-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="05e4f-132">Die Warteschlangen für ausgehende Nachrichten sollten geleert werden.</span><span class="sxs-lookup"><span data-stu-id="05e4f-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05e4f-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05e4f-133">Return value</span></span>

<span data-ttu-id="05e4f-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="05e4f-134">S_OK</span></span> 
  
> <span data-ttu-id="05e4f-135">Der Leerungsvorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="05e4f-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="05e4f-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="05e4f-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="05e4f-137">Ein weiterer Vorgang wird ausgeführt. Er sollte abgeschlossen oder beendet werden dürfen, bevor dieser Vorgang initiiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="05e4f-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="05e4f-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="05e4f-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="05e4f-139">Das status-Objekt unterstützt diesen Vorgang nicht, wie durch das Fehlen des STATUS_FLUSH_QUEUES-Flag in der **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft des Statusobjekts angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="05e4f-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05e4f-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05e4f-140">Remarks</span></span>

<span data-ttu-id="05e4f-141">Die **IMAPIStatus::FlushQueues-Methode** fordert an, dass der MAPI-Spooler oder ein Transportanbieter sofort alle Nachrichten in der ausgehenden Warteschlange senden oder alle Nachrichten aus der eingehenden Warteschlange empfangen.</span><span class="sxs-lookup"><span data-stu-id="05e4f-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="05e4f-142">**FlushQueues** wird nur vom MAPI-Spoolerstatusobjekt und von Statusobjekten implementiert, die von Transportanbietern zur Bereitstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05e4f-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="05e4f-143">MAPI_E_BUSY sollte für asynchrone Anforderungen zurückgegeben werden, damit Clients ihre Arbeit fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="05e4f-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="05e4f-144">**FlushQueues** ist standardmäßig ein synchroner Vorgang. das Steuerelement wird erst wieder an den Anrufer zurück, wenn die Leerung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="05e4f-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="05e4f-145">Nur der vom #A0 ausgeführte Leervorgang kann asynchron sein. Clients fordern dieses Verhalten an, indem sie FLUSH_ASYNC_OK festlegen.</span><span class="sxs-lookup"><span data-stu-id="05e4f-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="05e4f-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="05e4f-146">Notes to implementers</span></span>

<span data-ttu-id="05e4f-147">Die Implementierung von **FlushQueues** durch einen Remotetransportanbieter legt Bits in der **eigenschaft PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) in der Statuszeile des Anmeldeobjekts fest, um zu steuern, wie Warteschlangen geleert werden.</span><span class="sxs-lookup"><span data-stu-id="05e4f-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="05e4f-148">Wenn ein Remoteanzeiger das FLUSH_UPLOAD übergibt, sollte die **FlushQueues-Methode** die STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE festlegen.</span><span class="sxs-lookup"><span data-stu-id="05e4f-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="05e4f-149">Wenn ein Remoteanzeiger das FLUSH_DOWNLOAD übergibt, sollte die **FlushQueues-Methode** die STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE festlegen.</span><span class="sxs-lookup"><span data-stu-id="05e4f-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="05e4f-150">**FlushQueues** sollte dann eine S_OK.</span><span class="sxs-lookup"><span data-stu-id="05e4f-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="05e4f-151">Der MAPI-Spooler initiiert dann die entsprechenden Aktionen zum Hochladen und Herunterladen von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="05e4f-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="05e4f-152">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="05e4f-152">Notes to callers</span></span>

<span data-ttu-id="05e4f-153">Ein Aufruf des MAPI-Spoolerstatusobjekts ist eine Direktive zum Übertragen aller Nachrichten an oder vom entsprechenden Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="05e4f-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="05e4f-154">Wenn Sie das Statusobjekt eines einzelnen Transportanbieters aufrufen, sind nur die Nachrichten für den jeweiligen Anbieter betroffen.</span><span class="sxs-lookup"><span data-stu-id="05e4f-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05e4f-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05e4f-155">See also</span></span>



[<span data-ttu-id="05e4f-156">PidTagResourceMethods (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="05e4f-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="05e4f-157">PidTagStatusCode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="05e4f-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="05e4f-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="05e4f-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

