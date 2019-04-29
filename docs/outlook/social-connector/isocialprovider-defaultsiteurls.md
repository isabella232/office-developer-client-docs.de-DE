---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den Outlook Social Connector (OSC)-Anbieter angeben.
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413773"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="5bd75-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="5bd75-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="5bd75-104">Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den Outlook Social Connector (OSC)-Anbieter angeben.</span><span class="sxs-lookup"><span data-stu-id="5bd75-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="5bd75-105">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5bd75-105">Property value</span></span>

<span data-ttu-id="5bd75-106">Ein Zeiger auf eine Struktur, die ein Array von Zeichenfolgen angibt, die Website-URLs für den OSC-Anbieter darstellen.</span><span class="sxs-lookup"><span data-stu-id="5bd75-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5bd75-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bd75-107">Remarks</span></span>

<span data-ttu-id="5bd75-108">Ein Anbieter kann mehrere Website-URLs unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5bd75-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="5bd75-109">OSC legt die [ISocialSession:: siteurl](isocialsession-siteurl.md) -Eigenschaft fest, um den Anbieter über die ausgewählte Website-URL zu informieren.</span><span class="sxs-lookup"><span data-stu-id="5bd75-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="5bd75-110">OSC verwendet das erste Element des Arrays als Standardwebsite-URL.</span><span class="sxs-lookup"><span data-stu-id="5bd75-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="5bd75-111">Ein Anbieter kann zusätzliche Elemente im URL-Array der Website zurückgeben, aber der OSC verwendet Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="5bd75-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5bd75-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bd75-112">See also</span></span>

- [<span data-ttu-id="5bd75-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bd75-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

