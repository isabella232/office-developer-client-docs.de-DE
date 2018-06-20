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
ms.openlocfilehash: 5ff10d51fab03c3bca3eead52848088f2cd80bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795994"
---
# <a name="isocialprovidersocialnetworkguid"></a>ISocialProvider::SocialNetworkGuid

Gibt eine GUID, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf ein GUID-Wert, der einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.
  
## <a name="remarks"></a>Hinweise

Die GUID muss unveränderlich sein und darf nicht geändert werden, auch wenn die Anbieterversion wird geändert.
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

