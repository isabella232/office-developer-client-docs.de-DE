---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Zuletzt geändert: 18 Juni 2012'
ms.openlocfilehash: 8ffd3c8337edcd96af6c3c4e425d274b21fee9f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793267"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**Betrifft**: Outlook 
  
Vergleicht zwei Unicode-Zeichenfolgen.
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>Parameter

 _lpString1_
  
> [in] Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.
    
 _lpString2_
  
> [in] Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.
    
## <a name="return-value"></a>R�ckgabewert

Gibt die Werte für einen entsprechenden Aufruf **MNLS_CompareStringW** außer CSTR_EQUAL beschrieben. 
  
## <a name="remarks"></a>Hinweise

 _MNLS_lstrcmpW_ führt einen Vergleich durch Aufrufen von [MNLS_CompareStringW](mnls_comparestringw.md) mit der GetUserDefaultLCID, 0 für Flags, die ein Gebietsschema und-1 für cch1 und cch2. 
  
## <a name="see-also"></a>Siehe auch



[GetUserDefaultLCID](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)

