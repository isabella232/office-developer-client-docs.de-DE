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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348727"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="697c2-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="697c2-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="697c2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="697c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="697c2-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="697c2-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="697c2-106">MAPI bezieht diesen Aufruf nur dann an einen Dienstanbieter, wenn die eindeutigen IDs (in beiden Eingabe Bezeichnern), die verglichen werden sollen, von diesem Anbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="697c2-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="697c2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="697c2-107">Parameters</span></span>

 <span data-ttu-id="697c2-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="697c2-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="697c2-109">in Die Größe der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird, in Bytes _._</span><span class="sxs-lookup"><span data-stu-id="697c2-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="697c2-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="697c2-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="697c2-111">in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="697c2-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="697c2-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="697c2-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="697c2-113">in Die Größe der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird, in Bytes _._</span><span class="sxs-lookup"><span data-stu-id="697c2-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="697c2-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="697c2-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="697c2-115">in Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="697c2-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="697c2-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="697c2-116">_ulFlags_</span></span>
  
> <span data-ttu-id="697c2-117">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="697c2-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="697c2-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="697c2-118">_lpulResult_</span></span>
  
> <span data-ttu-id="697c2-119">Out Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="697c2-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="697c2-120">TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, andernfalls false. andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="697c2-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="697c2-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="697c2-121">Return value</span></span>

<span data-ttu-id="697c2-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="697c2-122">S_OK</span></span> 
  
> <span data-ttu-id="697c2-123">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="697c2-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="697c2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="697c2-124">Remarks</span></span>

<span data-ttu-id="697c2-125">Nachrichtenspeicher Anbieter implementieren die **IMSLogon:: CompareEntryIDs** -Methode, um zwei Eintragsbezeichner für einen bestimmten Eintrag in einem Nachrichtenspeicher zu vergleichen, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="697c2-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="697c2-126">Wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, legt **CompareEntryIDs** den _lpulResult_ -Parameter auf true fest; Wenn Sie auf verschiedene Objekte verweisen, **CompareEntryIDs** _lpulResult_ auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="697c2-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="697c2-127">**CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="697c2-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="697c2-128">Dies kann beispielsweise der Fall sein, nachdem eine neue Version eines Nachrichtenspeicher Anbieters installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="697c2-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="697c2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="697c2-129">See also</span></span>



[<span data-ttu-id="697c2-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="697c2-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

