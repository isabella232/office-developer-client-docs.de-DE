---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Gibt eine Zeichenfolge zurück, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt.
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438274"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Gibt eine Zeichenfolge zurück, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die die Versionsnummer des Anbieters enthält.
  
## <a name="remarks"></a>Hinweise

Die Versionszeichenfolge sollte _majorVersion verwenden._ _MinorVersion-Format_ (z. B. 1.4730). 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

