---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Last modified: June 18, 2012'
ms.openlocfilehash: da855762a601fdf28544cd75d50610f7964761c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575435"
---
# <a name="mnls_lstrcmpw"></a>MNLS_lstrcmpW

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Unicode-Zeichenfolgen.
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>Parameter

 _lpString1_
  
> [in] Zeiger auf die erste Unicode-Zeichenfolge, die verglichen werden soll.
    
 _lpString2_
  
> [in] Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.
    
## <a name="return-value"></a>Rückgabewert

Gibt die Werte zurück, die für einen gleichwertigen Aufruf **von MNLS_CompareStringW** mit Ausnahme von CSTR_EQUAL beschrieben wurden. 
  
## <a name="remarks"></a>HinwBemerkungeneise

 _MNLS_lstrcmpW_ führt einen Vergleich durch, indem [MNLS_CompareStringW](mnls_comparestringw.md) mit einem Gebietsschema von GetUserDefaultLCID, 0 für Flags und -1 für cch1 und cch2 aufgerufen wird. 
  
## <a name="see-also"></a>Siehe auch



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

