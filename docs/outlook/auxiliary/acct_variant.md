---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Eine Variable dieses Typs Daten enthält den Wert einer Eigenschaft, die einen variant-Datentyp ist.
ms.openlocfilehash: c85af4bd4fefffb4fadf671bb7cf5b7f072d5e95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790926"
---
# <a name="acctvariant"></a>ACCT_VARIANT

Eine Variable dieses Typs Daten enthält den Wert einer Eigenschaft, die einen variant-Datentyp ist.
  
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

## <a name="members"></a>Members

_dwType_
  
> Typ Variante:
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_dw_
  
> DWORD-Wert von Variant-Wert.
    
_pwsz_
  
> String-Wert von Variant-Wert.
    
_Papierkorb_
  
> Binärer Wert der Variante.
    

