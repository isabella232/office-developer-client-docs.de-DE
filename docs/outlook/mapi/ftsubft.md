---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408418"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Subtrahiert eine unsignierte 64-Bit-Ganzzahl von einem anderen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Parameter

 _Minuend_
  
> in Eine [FILETIME](filetime.md) -Struktur, die die unsignierte 64-Bit-Ganzzahl enthält, aus der der Wert im _Subtrahend_ -Parameter subtrahiert werden soll. 
    
 _Subtrahend_
  
> in Eine **FILETIME** -Struktur mit der unsignierten 64-Bit-Ganzzahl, die von dem vom _Minuend_ -Parameter angegebenen Wert subtrahiert wird. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtSubFt** -Funktion gibt **** eine FILETIME-Struktur zurück, die das Ergebnis der Subtraktion enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

