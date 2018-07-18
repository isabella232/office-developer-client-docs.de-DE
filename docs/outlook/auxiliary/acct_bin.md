---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Eine Variable dieses Typs Daten enthält einen Binärwert an.
ms.openlocfilehash: 6816fd21a51b86bda97353034e959685f22ff176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790934"
---
# <a name="acctbin"></a>ACCT_BIN

Eine Variable dieses Typs Daten enthält einen Binärwert an.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a>Elemente

_cb_
  
> Anzahl von Bytes, die auf _pb_ verweist. 
    
_pb_
  
> Zeiger auf binäre Informationen.
    

