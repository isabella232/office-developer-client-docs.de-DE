---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registriert einen Client beim Konto-Manager für Benachrichtigungen zu allen Konten.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427710"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="80c17-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="80c17-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="80c17-104">Registriert einen Client beim Konto-Manager für Benachrichtigungen zu allen Konten.</span><span class="sxs-lookup"><span data-stu-id="80c17-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="80c17-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="80c17-105">Quick info</span></span>

<span data-ttu-id="80c17-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="80c17-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="80c17-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="80c17-107">Parameters</span></span>

<span data-ttu-id="80c17-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="80c17-108">_pNotify_</span></span>
  
> <span data-ttu-id="80c17-109">[in] Eine [IOlkAccountNotify-Schnittstelle,](iolkaccountnotify.md) die der Kontomanager zum Senden von Benachrichtigungen an den Client verwendet.</span><span class="sxs-lookup"><span data-stu-id="80c17-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="80c17-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="80c17-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="80c17-111">[out] Ein Cookie, [das IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) verwendet, wenn die Registrierung für das Konto entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="80c17-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="80c17-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="80c17-112">Return values</span></span>

|<span data-ttu-id="80c17-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="80c17-113">**HRESULT**</span></span>|<span data-ttu-id="80c17-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="80c17-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80c17-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="80c17-115">S_OK</span></span>  <br/> |<span data-ttu-id="80c17-116">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="80c17-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="80c17-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="80c17-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="80c17-118">Es wurde ein ungültiges Argument bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="80c17-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="80c17-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="80c17-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="80c17-120">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="80c17-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80c17-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80c17-121">See also</span></span>

- [<span data-ttu-id="80c17-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="80c17-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="80c17-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="80c17-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)

