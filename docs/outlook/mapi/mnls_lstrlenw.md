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
ms.openlocfilehash: 70c15970ce69e4bc075da6bf55320cb23116b7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793297"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**Betrifft**: Outlook 
  
Bestimmt die Länge der angegebenen Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen.
  
> [!TIP]
> Erwägen Sie [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) . 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Die Null terminierte Unicode-Zeichenfolge überprüft werden soll.
    
## <a name="return-value"></a>R�ckgabewert

Die Funktion gibt eine ganze Zahl mit der Länge der Zeichenfolge zurück. Es ist die Anzahl der Zeichen in der Zeichenfolge, ausgenommen abschließende Null-Zeichen. Wenn _Lpsz_ NULL ist, gibt die Funktion 0 (null) zurück. 
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion umschließt die **Lstrlen** -Funktion. Weitere Informationen finden Sie unter [Lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

