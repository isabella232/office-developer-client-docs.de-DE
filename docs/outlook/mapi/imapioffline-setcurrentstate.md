---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96e00c3a5105a03f8869f893badcfc605b8ce6de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604901"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt den aktuellen Status eines Offlineobjekts auf "Online" oder "Offline" fest.
  
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
  
> [in] Ändert das Verhalten dieses Aufrufs. Die folgenden Werte werden unterstützt:
    
MAPIOFFLINE_FLAG_BLOCK
  
> Durch Festlegen von  _ulFlags_ auf diesen Wert wird der **SetCurrentState-Aufruf** blockiert, bis die Zustandsänderung abgeschlossen ist. Standardmäßig erfolgt der Übergang asynchron. Wenn der Übergang asynchron erfolgt, werden alle **SetCurrentState-Aufrufe** **E_PENDING** zurückgegeben, bis die Änderung abgeschlossen ist. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Legt den aktuellen Status ohne Blockierung fest.
    
 _ulMask_
  
> [in] Der Teil des Zustands, der geändert werden soll. Der einzige unterstützte Wert ist MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulState_
  
> [in] Der Zustand, in den geändert werden soll. Es muss einer der folgenden beiden Werte sein:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _Erhalten_
  
> Dieser Parameter ist für Outlook interne Verwendung reserviert und wird nicht unterstützt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Status des Offlineobjekts wurde erfolgreich geändert.
    
E_PENDING
  
> Dies gibt an, dass sich der Status des Offlineobjekts asynchron ändert. Dies tritt auf, wenn  _ulFlags_ in einem früheren **SetCurrentState-Aufruf** auf MAPIOFFLINE_FLAG_BLOCK festgelegt ist und jeder nachfolgende **SetCurrentState-Aufruf** diesen Wert zurückgibt, bis die asynchrone Zustandsänderung abgeschlossen ist. 
    
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[MAPI-Konstanten](mapi-constants.md)

