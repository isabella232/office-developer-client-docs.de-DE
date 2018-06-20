---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Ruft die Reihenfolge der angegebenen Kategorie von Konten.
ms.openlocfilehash: d05e354e25d49a51b3d3f8f053c2b39dc37b333f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791099"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="99931-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="99931-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="99931-104">Ruft die Reihenfolge der angegebenen Kategorie von Konten.</span><span class="sxs-lookup"><span data-stu-id="99931-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="99931-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="99931-105">Quick info</span></span>

<span data-ttu-id="99931-106">Finden Sie unter [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="99931-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="99931-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="99931-107">Parameters</span></span>

<span data-ttu-id="99931-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="99931-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="99931-109">[in] Die Kategorie Klassen-ID für die die Reihenfolge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="99931-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="99931-110">Der Wert muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="99931-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="99931-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="99931-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="99931-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="99931-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="99931-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="99931-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="99931-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="99931-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="99931-115">[out] Die Anzahl der Konten.</span><span class="sxs-lookup"><span data-stu-id="99931-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="99931-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="99931-116">_prgAccts_</span></span>
  
> <span data-ttu-id="99931-117">[out] Ein Zeiger auf ein Array von Konten.</span><span class="sxs-lookup"><span data-stu-id="99931-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="99931-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="99931-118">Return values</span></span>

|<span data-ttu-id="99931-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="99931-119">**HRESULT**</span></span>|<span data-ttu-id="99931-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99931-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99931-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="99931-121">S_OK</span></span>  <br/> |<span data-ttu-id="99931-122">Der Aufruf war erfolgreich</span><span class="sxs-lookup"><span data-stu-id="99931-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="99931-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="99931-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="99931-124">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="99931-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="99931-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="99931-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="99931-126">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="99931-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99931-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="99931-127">Remarks</span></span>

<span data-ttu-id="99931-128">Vor dem Aufrufen dieser Methode weist der Anrufer nur ein Array Zeiger *PrgAccts* jedoch kein Speicher für Arrays, an den *PrgAccts* zeigt.</span><span class="sxs-lookup"><span data-stu-id="99931-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="99931-129">Nachdem diese Methode zurückgegeben wird, muss der Aufrufer [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) verwenden, um Arbeitsspeicher für *PrgAccts* freizugeben.</span><span class="sxs-lookup"><span data-stu-id="99931-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99931-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99931-130">See also</span></span>

- [<span data-ttu-id="99931-131">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="99931-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="99931-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="99931-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

