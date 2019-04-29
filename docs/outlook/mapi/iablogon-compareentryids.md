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
# <a name="iablogoncompareentryids"></a><span data-ttu-id="7e53d-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="7e53d-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="7e53d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e53d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e53d-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="7e53d-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7e53d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e53d-106">Parameters</span></span>

 <span data-ttu-id="7e53d-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="7e53d-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="7e53d-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7e53d-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="7e53d-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="7e53d-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="7e53d-110">in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="7e53d-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="7e53d-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="7e53d-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="7e53d-112">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7e53d-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="7e53d-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="7e53d-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="7e53d-114">in Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e53d-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="7e53d-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e53d-115">_ulFlags_</span></span>
  
> <span data-ttu-id="7e53d-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="7e53d-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7e53d-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="7e53d-117">_lpulRet_</span></span>
  
> <span data-ttu-id="7e53d-118">Out Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="7e53d-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="7e53d-119">TRUE, um anzugeben, dass die beiden Eintragsbezeichner auf dasselbe Objekt verweisen; andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="7e53d-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7e53d-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e53d-120">Return value</span></span>

<span data-ttu-id="7e53d-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e53d-121">S_OK</span></span> 
  
> <span data-ttu-id="7e53d-122">Die Eintrags-IDs wurden erfolgreich verglichen.</span><span class="sxs-lookup"><span data-stu-id="7e53d-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="7e53d-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7e53d-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="7e53d-124">Eine oder beide der Eintrags-IDs gehören nicht zum Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="7e53d-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e53d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e53d-125">Remarks</span></span>

<span data-ttu-id="7e53d-126">Adressbuchanbieter implementieren die **CompareEntryIDs** -Methode, um zwei Eintragsbezeichner zu vergleichen, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="7e53d-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="7e53d-127">**CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann. eine solche Situation kann beispielsweise auftreten, wenn Sie eine kurzfristige Eintrags-ID mit einer langfristigen Eintrags-ID vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7e53d-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="7e53d-128">Weitere Informationen zum Erstellen von Eintrags Bezeichnern finden Sie unter [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="7e53d-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e53d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e53d-129">See also</span></span>



[<span data-ttu-id="7e53d-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e53d-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

