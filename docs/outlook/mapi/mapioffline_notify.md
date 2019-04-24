---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c5480a8f5e008c01c7ab8141317f5f19547ab10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270294"
---
# <a name="mapiofflinenotify"></a>MAPIOFFLINE_NOTIFY

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dies ist die Benachrichtigung für eine Änderung im Verbindungsstatus. Er gibt den Teil des Verbindungsstatus an, der geändert wurde, den alten Verbindungsstatus und den neuen Verbindungsstatus.
  
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

## <a name="members"></a>Elemente

 _ulSize_
  
> Größe der **MAPIOFFLINE_NOTIFY** -Struktur. 
    
 _Notifytype_
  
> Typ der Benachrichtigung. Beachten Sie, dass nur Benachrichtigungen zur Änderung des Verbindungsstatus unterstützt werden. die einzigen unterstützten Werte sind:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Ein vom Client definiertes Token in der **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** -Struktur in **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**. 
    
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
    
## <a name="remarks"></a>Bemerkungen

Die Offline Status-API unterstützt nur Benachrichtigungen für Online-und Offlineänderungen. Ein Client muss prüfen, ob Outlook die folgenden Werte zurückgibt, bevor die tatsächliche Änderung untersucht wird:
  
1.  *Notifytype* hat den Wert MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE oder MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. In diesem Fall kann der Client davon ausgehen, dass die Änderung eine Verbindungsstatusänderung ist und *Info* der Struktur *StateChange* ist. 
    
2.  *ulMask* hat den Wert MAPIOFFLINE_STATE_OFFLINE_MASK. In diesem Fall kann der Client davon ausgehen, dass es sich bei der Änderung um eine Online/Offline-Verbindungsstatusänderung handelt und die Untersuchung von *ulStateOld* und *ulStateNew* fortgesetzt werden kann. 
    
Es ist möglich, dass Outlook einen Client über andere Änderungen benachrichtigt, die nicht unterstützt werden. In solchen Fällen wäre *notifytype* keiner der drei zuvor angegebenen Werte, oder *ULMASK* wäre nicht MAPIOFFLINE_STATE_OFFLINE_MASK, und der Client muss die restlichen Daten in *Info* ignorieren. 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zur Offlinestatus-API](about-the-offline-state-api.md)  
- [MAPI-Konstanten](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

