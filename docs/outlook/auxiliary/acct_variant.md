---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Eine Variable dieses Datentyps enthält den Wert einer Eigenschaft, die einen Variant-Datentyp hat.
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316919"
---
# <a name="acctvariant"></a>ACCT_VARIANT

Eine Variable dieses Datentyps enthält den Wert einer Eigenschaft, die einen Variant-Datentyp hat.
  
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
    
_DW_
  
> DWORD-Wert von Variant.
    
_Pwsz_
  
> Zeichenfolgenwert von Variant.
    
_bin_
  
> Binärwert des Variant-Werts.
    

