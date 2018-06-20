---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Gibt ein Array von Zeichenfolgen, die Website-URLs für den Anbieter Outlook Social Connector (OSC) angeben.
ms.openlocfilehash: a2b2e0397c7c67476ac8067a53e2acbd4eddf270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795965"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="60c0e-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="60c0e-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="60c0e-104">Gibt ein Array von Zeichenfolgen, die Website-URLs für den Anbieter Outlook Social Connector (OSC) angeben.</span><span class="sxs-lookup"><span data-stu-id="60c0e-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="60c0e-105">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="60c0e-105">Property value</span></span>

<span data-ttu-id="60c0e-106">Ein Zeiger auf eine Struktur, die ein Array von Zeichenfolgen gibt an, die Website-URLs für den OSC-Anbieter darstellen.</span><span class="sxs-lookup"><span data-stu-id="60c0e-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60c0e-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60c0e-107">Remarks</span></span>

<span data-ttu-id="60c0e-108">Ein Anbieter kann mehrere Website-URLs unterstützen.</span><span class="sxs-lookup"><span data-stu-id="60c0e-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="60c0e-109">Die OSC wird die [ISocialSession::SiteUrl](isocialsession-siteurl.md) -Eigenschaft, um den Anbieter für die ausgewählte Website-URL zu informieren.</span><span class="sxs-lookup"><span data-stu-id="60c0e-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="60c0e-110">Die OSC wird das erste Element des Arrays als den Standard-URL der Website verwendet.</span><span class="sxs-lookup"><span data-stu-id="60c0e-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="60c0e-111">Ein Anbieter kann zusätzliche Elemente in der Website-URL-Array zurückgeben, aber die OSC nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="60c0e-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60c0e-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60c0e-112">See also</span></span>

- [<span data-ttu-id="60c0e-113">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="60c0e-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

