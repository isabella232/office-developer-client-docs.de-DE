---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Benachrichtigt den Client über Änderungen am angegebenen Konto.
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321966"
---
# <a name="iolkaccountnotifynotify"></a><span data-ttu-id="57983-103">IOlkAccountNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="57983-103">IOlkAccountNotify::Notify</span></span>

<span data-ttu-id="57983-104">Benachrichtigt den Client über Änderungen am angegebenen Konto.</span><span class="sxs-lookup"><span data-stu-id="57983-104">Notifies the client of changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="57983-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="57983-105">Quick info</span></span>

<span data-ttu-id="57983-106">Siehe [IOlkAccountNotify](iolkaccountnotify.md).</span><span class="sxs-lookup"><span data-stu-id="57983-106">See [IOlkAccountNotify](iolkaccountnotify.md).</span></span>
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="57983-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="57983-107">Parameters</span></span>

<span data-ttu-id="57983-108">_dwNotify_</span><span class="sxs-lookup"><span data-stu-id="57983-108">_dwNotify_</span></span>
  
> <span data-ttu-id="57983-109">in Der Benachrichtigungstyp.</span><span class="sxs-lookup"><span data-stu-id="57983-109">[in] The type of notification.</span></span> <span data-ttu-id="57983-110">Bei dem Wert muss es sich um Folgendes handeln:</span><span class="sxs-lookup"><span data-stu-id="57983-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="57983-111">NOTIFY_ACCT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="57983-111">NOTIFY_ACCT_CHANGED</span></span> 
    
   - <span data-ttu-id="57983-112">NOTIFY_ACCT_CREATED</span><span class="sxs-lookup"><span data-stu-id="57983-112">NOTIFY_ACCT_CREATED</span></span> 
    
   - <span data-ttu-id="57983-113">NOTIFY_ACCT_DELETED</span><span class="sxs-lookup"><span data-stu-id="57983-113">NOTIFY_ACCT_DELETED</span></span>
    
   - <span data-ttu-id="57983-114">NOTIFY_ACCT_ORDER_CHANGED</span><span class="sxs-lookup"><span data-stu-id="57983-114">NOTIFY_ACCT_ORDER_CHANGED</span></span> 
    
   - <span data-ttu-id="57983-115">NOTIFY_ACCT_PREDELETED</span><span class="sxs-lookup"><span data-stu-id="57983-115">NOTIFY_ACCT_PREDELETED</span></span> 
    
 <span data-ttu-id="57983-116">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="57983-116">_dwAcctID_</span></span>
  
> <span data-ttu-id="57983-117">in Die Konto-ID des Kontos, das erstellt, geändert, gelöscht oder vorab gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="57983-117">[in] The account ID of the account that has been created, changed, deleted, or pre-deleted.</span></span>
    
 <span data-ttu-id="57983-118">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="57983-118">_dwFlags_</span></span>
  
>  <span data-ttu-id="57983-119">in Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="57983-119">[in] Not used.</span></span> <span data-ttu-id="57983-120">OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.</span><span class="sxs-lookup"><span data-stu-id="57983-120">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="57983-121">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="57983-121">Return values</span></span>

<span data-ttu-id="57983-122">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="57983-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57983-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57983-123">See also</span></span>

- [<span data-ttu-id="57983-124">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="57983-124">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="57983-125">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="57983-125">IOlkAccountManager</span></span>](iolkaccountmanager.md)

