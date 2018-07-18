---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Gibt eine Zeichenfolge, die den Namen für soziale Netzwerke darstellt.
ms.openlocfilehash: 78424db0940b2c23914355b2b20ba5bc531ad3ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795979"
---
# <a name="isocialprovidersocialnetworkname"></a>ISocialProvider::SocialNetworkName

Gibt eine Zeichenfolge, die den Namen für soziale Netzwerke darstellt. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die den Namen für soziale Netzwerke enthält.
  
## <a name="remarks"></a>Bemerkungen

Outlook Social Connector (OSC)-Anbieter sollte den Namen für soziale Netzwerke zu lokalisieren.
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

