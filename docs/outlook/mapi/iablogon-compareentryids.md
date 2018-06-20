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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 03256f2dec62d0228c4d5456dcd1b60f66b13ad2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791974"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="a7743-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a7743-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="a7743-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7743-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7743-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="a7743-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a7743-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7743-106">Parameters</span></span>

 <span data-ttu-id="a7743-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="a7743-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="a7743-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID1_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="a7743-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="a7743-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="a7743-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="a7743-110">[in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="a7743-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="a7743-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="a7743-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="a7743-112">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID2_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="a7743-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="a7743-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="a7743-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="a7743-114">[in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="a7743-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="a7743-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7743-115">_ulFlags_</span></span>
  
> <span data-ttu-id="a7743-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="a7743-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a7743-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="a7743-117">_lpulRet_</span></span>
  
> <span data-ttu-id="a7743-118">[out] Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="a7743-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="a7743-119">True, um anzugeben, dass die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls, FALSE.</span><span class="sxs-lookup"><span data-stu-id="a7743-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a7743-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a7743-120">Return value</span></span>

<span data-ttu-id="a7743-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="a7743-121">S_OK</span></span> 
  
> <span data-ttu-id="a7743-122">Die Eintragsbezeichner wurden erfolgreich verglichen.</span><span class="sxs-lookup"><span data-stu-id="a7743-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="a7743-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a7743-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="a7743-124">Eine oder beide der Eintragsbezeichner gehören nicht zu den Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="a7743-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a7743-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a7743-125">Remarks</span></span>

<span data-ttu-id="a7743-126">Von adressbuchanbietern implementierte implementieren Sie die **CompareEntryIDs** -Methode zum Vergleichen von zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="a7743-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="a7743-127">**CompareEntryIDs** eignet sich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann. Diese Situation kann beispielsweise auftreten, wenn Sie eine kurzfristigen Eintrags-ID mit langfristige Eintrags-ID vergleichen.</span><span class="sxs-lookup"><span data-stu-id="a7743-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="a7743-128">Weitere Informationen zum Erstellen von Eintragsbezeichner finden Sie unter [MAPI-Eintragsbezeichner](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="a7743-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a7743-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7743-129">See also</span></span>



[<span data-ttu-id="a7743-130">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7743-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

