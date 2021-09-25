---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29fa50c92899ce0857a5a2934393c47b870e69ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567592"
---
# <a name="imapiofflinegetcurrentstate"></a>IMAPIOffline::GetCurrentState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den aktuellen Online- oder Offlinestatus eines Offlineobjekts ab.
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a>Parameter

 _pulState_
  
> [out] Der aktuelle Online- oder Offlinestatus eines Offlineobjekts. Es muss einer der folgenden beiden Werte sein:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)


[MAPI-Konstanten](mapi-constants.md)

