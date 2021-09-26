---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: 5f77c8457563212335255ec5bd9b76e689ffe757
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620429"
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
  
> [in] Gebietsschemabezeichner. Ausführliche Definitionen finden Sie im _Parameter "Locale"_ von [CompareString.](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
    
 _Dwflags_
  
> [in] Kennzeichen, um Groß- und Kleinschreibung und diakritische Zeichen zu ignorieren. Ausführliche Definitionen finden Sie im _Parameter "wetterCmpFlags"_ von [CompareStringEx.](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)
    
 _pstr1_
  
> [in] Zeiger auf die erste Unicode-Zeichenfolge, die verglichen werden soll.
    
 _cch1_
  
> [in] Länge in Zeichen der ersten Unicode-Zeichenfolge, mit Ausnahme des endenden NULL-Zeichens. Die Anwendung kann einen negativen Wert angeben, wenn die Zeichenfolge mit NULL beendet wird. In diesem Fall bestimmt die **funktion MNLS_CompareStringW** automatisch die Länge. 
    
 _pstr2_
  
> [in] Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.
    
 _cch2_
  
> [in] Länge in Zeichen der zweiten Unicode-Zeichenfolge, mit Ausnahme des endenden NULL-Zeichens. Die Anwendung kann einen negativen Wert angeben, wenn die Zeichenfolge mit NULL beendet wird. In diesem Fall bestimmt die Funktion automatisch die Länge.
    
## <a name="return-value"></a>Rückgabewert

Gibt die für [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)beschriebenen Werte zurück.
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion umschließt [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** verwendet dieselben Parameter und hat das gleiche Verhalten wie [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

