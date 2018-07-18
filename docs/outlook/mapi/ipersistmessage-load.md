---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eff192b0d2b5cde51a2909452b19ffe1a47b2c04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792737"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="9b2a5-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="9b2a5-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="9b2a5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b2a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b2a5-105">Lädt das Formular für eine angegebene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9b2a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b2a5-106">Parameters</span></span>

 <span data-ttu-id="9b2a5-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="9b2a5-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="9b2a5-108">[in] Ein Zeiger auf die Website für die Nachricht für das Formular geladen werden.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="9b2a5-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="9b2a5-109">_pMessage_</span></span>
  
> <span data-ttu-id="9b2a5-110">[in] Ein Zeiger auf die Meldung für die das Formular geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="9b2a5-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="9b2a5-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="9b2a5-112">[in] Eine Bitmaske vom Client definiert oder vom Anbieter definiertes Flags, kopiert aus der Nachricht **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft, bereitstellen, die Informationen zum Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="9b2a5-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="9b2a5-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="9b2a5-114">[in] Eine Bitmaske aus Flags, die aus der Nachricht **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft kopiert, die bieten weitere Informationen zum Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b2a5-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9b2a5-115">Return value</span></span>

<span data-ttu-id="9b2a5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b2a5-116">S_OK</span></span> 
  
> <span data-ttu-id="9b2a5-117">Das Formular wurde erfolgreich geladen.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b2a5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b2a5-118">Remarks</span></span>

<span data-ttu-id="9b2a5-119">Formular Viewer rufen Sie die **IPersistMessage::Load** -Methode, um ein Formular für eine vorhandene Nachricht zu laden.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9b2a5-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="9b2a5-120">Notes to implementers</span></span>

 <span data-ttu-id="9b2a5-121">**Load** wird nur aufgerufen, wenn ein Formular in einem der folgenden Zustände wird:</span><span class="sxs-lookup"><span data-stu-id="9b2a5-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="9b2a5-122">Nicht initialisiert</span><span class="sxs-lookup"><span data-stu-id="9b2a5-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="9b2a5-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="9b2a5-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="9b2a5-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="9b2a5-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="9b2a5-125">Wenn ein Formular Viewer **Load** anruft, während das Formular in jedem anderen Zustand befindet, gibt die Methode E_UNEXPECTED zurück.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="9b2a5-126">Wenn Ihr Formular einen Verweis auf eine aktive Nachricht Website als derjenigen, die in **Load**übergeben wird, lassen Sie die ursprüngliche Website, da sie nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="9b2a5-127">Der Zeiger auf die Nachricht-Website und die Nachricht der Parameter _pMessageSite_ und _pMessage_ gespeichert, und rufen beide Objekte [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) Methoden, um ihre Referenzzähler erhöhen.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="9b2a5-128">Nachdem **AddRef** abgeschlossen ist, speichern Sie die Eigenschaften der Parameter _UlMessageStatus_ und _UlMessageFlags_ in das Formular.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="9b2a5-129">Übergang zu seinem [normalen](normal-state.md) Zustand Formulars vor dem anzeigen, und Benachrichtigen der registrierten Viewer durch ihre [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="9b2a5-130">Wenn keine Fehler auftreten, geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="9b2a5-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b2a5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b2a5-131">See also</span></span>



[<span data-ttu-id="9b2a5-132">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9b2a5-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="9b2a5-133">PidTagMessageStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9b2a5-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="9b2a5-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b2a5-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="9b2a5-135">Status „Nicht initialisiert“</span><span class="sxs-lookup"><span data-stu-id="9b2a5-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="9b2a5-136">Status „HandsOffAfterSave“</span><span class="sxs-lookup"><span data-stu-id="9b2a5-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="9b2a5-137">Status „HandsOffFromNormal“</span><span class="sxs-lookup"><span data-stu-id="9b2a5-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="9b2a5-138">Formularstatus</span><span class="sxs-lookup"><span data-stu-id="9b2a5-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="9b2a5-139">IPersistStorage</span><span class="sxs-lookup"><span data-stu-id="9b2a5-139">IPersistStorage::Load</span></span>](http://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="9b2a5-140">IPersistStream:: Load</span><span class="sxs-lookup"><span data-stu-id="9b2a5-140">IPersistStream::Load</span></span>](http://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="9b2a5-141">IPersistFile:: Load</span><span class="sxs-lookup"><span data-stu-id="9b2a5-141">IPersistFile::Load</span></span>](http://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

