---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Ruft eine Zeichenfolge ab, die Anbieterfunktionen beschreibt.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408103"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Ruft eine Zeichenfolge ab, die Anbieterfunktionen beschreibt.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameter

_result_
  
> [out] Eine XML-Zeichenfolge, die die Funktionen eines Outlook Social Connector (OSC) darstellt.
    
## <a name="remarks"></a>Hinweise

Die zurückgegebene Ergebnis-XML-Zeichenfolge muss der Schemadefinition für das **Capabilities-Element** entsprechen, wie im XML-Schema für die Erweiterbarkeit des OSC-Anbieters definiert.  
  
Der Anbieter muss eine  _Ergebniszeichenfolge zurückgeben,_ damit nachfolgende Aufrufe vom OSC an den Anbieter ordnungsgemäß ausgeführt werden können. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

