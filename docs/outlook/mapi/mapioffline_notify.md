---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ea1238b128eeffe460240b835384a1055c11a287
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575470"
---
# <a name="mapioffline_notify"></a>MAPIOFFLINE_NOTIFY

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dies ist die Benachrichtigung für eine Änderung des Verbindungsstatus. Es gibt den Teil des Geänderten Verbindungszustands, den alten Verbindungsstatus und den neuen Verbindungsstatus an.
  
## <a name="quick-info"></a>QuickInfo

Siehe **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a>Members

 _ulSize_
  
> Größe der **MAPIOFFLINE_NOTIFY** Struktur. 
    
 _NotifyType_
  
> Typ der Benachrichtigung. Beachten Sie, dass nur eine Benachrichtigung über die Änderung des Verbindungsstatus unterstützt wird. Die einzigen unterstützten Werte sind:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Ein Token, das vom Client in der **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** Struktur in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** definiert wird. 
    
 _ulMask_
  
> Der Teil des Verbindungsstatus, der geändert wurde. Der einzige unterstützte Wert ist MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulStateOld_
  
> Der alte Verbindungsstatus. Die einzigen unterstützten Werte sind:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> Der neue Verbindungsstatus. Die einzigen unterstützten Werte sind:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Offlinestatus-API unterstützt nur Benachrichtigungen für Online-/Offlineänderungen. Ein Client muss überprüfen, ob Outlook die folgenden Werte zurückgibt, bevor die tatsächliche Änderung untersucht wird:
  
1.  *NotifyType*  hat den Wert MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE oder MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. In diesem Fall kann der Client davon ausgehen, dass es sich bei der Änderung um eine Änderung des Verbindungsstatus handelt, und  *Info*  ist der Struktur  *StateChange*  . 
    
2.  *ulMask*  hat den Wert MAPIOFFLINE_STATE_OFFLINE_MASK. In diesem Fall kann der Client davon ausgehen, dass es sich bei der Änderung um eine Änderung des Online-/Offlineverbindungsstatus handelt, und mit der Untersuchung von  *ulStateOld*  und  *ulStateNew*  fortfahren. 
    
Es ist möglich, dass Outlook einen Client über andere Änderungen benachrichtigt, die nicht unterstützt werden. In solchen Fällen wäre  *NotifyType*  keiner der drei zuvor angegebenen Werte, oder  *ulMask*  wäre nicht MAPIOFFLINE_STATE_OFFLINE_MASK, und der Client muss die restlichen Daten in  *Info*  ignorieren. 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zur Offlinestatus-API](about-the-offline-state-api.md)  
- [MAPI-Konstanten](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

