---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Eine Variable dieses Datentyps enthält einen binären Wert.
ms.openlocfilehash: 315336db9a62c3ae7e56feb871bcd0b2f7971d48
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596649"
---
# <a name="acct_bin"></a>ACCT_BIN

Eine Variable dieses Datentyps enthält einen binären Wert.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    DWORD cb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a>Elemente

_cb_
  
> Anzahl der Bytes, auf die  _pb_ zeigt. 
    
_pb_
  
> Zeiger auf binäre Informationen.
    

