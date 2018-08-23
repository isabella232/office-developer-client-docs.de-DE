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
ms.openlocfilehash: 640923511241b08e5a86e9733aab5cc2e9237c23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576575"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="44686-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="44686-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="44686-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44686-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44686-105">Vergleicht zwei Eintragsbezeichner, um festzustellen, ob sie auf dieselbe Rechtsgrundlage in einem Nachrichtenspeicher verweisen.</span><span class="sxs-lookup"><span data-stu-id="44686-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="44686-106">MAPI übergibt dieses Anrufs mit einem Dienstanbieter nur, wenn der eindeutige Bezeichner (UIDs) in beiden Eintragsbezeichner verglichen werden soll, die von diesem Provider behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="44686-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="44686-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="44686-107">Parameters</span></span>

 <span data-ttu-id="44686-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="44686-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="44686-109">[in] Die Byteanzahl von in die Eintrags-ID auf das durch den Parameter _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="44686-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="44686-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="44686-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="44686-111">[in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="44686-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="44686-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="44686-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="44686-113">[in] Die Byteanzahl von in die Eintrags-ID auf das durch den Parameter _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="44686-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="44686-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="44686-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="44686-115">[in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="44686-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="44686-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="44686-116">_ulFlags_</span></span>
  
> <span data-ttu-id="44686-117">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="44686-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="44686-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="44686-118">_lpulResult_</span></span>
  
> <span data-ttu-id="44686-119">[out] Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="44686-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="44686-120">True, wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls, FALSE.</span><span class="sxs-lookup"><span data-stu-id="44686-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="44686-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="44686-121">Return value</span></span>

<span data-ttu-id="44686-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="44686-122">S_OK</span></span> 
  
> <span data-ttu-id="44686-123">Der Vergleich war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="44686-123">The comparison was successful.</span></span>
    
<span data-ttu-id="44686-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="44686-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="44686-125">Stellen eine oder beide der Eintragsbezeichner angegeben, wie der Parameter nicht auf Objekte, möglicherweise verweisen, da die entsprechenden Objekte nicht geöffneten und nicht mehr verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="44686-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44686-126">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="44686-126">Remarks</span></span>

<span data-ttu-id="44686-127">Die **IMsgStore::CompareEntryIDs** -Methode vergleicht zwei Eintragsbezeichner, die mit dem Nachrichtenspeicher, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen gehören.</span><span class="sxs-lookup"><span data-stu-id="44686-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="44686-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="44686-128">Notes to callers</span></span>

 <span data-ttu-id="44686-129">**CompareEntryIDs** ist hilfreich, da ein Objekt mehr als eine gültige Eintrags-ID (beispielsweise nach der Installation einer neuen Version einer Nachricht Speicheranbieter) haben kann.</span><span class="sxs-lookup"><span data-stu-id="44686-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="44686-130">Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="44686-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="44686-131">In diesem Fall sollten Sie am häufigsten konservative Methode möglich.</span><span class="sxs-lookup"><span data-stu-id="44686-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="44686-132">**CompareEntryIDs** können Fehler auftreten, wenn Sie beispielsweise eine oder beide der Eintragsbezeichner enthält eine ungültige **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="44686-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="44686-133">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="44686-133">MFCMAPI reference</span></span>

<span data-ttu-id="44686-134">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="44686-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="44686-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="44686-135">**File**</span></span>|<span data-ttu-id="44686-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="44686-136">**Function**</span></span>|<span data-ttu-id="44686-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="44686-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="44686-138">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="44686-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="44686-139">CBaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="44686-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="44686-140">MFCMAPI (engl.) verwendet die **IMsgStore::CompareEntryIDs** -Methode zum Vergleichen von Eintrags-IDs.</span><span class="sxs-lookup"><span data-stu-id="44686-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44686-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44686-141">See also</span></span>



[<span data-ttu-id="44686-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="44686-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="44686-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="44686-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="44686-144">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="44686-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

