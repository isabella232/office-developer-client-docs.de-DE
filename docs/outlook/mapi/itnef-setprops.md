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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 480a50bd8c3738ad7d0c178cb4cabfdecd15412e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792861"
---
# <a name="itnefsetprops"></a><span data-ttu-id="3b04d-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="3b04d-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="3b04d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b04d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b04d-105">Legt den Wert einer oder mehrerer Eigenschaften für eine gekapselte Nachricht oder Anlage ohne Ändern der ursprünglichen Nachricht oder Anlage fest.</span><span class="sxs-lookup"><span data-stu-id="3b04d-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="3b04d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b04d-106">Parameters</span></span>

 <span data-ttu-id="3b04d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3b04d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3b04d-108">[in] Eine Bitmaske aus Flags, die steuert, wie die-Eigenschaftswerte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3b04d-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="3b04d-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3b04d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="3b04d-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="3b04d-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="3b04d-111">Nur Eigenschaften aus der Nachricht oder einer Anlage, die durch den _UlElemID_ -Parameter angegebenen codiert.</span><span class="sxs-lookup"><span data-stu-id="3b04d-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="3b04d-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="3b04d-112">_ulElemID_</span></span>
  
> <span data-ttu-id="3b04d-113">[in] Eine Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft, die eine Zahl, eindeutig enthält identifiziert die Anlage in der übergeordneten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3b04d-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="3b04d-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="3b04d-114">_cValues_</span></span>
  
> <span data-ttu-id="3b04d-115">[in] Durch den Parameter _LpProps_ auf zeigt die Anzahl der Eigenschaftswerte in der Struktur [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="3b04d-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="3b04d-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="3b04d-116">_lpProps_</span></span>
  
> <span data-ttu-id="3b04d-117">[in] Ein Zeiger auf eine **SPropValue** -Struktur, die Eigenschaftswerte der Eigenschaften enthält festlegen.</span><span class="sxs-lookup"><span data-stu-id="3b04d-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3b04d-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3b04d-118">Return value</span></span>

<span data-ttu-id="3b04d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b04d-119">S_OK</span></span> 
  
> <span data-ttu-id="3b04d-120">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b04d-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b04d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b04d-121">Remarks</span></span>

<span data-ttu-id="3b04d-122">Transport-Anbieter, Nachricht-Anbieter und Gateways Aufruf der **ITnef::SetProps** -Methode zum Festlegen der Eigenschaften zum Einschließen in die Kapselung einer Nachricht oder einer Anlage, ohne die ursprüngliche Nachricht oder Anlage zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3b04d-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="3b04d-123">Mit diesem Anruf festgelegten Eigenschaften außer Kraft setzen vorhandene Eigenschaften in die gekapselte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3b04d-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="3b04d-124">**SetProps** wird nur für TNEF-Objekten unterstützt, die mit dem TNEF_ENCODE-Flag für die Funktion [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder [OpenTnefStreamEx](opentnefstreamex.md) geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3b04d-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="3b04d-125">Mit diesem Anruf kann eine beliebige Anzahl von Eigenschaften festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3b04d-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3b04d-126">Keine tatsächlichen TNEF-Codierung für **SetProps** geschieht erst, nachdem die [ITnef::Finish](itnef-finish.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3b04d-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="3b04d-127">Dies bedeutet, dass Zeiger in **SetProps** übergeben gültig bis bleiben müssen nach dem Anruf auf **Fertig stellen** .</span><span class="sxs-lookup"><span data-stu-id="3b04d-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="3b04d-128">An dieser Stelle können alle Objekte und Daten in **SetProps** Aufrufe übergeben freigegeben oder freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3b04d-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b04d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b04d-129">See also</span></span>



[<span data-ttu-id="3b04d-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="3b04d-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="3b04d-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="3b04d-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="3b04d-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="3b04d-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="3b04d-133">PidTagAttachNumber (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3b04d-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="3b04d-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3b04d-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="3b04d-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b04d-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

