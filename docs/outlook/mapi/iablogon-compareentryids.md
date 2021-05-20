---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438372"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="ed149-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ed149-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="ed149-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed149-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed149-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="ed149-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a><span data-ttu-id="ed149-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed149-106">Parameters</span></span>

 <span data-ttu-id="ed149-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ed149-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="ed149-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID1-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="ed149-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="ed149-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ed149-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="ed149-110">[in] Ein Zeiger auf die erste Zutritts-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed149-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ed149-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ed149-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="ed149-112">[in] Die Byteanzahl in der Eintrags-ID, auf die der  _lpEntryID2-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="ed149-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="ed149-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ed149-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="ed149-114">[in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed149-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ed149-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ed149-115">_ulFlags_</span></span>
  
> <span data-ttu-id="ed149-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="ed149-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ed149-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="ed149-117">_lpulRet_</span></span>
  
> <span data-ttu-id="ed149-118">[out] Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="ed149-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="ed149-119">TRUE, um anzugeben, dass sich die beiden Eintragsbezeichner auf dasselbe Objekt beziehen. Andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="ed149-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ed149-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed149-120">Return value</span></span>

<span data-ttu-id="ed149-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed149-121">S_OK</span></span> 
  
> <span data-ttu-id="ed149-122">Die Eintragsbezeichner wurden erfolgreich verglichen.</span><span class="sxs-lookup"><span data-stu-id="ed149-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="ed149-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ed149-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="ed149-124">Eine oder beide eintragsbezeichner gehören nicht zum Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="ed149-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ed149-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed149-125">Remarks</span></span>

<span data-ttu-id="ed149-126">Adressbuchanbieter implementieren die **CompareEntryIDs-Methode,** um zwei Eintragsbezeichner zu vergleichen, um festzustellen, ob sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="ed149-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="ed149-127">**CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner enthalten kann. Eine solche Situation kann beispielsweise auftreten, wenn Sie eine kurzfristige Eintrags-ID mit einer langfristigen Eintrags-ID vergleichen.</span><span class="sxs-lookup"><span data-stu-id="ed149-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="ed149-128">Weitere Informationen zum Erstellen von Eintragsbezeichnern finden Sie unter [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="ed149-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ed149-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed149-129">See also</span></span>



[<span data-ttu-id="ed149-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed149-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

