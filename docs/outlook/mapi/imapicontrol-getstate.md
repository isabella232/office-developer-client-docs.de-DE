---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a6ae89bf9b2b16439cc06f0e106859dda10ea22c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792074"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="b30dc-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="b30dc-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="b30dc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b30dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b30dc-105">Ruft einen Wert, der angibt, ob das Schaltflächensteuerelement aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b30dc-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="b30dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b30dc-106">Parameters</span></span>

 <span data-ttu-id="b30dc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b30dc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b30dc-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="b30dc-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b30dc-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="b30dc-109">_lpulState_</span></span>
  
> <span data-ttu-id="b30dc-110">[out] Ein Zeiger auf einen Wert, der den Status des Schaltflächen-Steuerelements angibt.</span><span class="sxs-lookup"><span data-stu-id="b30dc-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="b30dc-111">Die folgenden Werte kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="b30dc-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="b30dc-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="b30dc-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="b30dc-113">Das Button-Steuerelement ist deaktiviert und kann nicht darauf geklickt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b30dc-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="b30dc-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="b30dc-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="b30dc-115">Das Schaltflächensteuerelement ist aktiviert und geklickt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b30dc-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b30dc-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b30dc-116">Return value</span></span>

<span data-ttu-id="b30dc-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b30dc-117">S_OK</span></span> 
  
> <span data-ttu-id="b30dc-118">Der Zustand des Schaltflächensteuerelements wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b30dc-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b30dc-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b30dc-119">Remarks</span></span>

<span data-ttu-id="b30dc-120">Dienstanbieter implementieren die **IMAPIControl::GetState** -Methode, um den Status eines Schaltflächen-Steuerelements MAPI bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b30dc-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="b30dc-121">Wenn die Schaltfläche aktiviert ist, kann es zu einem Klicken mit der Maus oder Drücken einer Taste reagieren.</span><span class="sxs-lookup"><span data-stu-id="b30dc-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="b30dc-122">Wenn es deaktiviert ist, wird die Schaltfläche abgeblendet und reagiert nicht auf einer klicken mit der Maus oder Drücken einer Taste.</span><span class="sxs-lookup"><span data-stu-id="b30dc-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="b30dc-123">Weitere Informationen zum Implementieren von **GetState** und ein weiterer [IMAPIControl: IUnknown](imapicontroliunknown.md) Methoden finden Sie unter [Implementierung der Steuerelement-Objekts](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="b30dc-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b30dc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b30dc-124">See also</span></span>



[<span data-ttu-id="b30dc-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="b30dc-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="b30dc-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b30dc-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

