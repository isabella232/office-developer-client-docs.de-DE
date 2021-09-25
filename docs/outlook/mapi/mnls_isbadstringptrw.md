---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: 56c2d84cf883f2452e6aa9a2904478eb8e3ec190
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571402"
---
# <a name="mnls_isbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft, ob ein Zeiger auf eine breite Zeichenfolge gültig ist.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Ein Zeiger auf die breite Zeichenfolge.
    
 _ucchMax_
  
> [in] Die maximale Länge der Zeichenfolge in Zeichen einschließlich Abschlusszeichen.
    
## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Typ Boolean , der true ist, wenn die Zeichenfolge ungültig ist.
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion umschließt [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx). Weitere Informationen finden Sie unter [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).
  

