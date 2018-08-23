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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f8ede3761ca10589c686e2ec4fac18fbe00fb2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588587"
---
# <a name="scode"></a>SCODE

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine 32-Bit Statuswert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>HinwBemerkungeneise

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

