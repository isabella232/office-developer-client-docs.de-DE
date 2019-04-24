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
# <a name="isocialprovidersocialnetworkicon"></a>ISocialProvider::SocialNetworkIcon

Gibt ein Bytearray zurück, das das Symbol für das soziale Netzwerk darstellt. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine Struktur, die ein Bytearray angibt, das das Symbol für das soziale Netzwerk enthält.
  
## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildressourcen sind BMP-, JPEG-und PNG-Formate.
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

