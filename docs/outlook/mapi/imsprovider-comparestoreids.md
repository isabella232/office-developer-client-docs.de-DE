---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9905a4e972f0e599629aac74b6fbc8bae06c93b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792672"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="ede93-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="ede93-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="ede93-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ede93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ede93-105">Vergleicht zwei e-Mail-Store-Eintragsbezeichner, um zu bestimmen, ob sie auf das gleiche Store-Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="ede93-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
```cpp
HRESULT CompareStoreIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="ede93-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ede93-106">Parameters</span></span>

 <span data-ttu-id="ede93-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ede93-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="ede93-108">[in] Die Größe in Bytes für die Eintrags-ID auf das durch den Parameter _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="ede93-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="ede93-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ede93-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="ede93-110">[in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="ede93-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ede93-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ede93-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="ede93-112">[in] Die Größe in Bytes für die Eintrags-ID auf das durch den Parameter _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="ede93-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="ede93-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ede93-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="ede93-114">[in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="ede93-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ede93-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ede93-115">_ulFlags_</span></span>
  
> <span data-ttu-id="ede93-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="ede93-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ede93-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="ede93-117">_lpulResult_</span></span>
  
> <span data-ttu-id="ede93-118">[out] Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="ede93-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="ede93-119">True, wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls, FALSE.</span><span class="sxs-lookup"><span data-stu-id="ede93-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ede93-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ede93-120">Return value</span></span>

<span data-ttu-id="ede93-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ede93-121">S_OK</span></span> 
  
> <span data-ttu-id="ede93-122">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="ede93-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ede93-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ede93-123">Remarks</span></span>

<span data-ttu-id="ede93-124">MAPI ruft die **IMSProvider::CompareStoreIDs** -Methode auf, wenn sie einen Anruf an die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ede93-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="ede93-125">**CompareStoreIDs** ist zu diesem Zeitpunkt aufgerufen, um zu bestimmen, welcher Profilabschnitt gegebenenfalls zugeordnet Nachrichtenspeicher wird geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="ede93-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="ede93-126">**CompareStoreIDs** können aufgerufen werden, wenn keine Nachrichtenspeicher für einen bestimmten Anbieter geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="ede93-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="ede93-127">Darüber hinaus ruft MAPI auch **CompareStoreIDs** bei der Verarbeitung eines Speicher-Anbieter Aufrufs der [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ede93-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="ede93-128">Die **CompareStoreIDs** bei einem Vergleich Eintragsbezeichner sind sowohl für die aktuelle Speichern des Anbieters Dynamic Link Library (DLL) und sind beide allein stehenden Store-Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="ede93-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="ede93-129">Weitere Informationen zum Umfließen eines Store-Eintragsbezeichner finden Sie unter [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="ede93-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="ede93-130">Vergleichen von Eintragsbezeichner ist hilfreich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann.</span><span class="sxs-lookup"><span data-stu-id="ede93-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="ede93-131">Dies kann beispielsweise vorkommen, nach der Installation einer neuen Version des Anbieters einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ede93-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ede93-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ede93-132">See also</span></span>



[<span data-ttu-id="ede93-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="ede93-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="ede93-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ede93-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="ede93-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="ede93-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="ede93-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ede93-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

