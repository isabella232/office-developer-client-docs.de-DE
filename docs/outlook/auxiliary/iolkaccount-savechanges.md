---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Übergibt Änderungen am Account-Objekt, indem er in den Registrierungsspeicher schreibt.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322260"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="b073b-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b073b-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="b073b-104">Übergibt Änderungen am Account-Objekt, indem er in den Registrierungsspeicher schreibt.</span><span class="sxs-lookup"><span data-stu-id="b073b-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b073b-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b073b-105">Quick info</span></span>

<span data-ttu-id="b073b-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="b073b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="b073b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b073b-107">Parameters</span></span>

<span data-ttu-id="b073b-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="b073b-108">_dwFlags_</span></span>
  
> <span data-ttu-id="b073b-109">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="b073b-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="b073b-110">OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.</span><span class="sxs-lookup"><span data-stu-id="b073b-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="b073b-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b073b-111">Return values</span></span>

|<span data-ttu-id="b073b-112">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="b073b-112">**HRESULT**</span></span>|<span data-ttu-id="b073b-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="b073b-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b073b-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="b073b-114">S_OK</span></span>  <br/> |<span data-ttu-id="b073b-115">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b073b-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="b073b-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b073b-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="b073b-117">Das angegebene Konto wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="b073b-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="b073b-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="b073b-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="b073b-119">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="b073b-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b073b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b073b-120">Remarks</span></span>

<span data-ttu-id="b073b-121">Nachdem Sie den Wert der Kontoeigenschaften mithilfe von [IOlkAccount:: setprop](iolkaccount-setprop.md)geändert haben, verwenden Sie **IOlkAccount:: SaveChanges** , um solche Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b073b-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b073b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b073b-122">See also</span></span>

- [<span data-ttu-id="b073b-123">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="b073b-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="b073b-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b073b-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

