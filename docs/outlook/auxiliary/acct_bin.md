---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Eine Variable dieses Datentyps enthält einen binären Wert.
ms.openlocfilehash: 8299230a30b65ef8fb7856dc74618dd15ae218ac
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061335"
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
  
> Die Anzahl der Bytes,  _auf die pb_ zeigt. 
    
_pb_
  
> Zeiger auf binäre Informationen.
    

