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
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386348"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="return-value"></a>Rückgabewert

Gibt die Werte für einen entsprechenden Aufruf **MNLS_CompareStringW** außer CSTR_EQUAL beschrieben. 
  
## <a name="remarks"></a>Hinweise

 _MNLS_lstrcmpW_ führt einen Vergleich durch Aufrufen von [MNLS_CompareStringW](mnls_comparestringw.md) mit der GetUserDefaultLCID, 0 für Flags, die ein Gebietsschema und-1 für cch1 und cch2. 
  
## <a name="see-also"></a>Siehe auch



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

