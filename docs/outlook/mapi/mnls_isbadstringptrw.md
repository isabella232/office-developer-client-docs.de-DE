---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Letzte Änderung: 20. Februar 2012'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356854"
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
  
> [in] Ein Zeiger auf die breite Zeichenzeichenfolge.
    
 _ucchMax_
  
> [in] Die maximale Länge der Zeichenfolge in Zeichen einschließlich Abschlusszeichen.
    
## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Typ Boolean zurück, der true ist, wenn die Zeichenfolge ungültig ist.
  
## <a name="remarks"></a>Hinweise

Diese Funktion umschließt [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx). Weitere Informationen finden Sie unter [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).
  

