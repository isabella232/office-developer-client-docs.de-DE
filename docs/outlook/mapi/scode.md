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
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430133"
---
# <a name="scode"></a>SCODE

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein 32-Bit-Statuswert, der zum Beschreiben eines Fehlers oder einer Warnung verwendet wird. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>Hinweise

Der **SCODE-Datentyp** ist identisch mit dem [HRESULT-Datentyp.](hresult.md) 
  
Ein **SCODE-Wert** ist in vier Felder unterteilt: 
  
- Ein Ein-Bit-Schweregradcode, der auf 0 festgelegt ist, um den Erfolg anzuzeigen, und 1, um einen Fehler anzuzeigen.
    
- Ein reserviertes 11-Bit-Feld
    
- Ein 4-Bit-Einrichtungscode, der den Bereich angibt, der für den Fehler oder die Warnung verantwortlich ist.
    
- Ein 16-Bit-Fehler oder Warnungscode, der das Problem beschreibt, das den Fehler oder die Warnung verursacht.
    
Viele der MAPI-Funktionen und -Methoden geben **SCODE-Werte** zurück, die als **HRESULT-Datentypen** definiert sind, ebenso wie die OLE-Methoden und -Funktionen. OLE definiert mehrere Makros, die zum Konvertieren zwischen einem **SCODE** und einem **HRESULT verwendet werden können.**
  
> [!NOTE]
> In 64-Bit-MAPI ist **SCODE** weiterhin ein 32-Bit-Wert. 
  
Weitere Informationen dazu, wie MAPI den **SCODE-Datentyp** verwendet, finden Sie unter [Error Handling](error-handling-in-mapi.md). Weitere Informationen zu OLE und dem **SCODE-Datentyp** finden Sie unter  *OLE Programmer's Reference*  . 
  
## <a name="see-also"></a>Siehe auch



[[HRESULT]](hresult.md)


[MAPI-Datentypen](mapi-data-types.md)

