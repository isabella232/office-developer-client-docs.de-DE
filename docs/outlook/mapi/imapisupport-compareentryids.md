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
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331570"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="2d9c3-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2d9c3-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="2d9c3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d9c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d9c3-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="2d9c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d9c3-106">Parameters</span></span>

 <span data-ttu-id="2d9c3-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2d9c3-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="2d9c3-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="2d9c3-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2d9c3-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="2d9c3-110">in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2d9c3-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2d9c3-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="2d9c3-112">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="2d9c3-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2d9c3-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="2d9c3-114">in Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2d9c3-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2d9c3-115">_ulFlags_</span></span>
  
> <span data-ttu-id="2d9c3-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2d9c3-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="2d9c3-117">_lpulResult_</span></span>
  
> <span data-ttu-id="2d9c3-118">Out Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="2d9c3-119">TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, andernfalls false. andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2d9c3-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d9c3-120">Return value</span></span>

<span data-ttu-id="2d9c3-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d9c3-121">S_OK</span></span> 
  
> <span data-ttu-id="2d9c3-122">Der Vergleich war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-122">The comparison was successful.</span></span>
    
<span data-ttu-id="2d9c3-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2d9c3-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="2d9c3-124">Eine oder beide der als Parameter angegebenen Eintragsbezeichner beziehen sich nicht auf gültige Objekte, möglicherweise weil Sie derzeit nicht geöffnet und nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d9c3-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d9c3-125">Remarks</span></span>

<span data-ttu-id="2d9c3-126">Die **IMAPISupport:: CompareEntryIDs** -Methode wird für Support Objekte des Adressbuchs und des Nachrichtenspeichers implementiert.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="2d9c3-127">**CompareEntryIDs** vergleicht zwei Eintrags-IDs, die zu einem einzelnen Dienstanbieter gehören, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="2d9c3-128">MAPI extrahiert den [MAPIUID](mapiuid.md) -Teil aus den Eintrags Bezeichnern, um den für die Objekte Verantwortlichen Dienstanbieter zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="2d9c3-129">MAPI ruft dann die **CompareEntryIDs** -Methode des LOGON-Objekts auf, um den Vergleich durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2d9c3-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="2d9c3-130">Notes to callers</span></span>

 <span data-ttu-id="2d9c3-131">**CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="2d9c3-132">Diese Situation kann beispielsweise auftreten, nachdem eine neue Version eines Dienstanbieters installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="2d9c3-133">Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs aus.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="2d9c3-134">Verwenden Sie stattdessen die konservativste Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="2d9c3-135">**CompareEntryIDs** kann fehlschlagen, wenn beispielsweise eine oder beide der Eintragsbezeichner eine ungültige **MAPIUID** -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="2d9c3-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d9c3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d9c3-136">See also</span></span>



[<span data-ttu-id="2d9c3-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="2d9c3-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="2d9c3-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d9c3-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

