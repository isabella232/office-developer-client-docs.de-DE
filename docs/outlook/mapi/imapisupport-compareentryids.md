---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c939189c2c8f7d3147c3146f55deac0e032ce9df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792359"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="39ecc-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="39ecc-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="39ecc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39ecc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39ecc-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="39ecc-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="39ecc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39ecc-106">Parameters</span></span>

 <span data-ttu-id="39ecc-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="39ecc-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="39ecc-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID1_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="39ecc-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="39ecc-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="39ecc-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="39ecc-110">[in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="39ecc-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="39ecc-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="39ecc-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="39ecc-112">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID2_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="39ecc-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="39ecc-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="39ecc-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="39ecc-114">[in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="39ecc-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="39ecc-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="39ecc-115">_ulFlags_</span></span>
  
> <span data-ttu-id="39ecc-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="39ecc-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="39ecc-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="39ecc-117">_lpulResult_</span></span>
  
> <span data-ttu-id="39ecc-118">[out] Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="39ecc-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="39ecc-119">True, wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls, FALSE.</span><span class="sxs-lookup"><span data-stu-id="39ecc-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="39ecc-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39ecc-120">Return value</span></span>

<span data-ttu-id="39ecc-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="39ecc-121">S_OK</span></span> 
  
> <span data-ttu-id="39ecc-122">Der Vergleich war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="39ecc-122">The comparison was successful.</span></span>
    
<span data-ttu-id="39ecc-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="39ecc-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="39ecc-124">Eine oder beide als Parameter angegebenen Eintrag Bezeichner verweisen nicht auf gültige Objekte möglicherweise, da sie derzeit nicht geöffneten und nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="39ecc-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="39ecc-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39ecc-125">Remarks</span></span>

<span data-ttu-id="39ecc-126">Die **IMAPISupport::CompareEntryIDs** -Methode wird für Adresse Adressbuch und Nachricht Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="39ecc-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="39ecc-127">**CompareEntryIDs** vergleicht zwei Eintragsbezeichner, die mit einem einzelnen Dienstanbieter zu bestimmen, ob sie sich auf dasselbe Objekt verweisen gehören.</span><span class="sxs-lookup"><span data-stu-id="39ecc-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="39ecc-128">MAPI extrahiert den [MAPIUID](mapiuid.md) Teil aus den Eintrag-IDs den Dienstanbieter verantwortlich für die Objekte zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="39ecc-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="39ecc-129">MAPI ruft dann **die Anmeldung des Objekts-Eintragsbezeichner zum Durchführen des Vergleichs** .</span><span class="sxs-lookup"><span data-stu-id="39ecc-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="39ecc-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="39ecc-130">Notes to callers</span></span>

 <span data-ttu-id="39ecc-131">**CompareEntryIDs** ist hilfreich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann.</span><span class="sxs-lookup"><span data-stu-id="39ecc-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="39ecc-132">Dies kann beispielsweise vorkommen, nach der Installation einer neuen Version von einem Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="39ecc-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="39ecc-133">Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="39ecc-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="39ecc-134">In diesem Fall sollten Sie am häufigsten konservative Methode möglich.</span><span class="sxs-lookup"><span data-stu-id="39ecc-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="39ecc-135">**CompareEntryIDs** können Fehler auftreten, wenn Sie beispielsweise eine oder beide der Eintragsbezeichner eine ungültige **MAPIUID** Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="39ecc-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39ecc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39ecc-136">See also</span></span>



[<span data-ttu-id="39ecc-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="39ecc-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="39ecc-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="39ecc-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

