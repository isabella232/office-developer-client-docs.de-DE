---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialisiert den Konto-Manager für die Verwendung.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322036"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="b3f9a-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="b3f9a-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="b3f9a-104">Initialisiert den Konto-Manager für die Verwendung.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b3f9a-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b3f9a-105">Quick info</span></span>

<span data-ttu-id="b3f9a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="b3f9a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="b3f9a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3f9a-107">Parameters</span></span>

<span data-ttu-id="b3f9a-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="b3f9a-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="b3f9a-109">[in] Eine [IOlkAccountHelper-Schnittstelle,](iolkaccounthelper.md) die Kontohilfsfunktionen bietet.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="b3f9a-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="b3f9a-110">_dwFlags_</span></span>
  
> <span data-ttu-id="b3f9a-111">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="b3f9a-112">**ACCT_INIT_NO_STORES_CHECK** – Verhindert die Synchronisierung eines Kontos (z. B. eines IMAP-Kontos) mit einem zugeordneten Speicher.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="b3f9a-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** – Verhindert die Synchronisierung von MAPI-Diensten mit Konten.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
   
   - <span data-ttu-id="b3f9a-114">**ACCT_INIT_NO_NOTIFICATIONS** – Verhindert, dass der Account Manager Übertragungsnachrichten abfängt, die für andere Anwendungen vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-114">**ACCT_INIT_NO_NOTIFICATIONS** —Prevents the Account Manager from intercepting broadcast messages intended for other applications.</span></span> 
   
   - <span data-ttu-id="b3f9a-115">**OLK_ACCOUNT_NO_FLAGS** – Synchronisiert MAPI-Dienste mit Konten.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-115">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b3f9a-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b3f9a-116">Return values</span></span>

|<span data-ttu-id="b3f9a-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="b3f9a-117">**HRESULT**</span></span>|<span data-ttu-id="b3f9a-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="b3f9a-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3f9a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3f9a-119">S_OK</span></span>  <br/> |<span data-ttu-id="b3f9a-120">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="b3f9a-121">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="b3f9a-121">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="b3f9a-122">**Init** wurde bereits aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-122">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="b3f9a-123">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="b3f9a-123">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="b3f9a-124">Der Konto-Manager konnte nicht auf die erforderlichen Registrierungseinstellungen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-124">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3f9a-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3f9a-125">Remarks</span></span>

<span data-ttu-id="b3f9a-126">Der Client muss **IOlkAccountManager::Init** aufrufen, um den Konto-Manager zu initialisieren, bevor der Konto-Manager auf Konten zugreifen oder Benachrichtigungen einrichten kann.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-126">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="b3f9a-127">Da Outlook automatisch die MAPI-Dienste mit Konten  beim Start synchronisiert, verwenden Sie ACCT_INIT_NOSYNCH_MAPI_ACCTS es sei denn, es gibt eine bestimmte Ursache für die Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="b3f9a-127">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3f9a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3f9a-128">See also</span></span>

- [<span data-ttu-id="b3f9a-129">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="b3f9a-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

