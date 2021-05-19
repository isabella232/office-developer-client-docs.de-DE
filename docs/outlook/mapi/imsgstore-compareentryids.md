---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424252"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="5ffd8-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="5ffd8-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="5ffd8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ffd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ffd8-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf denselben Eintrag in einem Nachrichtenspeicher verweisen.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="5ffd8-106">MAPI übergibt diesen Aufruf nur an einen Dienstanbieter, wenn die eindeutigen Bezeichner (UIDs) in beiden zu vergleichenden Eintragsbezeichnern von diesem Anbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="5ffd8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ffd8-107">Parameters</span></span>

 <span data-ttu-id="5ffd8-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="5ffd8-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="5ffd8-109">[in] Die Byteanzahl in der Eintrags-ID, auf die der  _lpEntryID1-Parameter_  _verweist._</span><span class="sxs-lookup"><span data-stu-id="5ffd8-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="5ffd8-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="5ffd8-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="5ffd8-111">[in] Ein Zeiger auf die erste Zutritts-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="5ffd8-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="5ffd8-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="5ffd8-113">[in] Die Byteanzahl in der Eintrags-ID, auf die der  _lpEntryID2-Parameter_  _verweist._</span><span class="sxs-lookup"><span data-stu-id="5ffd8-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="5ffd8-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="5ffd8-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="5ffd8-115">[in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="5ffd8-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ffd8-116">_ulFlags_</span></span>
  
> <span data-ttu-id="5ffd8-117">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5ffd8-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="5ffd8-118">_lpulResult_</span></span>
  
> <span data-ttu-id="5ffd8-119">[out] Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="5ffd8-120">TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen. Andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ffd8-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ffd8-121">Return value</span></span>

<span data-ttu-id="5ffd8-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ffd8-122">S_OK</span></span> 
  
> <span data-ttu-id="5ffd8-123">Der Vergleich war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-123">The comparison was successful.</span></span>
    
<span data-ttu-id="5ffd8-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5ffd8-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="5ffd8-125">Eine oder beide der als Parameter angegebenen Eintragsbezeichner beziehen sich nicht auf Objekte, möglicherweise weil die entsprechenden Objekte ungeöffnet sind und derzeit nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ffd8-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ffd8-126">Remarks</span></span>

<span data-ttu-id="5ffd8-127">Die **IMsgStore::CompareEntryIDs-Methode** vergleicht zwei Eintragsbezeichner, die zum Nachrichtenspeicher gehören, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5ffd8-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="5ffd8-128">Notes to callers</span></span>

 <span data-ttu-id="5ffd8-129">**CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner haben kann (z. B. nach der Installation einer neuen Version eines Nachrichtenspeicheranbieters).</span><span class="sxs-lookup"><span data-stu-id="5ffd8-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="5ffd8-130">Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs aus.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="5ffd8-131">Verwenden Sie stattdessen den möglichst konservativen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="5ffd8-132">**CompareEntryIDs** können fehlschlagen, wenn beispielsweise eine oder beide Eintragsbezeichner eine ungültige **MAPIUID enthalten.**</span><span class="sxs-lookup"><span data-stu-id="5ffd8-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5ffd8-133">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="5ffd8-133">MFCMAPI reference</span></span>

<span data-ttu-id="5ffd8-134">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5ffd8-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5ffd8-135">**File**</span></span>|<span data-ttu-id="5ffd8-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5ffd8-136">**Function**</span></span>|<span data-ttu-id="5ffd8-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5ffd8-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5ffd8-138">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="5ffd8-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="5ffd8-139">CBaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="5ffd8-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="5ffd8-140">MFCMAPI verwendet die **IMsgStore::CompareEntryIDs-Methode,** um Eintrags-IDs zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="5ffd8-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5ffd8-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ffd8-141">See also</span></span>



[<span data-ttu-id="5ffd8-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5ffd8-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5ffd8-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5ffd8-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="5ffd8-144">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5ffd8-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

