---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c50b658a956b1ccbaccafb707c9b60ffa13747f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610916"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Subtrahiert eine nicht signierte 64-Bit-Ganzzahl von einer anderen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Parameter

 _Minuend_
  
> [in] Eine [FILETIME-Struktur,](filetime.md) die die 64-Bit-Ganzzahl ohne Vorzeichen enthält, von der der Wert im  _Subtrahend-Parameter subtrahend subtrahent_ werden soll. 
    
 _Subtrahend_
  
> [in] Eine **FILETIME-Struktur,** die die nicht signierte 64-Bit-Ganzzahl enthält, die von dem durch den  _Minuend-Parameter angegebenen_ Wert subtrahiert wird. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtSubFt-Funktion** gibt eine **FILETIME-Struktur** zurück, die das Ergebnis der Subtraktion enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

