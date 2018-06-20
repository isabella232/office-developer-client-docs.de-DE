---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Zuletzt geändert: 20 Februar 2012'
ms.openlocfilehash: dd7d310c8e801ba1246a0ce948aced9fa6a1a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793274"
---
# <a name="mnlsisbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**Betrifft**: Outlook 
  
Überprüft, ob ein Zeiger auf eine Breite Zeichenfolge gültig ist.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Ein Zeiger auf die Breite Zeichenfolge.
    
 _ucchMax_
  
> [in] Die maximale Länge der Zeichenfolge in Zeichen einschließlich.
    
## <a name="return-value"></a>R�ckgabewert

Gibt einen booleschen Wert, der True, wenn die Zeichenfolge beschädigt ist.
  
## <a name="remarks"></a>Hinweise

Diese Funktion umschließt [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx). Weitere Informationen finden Sie unter [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).
  

