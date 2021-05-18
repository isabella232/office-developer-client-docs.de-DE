---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Ruft den Profilnamen eines Kontos ab.
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322106"
---
# <a name="iolkaccounthelpergetidentity"></a><span data-ttu-id="8adfb-103">IOlkAccountHelper::GetIdentity</span><span class="sxs-lookup"><span data-stu-id="8adfb-103">IOlkAccountHelper::GetIdentity</span></span>

<span data-ttu-id="8adfb-104">Ruft den Profilnamen eines Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="8adfb-104">Gets the profile name of an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8adfb-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="8adfb-105">Quick info</span></span>

<span data-ttu-id="8adfb-106">Siehe [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="8adfb-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a><span data-ttu-id="8adfb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8adfb-107">Parameters</span></span>

<span data-ttu-id="8adfb-108">_pwszIdentity_</span><span class="sxs-lookup"><span data-stu-id="8adfb-108">_pwszIdentity_</span></span>
  
> <span data-ttu-id="8adfb-109">[in] [out] Der Profilname.</span><span class="sxs-lookup"><span data-stu-id="8adfb-109">[in][out] The profile name.</span></span>
    
<span data-ttu-id="8adfb-110">_pcch_</span><span class="sxs-lookup"><span data-stu-id="8adfb-110">_pcch_</span></span>
  
> <span data-ttu-id="8adfb-111">[in] [out] Beim Aufrufen dieser Methode enthält die Größe (in Der Anzahl der Zeichen)  _von pwszIdentity,_ die zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8adfb-111">[in] [out] Upon calling this method, contains the size (in number of characters) of  _pwszIdentity_ that has been allocated.</span></span> <span data-ttu-id="8adfb-112">Enthält bei der Rückgabe die tatsächliche Länge des zurückgegebenen Profilnamens, einschließlich des 0-Endzeichens.</span><span class="sxs-lookup"><span data-stu-id="8adfb-112">Upon return, contains the actual length, including the 0-terminating character, of the returned profile name.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8adfb-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8adfb-113">Return values</span></span>

|<span data-ttu-id="8adfb-114">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="8adfb-114">**HRESULT**</span></span>|<span data-ttu-id="8adfb-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="8adfb-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8adfb-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8adfb-116">S_OK</span></span>  <br/> |<span data-ttu-id="8adfb-117">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8adfb-117">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="8adfb-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="8adfb-118">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="8adfb-119">Der zurückgegebene Profilname ist länger als die Größe von  _pwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="8adfb-119">The returned profile name is longer than the size of  _pwszIdentity_.</span></span>  <br/> |
|<span data-ttu-id="8adfb-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8adfb-120">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="8adfb-121">_pcch_ ist NULL.</span><span class="sxs-lookup"><span data-stu-id="8adfb-121">_pcch_ is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8adfb-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8adfb-122">Remarks</span></span>

<span data-ttu-id="8adfb-123">Wenn  _pwszIdentity_ zu klein ist, um den Profilnamen zu speichern, wird er bei rückgabe nicht festgelegt, und  _pcch_ wird auf die für  _pwszIdentity_ erforderliche Größe verweisen.</span><span class="sxs-lookup"><span data-stu-id="8adfb-123">If  _pwszIdentity_ is too small to hold the profile name, it will not be set on return, and  _pcch_ will point to the size required for  _pwszIdentity_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8adfb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8adfb-124">See also</span></span>

- [<span data-ttu-id="8adfb-125">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="8adfb-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="8adfb-126">PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="8adfb-126">PidTagProfileName</span></span>](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

