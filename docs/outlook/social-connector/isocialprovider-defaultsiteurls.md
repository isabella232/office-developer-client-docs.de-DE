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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285856"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den Outlook Social Connector (OSC)-Anbieter angeben.
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine Struktur, die ein Array von Zeichenfolgen angibt, die Website-URLs für den OSC-Anbieter darstellen.
  
## <a name="remarks"></a>Bemerkungen

Ein Anbieter kann mehrere Website-URLs unterstützen. OSC legt die [ISocialSession:: siteurl](isocialsession-siteurl.md) -Eigenschaft fest, um den Anbieter über die ausgewählte Website-URL zu informieren. 
  
OSC verwendet das erste Element des Arrays als Standardwebsite-URL. Ein Anbieter kann zusätzliche Elemente im URL-Array der Website zurückgeben, aber der OSC verwendet Sie nicht. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

