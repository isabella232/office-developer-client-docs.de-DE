---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Gibt ein Array von Bytes, die das Symbol für das soziale Netzwerk darstellt.
ms.openlocfilehash: b86a2d1c14c444ba79db495a3795dc61b1fe3660
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796105"
---
# <a name="isocialprovidersocialnetworkicon"></a>ISocialProvider::SocialNetworkIcon

Gibt ein Array von Bytes, die das Symbol für das soziale Netzwerk darstellt. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine Struktur, die ein Array von Bytes angibt, das das Symbol für das soziale Netzwerk enthält.
  
## <a name="remarks"></a>Hinweise

Die unterstützten Bild Ressourcen sind BMP, JPEG und PNG-Dateiformate.
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

