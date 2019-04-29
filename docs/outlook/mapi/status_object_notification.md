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
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Statusobjekt, das von einer Änderung betroffen ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpEntryID** -Element verwiesen wird. 
    
 **lpEntryID**
  
> Zeiger auf die Eintrags-ID des geänderten Status Objekts.
    
 **cValues**
  
> Die Anzahl der [SPropValue](spropvalue.md) -Strukturen im Array, auf die vom **lpPropVals** -Element verwiesen wird. 
    
 **lpPropVals**
  
> Zeiger auf ein Array von **SPropValue** -Strukturen, die die Eigenschaften des geänderten Status-Objekts beschreiben. 
    
## <a name="remarks"></a>Bemerkungen

Die **STATUS_OBJECT_NOTIFICATION** -Struktur ist ein Mitglied der Vereinigung von Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind. Die **STATUS_OBJECT_NOTIFICATION** -Struktur ist in einer Status Objekt Benachrichtigung für ein Ereignis vom Typ _fnevStatusObjectModified_enthalten. Status Objekt Benachrichtigung ist eine interne MAPI-Benachrichtigung; Clients und Dienstanbieter können sich nicht für IT registrieren, und Dienstanbieter können Sie nicht generieren.
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollen.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

