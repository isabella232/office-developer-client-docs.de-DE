---
title: IPropDataHrGetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5e36cf12b7a5b1643f5a0ec97223030718195a7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331591"
---
# <a name="ipropdatahrgetpropaccess"></a><span data-ttu-id="e08b9-103">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="e08b9-103">IPropData::HrGetPropAccess</span></span>

  
  
<span data-ttu-id="e08b9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e08b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e08b9-105">Ruft die Zugriffsebene und den Status f�r eine oder mehrere der Eigenschaften des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="e08b9-105">Retrieves the access level and status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="e08b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e08b9-106">Parameters</span></span>

 <span data-ttu-id="e08b9-107">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="e08b9-107">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="e08b9-p101">[in, out] Bei Eingabe ein Array von Eigenschaftentags, die angeben, die Eigenschaften f�r die Zugriffsebenen und Status abgerufen. Anderenfalls einen Zeiger auf NULL, die angibt, **HrGetPropAccess** Zugriffsebenen und Statusinformationen f�r alle Eigenschaften abrufen soll. Bei der Ausgabe ein Array von Eigenschaftentags f�r welche Flags Zugriff und Status abgerufen wurden. Die Flags werden in das Array auf die durch den Parameter  _lprgulAccess_ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e08b9-p101">[in, out] On input, an array of property tags that indicate the properties for which to retrieve access levels and status; otherwise, a pointer to NULL, which indicates that **HrGetPropAccess** should retrieve access levels and status for all properties. On output, an array of property tags for which access and status flags were retrieved. The flags are stored in the array pointed to by the  _lprgulAccess_ parameter.</span></span> 
    
 <span data-ttu-id="e08b9-111">_lprgulAccess_</span><span class="sxs-lookup"><span data-stu-id="e08b9-111">_lprgulAccess_</span></span>
  
> <span data-ttu-id="e08b9-p102">[out] Ein Zeiger auf ein Array von Bitmasken Kennzeichnung. Jede Bitmaske gibt an, auf die Zugriffsebenen, Status oder beides f�r jede Eigenschaft im Array auf die durch den Parameter  _lpPropTagArray_ identifiziert. Die beiden Arrays sind mit fester Breite, dass die erste Bitmaske, dass  _lprgulAccess_ verweist auf die erste Eigenschaft beschreibt zu usw.,  _lpPropTagArray_ verweist. F�r jedes Eigenschaftentags k�nnen die folgenden Kennzeichen festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e08b9-p102">[out] A pointer to an array of flag bitmasks. Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array pointed to by the  _lpPropTagArray_ parameter. The two arrays are positional in that the first bitmask that  _lprgulAccess_ points to describes the first property that  _lpPropTagArray_ points to, and so on. For each property tag, the following flags can be set:</span></span> 
    
|<span data-ttu-id="e08b9-116">**Zugriffsebene flag**</span><span class="sxs-lookup"><span data-stu-id="e08b9-116">**Access-level flag**</span></span>|<span data-ttu-id="e08b9-117">**Status-flag**</span><span class="sxs-lookup"><span data-stu-id="e08b9-117">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e08b9-118">IPROP_READONLY, die angibt, dass die Eigenschaft nicht ge�ndert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e08b9-118">IPROP_READONLY, which indicates that the property cannot be modified.</span></span>  <br/> |<span data-ttu-id="e08b9-119">IPROP_CLEAN, die angibt, dass die Eigenschaft nicht ge�ndert wurde.</span><span class="sxs-lookup"><span data-stu-id="e08b9-119">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="e08b9-120">IPROP_READWRITE, die angibt, dass die Eigenschaft ge�ndert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e08b9-120">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="e08b9-121">IPROP_DIRTY, die angibt, dass die Eigenschaft ge�ndert wurde.</span><span class="sxs-lookup"><span data-stu-id="e08b9-121">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="e08b9-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e08b9-122">Return value</span></span>

<span data-ttu-id="e08b9-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="e08b9-123">S_OK</span></span> 
  
> <span data-ttu-id="e08b9-124">Die Access-Ebene und den Status Kennzeichen f�r die Eigenschaften wurden erfolgreich zur�ckgegeben.</span><span class="sxs-lookup"><span data-stu-id="e08b9-124">The access level and status flags for the properties were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e08b9-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e08b9-125">Remarks</span></span>

<span data-ttu-id="e08b9-126">Die **IPropData::HrGetPropAccess** -Methode ruft eine Reihe von Flags, die die Zugriffsebene und den Status f�r eine oder mehrere Eigenschaften angibt.</span><span class="sxs-lookup"><span data-stu-id="e08b9-126">The **IPropData::HrGetPropAccess** method retrieves a set of flags that indicates the access level and status for one or more properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e08b9-127">Hinweise für Aufrufer:</span><span class="sxs-lookup"><span data-stu-id="e08b9-127">Notes to callers:</span></span>

<span data-ttu-id="e08b9-128">Sie k�nnen **HrGetPropAccess** f�r folgende Zwecke verwenden:</span><span class="sxs-lookup"><span data-stu-id="e08b9-128">You can use **HrGetPropAccess** for the following purposes:</span></span> 
  
- <span data-ttu-id="e08b9-129">Um zu bestimmen, ob ein Client ge�ndert oder schreibbare Eigenschaft gel�scht.</span><span class="sxs-lookup"><span data-stu-id="e08b9-129">To determine whether a client changed or deleted a writable property.</span></span>
    
- <span data-ttu-id="e08b9-130">Um einen Client nicht �ndern oder L�schen einer Eigenschaft mithilfe der Methods [IMAPIProp](imapipropiunknown.md) zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="e08b9-130">To prevent a client from changing or deleting a property by using the [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
    
<span data-ttu-id="e08b9-p103">Wenn eine der Eigenschaften in die Array-Tag-Eigenschaft auf das  _lppPropTagArray_ gel�scht wurde, wird **HrGetPropAccess** den Arrayeintrag auf Ausgabe 0 festgelegt. Wenn Sie  _lppPropTagArray_ auf NULL festgelegt wurde und eine der Eigenschaften f�r das Objekt gel�scht wurde, wird die Eigenschaft deleted im Array zur�ckgegeben.</span><span class="sxs-lookup"><span data-stu-id="e08b9-p103">If one of the properties in the property tag array pointed to by  _lppPropTagArray_ has been deleted, **HrGetPropAccess** sets the array entry to 0 on output. If you set  _lppPropTagArray_ to NULL and one of the object's properties has been deleted, the deleted property is returned in the array.</span></span> 
  
<span data-ttu-id="e08b9-p104">Wenn eine Eigenschaft ge�ndert wurde, ist seine IPROP_DIRTY-Flag in den entsprechenden Eintrag im Array, zeigt  _lprgulAccess_ festgelegt. Weder IPROP_READONLY noch IPROP_READWRITE wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e08b9-p104">If a property has been modified, its IPROP_DIRTY flag is set in the corresponding entry in the array that  _lprgulAccess_ points to. Neither IPROP_READONLY nor IPROP_READWRITE will be set.</span></span> 
  
<span data-ttu-id="e08b9-135">Wenn eine Eigenschaft nicht ge�ndert oder gel�scht wurde, wird nur das Flag IPROP_READONLY oder IPROP_READWRITE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e08b9-135">If a property has not been modified or deleted, only the IPROP_READONLY or IPROP_READWRITE flag will be set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e08b9-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e08b9-136">See also</span></span>



[<span data-ttu-id="e08b9-137">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e08b9-137">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="e08b9-138">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e08b9-138">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

