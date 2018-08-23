---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d6f983e49132e7ab6ea402a8e32bb5ec56d1efba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564850"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="97186-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="97186-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="97186-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97186-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97186-105">Vergleicht zwei Eintragsbezeichner, die gehören zu einer bestimmten Adressbuchanbieter um festzustellen, ob diese auf das gleiche Address Book-Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="97186-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="97186-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97186-106">Parameters</span></span>

 <span data-ttu-id="97186-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="97186-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="97186-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID1_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="97186-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="97186-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="97186-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="97186-110">[in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="97186-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="97186-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="97186-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="97186-112">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID2_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="97186-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="97186-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="97186-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="97186-114">[in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="97186-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="97186-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="97186-115">_ulFlags_</span></span>
  
> <span data-ttu-id="97186-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="97186-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="97186-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="97186-117">_lpulResult_</span></span>
  
> <span data-ttu-id="97186-118">[out] Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="97186-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="97186-119">Der Inhalt der _LpulResult_ sind auf TRUE festlegen, wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. Andernfalls werden die Inhalte auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97186-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="97186-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="97186-120">Return value</span></span>

<span data-ttu-id="97186-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="97186-121">S_OK</span></span> 
  
> <span data-ttu-id="97186-122">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="97186-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="97186-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="97186-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="97186-124">Eine oder beide der mit dem Parameter _lpEntryID1_ oder _lpEntryID2_ übergebene Eintrags-IDs werden durch eine beliebige Adressbuchanbieter nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="97186-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="97186-125">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="97186-125">Remarks</span></span>

<span data-ttu-id="97186-126">Clientanwendungen und Anbieter aufzurufen **CompareEntryIDs** -Methode zum Vergleichen von zwei Eintragsbezeichner, die gehört zu einer einzelnen Adressbuchanbieter um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="97186-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="97186-127">**CompareEntryIDs** ist hilfreich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann.</span><span class="sxs-lookup"><span data-stu-id="97186-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="97186-128">Dies kann beispielsweise auftreten, wenn eine neue Version des Adressbuch-Dienstanbieter installiert ist.</span><span class="sxs-lookup"><span data-stu-id="97186-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="97186-129">MAPI übergibt dieser Aufruf der Adressbuchanbieter, die für die Eintragsbezeichner verantwortlich ist bestimmen den entsprechenden Anbieter durch entsprechende [MAPIUID](mapiuid.md) Strukturänderung in der Eintragsbezeichner mit der **MAPIUID** -Struktur registriert, indem die Anbieter.</span><span class="sxs-lookup"><span data-stu-id="97186-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="97186-130">Wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen möchten, legt **CompareEntryIDs** den Inhalt des Parameters _LpulResult_ auf "true" fest. Wenn sie verschiedene Objekte verweisen möchten, werden die Inhalte von **CompareEntryIDs** auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97186-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="97186-131">In beiden Fällen gibt **CompareEntryIDs** S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="97186-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="97186-132">**CompareEntryIDs** einen Fehler zurück, die auftreten, wenn kein Adressbuch eine Struktur **MAPIUID** registriert hat, die in der Eintragsbezeichner übereinstimmt, Clients und Anbieter sollte keine Aktion basierend auf das Ergebnis der Vergleich.</span><span class="sxs-lookup"><span data-stu-id="97186-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="97186-133">Sie sollten stattdessen die Aktion den am häufigsten konservativen Ansatz dauern.</span><span class="sxs-lookup"><span data-stu-id="97186-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97186-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97186-134">See also</span></span>



[<span data-ttu-id="97186-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="97186-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

