---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Gibt eine Zeichenfolge zurück, die den Namen des sozialen Netzwerks darstellt.
ms.openlocfilehash: 400765e72567bb5e24bf806c279a02619ccefaa9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574517"
---
# <a name="isocialprovidersocialnetworkname"></a>ISocialProvider::SocialNetworkName

Gibt eine Zeichenfolge zurück, die den Namen des sozialen Netzwerks darstellt. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die den Namen des sozialen Netzwerks enthält.
  
## <a name="remarks"></a>HinwBemerkungeneise

Outlook Osc-Anbieter (Social Connector) sollten den Namen des sozialen Netzwerks lokalisieren.
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

