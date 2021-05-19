---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Letzte Änderung: 21. Februar 2012'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338465"
---
# <a name="mnls_lstrlenw"></a>MNLS_lstrlenW

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Länge der angegebenen Unicode-Zeichenfolge, mit Ausnahme des endenden Nullzeichens.
  
> [!TIP]
> Erwägen Sie stattdessen die Verwendung von [StringCchLength.](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Die zu überprüfende Nullend-Unicode-Zeichenfolge.
    
## <a name="return-value"></a>Rückgabewert

Die Funktion gibt eine ganze Zahl mit der Länge der Zeichenfolge zurück. Es handelt sich um eine Anzahl von Zeichen in der Zeichenfolge, mit Ausnahme des endenden Nullzeichens. Wenn  _lpsz_ NULL ist, gibt die Funktion Null zurück. 
  
## <a name="remarks"></a>Hinweise

Diese Funktion umschließt die **lstrlen-Funktion.** Weitere Informationen finden Sie unter [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

