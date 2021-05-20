---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430791"
---
# <a name="itnefsetprops"></a><span data-ttu-id="bc8fa-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="bc8fa-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="bc8fa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc8fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc8fa-105">Legt den Wert einer oder mehreren Eigenschaften für eine gekapselte Nachricht oder Anlage fest, ohne die ursprüngliche Nachricht oder Anlage zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="bc8fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc8fa-106">Parameters</span></span>

 <span data-ttu-id="bc8fa-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc8fa-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bc8fa-108">[in] Eine Bitmaske mit Flags, die steuert, wie Eigenschaftswerte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="bc8fa-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="bc8fa-109">The following flag can be set:</span></span>
    
<span data-ttu-id="bc8fa-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="bc8fa-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="bc8fa-111">Codiert nur Eigenschaften aus der Nachricht oder Anlage, die durch den  _ulElemID-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="bc8fa-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="bc8fa-112">_ulElemID_</span></span>
  
> <span data-ttu-id="bc8fa-113">[in] Die eigenschaft PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) einer Anlage, die eine Zahl enthält, die die Anlage in ihrer übergeordneten Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="bc8fa-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="bc8fa-114">_cValues_</span></span>
  
> <span data-ttu-id="bc8fa-115">[in] Die Anzahl der Eigenschaftswerte in der [SPropValue-Struktur,](spropvalue.md) auf die der  _lpProps-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="bc8fa-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="bc8fa-116">_lpProps_</span></span>
  
> <span data-ttu-id="bc8fa-117">[in] Ein Zeiger auf eine **SPropValue-Struktur,** die die Eigenschaftswerte der festgelegten Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bc8fa-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc8fa-118">Return value</span></span>

<span data-ttu-id="bc8fa-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc8fa-119">S_OK</span></span> 
  
> <span data-ttu-id="bc8fa-120">Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc8fa-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc8fa-121">Remarks</span></span>

<span data-ttu-id="bc8fa-122">Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::SetProps-Methode** auf, um Eigenschaften so zu festlegen, dass sie in die Kapselung einer Nachricht oder Anlage ohne Änderung der ursprünglichen Nachricht oder Anlage enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="bc8fa-123">Mit diesem Aufruf festgelegte Eigenschaften überschreiben vorhandene Eigenschaften in der gekapselten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="bc8fa-124">**SetProps wird** nur für TNEF-Objekte unterstützt, die mit dem TNEF_ENCODE für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion geöffnet](opentnefstreamex.md) werden.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="bc8fa-125">Mit diesem Aufruf kann eine beliebige Anzahl von Eigenschaften festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bc8fa-126">Eine tatsächliche TNEF-Codierung für **SetProps** erfolgt erst, nachdem die [ITnef::Finish-Methode](itnef-finish.md) aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="bc8fa-127">Diese Funktionalität bedeutet, dass Zeiger, die an **SetProps** übergeben werden, bis nach dem Aufruf von **Finish** gültig bleiben müssen.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="bc8fa-128">An diesem Punkt können alle an **SetProps-Aufrufe** übergebenen Objekte und Daten freigegeben oder freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc8fa-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc8fa-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc8fa-129">See also</span></span>



[<span data-ttu-id="bc8fa-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="bc8fa-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="bc8fa-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="bc8fa-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="bc8fa-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="bc8fa-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="bc8fa-133">PidTagAttachNumber (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bc8fa-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="bc8fa-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bc8fa-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="bc8fa-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc8fa-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

