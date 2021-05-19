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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419009"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="231e9-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="231e9-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="231e9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="231e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="231e9-105">Ruft einen Wert ab, der angibt, ob das Schaltflächensteuerelement aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="231e9-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="231e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="231e9-106">Parameters</span></span>

 <span data-ttu-id="231e9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="231e9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="231e9-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="231e9-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="231e9-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="231e9-109">_lpulState_</span></span>
  
> <span data-ttu-id="231e9-110">[out] Ein Zeiger auf einen Wert, der den Status des Schaltflächensteuerelements angibt.</span><span class="sxs-lookup"><span data-stu-id="231e9-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="231e9-111">Einer der folgenden Werte kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="231e9-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="231e9-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="231e9-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="231e9-113">Das Schaltflächensteuerelement ist deaktiviert und kann nicht geklickt werden.</span><span class="sxs-lookup"><span data-stu-id="231e9-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="231e9-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="231e9-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="231e9-115">Das Schaltflächensteuerelement ist aktiviert und kann geklickt werden.</span><span class="sxs-lookup"><span data-stu-id="231e9-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="231e9-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="231e9-116">Return value</span></span>

<span data-ttu-id="231e9-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="231e9-117">S_OK</span></span> 
  
> <span data-ttu-id="231e9-118">Der Status des Schaltflächensteuerelements wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="231e9-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="231e9-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="231e9-119">Remarks</span></span>

<span data-ttu-id="231e9-120">Dienstanbieter implementieren die **IMAPIControl::GetState-Methode,** um MAPI den Status eines Schaltflächensteuerelements zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="231e9-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="231e9-121">Wenn die Schaltfläche aktiviert ist, kann sie auf einen Mausklick oder eine Tastendrucktaste reagieren.</span><span class="sxs-lookup"><span data-stu-id="231e9-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="231e9-122">Wenn sie deaktiviert ist, wird die Schaltfläche abgeblendet angezeigt und reagiert nicht auf einen Mausklick oder die Tastendrucktaste.</span><span class="sxs-lookup"><span data-stu-id="231e9-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="231e9-123">Weitere Informationen zum Implementieren von **GetState** und den anderen [IMAPIControl : IUnknown-Methoden](imapicontroliunknown.md) finden Sie unter [Control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="231e9-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="231e9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="231e9-124">See also</span></span>



[<span data-ttu-id="231e9-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="231e9-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="231e9-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="231e9-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

