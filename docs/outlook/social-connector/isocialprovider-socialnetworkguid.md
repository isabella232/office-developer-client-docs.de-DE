---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Gibt eine GUID zurück, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.
ms.openlocfilehash: 3e8e4e4f4fc2ed0a1f853e3f7dee8796ef661805
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560333"
---
# <a name="isocialprovidersocialnetworkguid"></a>ISocialProvider::SocialNetworkGuid

Gibt eine GUID zurück, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen GUID-Wert, der einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die GUID muss unveränderlich sein und darf sich nicht ändern, auch wenn sich die Anbieterversion ändert.
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

