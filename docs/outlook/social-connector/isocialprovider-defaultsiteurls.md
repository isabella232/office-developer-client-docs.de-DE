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
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Gibt ein Array von Zeichenfolgen, die Website-URLs für den Anbieter Outlook Social Connector (OSC) angeben.
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine Struktur, die ein Array von Zeichenfolgen gibt an, die Website-URLs für den OSC-Anbieter darstellen.
  
## <a name="remarks"></a>Hinweise

Ein Anbieter kann mehrere Website-URLs unterstützen. Die OSC wird die [ISocialSession::SiteUrl](isocialsession-siteurl.md) -Eigenschaft, um den Anbieter für die ausgewählte Website-URL zu informieren. 
  
Die OSC wird das erste Element des Arrays als den Standard-URL der Website verwendet. Ein Anbieter kann zusätzliche Elemente in der Website-URL-Array zurückgeben, aber die OSC nicht verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

