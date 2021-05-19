---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Ruft die Reihenfolge der angegebenen Kategorie von Konten ab.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424623"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="01ad7-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="01ad7-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="01ad7-104">Ruft die Reihenfolge der angegebenen Kategorie von Konten ab.</span><span class="sxs-lookup"><span data-stu-id="01ad7-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="01ad7-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="01ad7-105">Quick info</span></span>

<span data-ttu-id="01ad7-106">Siehe [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="01ad7-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="01ad7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="01ad7-107">Parameters</span></span>

<span data-ttu-id="01ad7-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="01ad7-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="01ad7-109">[in] Die Kategorieklassen-ID, für die die Bestellung erhalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="01ad7-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="01ad7-110">Der Wert muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="01ad7-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="01ad7-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="01ad7-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="01ad7-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="01ad7-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="01ad7-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="01ad7-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="01ad7-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="01ad7-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="01ad7-115">[out] Die Anzahl der Konten.</span><span class="sxs-lookup"><span data-stu-id="01ad7-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="01ad7-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="01ad7-116">_prgAccts_</span></span>
  
> <span data-ttu-id="01ad7-117">[out] Ein Zeiger auf ein Array von Konten.</span><span class="sxs-lookup"><span data-stu-id="01ad7-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="01ad7-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="01ad7-118">Return values</span></span>

|<span data-ttu-id="01ad7-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="01ad7-119">**HRESULT**</span></span>|<span data-ttu-id="01ad7-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="01ad7-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="01ad7-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="01ad7-121">S_OK</span></span>  <br/> |<span data-ttu-id="01ad7-122">Der Aufruf ist erfolgreich</span><span class="sxs-lookup"><span data-stu-id="01ad7-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="01ad7-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="01ad7-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="01ad7-124">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="01ad7-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="01ad7-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="01ad7-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="01ad7-126">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="01ad7-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01ad7-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01ad7-127">Remarks</span></span>

<span data-ttu-id="01ad7-128">Vor dem Aufrufen dieser Methode weist der Aufrufer nur einen Arrayzeiger  *prgAccts*  zu, aber keinen Speicher für das Array, bei dem  *prgAccts-Punkte vorhanden*  sind.</span><span class="sxs-lookup"><span data-stu-id="01ad7-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="01ad7-129">Nachdem diese Methode zurückgegeben wurde, muss der Aufrufer [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) verwenden, um den für  *prgAccts*  zugewiesenen Arbeitsspeicher frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="01ad7-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01ad7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01ad7-130">See also</span></span>

- [<span data-ttu-id="01ad7-131">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="01ad7-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="01ad7-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="01ad7-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

