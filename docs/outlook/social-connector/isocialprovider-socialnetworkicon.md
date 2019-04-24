---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Gibt ein Bytearray zurück, das das Symbol für das soziale Netzwerk darstellt.
ms.openlocfilehash: c63d9996d4478c8ce7e46210aae34791bcfe9222
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285498"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="c4819-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="c4819-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="c4819-104">Gibt ein Bytearray zurück, das das Symbol für das soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4819-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="c4819-105">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c4819-105">Property value</span></span>

<span data-ttu-id="c4819-106">Ein Zeiger auf eine Struktur, die ein Bytearray angibt, das das Symbol für das soziale Netzwerk enthält.</span><span class="sxs-lookup"><span data-stu-id="c4819-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4819-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4819-107">Remarks</span></span>

<span data-ttu-id="c4819-108">Die unterstützten Bildressourcen sind BMP-, JPEG-und PNG-Formate.</span><span class="sxs-lookup"><span data-stu-id="c4819-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c4819-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4819-109">See also</span></span>

- [<span data-ttu-id="c4819-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4819-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

