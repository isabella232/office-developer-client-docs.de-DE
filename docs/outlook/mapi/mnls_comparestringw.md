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
ms.openlocfilehash: f7889a255e2aa8ea4b6908f2f10a7b546a8ee3f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793265"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Gebietsschema-ID. Ausführliche Definitionen finden Sie unter der Parameter _Locale_ der [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [in] Kennzeichen, die Groß-/Kleinschreibung und diakritische Zeichen ignorieren. Ausführliche Definitionen finden Sie unter den _DwCmpFlags_ -Parameter der [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.
    
 _cch1_
  
> [in] Länge in Zeichen der ersten Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen. Die Anwendung kann einen negativen Wert bereitstellen, wenn die Zeichenfolge Null endende ist. In diesem Fall bestimmt die **MNLS_CompareStringW** -Funktion die Länge automatisch. 
    
 _pstr2_
  
> [in] Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.
    
 _cch2_
  
> [in] Die Länge des zweiten Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen in Zeichen. Die Anwendung kann einen negativen Wert bereitstellen, wenn die Zeichenfolge Null endende ist. In diesem Fall bestimmt die Funktion die Länge automatisch.
    
## <a name="return-value"></a>R�ckgabewert

Gibt die Werte für [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)beschrieben.
  
## <a name="remarks"></a>Hinweise

Diese Funktion umschließt [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** weist die gleichen Parameter und hat die gleiche Wirkung wie [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

