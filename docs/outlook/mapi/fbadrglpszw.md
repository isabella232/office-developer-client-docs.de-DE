---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2d677c6d4e1eb416e5dabf466f24d9b77c48c03e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621115"
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
  
> [in] Zeiger auf ein Array von Unicode-Zeichenfolgen, die mit Null terminiert sind. 
    
 _cStrings_
  
> [in] Anzahl der Zeichenfolgen in dem Array, auf das der  _lppszW-Parameter_ verweist. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Eine oder mehrere Zeichenfolgen im angegebenen Array sind ungültig. 
    
FALSE 
  
> Die Zeichenfolgen im angegebenen Array sind gültig.
    

