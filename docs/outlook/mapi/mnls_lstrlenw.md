---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: 32d9dfef7a03c16998b007a1bddca49ed04118c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575407"
---
# <a name="mnls_lstrlenw"></a>MNLS_lstrlenW

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Länge der angegebenen Unicode-Zeichenfolge, mit Ausnahme des endenden NULL-Zeichens.
  
> [!TIP]
> Erwägen Sie stattdessen die Verwendung von [StringCchLength.](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Die unicode-Zeichenfolge, die mit NULL terminiert wird und überprüft werden soll.
    
## <a name="return-value"></a>Rückgabewert

Die Funktion gibt eine ganze Zahl mit der Länge der Zeichenfolge zurück. Es handelt sich um eine Anzahl von Zeichen in der Zeichenfolge, mit Ausnahme des endenden NULL-Zeichens. Wenn  _lpsz_ NULL ist, gibt die Funktion Null zurück. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion umschließt die **lstrlen-Funktion.** Weitere Informationen finden Sie unter [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

