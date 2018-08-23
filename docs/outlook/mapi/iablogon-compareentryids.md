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
ms.openlocfilehash: b161c8c0da78b5ca872b87cad9a297169426d4cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565004"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="85d17-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="85d17-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="85d17-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85d17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85d17-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="85d17-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="85d17-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85d17-106">Parameters</span></span>

 <span data-ttu-id="85d17-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="85d17-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="85d17-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID1_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="85d17-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="85d17-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="85d17-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="85d17-110">[in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="85d17-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="85d17-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="85d17-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="85d17-112">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID2_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="85d17-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="85d17-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="85d17-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="85d17-114">[in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="85d17-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="85d17-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85d17-115">_ulFlags_</span></span>
  
> <span data-ttu-id="85d17-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="85d17-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="85d17-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="85d17-117">_lpulRet_</span></span>
  
> <span data-ttu-id="85d17-118">[out] Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="85d17-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="85d17-119">True, um anzugeben, dass die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls, FALSE.</span><span class="sxs-lookup"><span data-stu-id="85d17-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="85d17-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="85d17-120">Return value</span></span>

<span data-ttu-id="85d17-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="85d17-121">S_OK</span></span> 
  
> <span data-ttu-id="85d17-122">Die Eintragsbezeichner wurden erfolgreich verglichen.</span><span class="sxs-lookup"><span data-stu-id="85d17-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="85d17-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="85d17-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="85d17-124">Eine oder beide der Eintragsbezeichner gehören nicht zu den Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="85d17-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85d17-125">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="85d17-125">Remarks</span></span>

<span data-ttu-id="85d17-126">Von adressbuchanbietern implementierte implementieren Sie die **CompareEntryIDs** -Methode zum Vergleichen von zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="85d17-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="85d17-127">**CompareEntryIDs** eignet sich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann. Diese Situation kann beispielsweise auftreten, wenn Sie eine kurzfristigen Eintrags-ID mit langfristige Eintrags-ID vergleichen.</span><span class="sxs-lookup"><span data-stu-id="85d17-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="85d17-128">Weitere Informationen zum Erstellen von Eintragsbezeichner finden Sie unter [MAPI-Eintragsbezeichner](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="85d17-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="85d17-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85d17-129">See also</span></span>



[<span data-ttu-id="85d17-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85d17-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

