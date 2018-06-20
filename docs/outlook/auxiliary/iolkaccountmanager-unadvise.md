---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Hebt die Registrierung einer-Clients mit der Konto-Manager für Benachrichtigungen für alle Konten.
ms.openlocfilehash: 0632bc6bd98e218cf323262ea480b020185438f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791101"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="a9a8e-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a9a8e-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="a9a8e-104">Hebt die Registrierung einer-Clients mit der Konto-Manager für Benachrichtigungen für alle Konten.</span><span class="sxs-lookup"><span data-stu-id="a9a8e-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a9a8e-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a9a8e-105">Quick info</span></span>

<span data-ttu-id="a9a8e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="a9a8e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="a9a8e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9a8e-107">Parameters</span></span>

<span data-ttu-id="a9a8e-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="a9a8e-108">_dwCookie_</span></span>
  
> <span data-ttu-id="a9a8e-109">[in] Das Cookie von [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9a8e-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a9a8e-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a9a8e-110">Return values</span></span>

|<span data-ttu-id="a9a8e-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="a9a8e-111">**HRESULT**</span></span>|<span data-ttu-id="a9a8e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9a8e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a9a8e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9a8e-113">S_OK</span></span>  <br/> |<span data-ttu-id="a9a8e-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a9a8e-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="a9a8e-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a9a8e-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="a9a8e-116">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a9a8e-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="a9a8e-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="a9a8e-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="a9a8e-118">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="a9a8e-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9a8e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9a8e-119">See also</span></span>

- [<span data-ttu-id="a9a8e-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="a9a8e-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="a9a8e-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="a9a8e-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

