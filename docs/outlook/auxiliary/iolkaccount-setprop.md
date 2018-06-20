---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Legt den Wert der Eigenschaft angegebene Konto.
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791056"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="1efca-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="1efca-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="1efca-104">Legt den Wert der Eigenschaft angegebene Konto.</span><span class="sxs-lookup"><span data-stu-id="1efca-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1efca-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="1efca-105">Quick info</span></span>

<span data-ttu-id="1efca-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="1efca-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="1efca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1efca-107">Parameters</span></span>

<span data-ttu-id="1efca-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="1efca-108">_dwProp_</span></span>
  
> <span data-ttu-id="1efca-109">[in] Die Eigenschaftstag der Konto-Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1efca-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="1efca-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="1efca-110">_pVar_</span></span>
  
> <span data-ttu-id="1efca-111">[in] Der Wert der angegebenen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1efca-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="1efca-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1efca-112">Return values</span></span>

|<span data-ttu-id="1efca-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="1efca-113">**HRESULT**</span></span>|<span data-ttu-id="1efca-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1efca-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1efca-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="1efca-115">S_OK</span></span>  <br/> |<span data-ttu-id="1efca-116">Methodenaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1efca-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="1efca-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1efca-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="1efca-118">Eine ungültige Eigenschafts-Tag angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1efca-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1efca-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1efca-119">Remarks</span></span>

<span data-ttu-id="1efca-120">Verwenden Sie [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) , um Änderungen auf den Wert der Eigenschaften von Benutzerkonten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1efca-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1efca-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1efca-121">See also</span></span>

- [<span data-ttu-id="1efca-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="1efca-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="1efca-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="1efca-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

