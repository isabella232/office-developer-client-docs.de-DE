---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Zuletzt geändert: 18, 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341727"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert eine Zeichenfolge in einen Puffer.
  
> [!CAUTION]
> Nicht verwenden. Verwenden Sie stattdessen [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) . 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Parameter

lpString1
  
> Out Ein Puffer zum Empfangen des Inhalts der Zeichenfolge, auf die durch den lpString2-Parameter verwiesen wird.
    
lpString2
  
> in Die zu kopierende Zeichenfolge mit NULL.
    
## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Puffer.
  
Wenn die Funktion fehlschlägt, ist der Rückgabewert NULL, und lpString1 darf nicht NULL-terminiert sein.
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion umschließt die **lstrcpy** -Funktion. Weitere Informationen finden Sie unter [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

