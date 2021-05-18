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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309716"
---
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="83fcc-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="83fcc-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="83fcc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83fcc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83fcc-105">Bewirkt, dass das Formular seine aktuelle Nachricht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="83fcc-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="83fcc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83fcc-106">Parameters</span></span>

<span data-ttu-id="83fcc-107">Keine</span><span class="sxs-lookup"><span data-stu-id="83fcc-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="83fcc-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83fcc-108">Return value</span></span>

<span data-ttu-id="83fcc-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="83fcc-109">S_OK</span></span> 
  
> <span data-ttu-id="83fcc-110">Die Nachricht wurde erfolgreich freigegeben.</span><span class="sxs-lookup"><span data-stu-id="83fcc-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="83fcc-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="83fcc-111">Remarks</span></span>

<span data-ttu-id="83fcc-112">Formulare werden in zwei HandsOff-Zustände übergewechselt:</span><span class="sxs-lookup"><span data-stu-id="83fcc-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="83fcc-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="83fcc-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="83fcc-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="83fcc-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="83fcc-115">Wenn sich ein Formular in einem dieser Zustände befindet, wird es dauerhaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="83fcc-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="83fcc-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="83fcc-116">Notes to implementers</span></span>

<span data-ttu-id="83fcc-117">Wenn ein Formularbetrachter die **IPersistMessage::HandsOffMessage-Methode** aufruft, während sich Ihr Formular im Normal- oder [NoScribble-Zustand](noscribble-state.md) befindet, rufen Sie für jede in die aktuelle Nachricht eingebettete Nachricht und die [IPersistStorage::HandsOffStorage-Methode](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) für jedes in die aktuelle Nachricht eingebettete OLE-Objekt rekursiv **HandsOffMessage** auf. [](normal-state.md)</span><span class="sxs-lookup"><span data-stu-id="83fcc-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="83fcc-118">Geben Sie dann die aktuelle Nachricht und alle eingebetteten Nachrichten und OLE-Objekte frei.</span><span class="sxs-lookup"><span data-stu-id="83fcc-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="83fcc-119">Wenn ihr Formular den Status Normal hatte, müssen Sie zum Status HandsOffFromNormal überwechseln.</span><span class="sxs-lookup"><span data-stu-id="83fcc-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="83fcc-120">Wenn ihr Formular den Status "NoScribble" hatte, gehen Sie in den Status HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="83fcc-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="83fcc-121">Rufen Sie nach einem erfolgreichen Übergang die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) der Nachricht auf, und geben Sie S_OK.</span><span class="sxs-lookup"><span data-stu-id="83fcc-121">After a successful transition, call the message's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="83fcc-122">Wenn ein Formularbetrachter **HandsOffMessage aufruft,** während sich Ihr Formular in einem der HandsOff-Zustände befindet, geben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="83fcc-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="83fcc-123">Weitere Informationen zu den verschiedenen Zuständen eines Formulars finden Sie unter [Formularzustände](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="83fcc-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="83fcc-124">Weitere Informationen zum Arbeiten mit dem HandsOff-Status von Speicherobjekten finden Sie unter [der IPersistStorage::HandsOffStorage-Methode.](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)</span><span class="sxs-lookup"><span data-stu-id="83fcc-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83fcc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83fcc-125">See also</span></span>



[<span data-ttu-id="83fcc-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="83fcc-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="83fcc-127">Formularzustände</span><span class="sxs-lookup"><span data-stu-id="83fcc-127">Form States</span></span>](form-states.md)

