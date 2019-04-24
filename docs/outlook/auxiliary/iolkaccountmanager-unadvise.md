---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Hebt die Registrierung eines Clients mit dem Kontomanager für Benachrichtigungen für alle Konten auf.
ms.openlocfilehash: 0b954413b06cb1aa1b6fc4e0e9666f108bf81fbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322008"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="75429-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="75429-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="75429-104">Hebt die Registrierung eines Clients mit dem Kontomanager für Benachrichtigungen für alle Konten auf.</span><span class="sxs-lookup"><span data-stu-id="75429-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="75429-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="75429-105">Quick info</span></span>

<span data-ttu-id="75429-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="75429-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="75429-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="75429-107">Parameters</span></span>

<span data-ttu-id="75429-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="75429-108">_dwCookie_</span></span>
  
> <span data-ttu-id="75429-109">in Das von [IOlkAccountManager:: Advise](iolkaccountmanager-advise.md)zurückgegebene Cookie.</span><span class="sxs-lookup"><span data-stu-id="75429-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="75429-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="75429-110">Return values</span></span>

|<span data-ttu-id="75429-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="75429-111">**HRESULT**</span></span>|<span data-ttu-id="75429-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="75429-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75429-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="75429-113">S_OK</span></span>  <br/> |<span data-ttu-id="75429-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="75429-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="75429-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="75429-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="75429-116">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="75429-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="75429-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="75429-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="75429-118">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="75429-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75429-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75429-119">See also</span></span>

- [<span data-ttu-id="75429-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="75429-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="75429-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="75429-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

