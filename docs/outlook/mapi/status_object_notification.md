---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426268"
---
# <a name="status_object_notification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Statusobjekt, das von einer Änderung betroffen ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a>Elemente

 **cbEntryID**
  
> Anzahl der Bytes in der Eintrags-ID, auf die das **lpEntryID-Element** verweist. 
    
 **lpEntryID**
  
> Zeiger auf die Eintrags-ID des geänderten Statusobjekts.
    
 **cValues**
  
> Anzahl der [SPropValue-Strukturen](spropvalue.md) im Array, auf das das **lpPropVals-Element verweist.** 
    
 **lpPropVals**
  
> Zeiger auf ein Array von **SPropValue-Strukturen,** die die Eigenschaften des geänderten Statusobjekts beschreiben. 
    
## <a name="remarks"></a>Hinweise

Die **STATUS_OBJECT_NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **info-Element** der [NOTIFICATION-Struktur enthalten](notification.md) ist. Die **STATUS_OBJECT_NOTIFICATION** ist in einer Statusobjektbenachrichtigung für ein Ereignis vom Typ _fnevStatusObjectModified enthalten._ Status-Objektbenachrichtigung ist eine interne #A0 Clients und Dienstanbieter können sich nicht dafür registrieren, und Dienstanbieter können sie nicht generieren.
  
Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Hier erfahren Sie, wie Dienstanbieter die **IMAPISupport-Methode** zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

