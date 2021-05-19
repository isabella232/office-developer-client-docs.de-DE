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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414767"
---
# <a name="mapioffline_notify"></a>MAPIOFFLINE_NOTIFY

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dies ist die Benachrichtigung für eine Änderung des Verbindungsstatus. Er gibt den Teil des geänderten Verbindungsstatus, den alten Verbindungsstatus und den neuen Verbindungsstatus an.
  
## <a name="quick-info"></a>QuickInfo

Weitere Informationen finden Sie unter **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
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
  
> Größe der **MAPIOFFLINE_NOTIFY** Struktur. 
    
 _NotifyType_
  
> Typ der Benachrichtigung. Beachten Sie, dass nur Benachrichtigungen über die Änderung des Verbindungsstatus unterstützt werden. Die einzigen unterstützten Werte sind:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Ein vom Client in **[](mapioffline_adviseinfo.md)** der MAPIOFFLINE_ADVISEINFO in **[IMAPIOfflineMgr::Advise definiertes Token.](imapiofflinemgr-advise.md)** 
    
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
    
## <a name="remarks"></a>Hinweise

Die Offlinestatus-API unterstützt nur Benachrichtigungen für Online-/Offlineänderungen. Ein Client muss überprüfen, Outlook die folgenden Werte zurückgibt, bevor die tatsächliche Änderung untersucht wird:
  
1.  *NotifyType*  hat den Wert MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE oder MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. In diesem Fall kann der Client davon ausgehen, dass es sich bei der Änderung um eine Verbindungsstatusänderung handelt, und  *Info*  hat die Struktur  *StateChange*  . 
    
2.  *ulMask*  hat den Wert MAPIOFFLINE_STATE_OFFLINE_MASK. In diesem Fall kann der Client davon ausgehen, dass es sich bei der Änderung um eine Änderung des Online-/Offlineverbindungsstatus handelt, und er kann mit der Prüfung *von ulStateOld* und *ulStateNew fortfahren.* 
    
Es ist möglich, Outlook einen Client über andere Änderungen benachrichtigt, die nicht unterstützt werden. In solchen Fällen wäre *NotifyType* keiner der drei zuvor angegebenen Werte, oder *ulMask* wäre nicht MAPIOFFLINE_STATE_OFFLINE_MASK, und der Client muss die restlichen Daten in *Info ignorieren.* 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zur Offlinestatus-API](about-the-offline-state-api.md)  
- [MAPI-Konstanten](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

