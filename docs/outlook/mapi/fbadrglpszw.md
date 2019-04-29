---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436440"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft alle Zeichenfolgen in einem Array von Unicode-Zeichenfolgen. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>Parameter

 _lppszW_
  
> in Zeiger auf ein Array von null-terminierten Unicode-Zeichenfolgen. 
    
 _cStrings_
  
> in Anzahl der Zeichenfolgen im Array, auf die durch den _lppszW_ -Parameter verwiesen wird. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Mindestens eine der Zeichenfolgen im angegebenen Array ist ungültig. 
    
FALSE 
  
> Die Zeichenfolgen im angegebenen Array sind gültig.
    

