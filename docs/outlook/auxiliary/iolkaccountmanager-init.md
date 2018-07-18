---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialisiert den Kontomanager für die Verwendung.
ms.openlocfilehash: 621c6a73ab2bcbdff17b87ce15af8b4e0c2e1e24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791089"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="32eb5-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="32eb5-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="32eb5-104">Initialisiert den Kontomanager für die Verwendung.</span><span class="sxs-lookup"><span data-stu-id="32eb5-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="32eb5-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="32eb5-105">Quick info</span></span>

<span data-ttu-id="32eb5-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="32eb5-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="32eb5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="32eb5-107">Parameters</span></span>

<span data-ttu-id="32eb5-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="32eb5-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="32eb5-109">[in] Eine [IOlkAccountHelper](iolkaccounthelper.md) -Schnittstelle, die Konto Hilfsfunktionen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="32eb5-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="32eb5-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="32eb5-110">_dwFlags_</span></span>
  
> <span data-ttu-id="32eb5-111">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="32eb5-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="32eb5-112">**ACCT_INIT_NO_STORES_CHECK** – verhindert, dass ein Konto (beispielsweise ein IMAP-Konto) synchronisieren mit einer zugeordneten Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="32eb5-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="32eb5-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** – verhindert, dass MAPI-Dienste nicht mit Konten synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="32eb5-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
    
   - <span data-ttu-id="32eb5-114">**OLK_ACCOUNT_NO_FLAGS** – synchronisiert MAPI-Dienste mit Konten.</span><span class="sxs-lookup"><span data-stu-id="32eb5-114">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="32eb5-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="32eb5-115">Return values</span></span>

|<span data-ttu-id="32eb5-116">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="32eb5-116">**HRESULT**</span></span>|<span data-ttu-id="32eb5-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32eb5-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32eb5-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="32eb5-118">S_OK</span></span>  <br/> |<span data-ttu-id="32eb5-119">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="32eb5-119">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="32eb5-120">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="32eb5-120">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="32eb5-121">**"Init"** wurde bereits aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="32eb5-121">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="32eb5-122">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="32eb5-122">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="32eb5-123">Konto-Manager konnte die erforderlichen Registrierungseinträge nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="32eb5-123">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32eb5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32eb5-124">Remarks</span></span>

<span data-ttu-id="32eb5-125">Der Client muss **IOlkAccountManager::Init** zum Initialisieren des Kontos aufrufen Manager vor der Nutzung des Konto-Managers auf Konten zugreifen oder Benachrichtigungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="32eb5-125">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="32eb5-126">Da MAPI-Dienste mit Konten beim Starten von Outlook automatisch synchronisiert werden, verwenden Sie **ACCT_INIT_NOSYNCH_MAPI_ACCTS** , es sei denn, es eine bestimmte Ursache ist zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="32eb5-126">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="32eb5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32eb5-127">See also</span></span>

- [<span data-ttu-id="32eb5-128">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="32eb5-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

