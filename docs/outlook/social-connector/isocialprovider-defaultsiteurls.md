---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den Anbieter Outlook Connector für soziale Netzwerke (OSC) angeben.
ms.openlocfilehash: bbdd30265c45ea140361149ecc97f5678beb54b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629144"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den Anbieter Outlook Connector für soziale Netzwerke (OSC) angeben.
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine Struktur, die ein Array von Zeichenfolgen angibt, die Website-URLs für den OSC-Anbieter darstellen.
  
## <a name="remarks"></a>Bemerkungen

Ein Anbieter kann mehrere Website-URLs unterstützen. Der OSC legt die [ISocialSession::SiteUrl-Eigenschaft](isocialsession-siteurl.md) fest, um den Anbieter über die ausgewählte Website-URL zu informieren. 
  
Das OSC verwendet das erste Element des Arrays als Standardwebsite-URL. Ein Anbieter kann zusätzliche Elemente im Website-URL-Array zurückgeben, aber der OSC verwendet sie nicht. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

