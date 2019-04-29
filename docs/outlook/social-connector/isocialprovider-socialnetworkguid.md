---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Gibt eine GUID, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.
ms.openlocfilehash: fc96799ada773cc7260e156d3e2ab8423b73884b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407872"
---
# <a name="isocialprovidersocialnetworkguid"></a>ISocialProvider::SocialNetworkGuid

Gibt eine GUID, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen GUID-Wert, der einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.
  
## <a name="remarks"></a>Bemerkungen

Die GUID muss unveränderlich sein und darf auch dann nicht geändert werden, wenn sich die Anbieterversion ändert.
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

