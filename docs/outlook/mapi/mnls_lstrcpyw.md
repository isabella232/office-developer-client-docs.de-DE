---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Zuletzt geändert: 18 Juni 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382708"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert eine Zeichenfolge in einen Puffer.
  
> [!CAUTION]
> Nicht verwenden. Erwägen Sie [StringCchCopy hin](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) . 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Parameter

lpString1
  
> [out] Durch den Parameter lpString2 auf ein Puffer den Inhalt der Zeichenfolge empfängt das.
    
lpString2
  
> [in] Die Null endende Zeichenfolge kopiert werden soll.
    
## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Puffer.
  
Wenn die Funktion fehlschlägt, wird NULL zurückgegeben und lpString1 möglicherweise nicht Null endende.
  
## <a name="remarks"></a>Hinweise

Diese Funktion umschließt die **Lstrcpy** -Funktion. Weitere Informationen finden Sie unter [Lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

