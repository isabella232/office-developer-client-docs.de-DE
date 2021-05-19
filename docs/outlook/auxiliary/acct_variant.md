---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Eine Variable dieses Datentyps enthält den Wert einer Eigenschaft, die einen Variant-Datentyp besitzt.
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424399"
---
# <a name="acct_variant"></a>ACCT_VARIANT

Eine Variable dieses Datentyps enthält den Wert einer Eigenschaft, die einen Variant-Datentyp besitzt.
  
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

_dwType_
  
> Typ der Variante:
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_dw_
  
> DWORD-Wert der Variante.
    
_pwsz_
  
> Zeichenfolgenwert von variant.
    
_bin_
  
> Binärwert der Variante.
    

