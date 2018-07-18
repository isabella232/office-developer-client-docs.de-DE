---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Ruft eine Zeichenfolge, die vom Anbieterfunktionen beschreibt.
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795975"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Ruft eine Zeichenfolge, die vom Anbieterfunktionen beschreibt.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameter

_Ergebnis_
  
> [out] Eine XML-Zeichenfolge, die die Funktionen von einem Anbieter Outlook Social Connector (OSC) darstellt.
    
## <a name="remarks"></a>Bemerkungen

Die zurückgegebene _Ergebnis_ -XML-Zeichenfolge muss die Schemadefinition für das **Capabilities** -Element gemäß Definition im XML-Schema für die Erweiterbarkeit des OSC-Providers entsprechen. 
  
Der Anbieter muss eine Zeichenfolge _Ergebnis_ , um nachfolgende Aufrufe aus der OSC an den Anbieter ordnungsgemäß ermöglichen zurück. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

