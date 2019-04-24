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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280280"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="9fbaf-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="9fbaf-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="9fbaf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fbaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fbaf-105">Ruft einen Wert ab, der angibt, ob das Schaltflächen-Steuerelement aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="9fbaf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fbaf-106">Parameters</span></span>

 <span data-ttu-id="9fbaf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9fbaf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9fbaf-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9fbaf-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="9fbaf-109">_lpulState_</span></span>
  
> <span data-ttu-id="9fbaf-110">Out Ein Zeiger auf einen Wert, der den Zustand des Schaltflächen-Steuerelements angibt.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="9fbaf-111">Einer der folgenden Werte kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="9fbaf-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="9fbaf-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="9fbaf-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="9fbaf-113">Das Schaltflächen-Steuerelement ist deaktiviert und kann nicht angeklickt werden.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="9fbaf-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="9fbaf-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="9fbaf-115">Das Schaltflächen-Steuerelement ist aktiviert und kann angeklickt werden.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9fbaf-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fbaf-116">Return value</span></span>

<span data-ttu-id="9fbaf-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="9fbaf-117">S_OK</span></span> 
  
> <span data-ttu-id="9fbaf-118">Der Status des Schaltflächen-Steuerelements wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9fbaf-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fbaf-119">Remarks</span></span>

<span data-ttu-id="9fbaf-120">Dienstanbieter implementieren die **IMAPIControl:: GetState** -Methode, um MAPI den Status eines Schaltflächen-Steuerelements bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="9fbaf-121">Wenn die Schaltfläche aktiviert ist, kann Sie auf einen Mausklick oder eine Tastenkombination reagieren.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="9fbaf-122">Wenn es deaktiviert ist, wird die Schaltfläche abgeblendet angezeigt und reagiert nicht auf einen Mausklick oder eine Tastenkombination.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="9fbaf-123">Weitere Informationen zum Implementieren von GetState \*\*\*\* und den anderen [IMAPIControl: IUnknown](imapicontroliunknown.md) -Methoden finden Sie unter [Control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="9fbaf-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9fbaf-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fbaf-124">See also</span></span>



[<span data-ttu-id="9fbaf-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="9fbaf-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="9fbaf-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9fbaf-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

