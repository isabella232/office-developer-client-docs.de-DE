---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Zuletzt geändert: 20 Februar 2012'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396211"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
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
  
> [in] Gebietsschema-ID. Ausführliche Definitionen finden Sie unter der Parameter _Locale_ der [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [in] Kennzeichen, die Groß-/Kleinschreibung und diakritische Zeichen ignorieren. Ausführliche Definitionen finden Sie unter den _DwCmpFlags_ -Parameter der [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.
    
 _cch1_
  
> [in] Länge in Zeichen der ersten Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen. Die Anwendung kann einen negativen Wert bereitstellen, wenn die Zeichenfolge Null endende ist. In diesem Fall bestimmt die **MNLS_CompareStringW** -Funktion die Länge automatisch. 
    
 _pstr2_
  
> [in] Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.
    
 _cch2_
  
> [in] Die Länge des zweiten Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen in Zeichen. Die Anwendung kann einen negativen Wert bereitstellen, wenn die Zeichenfolge Null endende ist. In diesem Fall bestimmt die Funktion die Länge automatisch.
    
## <a name="return-value"></a>Rückgabewert

Gibt die Werte für [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)beschrieben.
  
## <a name="remarks"></a>Hinweise

Diese Funktion umschließt [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** weist die gleichen Parameter und hat die gleiche Wirkung wie [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

