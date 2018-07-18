---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Ruft den Profilnamen eines Kontos ab.
ms.openlocfilehash: 81417282faa9ba0e7ec99990ac78045b54752acb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791091"
---
# <a name="iolkaccounthelpergetidentity"></a><span data-ttu-id="e2756-103">IOlkAccountHelper::GetIdentity</span><span class="sxs-lookup"><span data-stu-id="e2756-103">IOlkAccountHelper::GetIdentity</span></span>

<span data-ttu-id="e2756-104">Ruft den Profilnamen eines Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="e2756-104">Gets the profile name of an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e2756-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e2756-105">Quick info</span></span>

<span data-ttu-id="e2756-106">Finden Sie unter [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="e2756-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a><span data-ttu-id="e2756-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2756-107">Parameters</span></span>

<span data-ttu-id="e2756-108">_pwszIdentity_</span><span class="sxs-lookup"><span data-stu-id="e2756-108">_pwszIdentity_</span></span>
  
> <span data-ttu-id="e2756-109">[in] [out] Der Profilname.</span><span class="sxs-lookup"><span data-stu-id="e2756-109">[in][out] The profile name.</span></span>
    
<span data-ttu-id="e2756-110">_pcch_</span><span class="sxs-lookup"><span data-stu-id="e2756-110">_pcch_</span></span>
  
> <span data-ttu-id="e2756-111">[in] [out] Beim Aufrufen dieser Methode enthält die Größe (in Anzahl von Zeichen) der _PwszIdentity_ , der zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="e2756-111">[in] [out] Upon calling this method, contains the size (in number of characters) of  _pwszIdentity_ that has been allocated.</span></span> <span data-ttu-id="e2756-112">Bei der Rückgabe enthält die tatsächliche Länge, einschließlich des Zeichens 0 zum Abbruch des Namens zurückgegebene Profil.</span><span class="sxs-lookup"><span data-stu-id="e2756-112">Upon return, contains the actual length, including the 0-terminating character, of the returned profile name.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e2756-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e2756-113">Return values</span></span>

|<span data-ttu-id="e2756-114">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="e2756-114">**HRESULT**</span></span>|<span data-ttu-id="e2756-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2756-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2756-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2756-116">S_OK</span></span>  <br/> |<span data-ttu-id="e2756-117">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e2756-117">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="e2756-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="e2756-118">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="e2756-119">Der zurückgegebene Profilname ist länger als die Größe der _PwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="e2756-119">The returned profile name is longer than the size of  _pwszIdentity_.</span></span>  <br/> |
|<span data-ttu-id="e2756-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e2756-120">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="e2756-121">_Pcch_ ist NULL.</span><span class="sxs-lookup"><span data-stu-id="e2756-121">_pcch_ is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2756-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2756-122">Remarks</span></span>

<span data-ttu-id="e2756-123">Wenn _PwszIdentity_ zu klein, um den Profilnamen enthalten ist, wird bei der Rückgabe nicht festgelegt werden, und _Pcch_ verweist auf die Größe für _PwszIdentity_erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e2756-123">If  _pwszIdentity_ is too small to hold the profile name, it will not be set on return, and  _pcch_ will point to the size required for  _pwszIdentity_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2756-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2756-124">See also</span></span>

- [<span data-ttu-id="e2756-125">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="e2756-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="e2756-126">PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="e2756-126">PidTagProfileName</span></span>](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

