---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Gibt eine GUID, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.
ms.openlocfilehash: fc96799ada773cc7260e156d3e2ab8423b73884b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407872"
---
# <a name="isocialprovidersocialnetworkguid"></a><span data-ttu-id="758ef-103">ISocialProvider::SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="758ef-103">ISocialProvider::SocialNetworkGuid</span></span>

<span data-ttu-id="758ef-104">Gibt eine GUID, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="758ef-104">Returns a GUID that represents a unique identifier for the social network.</span></span>
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a><span data-ttu-id="758ef-105">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="758ef-105">Property value</span></span>

<span data-ttu-id="758ef-106">Ein Zeiger auf einen GUID-Wert, der einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="758ef-106">A pointer to a GUID value that represents a unique identifier for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="758ef-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="758ef-107">Remarks</span></span>

<span data-ttu-id="758ef-108">Die GUID muss unveränderlich sein und darf auch dann nicht geändert werden, wenn sich die Anbieterversion ändert.</span><span class="sxs-lookup"><span data-stu-id="758ef-108">The GUID must be immutable and must not change even if the provider version changes.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="758ef-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="758ef-109">See also</span></span>

- [<span data-ttu-id="758ef-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="758ef-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

