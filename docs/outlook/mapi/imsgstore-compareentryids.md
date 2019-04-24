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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348790"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="ff988-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ff988-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="ff988-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff988-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff988-105">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf den gleichen Eintrag in einem Nachrichtenspeicher verweisen.</span><span class="sxs-lookup"><span data-stu-id="ff988-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="ff988-106">Dieser Aufruf wird von MAPI nur dann an einen Dienstanbieter weitergeleitet, wenn die eindeutigen IDs in beiden Eintrags Bezeichnern, die verglichen werden sollen, von diesem Anbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ff988-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ff988-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff988-107">Parameters</span></span>

 <span data-ttu-id="ff988-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ff988-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="ff988-109">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird _._</span><span class="sxs-lookup"><span data-stu-id="ff988-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="ff988-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ff988-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="ff988-111">in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="ff988-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ff988-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ff988-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="ff988-113">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird _._</span><span class="sxs-lookup"><span data-stu-id="ff988-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="ff988-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ff988-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="ff988-115">in Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff988-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ff988-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff988-116">_ulFlags_</span></span>
  
> <span data-ttu-id="ff988-117">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="ff988-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ff988-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="ff988-118">_lpulResult_</span></span>
  
> <span data-ttu-id="ff988-119">Out Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="ff988-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="ff988-120">TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, andernfalls false. andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="ff988-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ff988-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff988-121">Return value</span></span>

<span data-ttu-id="ff988-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff988-122">S_OK</span></span> 
  
> <span data-ttu-id="ff988-123">Der Vergleich war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ff988-123">The comparison was successful.</span></span>
    
<span data-ttu-id="ff988-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ff988-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="ff988-125">Eine oder beide der als Parameter angegebenen Eintragsbezeichner verweisen nicht auf Objekte, möglicherweise weil die entsprechenden Objekte ungeöffnet und derzeit nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ff988-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff988-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff988-126">Remarks</span></span>

<span data-ttu-id="ff988-127">Die **IMsgStore:: CompareEntryIDs** -Methode vergleicht zwei Eintragsbezeichner, die zum Nachrichtenspeicher gehören, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="ff988-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ff988-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ff988-128">Notes to callers</span></span>

 <span data-ttu-id="ff988-129">**CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann (beispielsweise nach der Installation einer neuen Version eines Nachrichtenspeicher Anbieters).</span><span class="sxs-lookup"><span data-stu-id="ff988-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="ff988-130">Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs aus.</span><span class="sxs-lookup"><span data-stu-id="ff988-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="ff988-131">Verwenden Sie stattdessen die konservativste Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="ff988-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="ff988-132">**CompareEntryIDs** kann fehlschlagen, wenn beispielsweise eine oder beide der Eintragsbezeichner eine ungültige **MAPIUID**enthält.</span><span class="sxs-lookup"><span data-stu-id="ff988-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff988-133">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="ff988-133">MFCMAPI reference</span></span>

<span data-ttu-id="ff988-134">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ff988-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff988-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ff988-135">**File**</span></span>|<span data-ttu-id="ff988-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ff988-136">**Function**</span></span>|<span data-ttu-id="ff988-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ff988-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff988-138">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="ff988-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="ff988-139">CBaseDialog:: OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ff988-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="ff988-140">MFCMAPI verwendet die **IMsgStore:: CompareEntryIDs** -Methode, um Eintrags-IDs zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="ff988-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff988-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff988-141">See also</span></span>



[<span data-ttu-id="ff988-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ff988-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ff988-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ff988-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="ff988-144">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ff988-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

