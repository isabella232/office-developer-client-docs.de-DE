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
ms.openlocfilehash: 4d3210c098d0a7c83721798c8c32ffd9f1e5ebb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575462"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Kopiert eine Zeichenfolge in einen Puffer.
  
> [!CAUTION]
> Nicht verwenden. Erwägen Sie [StringCchCopy hin](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) . 
  
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
    
## <a name="return-value"></a>R�ckgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Puffer.
  
Wenn die Funktion fehlschlägt, wird NULL zurückgegeben und lpString1 möglicherweise nicht Null endende.
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion umschließt die **Lstrcpy** -Funktion. Weitere Informationen finden Sie unter [Lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

