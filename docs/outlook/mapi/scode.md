---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 781d0a0485740f5f13175307a5d5c6939d7d71fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586761"
---
# <a name="scode"></a>SCODE

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein 32-Bit-Statuswert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>HinwBemerkungeneise

Der **SCODE-Datentyp** ist identisch mit dem [HRESULT-Datentyp.](hresult.md) 
  
Ein **SCODE-Wert** ist in vier Felder unterteilt: 
  
- Ein Single-Bit-Schweregradcode, der auf 0 festgelegt ist, um den Erfolg anzuzeigen, und 1, um einen Fehler anzugeben.
    
- Ein reserviertes 11-Bit-Feld
    
- Ein 4-Bit-Einrichtungscode, der den Bereich angibt, der für den Fehler oder die Warnung verantwortlich ist.
    
- Ein 16-Bit-Fehler- oder Warnungscode, der das Problem beschreibt, das den Fehler oder die Warnung verursacht.
    
Viele der MAPI-Funktionen und -Methoden geben **SCODE-Werte** zurück, die als **HRESULT-Datentypen** definiert sind, ebenso wie die OLE-Methoden und -Funktionen. OLE definiert mehrere Makros, die zum Konvertieren zwischen einem **SCODE** und einem **HRESULT** verwendet werden können.
  
> [!NOTE]
> In der 64-Bit-MAPI ist **SCODE** immer noch ein 32-Bit-Wert. 
  
Weitere Informationen dazu, wie MAPI den **SCODE-Datentyp** verwendet, finden Sie unter [Fehlerbehandlung.](error-handling-in-mapi.md) Weitere Informationen zu OLE und dem **SCODE-Datentyp** finden Sie in der *OLE-Programmierreferenz.* 
  
## <a name="see-also"></a>Siehe auch



[[HRESULT]](hresult.md)


[MAPI-Datentypen](mapi-data-types.md)

