---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f5170ceb443dcde075440bf84d29000afe4680c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419870"
---
# <a name="imapiofflinegetcurrentstate"></a>IMAPIOffline::GetCurrentState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den aktuellen Online-oder Offlinestatus eines Offline Objekts ab.
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a>Parameter

 _pulState_
  
> Out Der aktuelle Online-oder Offlinestatus eines Offline Objekts. Es muss einer der folgenden Werte sein:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)


[MAPI-Konstanten](mapi-constants.md)

