---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Zuletzt geändert: 18, 2012'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356840"
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
  
> in Zeiger auf die erste Unicode-Zeichenfolge, die verglichen werden soll.
    
 _lpString2_
  
> in Zeiger auf die zweite Unicode-Zeichenfolge, die verglichen werden soll.
    
## <a name="return-value"></a>Rückgabewert

Gibt die für einen äquivalenten Aufruf von **MNLS_CompareStringW** mit Ausnahme von CSTR_EQUAL beschriebenen Werte zurück. 
  
## <a name="remarks"></a>Bemerkungen

 _MNLS_lstrcmpW_ führt einen Vergleich durch Aufrufen von [MNLS_CompareStringW](mnls_comparestringw.md) mit einem Gebietsschema von GetUserDefaultLCID, 0 für Flags und-1 für Kmk1 und Kmk2 aus. 
  
## <a name="see-also"></a>Siehe auch



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

