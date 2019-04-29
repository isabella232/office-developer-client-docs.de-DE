---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427815"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="57060-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="57060-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="57060-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57060-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57060-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="57060-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="57060-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57060-106">Parameters</span></span>

 <span data-ttu-id="57060-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="57060-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="57060-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="57060-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="57060-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="57060-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="57060-110">in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="57060-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="57060-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="57060-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="57060-112">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="57060-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="57060-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="57060-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="57060-114">in Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="57060-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="57060-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57060-115">_ulFlags_</span></span>
  
> <span data-ttu-id="57060-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="57060-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="57060-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="57060-117">_lpulResult_</span></span>
  
> <span data-ttu-id="57060-118">Out Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="57060-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="57060-119">TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, andernfalls false. andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="57060-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57060-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57060-120">Return value</span></span>

<span data-ttu-id="57060-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="57060-121">S_OK</span></span> 
  
> <span data-ttu-id="57060-122">Der Vergleich war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="57060-122">The comparison was successful.</span></span>
    
<span data-ttu-id="57060-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="57060-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="57060-124">Eine oder beide der als Parameter angegebenen Eintragsbezeichner verweisen nicht auf Objekte, möglicherweise, da diese Objekte derzeit nicht geöffnet und nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="57060-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57060-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57060-125">Remarks</span></span>

<span data-ttu-id="57060-126">Die **IMAPISession:: CompareEntryIDs** -Methode vergleicht zwei Eintragsbezeichner, die zu einem einzelnen Dienstanbieter gehören, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="57060-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="57060-127">MAPI extrahiert den [MAPIUID](mapiuid.md) -Teil aus den Eintrags Bezeichnern, um den für die Objekte Verantwortlichen Dienstanbieter zu bestimmen, und ruft dann die **CompareEntryIDs** -Methode des Logo-Objekts auf, um den Vergleich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="57060-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="57060-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="57060-128">Notes to callers</span></span>

<span data-ttu-id="57060-129">Die **CompareEntryIDs** -Methode ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="57060-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="57060-130">Diese Situation kann beispielsweise auftreten, nachdem eine neue Version eines Dienstanbieters installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="57060-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="57060-131">Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs aus.</span><span class="sxs-lookup"><span data-stu-id="57060-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="57060-132">Verwenden Sie stattdessen die konservativste Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="57060-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="57060-133">**CompareEntryIDs** kann fehlschlagen, wenn beispielsweise eine oder beide der Eintragsbezeichner eine ungültige **MAPIUID**enthalten.</span><span class="sxs-lookup"><span data-stu-id="57060-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="57060-134">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="57060-134">MFCMAPI reference</span></span>

<span data-ttu-id="57060-135">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="57060-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="57060-136">**Datei**</span><span class="sxs-lookup"><span data-stu-id="57060-136">**File**</span></span>|<span data-ttu-id="57060-137">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="57060-137">**Function**</span></span>|<span data-ttu-id="57060-138">**Comment**</span><span class="sxs-lookup"><span data-stu-id="57060-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="57060-139">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="57060-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="57060-140">CbaseDialog:: OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="57060-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="57060-141">MFCMAPI verwendet die **IMAPISession:: CompareEntryIDs** -Methode, um zwei Eintrags-IDs zu vergleichen, die ein Benutzer eingibt.</span><span class="sxs-lookup"><span data-stu-id="57060-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57060-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57060-142">See also</span></span>



[<span data-ttu-id="57060-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="57060-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="57060-144">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="57060-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="57060-145">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="57060-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

