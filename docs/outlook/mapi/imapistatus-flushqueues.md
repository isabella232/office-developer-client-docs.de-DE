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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328194"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="33cb3-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="33cb3-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="33cb3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33cb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33cb3-105">ErZwingt, dass alle Nachrichten, die darauf warten, gesendet oder empfangen werden, sofort hochgeladen oder heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="33cb3-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="33cb3-106">Das MAPI-Spooler-Statusobjekt und die Statusobjekte, die von Transportanbietern implementiert werden, unterstützen diese Methode.</span><span class="sxs-lookup"><span data-stu-id="33cb3-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="33cb3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="33cb3-107">Parameters</span></span>

 <span data-ttu-id="33cb3-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="33cb3-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="33cb3-109">in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.</span><span class="sxs-lookup"><span data-stu-id="33cb3-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="33cb3-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="33cb3-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="33cb3-111">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpTargetTransport_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="33cb3-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="33cb3-112">Der _cbTargetTransport_ -Parameter wird nur bei Aufrufen des Status-Objekts des MAPI-Spoolers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="33cb3-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="33cb3-113">Bei Aufrufen eines Transportanbieters wird der Parameter _cbTargetTransport_ auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="33cb3-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="33cb3-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="33cb3-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="33cb3-115">in Ein Zeiger auf die Eintrags-ID des Transportanbieters, der die Nachrichtenwarteschlangen leeren soll.</span><span class="sxs-lookup"><span data-stu-id="33cb3-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="33cb3-116">Der _lpTargetTransport_ -Parameter wird nur bei Aufrufen des Status-Objekts des MAPI-Spoolers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="33cb3-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="33cb3-117">Bei Aufrufen eines Transportanbieters wird der Parameter _lpTargetTransport_ auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="33cb3-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="33cb3-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="33cb3-118">_ulFlags_</span></span>
  
> <span data-ttu-id="33cb3-119">in Eine Bitmaske von Flags, die den Flush-Vorgang steuert.</span><span class="sxs-lookup"><span data-stu-id="33cb3-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="33cb3-120">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="33cb3-120">The following flags can be set:</span></span>
    
<span data-ttu-id="33cb3-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="33cb3-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="33cb3-122">Der Flush-Vorgang kann asynchron ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="33cb3-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="33cb3-123">Dieses Flag gilt nur für das Statusobjekt des MAPI-Spoolers.</span><span class="sxs-lookup"><span data-stu-id="33cb3-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="33cb3-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="33cb3-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="33cb3-125">Die Warteschlangen für eingehende Nachrichten sollten geleert werden.</span><span class="sxs-lookup"><span data-stu-id="33cb3-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="33cb3-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="33cb3-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="33cb3-127">Der Flush-Vorgang sollte unabhängig von der Wahrscheinlichkeit einer Leistungsminderung auftreten.</span><span class="sxs-lookup"><span data-stu-id="33cb3-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="33cb3-128">Dieses Flag muss festgelegt werden, wenn ein asynchroner Transportanbieter zielgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="33cb3-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="33cb3-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="33cb3-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="33cb3-130">Das Status-Objekt sollte keine Statusanzeige anzeigen.</span><span class="sxs-lookup"><span data-stu-id="33cb3-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="33cb3-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="33cb3-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="33cb3-132">Die Warteschlangen für ausgehende Nachrichten sollten geleert werden.</span><span class="sxs-lookup"><span data-stu-id="33cb3-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="33cb3-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33cb3-133">Return value</span></span>

<span data-ttu-id="33cb3-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="33cb3-134">S_OK</span></span> 
  
> <span data-ttu-id="33cb3-135">Der Flush-Vorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="33cb3-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="33cb3-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="33cb3-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="33cb3-137">Ein anderer Vorgang wird ausgeführt; Es sollte zugelassen werden, oder es sollte beendet werden, bevor dieser Vorgang eingeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="33cb3-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="33cb3-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="33cb3-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="33cb3-139">Das Status-Objekt unterstützt diesen Vorgang nicht, wie durch das Fehlen des STATUS_FLUSH_QUEUES-Flags in der **PR_RESOURCE_METHODS** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))-Eigenschaft des Status-Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="33cb3-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33cb3-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33cb3-140">Remarks</span></span>

<span data-ttu-id="33cb3-141">Die **IMAPIStatus:: FlushQueues** -Methode fordert, dass der MAPI-Spooler oder ein Transportanbieter sofort alle Nachrichten in der ausgehenden Warteschlange sendet oder alle Nachrichten von der eingehenden Warteschlange empfängt.</span><span class="sxs-lookup"><span data-stu-id="33cb3-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="33cb3-142">**FlushQueues** wird nur vom MAPI-Spooler-Statusobjekt und von Statusobjekten implementiert, die von den Transportanbietern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="33cb3-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="33cb3-143">MAPI_E_BUSY sollte für asynchrone Anforderungen zurückgegeben werden, damit Clients weiterhin arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="33cb3-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="33cb3-144">Standardmäßig ist **FlushQueues** eine synchrone Operation; die Steuerung kehrt erst dann zum Aufrufer zurück, wenn der Flush abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="33cb3-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="33cb3-145">Nur der Flush-Vorgang, der vom MAPI-Spooler ausgeführt wird, kann asynchron sein; Clients fordern dieses Verhalten, indem Sie das FLUSH_ASYNC_OK-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="33cb3-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="33cb3-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="33cb3-146">Notes to implementers</span></span>

<span data-ttu-id="33cb3-147">Die Implementierung eines Remote Transportanbieters von **FlushQueues** legt Bits in der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft in der Status Zeile des LOGON-Objekts fest, um zu steuern, wie Warteschlangen geleert werden.</span><span class="sxs-lookup"><span data-stu-id="33cb3-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="33cb3-148">Wenn ein Remote Viewer das FLUSH_UPLOAD-Flag übergibt, sollte die **FlushQueues** -Methode die Bits STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE festlegen.</span><span class="sxs-lookup"><span data-stu-id="33cb3-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="33cb3-149">Wenn ein Remote Viewer das FLUSH_DOWNLOAD-Flag übergibt, sollte die **FlushQueues** -Methode die Bits STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE festlegen.</span><span class="sxs-lookup"><span data-stu-id="33cb3-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="33cb3-150">**FlushQueues** sollte dann S_OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="33cb3-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="33cb3-151">Der MAPI-Spooler startet dann die entsprechenden Aktionen, um Nachrichten hoch-und herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="33cb3-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="33cb3-152">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="33cb3-152">Notes to callers</span></span>

<span data-ttu-id="33cb3-153">Ein Aufruf des MAPI-Spooler-Status Objekts ist eine Direktive, mit der alle Nachrichten an den oder vom entsprechenden Transportanbieter übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="33cb3-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="33cb3-154">Wenn Sie das Status-Objekt eines einzelnen Transportanbieters aufrufen, sind nur die Nachrichten für diesen Anbieter betroffen.</span><span class="sxs-lookup"><span data-stu-id="33cb3-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33cb3-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33cb3-155">See also</span></span>



[<span data-ttu-id="33cb3-156">Kanonische Pidtagresourcemethods (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33cb3-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="33cb3-157">Kanonische Pidtagstatuscode (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33cb3-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="33cb3-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="33cb3-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

