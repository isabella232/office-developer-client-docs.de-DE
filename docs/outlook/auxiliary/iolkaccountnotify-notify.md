---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Benachrichtigt den Client von Änderungen an das angegebene Konto.
ms.openlocfilehash: ea4cab8cb8571cf5f34637c08935c78c657e5503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791112"
---
# <a name="iolkaccountnotifynotify"></a><span data-ttu-id="56404-103">IOlkAccountNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="56404-103">IOlkAccountNotify::Notify</span></span>

<span data-ttu-id="56404-104">Benachrichtigt den Client von Änderungen an das angegebene Konto.</span><span class="sxs-lookup"><span data-stu-id="56404-104">Notifies the client of changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="56404-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="56404-105">Quick info</span></span>

<span data-ttu-id="56404-106">Finden Sie unter [IOlkAccountNotify](iolkaccountnotify.md).</span><span class="sxs-lookup"><span data-stu-id="56404-106">See [IOlkAccountNotify](iolkaccountnotify.md).</span></span>
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="56404-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="56404-107">Parameters</span></span>

<span data-ttu-id="56404-108">_dwNotify_</span><span class="sxs-lookup"><span data-stu-id="56404-108">_dwNotify_</span></span>
  
> <span data-ttu-id="56404-109">[in] Der Typ der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="56404-109">[in] The type of notification.</span></span> <span data-ttu-id="56404-110">Der Wert muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="56404-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="56404-111">NOTIFY_ACCT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="56404-111">NOTIFY_ACCT_CHANGED</span></span> 
    
   - <span data-ttu-id="56404-112">NOTIFY_ACCT_CREATED</span><span class="sxs-lookup"><span data-stu-id="56404-112">NOTIFY_ACCT_CREATED</span></span> 
    
   - <span data-ttu-id="56404-113">NOTIFY_ACCT_DELETED</span><span class="sxs-lookup"><span data-stu-id="56404-113">NOTIFY_ACCT_DELETED</span></span>
    
   - <span data-ttu-id="56404-114">NOTIFY_ACCT_ORDER_CHANGED</span><span class="sxs-lookup"><span data-stu-id="56404-114">NOTIFY_ACCT_ORDER_CHANGED</span></span> 
    
   - <span data-ttu-id="56404-115">NOTIFY_ACCT_PREDELETED</span><span class="sxs-lookup"><span data-stu-id="56404-115">NOTIFY_ACCT_PREDELETED</span></span> 
    
 <span data-ttu-id="56404-116">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="56404-116">_dwAcctID_</span></span>
  
> <span data-ttu-id="56404-117">[in] Die Konto-ID des Kontos, das geändert, erstellt worden ist, gelöscht oder vor dem gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="56404-117">[in] The account ID of the account that has been created, changed, deleted, or pre-deleted.</span></span>
    
 <span data-ttu-id="56404-118">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="56404-118">_dwFlags_</span></span>
  
>  <span data-ttu-id="56404-119">[in] Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="56404-119">[in] Not used.</span></span> <span data-ttu-id="56404-120">OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.</span><span class="sxs-lookup"><span data-stu-id="56404-120">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="56404-121">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="56404-121">Return values</span></span>

<span data-ttu-id="56404-122">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="56404-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56404-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56404-123">See also</span></span>

- [<span data-ttu-id="56404-124">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="56404-124">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="56404-125">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="56404-125">IOlkAccountManager</span></span>](iolkaccountmanager.md)

