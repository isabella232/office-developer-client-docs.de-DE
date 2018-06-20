---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9d8eb3f2c52f20ffe57d84823a0ed736337b4d9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793139"
---
# <a name="mapiofflinenotify"></a>MAPIOFFLINE_NOTIFY

**Betrifft**: Outlook 
  
Hierbei handelt es sich um die Benachrichtigung für eine Änderung in den Verbindungsstatus. Es gibt den Teil des Verbindungsstatus, der geändert wurde, den alten Verbindungsstatus und den neuen Verbindungsstatus.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
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
  
> Größe der Struktur **MAPIOFFLINE_NOTIFY** . 
    
 _NotifyType_
  
> Typ der Benachrichtigung. Beachten Sie, dass nur Benachrichtigung über die Änderung der Verbindungsstatus unterstützt wird. Die einzigen unterstützten Werte sind:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Ein Token vom Client in der Struktur **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** definiert. 
    
 _ulMask_
  
> Der Teil der Status der Verbindung, der sich geändert hat. Der einzige unterstützte Wert ist MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulStateOld_
  
> Die alte Verbindungsstatus. Die einzigen unterstützten Werte sind:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> Die neue Verbindungsstatus. Die einzigen unterstützten Werte sind:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>Hinweise

Die Offline Zustand API unterstützt nur Benachrichtigungen für Online-/offline geändert wird. Ein Client muss überprüfen, dass Outlook die folgenden Werte zurückgibt, bevor Sie die eigentliche Änderung untersuchen:
  
1.  *NotifyType* hat den Wert MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE oder MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. In diesem Fall kann der Client wird vorausgesetzt, dass die Änderung eine Verbindung Zustand ist und *Info* der Struktur *StateChange* ist. 
    
2.  *UlMask* hat den Wert MAPIOFFLINE_STATE_OFFLINE_MASK. In diesem Fall kann der Client wird vorausgesetzt, dass die Änderung eine Änderung der Verbindung online/offline-Status ist, und mit *UlStateOld* und *UlStateNew* untersuchen fortfahren kann. 
    
Es ist möglich, dass Outlook einen Client weitere Änderungen darüber informiert werden, die nicht unterstützt werden. In solchen Fällen *NotifyType* wäre nicht eine der drei Werte zuvor erwähnt oder *UlMask* wäre nicht MAPIOFFLINE_STATE_OFFLINE_MASK, und der Client muss den Rest der Daten in *Info* ignorieren. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Offline State-API](about-the-offline-state-api.md)  
- [MAPI-Konstanten](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

