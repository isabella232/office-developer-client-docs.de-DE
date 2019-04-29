---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430448"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="a4d67-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="a4d67-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="a4d67-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4d67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4d67-105">Konvertiert die interne Eintrags-ID eines Nachrichtenspeichers in eine Eintrags-ID im MAPI-Standardformat.</span><span class="sxs-lookup"><span data-stu-id="a4d67-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="a4d67-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4d67-106">Parameters</span></span>

 <span data-ttu-id="a4d67-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="a4d67-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="a4d67-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpOrigEntry_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a4d67-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="a4d67-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="a4d67-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="a4d67-110">in Ein Zeiger auf die ID des privaten Eintrags für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="a4d67-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="a4d67-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="a4d67-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="a4d67-112">Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppWrappedEntry_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a4d67-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="a4d67-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="a4d67-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="a4d67-114">Out Ein Zeiger auf einen Zeiger auf den eingebundenen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="a4d67-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4d67-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4d67-115">Return value</span></span>

<span data-ttu-id="a4d67-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4d67-116">S_OK</span></span> 
  
> <span data-ttu-id="a4d67-117">Die Eintrags-ID wurde erfolgreich umbrochen.</span><span class="sxs-lookup"><span data-stu-id="a4d67-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4d67-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4d67-118">Remarks</span></span>

<span data-ttu-id="a4d67-119">Die **IMAPISupport:: WrapStoreEntryID** -Methode wird für alle Support Objekte des Dienstanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="a4d67-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="a4d67-120">Dienstanbieter verwenden **WrapStoreEntryID** , um MAPI eine Eintrags-ID für einen Nachrichtenspeicher zu generieren, der die interne Eintrags-ID des Speichers umschließt.</span><span class="sxs-lookup"><span data-stu-id="a4d67-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a4d67-121">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a4d67-121">Notes to callers</span></span>

<span data-ttu-id="a4d67-122">Wenn ein Client die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Nachrichtenspeichers zum Abrufen seiner **PR_STORE_ENTRYID** ([pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))-Eigenschaft aufruft und Ihr Nachrichtenspeicher eine Eintrags-ID in einem privaten Format verwendet, rufen Sie WrapStoreEntryID auf. \*\* \*\*, und geben Sie die Eintrags-ID zurück, auf die durch den _lppWrappedEntry_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a4d67-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="a4d67-123">Aufrufe der [IMSProvider:: Login](imsprovider-logon.md) -und [IMSLogon:: CompareEntryIDs](imslogon-compareentryids.md) -Methoden rufen immer den privaten Eintragsbezeichner des Speichers ab; die Wrapped-Version wird nur zwischen Clientanwendungen und MAPI verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4d67-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="a4d67-124">Freigeben des Speichers für die Eintrags-ID, auf die durch den _lppWrappedEntry_ -Parameter verwiesen wird, mithilfe der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, wenn Sie die Eintrags-ID nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4d67-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4d67-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4d67-125">See also</span></span>



[<span data-ttu-id="a4d67-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="a4d67-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="a4d67-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a4d67-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="a4d67-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a4d67-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="a4d67-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="a4d67-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="a4d67-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a4d67-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a4d67-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4d67-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

