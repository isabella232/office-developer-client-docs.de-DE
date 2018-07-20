---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 39dbf3d3c8a8e22a7b7087929f749589cdeb2090
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792796"
---
# <a name="ipropdatahrsetpropaccess"></a><span data-ttu-id="b7ef2-103">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="b7ef2-103">IPropData::HrSetPropAccess</span></span>

  
  
<span data-ttu-id="b7ef2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7ef2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7ef2-105">Legt die Zugriffsebene oder Status für eine oder mehrere der Eigenschaften des Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-105">Sets the access level or status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="b7ef2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7ef2-106">Parameters</span></span>

 <span data-ttu-id="b7ef2-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="b7ef2-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="b7ef2-108">[in] Ein Zeiger auf ein Array von Eigenschaftentags, die angeben, die Eigenschaften geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-108">[in] A pointer to an array of property tags that indicate the properties to be modified.</span></span> 
    
 <span data-ttu-id="b7ef2-109">_rgulAccess_</span><span class="sxs-lookup"><span data-stu-id="b7ef2-109">_rgulAccess_</span></span>
  
> <span data-ttu-id="b7ef2-p101">[in] Ein Array von Bitmasken Kennzeichnung. Jede Bitmaske gibt an, auf die Zugriffsebenen, Status oder beides für jede Eigenschaft im Array, dem der  _lpPropTagArray_ -Parameter verweist identifiziert. Die beiden Arrays sind mit fester Breite, dass die erste Bitmaske in  _rgulAccess_ die ersten-Eigenschaft, zeigt  _lpPropTagArray_ zu, und so weiter beschreibt. F�r jedes Eigenschaftentags kann ein Zugriffsebene Flag und ein Status-Flag festgelegt werden. Die folgende Tabelle zeigt die möglichen Flags.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-p101">[in] An array of flag bitmasks. Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array that the  _lpPropTagArray_ parameter points to. The two arrays are positional in that the first bitmask in  _rgulAccess_ describes the first property that  _lpPropTagArray_ points to, and so on. For each property tag, one access-level flag and one status flag can be set. The following table shows the possible flags.</span></span> 
    
|<span data-ttu-id="b7ef2-115">**Zugriffsebene flag**</span><span class="sxs-lookup"><span data-stu-id="b7ef2-115">**Access-level flag**</span></span>|<span data-ttu-id="b7ef2-116">**Status-flag**</span><span class="sxs-lookup"><span data-stu-id="b7ef2-116">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7ef2-117">IPROP_READONLY, die angibt, dass die Eigenschaft nicht geändert werden kann</span><span class="sxs-lookup"><span data-stu-id="b7ef2-117">IPROP_READONLY, which indicates that the property cannot be modified</span></span>  <br/> |<span data-ttu-id="b7ef2-118">IPROP_CLEAN, die angibt, dass die Eigenschaft nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-118">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="b7ef2-119">IPROP_READWRITE, die angibt, dass die Eigenschaft geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-119">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="b7ef2-120">IPROP_DIRTY, die angibt, dass die Eigenschaft geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-120">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="b7ef2-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7ef2-121">Return value</span></span>

<span data-ttu-id="b7ef2-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7ef2-122">S_OK</span></span> 
  
> <span data-ttu-id="b7ef2-123">Die Zugriffsebene und den Status Kennzeichen wurden erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-123">The access-level and status flags have been successfully set.</span></span>
    
<span data-ttu-id="b7ef2-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b7ef2-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b7ef2-125">Es wurde versucht, eine Eigenschaft für ein schreibgeschütztes Objekt oder ein Objekt für den Anrufer nicht �ber ausreichende Berechtigungen verfügt festlegen.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-125">An attempt was made to set a property on a read-only object or an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="b7ef2-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b7ef2-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b7ef2-127">Der Parameter  _rgulAccess_ enthält eine ungültige Kombination von Flags, die wie IPROP_READONLY und IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-127">The  _rgulAccess_ parameter contains an invalid combination of flags, such as IPROP_READONLY and IPROP_READWRITE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b7ef2-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7ef2-128">Remarks</span></span>

<span data-ttu-id="b7ef2-p102">Die **IPropData::HrSetPropAccess** -Methode �ndert die Zugriffsebene und den Status für die Eigenschaften, die durch die Eigenschaftstags in der [SPropTagArray](sproptagarray.md) -Struktur, die auf die durch den Parameter  _lpPropTagArray_ identifiziert werden. F�r jede Eigenschaft ist vorhanden ein entsprechender Eintrag im  _rgulAccess_ -Array. Der Eintrag kann festgelegt werden, um ein Flag, das die Eigenschaft Zugriffsebene und ein weiteres angibt Flag, das den Status angibt.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-p102">The **IPropData::HrSetPropAccess** method changes the access level and status for the properties that are identified by the property tags in the [SPropTagArray](sproptagarray.md) structure pointed to by the  _lpPropTagArray_ parameter. For each property, there is a corresponding entry in the  _rgulAccess_ array. The entry can be set to one flag that indicates the property's access level and another flag that indicates its status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b7ef2-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b7ef2-132">Notes to callers</span></span>

<span data-ttu-id="b7ef2-133">Verwenden Sie **HrSetPropAccess**, um bei �nderung eines bestimmten-Eigenschaft ermitteln und die Zugriffsebene für eine oder mehrere der Eigenschaften eines Objekts zu �ndern.</span><span class="sxs-lookup"><span data-stu-id="b7ef2-133">Use **HrSetPropAccess** to determine when a particular property value changes and to change the access level for one or more of an object's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7ef2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7ef2-134">See also</span></span>



[<span data-ttu-id="b7ef2-135">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b7ef2-135">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b7ef2-136">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b7ef2-136">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

