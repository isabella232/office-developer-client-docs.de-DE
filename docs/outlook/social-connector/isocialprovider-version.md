---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Gibt eine Zeichenfolge, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt.
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285385"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="2c7ea-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="2c7ea-103">ISocialProvider::Version</span></span>

<span data-ttu-id="2c7ea-104">Gibt eine Zeichenfolge, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="2c7ea-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="2c7ea-105">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2c7ea-105">Property value</span></span>

<span data-ttu-id="2c7ea-106">Eine Zeichenfolge, die die Versionsnummer des Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="2c7ea-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c7ea-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c7ea-107">Remarks</span></span>

<span data-ttu-id="2c7ea-108">Die Versionszeichenfolge sollte den _"MajorVersion"_ verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c7ea-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="2c7ea-109">_MinorVersion_ -Format (beispielsweise 1,4730).</span><span class="sxs-lookup"><span data-stu-id="2c7ea-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c7ea-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c7ea-110">See also</span></span>

- [<span data-ttu-id="2c7ea-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c7ea-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

