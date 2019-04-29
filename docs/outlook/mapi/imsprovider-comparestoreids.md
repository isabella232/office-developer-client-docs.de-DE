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
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431708"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="e6af2-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="e6af2-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="e6af2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6af2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6af2-105">Vergleicht zwei Nachrichtenspeicher Eintrags-IDs, um zu bestimmen, ob Sie auf dasselbe Store-Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="e6af2-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="e6af2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6af2-106">Parameters</span></span>

 <span data-ttu-id="e6af2-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="e6af2-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="e6af2-108">in Die Größe der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird, in Bytes _._</span><span class="sxs-lookup"><span data-stu-id="e6af2-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="e6af2-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="e6af2-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="e6af2-110">in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="e6af2-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="e6af2-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="e6af2-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="e6af2-112">in Die Größe der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird, in Bytes _._</span><span class="sxs-lookup"><span data-stu-id="e6af2-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="e6af2-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="e6af2-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="e6af2-114">in Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6af2-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="e6af2-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6af2-115">_ulFlags_</span></span>
  
> <span data-ttu-id="e6af2-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="e6af2-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e6af2-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="e6af2-117">_lpulResult_</span></span>
  
> <span data-ttu-id="e6af2-118">Out Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="e6af2-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="e6af2-119">TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, andernfalls false. andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="e6af2-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6af2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6af2-120">Return value</span></span>

<span data-ttu-id="e6af2-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6af2-121">S_OK</span></span> 
  
> <span data-ttu-id="e6af2-122">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e6af2-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6af2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6af2-123">Remarks</span></span>

<span data-ttu-id="e6af2-124">MAPI Ruft die **IMSProvider:: CompareStoreIDs** -Methode auf, wenn ein Aufruf der [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) -Methode verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e6af2-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="e6af2-125">**CompareStoreIDs** wird an dieser Stelle aufgerufen, um zu bestimmen, welcher Profil Abschnitt, falls vorhanden, dem zu öffnenden Nachrichtenspeicher zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e6af2-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="e6af2-126">Ein **CompareStoreIDs** -Aufruf kann vorgenommen werden, wenn kein Nachrichtenspeicher für einen bestimmten Speicheranbieter geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="e6af2-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="e6af2-127">Außerdem ruft MAPI **CompareStoreIDs** auf, wenn ein Speicheranbieter Aufruf an die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e6af2-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="e6af2-128">Die Eintrags-IDs, die von **CompareStoreIDs** verglichen werden, sind sowohl für die Dynamic Link Library (dll) des aktuellen Speicheranbieters als auch für unwrappede Speicher Eintrags-IDs.</span><span class="sxs-lookup"><span data-stu-id="e6af2-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="e6af2-129">Weitere Informationen zum Einbinden von Speicher Eintrags Bezeichnern finden Sie unter [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="e6af2-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="e6af2-130">Das Vergleichen von Eintrags Bezeichnern ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="e6af2-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="e6af2-131">Dies kann beispielsweise der Fall sein, nachdem eine neue Version eines Nachrichtenspeicher Anbieters installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e6af2-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6af2-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6af2-132">See also</span></span>



[<span data-ttu-id="e6af2-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="e6af2-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="e6af2-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="e6af2-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="e6af2-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="e6af2-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="e6af2-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6af2-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

