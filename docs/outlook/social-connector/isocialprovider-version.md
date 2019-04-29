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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438274"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="7e47c-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="7e47c-103">ISocialProvider::Version</span></span>

<span data-ttu-id="7e47c-104">Gibt eine Zeichenfolge, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="7e47c-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="7e47c-105">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7e47c-105">Property value</span></span>

<span data-ttu-id="7e47c-106">Eine Zeichenfolge, die die Versionsnummer des Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="7e47c-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7e47c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e47c-107">Remarks</span></span>

<span data-ttu-id="7e47c-108">Die Versionszeichenfolge sollte den _"MajorVersion"_ verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e47c-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="7e47c-109">_MinorVersion_ -Format (beispielsweise 1,4730).</span><span class="sxs-lookup"><span data-stu-id="7e47c-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e47c-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e47c-110">See also</span></span>

- [<span data-ttu-id="7e47c-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e47c-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

