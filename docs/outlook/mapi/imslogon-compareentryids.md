---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410133"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="9e8b3-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="9e8b3-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="9e8b3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e8b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e8b3-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="9e8b3-106">MAPI verweist diesen Aufruf nur dann an einen Dienstanbieter, wenn die eindeutigen Bezeichner (UIDs) in beiden zu vergleichenden Eintragsbezeichnern von diesem Anbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="9e8b3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e8b3-107">Parameters</span></span>

 <span data-ttu-id="9e8b3-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="9e8b3-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="9e8b3-109">[in] Die Größe des Eintragsbezeichners in Bytes, auf den der  _lpEntryID1-Parameter_  _verweist._</span><span class="sxs-lookup"><span data-stu-id="9e8b3-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="9e8b3-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="9e8b3-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="9e8b3-111">[in] Ein Zeiger auf die erste Zutritts-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="9e8b3-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="9e8b3-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="9e8b3-113">[in] Die Größe des Eintragsbezeichners in Bytes, auf den der  _lpEntryID2-Parameter_  _verweist._</span><span class="sxs-lookup"><span data-stu-id="9e8b3-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="9e8b3-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="9e8b3-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="9e8b3-115">[in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="9e8b3-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e8b3-116">_ulFlags_</span></span>
  
> <span data-ttu-id="9e8b3-117">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9e8b3-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="9e8b3-118">_lpulResult_</span></span>
  
> <span data-ttu-id="9e8b3-119">[out] Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="9e8b3-120">TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen. Andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e8b3-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e8b3-121">Return value</span></span>

<span data-ttu-id="9e8b3-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e8b3-122">S_OK</span></span> 
  
> <span data-ttu-id="9e8b3-123">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e8b3-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9e8b3-124">Remarks</span></span>

<span data-ttu-id="9e8b3-125">Nachrichtenspeicheranbieter implementieren die **IMSLogon::CompareEntryIDs-Methode,** um zwei Eintragsbezeichner für einen bestimmten Eintrag in einem Nachrichtenspeicher zu vergleichen, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="9e8b3-126">Wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, legt **CompareEntryIDs** den  _lpulResult-Parameter_ auf TRUE fest. Wenn sie auf verschiedene Objekte verweisen, **legt CompareEntryIDs**  _lpulResult auf_ FALSE fest.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="9e8b3-127">**CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="9e8b3-128">Dies kann beispielsweise auftreten, nachdem eine neue Version eines Nachrichtenspeicheranbieters installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9e8b3-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e8b3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e8b3-129">See also</span></span>



[<span data-ttu-id="9e8b3-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e8b3-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

