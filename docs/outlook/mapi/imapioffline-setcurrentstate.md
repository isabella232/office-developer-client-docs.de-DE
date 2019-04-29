---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421739"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt den aktuellen Status eines Offline Objekts auf Online oder offline fest.
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Ändert das Verhalten dieses Aufrufs. Die folgenden Werte werden unterstützt:
    
MAPIOFFLINE_FLAG_BLOCK
  
> Wenn Sie _ulFlags_ auf diesen Wert festlegen, wird der **SetCurrentState** -Aufruf blockiert, bis die Statusänderung abgeschlossen ist. Standardmäßig erfolgt der Übergang asynchron. Wenn der Übergang asynchron erfolgt, werden alle **SetCurrentState** -Aufrufe **E_PENDING** zurückgegeben, bis die Änderung abgeschlossen ist. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Legt den aktuellen Status ohne Blockierung fest.
    
 _ulMask_
  
> in Der Teil des zu ändernden Status. Der einzige unterstützte Wert ist MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulState_
  
> in Der Zustand, in den gewechselt werden soll. Es muss einer der folgenden Werte sein:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _Beibehalten_
  
> Dieser Parameter ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Status des Offline Objekts wurde erfolgreich geändert.
    
E_PENDING
  
> Dies gibt an, dass der Status des Offline Objekts asynchron geändert wird. Dies tritt auf, wenn _ulFlags_ in einem früheren **SetCurrentState** -Aufruf auf MAPIOFFLINE_FLAG_BLOCK festgelegt ist und jeder nachfolgende **SetCurrentState** -Aufruf diesen Wert zurückgibt, bis die asynchrone Statusänderung abgeschlossen ist. 
    
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[MAPI-Konstanten](mapi-constants.md)

