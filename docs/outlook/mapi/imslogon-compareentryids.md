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
ms.openlocfilehash: c5b2d7db745cc270c0be7ee2184e86c6a4f97aad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594299"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="75908-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="75908-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="75908-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75908-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75908-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="75908-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="75908-106">MAPI verweist dieses Anrufs mit einem Dienstanbieter nur, wenn der eindeutige Bezeichner (UIDs) in beiden Eintragsbezeichner verglichen werden soll, die von diesem Provider behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="75908-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="75908-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="75908-107">Parameters</span></span>

 <span data-ttu-id="75908-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="75908-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="75908-109">[in] Die Größe in Bytes für die Eintrags-ID auf das durch den Parameter _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="75908-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="75908-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="75908-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="75908-111">[in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="75908-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="75908-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="75908-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="75908-113">[in] Die Größe in Bytes für die Eintrags-ID auf das durch den Parameter _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="75908-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="75908-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="75908-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="75908-115">[in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="75908-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="75908-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75908-116">_ulFlags_</span></span>
  
> <span data-ttu-id="75908-117">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="75908-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="75908-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="75908-118">_lpulResult_</span></span>
  
> <span data-ttu-id="75908-119">[out] Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="75908-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="75908-120">True, wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls, FALSE.</span><span class="sxs-lookup"><span data-stu-id="75908-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="75908-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="75908-121">Return value</span></span>

<span data-ttu-id="75908-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="75908-122">S_OK</span></span> 
  
> <span data-ttu-id="75908-123">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="75908-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="75908-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="75908-124">Remarks</span></span>

<span data-ttu-id="75908-125">Nachricht-Anbieter implementiert die **IMSLogon::CompareEntryIDs** -Methode zum Vergleichen von zwei Eintragsbezeichner für einen bestimmten Eintrag in einem Nachrichtenspeicher, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="75908-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="75908-126">Wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen, wird **CompareEntryIDs** den _LpulResult_ -Parameter auf true festgelegt; Wenn sie auf verschiedene Objekte verweisen, wird **CompareEntryIDs** _LpulResult_ auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="75908-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="75908-127">**CompareEntryIDs** ist hilfreich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann.</span><span class="sxs-lookup"><span data-stu-id="75908-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="75908-128">Dies kann beispielsweise vorkommen, nach der Installation einer neuen Version des Anbieters einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="75908-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="75908-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75908-129">See also</span></span>



[<span data-ttu-id="75908-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="75908-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

