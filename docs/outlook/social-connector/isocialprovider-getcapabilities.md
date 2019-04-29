---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Ruft eine Zeichenfolge ab, die die Anbieter Funktionen beschreibt.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408103"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Ruft eine Zeichenfolge ab, die die Anbieter Funktionen beschreibt.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameter

_result_
  
> Out Eine XML-Zeichenfolge, die die Funktionen eines Outlook Social Connector (OSC)-Anbieters darstellt.
    
## <a name="remarks"></a>Bemerkungen

Die zurückgegebene _Ergebnis_ -XML-Zeichenfolge muss der Schema Definition für das **Capabilities** -Element entsprechen, wie im XML-Schema für osc-Anbieter Erweiterbarkeit definiert. 
  
Der Anbieter muss eine _Ergebnis_ Zeichenfolge zurückgeben, damit nachfolgende Aufrufe vom osc an den Anbieter ordnungsgemäß ausgeführt werden können. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

