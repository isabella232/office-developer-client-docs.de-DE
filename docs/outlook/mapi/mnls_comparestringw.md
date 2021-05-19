---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Letzte Änderung: 20. Februar 2012'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356847"
---
# <a name="mnls_comparestringw"></a>MNLS_CompareStringW

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Unicode-Zeichenfolgen.
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a>Parameter

 _lcid_
  
> [in] Locale-ID. Ausführliche Definitionen finden Sie im  _Parameter Locale_ von [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [in] Kennzeichen zum Ignorieren von Fall- und Diakritischen Zeichen. Ausführliche Definitionen finden Sie im  _parameter dwCmpFlags_ von [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.
    
 _cch1_
  
> [in] Länge in Zeichen der ersten Unicode-Zeichenfolge, mit Ausnahme des endenden Nullzeichens. Die Anwendung kann einen negativen Wert angeben, wenn die Zeichenfolge null-terminated ist. In diesem Fall bestimmt **die MNLS_CompareStringW** die Länge automatisch. 
    
 _pstr2_
  
> [in] Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.
    
 _cch2_
  
> [in] Länge in Zeichen der zweiten Unicode-Zeichenfolge, mit Ausnahme des endenden Nullzeichens. Die Anwendung kann einen negativen Wert angeben, wenn die Zeichenfolge null-terminated ist. In diesem Fall bestimmt die Funktion die Länge automatisch.
    
## <a name="return-value"></a>Rückgabewert

Gibt die für [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)beschriebenen Werte zurück.
  
## <a name="remarks"></a>Hinweise

Diese Funktion umschließt [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** verwendet dieselben Parameter und hat dasselbe Verhalten wie [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

