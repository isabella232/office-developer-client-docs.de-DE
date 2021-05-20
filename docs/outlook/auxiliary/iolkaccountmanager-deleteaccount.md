---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Löscht das angegebene Konto.
ms.openlocfilehash: 3e39b7b9af57f64dd124e1bf836db68664709b8c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431239"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="71b5b-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="71b5b-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="71b5b-104">Löscht das angegebene Konto.</span><span class="sxs-lookup"><span data-stu-id="71b5b-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="71b5b-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="71b5b-105">Quick info</span></span>

<span data-ttu-id="71b5b-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="71b5b-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="71b5b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="71b5b-107">Parameters</span></span>

<span data-ttu-id="71b5b-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="71b5b-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="71b5b-109">[in] Die Konto-ID des zu löschende Kontos.</span><span class="sxs-lookup"><span data-stu-id="71b5b-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="71b5b-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="71b5b-110">Return values</span></span>

|<span data-ttu-id="71b5b-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="71b5b-111">**HRESULT**</span></span>|<span data-ttu-id="71b5b-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="71b5b-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="71b5b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="71b5b-113">S_OK</span></span>  <br/> |<span data-ttu-id="71b5b-114">Der Aufruf ist erfolgreich</span><span class="sxs-lookup"><span data-stu-id="71b5b-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="71b5b-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="71b5b-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="71b5b-116">Das angegebene Konto wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="71b5b-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="71b5b-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="71b5b-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="71b5b-118">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="71b5b-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71b5b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71b5b-119">See also</span></span>

- [<span data-ttu-id="71b5b-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="71b5b-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="71b5b-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="71b5b-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)

