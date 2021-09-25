---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Eine Variable dieses Datentyps enthält den Wert einer Eigenschaft, die einen Variant-Datentyp aufweist.
ms.openlocfilehash: 07b6280d7f2dd710375fe59a1811fdd3bb87b695
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621171"
---
# <a name="acct_variant"></a>ACCT_VARIANT

Eine Variable dieses Datentyps enthält den Wert einer Eigenschaft, die einen Variant-Datentyp aufweist.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct 
    { 
        DWORD dwType; 
        union  
            { 
            DWORD dw; 
            WCHAR *pwsz; 
            ACCT_BIN bin; 
            } Val; 
    } ACCT_VARIANT; 

```

## <a name="members"></a>Elemente

_für "wettertype"_
  
> Typ der Variante:
    
  - PT_LONG
  - PT_UNICODE
  - PT_BINARY
    
_Dw_
  
> DWORD-Wert der Variante.
    
_pwsz_
  
> Zeichenfolgenwert der Variante.
    
_Bin_
  
> Binärer Wert der Variante.
    

