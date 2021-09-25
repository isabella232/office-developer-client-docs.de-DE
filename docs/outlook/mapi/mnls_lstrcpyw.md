---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Last modified: June 18, 2012'
ms.openlocfilehash: ad7323d02a8a3f080614f09b610175976cd4c01f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584038"
---
# <a name="mnls_lstrcpyw"></a>MNLS_lstrcpyW

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert eine Zeichenfolge in einen Puffer.
  
> [!CAUTION]
> Nicht verwenden. Erwägen Sie stattdessen die Verwendung von [StringCchCopy.](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Parameter

lpString1
  
> [out] Ein Puffer zum Empfangen des Inhalts der Zeichenfolge, auf die der parameter lpString2 verweist.
    
lpString2
  
> [in] Die zu kopierende Zeichenfolge mit NULL-Termin.
    
## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Puffer.
  
Wenn die Funktion fehlschlägt, ist der Rückgabewert NULL, und lpString1 wird möglicherweise nicht mit NULL beendet.
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion umschließt die **lstrcpy-Funktion.** Weitere Informationen finden Sie unter [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

