---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439856"
---
# <a name="newmail_notification"></a>NEWMAIL_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt Informationen, die sich auf das Eintreffen einer neuen Nachricht beziehen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a>Elemente

 **cbEntryID**
  
> Anzahl der Bytes in der Eintrags-ID, auf die das **lpEntryID-Element** verweist. 
    
 **lpEntryID**
  
> Zeiger auf die Eintrags-ID der neu eingetroffenen Nachricht.
    
 **cbParentID**
  
> Anzahl der Bytes in der Eintrags-ID, auf die das **lpParentID-Element** verweist. 
    
 **lpParentID**
  
> Zeiger auf die Eintrags-ID des Empfangsordners für die neu eingetroffene Nachricht.
    
 **ulFlags**
  
> Bitmaske von Flags, die verwendet werden, um das Format der Zeichenfolgeneigenschaften zu beschreiben, die in der Nachricht enthalten sind. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 **lpszMessageClass**
  
> Zeiger auf die Nachrichtenklasse der neu eingetroffenen Nachricht. 
    
 **ulMessageFlags**
  
> Bitmaske von Flags, die den aktuellen Status der neu eingetroffenen Nachricht beschreibt. Das **ulMessageFlags-Element** ist eine Kopie der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft der Nachricht.
    
## <a name="remarks"></a>Hinweise

Die **NEWMAIL_NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **info-Element** der [NOTIFICATION-Struktur enthalten](notification.md) ist. Wenn das **Infom** member einer **NOTIFICATION-Struktur** eine NEWMAIL_NOTIFICATION **enthält,** wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf  _fnevNewMail festgelegt._
  
MAPI verwendet die **NEWMAIL_NOTIFICATION** nur als Mitglied der **NOTIFICATION-Struktur,** die Informationen zu einem Benachrichtigungsereignis für die Hinweissenke enthält. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Hier erfahren Sie, wie Dienstanbieter die [IMAPISupport-Methode](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

