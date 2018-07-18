---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6cd9dfe8fabd1ae7a4389550c628fb7ceff09ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795450"
---
# <a name="scode"></a>SCODE

**Betrifft**: Outlook 
  
Eine 32-Bit Statuswert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>Bemerkungen

Der Datentyp **SCODE** ist identisch mit der [HRESULT](hresult.md) -Datentyp. 
  
Ein **SCODE** -Wert wird in vier Felder unterteilt: 
  
- Ein Einzel-Bit Schweregradcode, der auf 0 festgelegt ist, um Erfolg und 1 Fehler anzuzeigen.
    
- Ein reserviertes 11-Bit-Feld
    
- Ein 4-Bit-Facility-Code, der den Bereich verantwortlich für die Fehlermeldung oder einer Warnung angibt.
    
- Eine 16-Bit-Fehler oder eine Warnung Code, der das Problem beschreibt, das den Fehler verursacht oder einer Warnung.
    
Viele der MAPI-Funktionen und Methoden zurückgeben **SCODE** -Werte als **HRESULT** -Datentypen definiert, wie die OLE-Methoden und Funktionen. OLE definiert verschiedene Makros, die für die Konvertierung zwischen **SCODE** und ein **HRESULT**verwendet werden können.
  
> [!NOTE]
> In 64-Bit-MAPI ist **SCODE** noch ein 32-Bit-Wert. 
  
Weitere Informationen dazu, wie den **SCODE** -Datentyp in MAPI verwendet werden finden Sie unter [Fehlerbehandlung](error-handling-in-mapi.md). Weitere Informationen zu OLE und den Datentyp **SCODE** finden Sie unter der *OLE Programmer's Reference* . 
  
## <a name="see-also"></a>Siehe auch



[[HRESULT]](hresult.md)


[MAPI-Datentypen](mapi-data-types.md)

