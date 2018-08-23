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
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578262"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  

