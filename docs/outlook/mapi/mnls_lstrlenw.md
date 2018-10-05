---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Zuletzt geändert: 21 Februar 2012'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392088"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Länge der angegebenen Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen.
  
> [!TIP]
> Erwägen Sie [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) . 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Die Null terminierte Unicode-Zeichenfolge überprüft werden soll.
    
## <a name="return-value"></a>Rückgabewert

Die Funktion gibt eine ganze Zahl mit der Länge der Zeichenfolge zurück. Es ist die Anzahl der Zeichen in der Zeichenfolge, ausgenommen abschließende Null-Zeichen. Wenn _Lpsz_ NULL ist, gibt die Funktion 0 (null) zurück. 
  
## <a name="remarks"></a>Hinweise

Diese Funktion umschließt die **Lstrlen** -Funktion. Weitere Informationen finden Sie unter [Lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

