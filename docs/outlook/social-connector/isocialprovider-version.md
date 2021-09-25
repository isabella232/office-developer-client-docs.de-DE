---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Gibt eine Zeichenfolge zurück, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt.
ms.openlocfilehash: 5f3e285d4a22f667eaef6008982057673dfcbcd0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629123"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Gibt eine Zeichenfolge zurück, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die die Versionsnummer des Anbieters enthält.
  
## <a name="remarks"></a>Bemerkungen

Die Versionszeichenfolge sollte die  _MajorVersion_ verwenden. _MinorVersion-Format_ (z. B. 1,4730). 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

