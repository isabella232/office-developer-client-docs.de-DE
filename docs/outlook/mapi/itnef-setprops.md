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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315043"
---
# <a name="itnefsetprops"></a><span data-ttu-id="4d262-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="4d262-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="4d262-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d262-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d262-105">Legt den Wert einer oder mehrerer Eigenschaften für eine gekapselte Nachricht oder Anlage fest, ohne die ursprüngliche Nachricht oder Anlage zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4d262-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="4d262-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d262-106">Parameters</span></span>

 <span data-ttu-id="4d262-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4d262-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4d262-108">in Eine Bitmaske von Flags, die steuert, wie Eigenschaftswerte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4d262-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="4d262-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4d262-109">The following flag can be set:</span></span>
    
<span data-ttu-id="4d262-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="4d262-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="4d262-111">Codiert nur Eigenschaften aus der Nachricht oder Anlage, die durch den _ulElemID_ -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4d262-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="4d262-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="4d262-112">_ulElemID_</span></span>
  
> <span data-ttu-id="4d262-113">in Die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft einer Anlage, die eine Zahl enthält, die die Anlage in der übergeordneten Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4d262-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="4d262-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="4d262-114">_cValues_</span></span>
  
> <span data-ttu-id="4d262-115">in Die Anzahl der Eigenschaftswerte in der [SPropValue](spropvalue.md) -Struktur, auf die durch den _lpProps_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4d262-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="4d262-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="4d262-116">_lpProps_</span></span>
  
> <span data-ttu-id="4d262-117">in Ein Zeiger auf eine **SPropValue** -Struktur, die die Eigenschaftswerte der festzulegenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="4d262-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d262-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d262-118">Return value</span></span>

<span data-ttu-id="4d262-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d262-119">S_OK</span></span> 
  
> <span data-ttu-id="4d262-120">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4d262-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d262-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d262-121">Remarks</span></span>

<span data-ttu-id="4d262-122">Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef::** SetProps-Methode auf, um die Eigenschaften festzulegen, die in die Kapselung einer Nachricht oder Anlage eingeschlossen werden sollen, ohne die ursprüngliche Nachricht oder Anlage zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4d262-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="4d262-123">Alle Eigenschaften, die mit diesem Aufruf festgelegt wurden, überschreiben vorhandene Eigenschaften in der gekapselte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4d262-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="4d262-124">\*\*\*\* SetProps wird nur für TNEF-Objekte unterstützt, die mit dem TNEF_ENCODE-Flag für die [OpenTnefStream](opentnefstream.md) -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="4d262-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="4d262-125">Mit diesem Aufruf kann eine beliebige Anzahl von Eigenschaften festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4d262-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4d262-126">Es erfolgt keine tatsächliche TNEF \*\*\*\* -Codierung für SetProps, bevor die [ITnef:: Finish](itnef-finish.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4d262-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="4d262-127">Diese Funktionalität bedeutet, dass Zeiger, \*\*\*\* die an SetProps übergeben werden, gültig bleiben müssen, bis der Aufruf **beendet** wurde.</span><span class="sxs-lookup"><span data-stu-id="4d262-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="4d262-128">An diesem Punkt können alle Objekte und Daten, die \*\*\*\* an SetProps-Aufrufe übergeben werden, freigegeben oder freigeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="4d262-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d262-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d262-129">See also</span></span>



[<span data-ttu-id="4d262-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="4d262-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="4d262-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="4d262-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="4d262-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="4d262-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="4d262-133">Kanonische Pidtagattachnumber (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d262-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="4d262-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4d262-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="4d262-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d262-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

