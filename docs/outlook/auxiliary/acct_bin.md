---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Eine Variable dieses Datentyps enthält einen Binärwert.
ms.openlocfilehash: 3dcaaf73a04ddc608e68ca7bd1f801d0a5d99bb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408124"
---
# <a name="acctbin"></a>ACCT_BIN

Eine Variable dieses Datentyps enthält einen Binärwert.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a>Elemente

_cb_
  
> Die Anzahl der Bytes, auf die _PB_ verweist. 
    
_pb_
  
> Zeiger auf Binärinformationen.
    

