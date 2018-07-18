---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Führt ein Commit für Änderungen an das Account-Objekt durch Schreiben der Registrierung gespeichert.
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791037"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="8ce4a-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8ce4a-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="8ce4a-104">Führt ein Commit für Änderungen an das Account-Objekt durch Schreiben der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8ce4a-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8ce4a-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="8ce4a-105">Quick info</span></span>

<span data-ttu-id="8ce4a-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="8ce4a-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="8ce4a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ce4a-107">Parameters</span></span>

<span data-ttu-id="8ce4a-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="8ce4a-108">_dwFlags_</span></span>
  
> <span data-ttu-id="8ce4a-109">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="8ce4a-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="8ce4a-110">OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.</span><span class="sxs-lookup"><span data-stu-id="8ce4a-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8ce4a-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8ce4a-111">Return values</span></span>

|<span data-ttu-id="8ce4a-112">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="8ce4a-112">**HRESULT**</span></span>|<span data-ttu-id="8ce4a-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ce4a-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ce4a-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ce4a-114">S_OK</span></span>  <br/> |<span data-ttu-id="8ce4a-115">Die Methode erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8ce4a-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="8ce4a-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8ce4a-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="8ce4a-117">Das angegebene Konto nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="8ce4a-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="8ce4a-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8ce4a-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="8ce4a-119">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="8ce4a-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ce4a-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8ce4a-120">Remarks</span></span>

<span data-ttu-id="8ce4a-121">Verwenden Sie nach dem Ändern des Werts der Eigenschaften von Benutzerkonten mithilfe von [IOlkAccount::SetProp](iolkaccount-setprop.md), **IOlkAccount::SaveChanges** , um derartige Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8ce4a-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ce4a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ce4a-122">See also</span></span>

- [<span data-ttu-id="8ce4a-123">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="8ce4a-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="8ce4a-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8ce4a-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

