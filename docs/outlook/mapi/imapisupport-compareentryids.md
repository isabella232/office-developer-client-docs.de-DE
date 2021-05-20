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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431043"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="ca9ad-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ca9ad-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="ca9ad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca9ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca9ad-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="ca9ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca9ad-106">Parameters</span></span>

 <span data-ttu-id="ca9ad-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ca9ad-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="ca9ad-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID1-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="ca9ad-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ca9ad-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="ca9ad-110">[in] Ein Zeiger auf die erste Zutritts-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ca9ad-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ca9ad-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="ca9ad-112">[in] Die Byteanzahl in der Eintrags-ID, auf die der  _lpEntryID2-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="ca9ad-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ca9ad-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="ca9ad-114">[in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ca9ad-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca9ad-115">_ulFlags_</span></span>
  
> <span data-ttu-id="ca9ad-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ca9ad-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="ca9ad-117">_lpulResult_</span></span>
  
> <span data-ttu-id="ca9ad-118">[out] Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="ca9ad-119">TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen. Andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca9ad-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca9ad-120">Return value</span></span>

<span data-ttu-id="ca9ad-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca9ad-121">S_OK</span></span> 
  
> <span data-ttu-id="ca9ad-122">Der Vergleich war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-122">The comparison was successful.</span></span>
    
<span data-ttu-id="ca9ad-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ca9ad-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="ca9ad-124">Eine oder beide der als Parameter angegebenen Eintragsbezeichner verweisen nicht auf gültige Objekte, möglicherweise weil sie derzeit ungeöffnet sind und nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca9ad-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca9ad-125">Remarks</span></span>

<span data-ttu-id="ca9ad-126">Die **IMAPISupport::CompareEntryIDs-Methode** wird für Unterstützungsobjekte für Adressbuch- und Nachrichtenspeicheranbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="ca9ad-127">**CompareEntryIDs** vergleicht zwei Eintragsbezeichner, die zu einem einzelnen Dienstanbieter gehören, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="ca9ad-128">MAPI extrahiert den [MAPIUID-Teil](mapiuid.md) aus den Eintragsbezeichnern, um den für die Objekte zuständigen Dienstanbieter zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="ca9ad-129">MAPI ruft dann die **CompareEntryIDs-Methode** des Anmeldeobjekts auf, um den Vergleich durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ca9ad-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ca9ad-130">Notes to callers</span></span>

 <span data-ttu-id="ca9ad-131">**CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="ca9ad-132">Diese Situation kann beispielsweise auftreten, nachdem eine neue Version eines Dienstanbieters installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="ca9ad-133">Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs aus.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="ca9ad-134">Verwenden Sie stattdessen den möglichst konservativen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="ca9ad-135">**CompareEntryIDs** können fehlschlagen, wenn beispielsweise eine oder beide Eintragsbezeichner eine ungültige **MAPIUID-Struktur** enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca9ad-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca9ad-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca9ad-136">See also</span></span>



[<span data-ttu-id="ca9ad-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ca9ad-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ca9ad-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca9ad-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

