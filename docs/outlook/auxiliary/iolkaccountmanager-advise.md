---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registriert einen Client mit dem Kontomanager für Benachrichtigungen bezüglich alle Konten.
ms.openlocfilehash: 1fb697fef44b9ed32888527c3c9e467be69ba4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791085"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="2551c-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="2551c-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="2551c-104">Registriert einen Client mit dem Kontomanager für Benachrichtigungen bezüglich alle Konten.</span><span class="sxs-lookup"><span data-stu-id="2551c-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2551c-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2551c-105">Quick info</span></span>

<span data-ttu-id="2551c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="2551c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="2551c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2551c-107">Parameters</span></span>

<span data-ttu-id="2551c-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="2551c-108">_pNotify_</span></span>
  
> <span data-ttu-id="2551c-109">[in] Eine [IOlkAccountNotify](iolkaccountnotify.md) -Schnittstelle, die der Konto-Manager zum Senden von Benachrichtigungen an den Client verwenden.</span><span class="sxs-lookup"><span data-stu-id="2551c-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="2551c-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="2551c-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="2551c-111">[out] Ein Cookie, das [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) verwendet wird, wenn Sie die Registrierung für das Konto zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2551c-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2551c-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2551c-112">Return values</span></span>

|<span data-ttu-id="2551c-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="2551c-113">**HRESULT**</span></span>|<span data-ttu-id="2551c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2551c-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2551c-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="2551c-115">S_OK</span></span>  <br/> |<span data-ttu-id="2551c-116">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2551c-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="2551c-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2551c-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="2551c-118">Ein ungültiges Argument wurde bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2551c-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="2551c-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="2551c-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="2551c-120">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="2551c-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2551c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2551c-121">See also</span></span>

- [<span data-ttu-id="2551c-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="2551c-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="2551c-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="2551c-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)

