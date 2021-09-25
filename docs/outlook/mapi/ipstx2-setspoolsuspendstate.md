---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9b8205a0d73ac1cd3c49adecdede282e97dca685
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556287"
---
# <a name="ipstx2setspoolsuspendstate"></a>IPSTX2::SetSpoolSuspendState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt den Angehalten-Zustand für den Spooler fest.
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a>Parameter

 _ulState_
  
> [in] Der Zustand, auf den der Spooler festgelegt werden soll. Es muss einer der folgenden Werte sein:
    
 **SS_ACTIVE**
  
> 
    
 **SS_SUSPENDED**
  
> 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Konstanten](mapi-constants.md)

