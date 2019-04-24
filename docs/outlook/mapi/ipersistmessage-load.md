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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317129"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="5b1ca-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="5b1ca-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="5b1ca-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b1ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b1ca-105">Lädt das Formular für eine angegebene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5b1ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b1ca-106">Parameters</span></span>

 <span data-ttu-id="5b1ca-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="5b1ca-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="5b1ca-108">in Ein Zeiger auf die Nachrichtenwebsite für das zu ladende Formular.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="5b1ca-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="5b1ca-109">_pMessage_</span></span>
  
> <span data-ttu-id="5b1ca-110">in Ein Zeiger auf die Nachricht, für die das Formular geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="5b1ca-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="5b1ca-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="5b1ca-112">in Eine Bitmaske von Client definierten oder Anbieter definierten Flags, die aus der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht kopiert werden und Informationen zum Status der Nachricht enthalten.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="5b1ca-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="5b1ca-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="5b1ca-114">in Eine Bitmaske von Flags, die aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht kopiert werden und weitere Informationen zum Status der Nachricht enthalten.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b1ca-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b1ca-115">Return value</span></span>

<span data-ttu-id="5b1ca-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b1ca-116">S_OK</span></span> 
  
> <span data-ttu-id="5b1ca-117">Das Formular wurde erfolgreich geladen.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b1ca-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b1ca-118">Remarks</span></span>

<span data-ttu-id="5b1ca-119">Formular Betrachter rufen die **IPersistMessage:: Laden** -Methode auf, um ein Formular für eine vorhandene Nachricht zu laden.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5b1ca-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="5b1ca-120">Notes to implementers</span></span>

 <span data-ttu-id="5b1ca-121">**Laden** wird nur aufgerufen, wenn sich ein Formular in einem der folgenden Zustände befindet:</span><span class="sxs-lookup"><span data-stu-id="5b1ca-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="5b1ca-122">Initialisierten</span><span class="sxs-lookup"><span data-stu-id="5b1ca-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="5b1ca-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="5b1ca-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="5b1ca-124">Status "handsofffromnormal</span><span class="sxs-lookup"><span data-stu-id="5b1ca-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="5b1ca-125">Wenn ein Formular-Viewer **Laden** aufruft, während sich das Formular in einem anderen Zustand befindet, gibt die Methode E_UNEXPECTED zurück.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="5b1ca-126">Wenn das Formular einen Verweis auf eine aktive Nachrichtenwebsite hat, die nicht an den **Laden**übergeben wird, lassen Sie die ursprüngliche Website frei, da Sie nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="5b1ca-127">Speichern Sie die Zeiger auf den Nachrichten Standort und die Nachricht aus den Parametern _pMessageSite_ und _pMessage_ , und rufen Sie die Methoden [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) der Objekte auf, um Ihre Verweisanzahl zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="5b1ca-128">Nachdem **AddRef** abgeschlossen ist, speichern Sie die Eigenschaften aus den Parametern _ulMessageStatus_ und _ulMessageFlags_ in dem Formular.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="5b1ca-129">Wechseln Sie das Formular in den [Normal](normal-state.md) Zustand, bevor Sie es anzeigen, und Benachrichtigen Sie registrierte Betrachter, indem Sie Ihre [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="5b1ca-130">Wenn keine Fehler auftreten, geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b1ca-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b1ca-131">See also</span></span>



[<span data-ttu-id="5b1ca-132">Kanonische PidTagMessageFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5b1ca-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="5b1ca-133">Kanonische Pidtagmessagestatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5b1ca-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="5b1ca-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b1ca-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="5b1ca-135">Nicht initialisierter Status</span><span class="sxs-lookup"><span data-stu-id="5b1ca-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="5b1ca-136">HandsOffAfterSave-Status</span><span class="sxs-lookup"><span data-stu-id="5b1ca-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="5b1ca-137">Status "handsofffromnormal-Status</span><span class="sxs-lookup"><span data-stu-id="5b1ca-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="5b1ca-138">Formular Status</span><span class="sxs-lookup"><span data-stu-id="5b1ca-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="5b1ca-139">IPersistStorage:: Laden</span><span class="sxs-lookup"><span data-stu-id="5b1ca-139">IPersistStorage::Load</span></span>](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="5b1ca-140">IPersistStream:: Laden</span><span class="sxs-lookup"><span data-stu-id="5b1ca-140">IPersistStream::Load</span></span>](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="5b1ca-141">IPersistFile:: Laden</span><span class="sxs-lookup"><span data-stu-id="5b1ca-141">IPersistFile::Load</span></span>](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

