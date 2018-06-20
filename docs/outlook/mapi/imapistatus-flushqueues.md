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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d6c221ae307edb9d84cfcc0026660ea4bce7fadd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792336"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="3e1db-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="3e1db-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="3e1db-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3e1db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3e1db-105">Erzwingt, dass alle Nachrichten gesendet oder empfangen, um sofort hoch- oder heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="3e1db-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="3e1db-106">Die MAPI-Warteschlange Statusobjekt und die Status-Objekte, mit denen Transportanbieter implementiert unterstützt diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3e1db-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3e1db-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e1db-107">Parameters</span></span>

 <span data-ttu-id="3e1db-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3e1db-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="3e1db-109">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3e1db-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="3e1db-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="3e1db-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="3e1db-111">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpTargetTransport_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="3e1db-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="3e1db-112">Der Parameter _CbTargetTransport_ wird nur für Anrufe an die MAPI-Warteschlange Status-Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3e1db-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="3e1db-113">Für Anrufe eines Transportdienstes ist der Parameter _CbTargetTransport_ auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3e1db-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="3e1db-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="3e1db-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="3e1db-115">[in] Ein Zeiger auf die Eintrags-ID des Anbieters Transport, der seine Nachrichtenwarteschlangen zu leeren.</span><span class="sxs-lookup"><span data-stu-id="3e1db-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="3e1db-116">Der Parameter _LpTargetTransport_ wird nur für Anrufe an die MAPI-Warteschlange Status-Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3e1db-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="3e1db-117">Für Anrufe eines Transportdienstes ist der _LpTargetTransport_ -Parameter auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3e1db-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="3e1db-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3e1db-118">_ulFlags_</span></span>
  
> <span data-ttu-id="3e1db-119">[in] Eine Bitmaske aus Flags, die die Schreibvorgang wurde steuert.</span><span class="sxs-lookup"><span data-stu-id="3e1db-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="3e1db-120">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3e1db-120">The following flags can be set:</span></span>
    
<span data-ttu-id="3e1db-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="3e1db-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="3e1db-122">Flush-Vorgang kann asynchron auftreten.</span><span class="sxs-lookup"><span data-stu-id="3e1db-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="3e1db-123">Dieser Parameter gilt nur für die MAPI-Warteschlange Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3e1db-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="3e1db-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="3e1db-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="3e1db-125">Die eingehende Nachrichtenwarteschlangen sollten entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3e1db-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="3e1db-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="3e1db-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="3e1db-127">Der Schreibvorgang wurde sollte unabhängig davon, obwohl die Wahrscheinlichkeit, dass eine Beeinträchtigung der Systemleistung auftreten.</span><span class="sxs-lookup"><span data-stu-id="3e1db-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="3e1db-128">Dieses Kennzeichen müssen festgelegt werden, wenn eine asynchrone Adressbuchhierarchie gerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="3e1db-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="3e1db-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="3e1db-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="3e1db-130">Das Statusobjekt sollte eine Statusanzeige nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3e1db-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="3e1db-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="3e1db-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="3e1db-132">Ausgehende Nachrichtenwarteschlangen sollten entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3e1db-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3e1db-133">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3e1db-133">Return value</span></span>

<span data-ttu-id="3e1db-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e1db-134">S_OK</span></span> 
  
> <span data-ttu-id="3e1db-135">Der Schreibvorgang wurde erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3e1db-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="3e1db-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="3e1db-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="3e1db-137">Ein anderer Vorgang ist in Bearbeitung. Es dürfen für die Durchführung, oder er angehalten werden sollte, bevor Sie diesen Vorgang initiiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3e1db-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="3e1db-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3e1db-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3e1db-139">Das Statusobjekt unterstützt keine dieser Vorgang, wie durch die Abwesenheit des STATUS_FLUSH_QUEUES-Flags in den Status des Objekts **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="3e1db-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e1db-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3e1db-140">Remarks</span></span>

<span data-ttu-id="3e1db-141">Die Methode **IMAPIStatus::FlushQueues** fordert an, dass die MAPI-Warteschlange oder eines Transportdienstes sofort alle Nachrichten in der Warteschlange für ausgehende Nachrichten senden oder empfangen alle aus der Warteschlange für eingehende.</span><span class="sxs-lookup"><span data-stu-id="3e1db-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="3e1db-142">**FlushQueues** ist nur durch das MAPI-Warteschlange Status-Objekt und von Status-Objekten, die transport-Anbieter Kooperation implementiert.</span><span class="sxs-lookup"><span data-stu-id="3e1db-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="3e1db-143">MAPI_E_BUSY sollten für asynchrone Anfragen zurückgegeben werden, damit Clients Arbeit fortgesetzt werden können.</span><span class="sxs-lookup"><span data-stu-id="3e1db-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="3e1db-144">Standardmäßig ist **FlushQueues** eine synchrone Operation. Steuerelement gibt keine an den Anrufer zurück, bis der Löschvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3e1db-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="3e1db-145">Nur der flush durch die MAPI-Warteschlange ausgeführte Vorgang kann asynchrone sein. Clients fordern dieses Verhalten, indem Sie das FLUSH_ASYNC_OK-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="3e1db-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3e1db-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="3e1db-146">Notes to implementers</span></span>

<span data-ttu-id="3e1db-147">Implementierung eines remote-Transport-Anbieters von **FlushQueues** legt Bits in der Eigenschaft **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) in das Anmeldeobjekt Statuszeile steuern, wie Warteschlangen geleert werden.</span><span class="sxs-lookup"><span data-stu-id="3e1db-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="3e1db-148">Wenn Sie ein remote-Viewer das Flag FLUSH_UPLOAD übergibt, sollte die **FlushQueues** -Methode die Bits STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE festlegen.</span><span class="sxs-lookup"><span data-stu-id="3e1db-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="3e1db-149">Wenn Sie ein remote-Viewer das Flag FLUSH_DOWNLOAD übergibt, sollte die **FlushQueues** -Methode die Bits STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE festlegen.</span><span class="sxs-lookup"><span data-stu-id="3e1db-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="3e1db-150">**FlushQueues** sollte dann S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e1db-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="3e1db-151">Die MAPI-Warteschlange initiieren Sie dann die entsprechenden Aktionen zum Hoch- und Herunterladen von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="3e1db-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3e1db-152">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3e1db-152">Notes to callers</span></span>

<span data-ttu-id="3e1db-153">Ein Anruf an das MAPI-Warteschlange Status-Objekt ist eine Richtlinie auf alle Nachrichten oder von der entsprechenden Adressbuchhierarchie übertragen.</span><span class="sxs-lookup"><span data-stu-id="3e1db-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="3e1db-154">Wenn Sie eine einzelne Adressbuchhierarchie Status-Objekts aufrufen, sind nur die Nachrichten für diesen Anbieter betroffen.</span><span class="sxs-lookup"><span data-stu-id="3e1db-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e1db-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e1db-155">See also</span></span>



[<span data-ttu-id="3e1db-156">Kanonische PidTagResourceMethods-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3e1db-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="3e1db-157">Kanonische PidTagStatusCode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3e1db-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="3e1db-158">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3e1db-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

