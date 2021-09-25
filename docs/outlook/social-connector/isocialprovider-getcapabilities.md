---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Ruft eine Zeichenfolge ab, die die Anbieterfunktionen beschreibt.
ms.openlocfilehash: d0c6772d38d0bdf6d1c6d3b482eb0dc7b70f7f50
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574510"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Ruft eine Zeichenfolge ab, die die Anbieterfunktionen beschreibt.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameter

_result_
  
> [out] Eine XML-Zeichenfolge, die die Funktionen eines anbieters für den Outlook Connector für soziale Netzwerke (SOCIAL Connector, OSC) darstellt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die  zurückgegebene ERGEBNIS-XML-Zeichenfolge muss der Schemadefinition für das **Capabilities-Element** entsprechen, wie im XML-Schema für die OSC-Anbietererweiterung definiert. 
  
Der Anbieter muss eine  _Ergebniszeichenfolge_ zurückgeben, damit nachfolgende Aufrufe von OSC an den Anbieter ordnungsgemäß ausgeführt werden können. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

