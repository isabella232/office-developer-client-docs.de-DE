---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384066"
---
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="55d14-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="55d14-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="55d14-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55d14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55d14-105">Bewirkt, dass das Formular, um die aktuelle Nachricht freigeben.</span><span class="sxs-lookup"><span data-stu-id="55d14-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="55d14-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55d14-106">Parameters</span></span>

<span data-ttu-id="55d14-107">Keine</span><span class="sxs-lookup"><span data-stu-id="55d14-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="55d14-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55d14-108">Return value</span></span>

<span data-ttu-id="55d14-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="55d14-109">S_OK</span></span> 
  
> <span data-ttu-id="55d14-110">Die Nachricht wurde erfolgreich veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="55d14-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="55d14-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="55d14-111">Remarks</span></span>

<span data-ttu-id="55d14-112">Formulare Übergang in zwei HandsOff Zustände:</span><span class="sxs-lookup"><span data-stu-id="55d14-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="55d14-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="55d14-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="55d14-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="55d14-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="55d14-115">Wenn ein Formular in einem dieser Zustände ist, ist es gerade dauerhaft gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="55d14-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="55d14-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="55d14-116">Notes to implementers</span></span>

<span data-ttu-id="55d14-117">Wenn ein Formular Viewer die **IPersistMessage::HandsOffMessage** -Methode aufruft, während das Formular im [Normal](normal-state.md) oder [NoScribble](noscribble-state.md) Zustand befindet, rekursiv Anruf **HandsOffMessage** für jede Nachricht in der aktuellen Nachricht und die [eingebettet. IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) -Methode für jedes OLE-Objekt in der aktuellen Nachricht eingebettet.</span><span class="sxs-lookup"><span data-stu-id="55d14-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="55d14-118">Klicken Sie dann die aktuelle Nachricht freigeben, und alle eingebettete Nachrichten und OLE-Objekte.</span><span class="sxs-lookup"><span data-stu-id="55d14-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="55d14-119">Wenn das Formular im Normalzustand Übergangs in den Zustand HandsOffFromNormal war.</span><span class="sxs-lookup"><span data-stu-id="55d14-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="55d14-120">Wenn das Formular im NoScribble Zustand, Übergang in den Zustand HandsOffAfterSave war.</span><span class="sxs-lookup"><span data-stu-id="55d14-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="55d14-121">Rufen Sie nach einem erfolgreichen Übergang die Nachricht [IUnknown](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode, und geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="55d14-121">After a successful transition, call the message's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="55d14-122">Wenn ein Formular Viewer **HandsOffMessage** aufruft, während das Formular in einem der HandsOff Status ist, zurückgeben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="55d14-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="55d14-123">Weitere Informationen zu den unterschiedlichen Zustände eines Formulars finden Sie unter [Formular Zustände](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="55d14-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="55d14-124">Weitere Informationen dazu, wie Sie den Status HandsOff Speicherobjekte entwickelt finden Sie unter der [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="55d14-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55d14-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55d14-125">See also</span></span>



[<span data-ttu-id="55d14-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55d14-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="55d14-127">Formularstatus</span><span class="sxs-lookup"><span data-stu-id="55d14-127">Form States</span></span>](form-states.md)

