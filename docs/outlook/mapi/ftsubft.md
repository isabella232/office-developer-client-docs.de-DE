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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 954630b0b92772d961dc61084c28a9ab419e4c2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791769"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Betrifft**: Outlook 
  
Eine 64-Bit-Ganzzahl von einem anderen subtrahiert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Parameter

 _Minuend_
  
> [in] Ein [FILETIME](filetime.md) -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen enthält, von der der Wert in der _Subtrahend_ -Parameter ist, subtrahiert werden soll. 
    
 _Subtrahend_
  
> [in] Ein **FILETIME** -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen enthält, die von dem Wert, der durch den Parameter _Minuend_ subtrahiert wird. 
    
## <a name="return-value"></a>R�ckgabewert

Die **FtSubFt** -Funktion gibt eine **FILETIME** -Struktur, die das Ergebnis der Subtraktion enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

