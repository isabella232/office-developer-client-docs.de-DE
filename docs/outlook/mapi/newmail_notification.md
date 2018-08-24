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
ms.openlocfilehash: 779585f73a7032ae0259b30ebfc16868c733c7fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569512"
---
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt die Informationen, die über den Eingang einer neuen Nachricht beziehen. 
  
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
  
> Anzahl der Bytes in die Eintrags-ID auf den Member **LpEntryID** zeigt. 
    
 **lpEntryID**
  
> Zeiger auf die Eintrags-ID der neu empfangene Meldung.
    
 **cbParentID**
  
> Anzahl der Bytes in die Eintrags-ID auf den Member **LpParentID** zeigt. 
    
 **lpParentID**
  
> Zeiger auf die Eintrags-ID des Ordners für die neu empfangene Nachricht empfangen.
    
 **ulFlags**
  
> Bitmaske aus Flags verwendet, um das Format der Zeichenfolgeneigenschaften der Nachricht enthaltene beschreiben. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 **lpszMessageClass**
  
> Zeiger auf die Nachrichtenklasse der neu empfangene Meldung. 
    
 **ulMessageFlags**
  
> Bitmaske aus Flags, die den aktuellen Status der neu empfangene Nachricht beschreibt. Der **UlMessageFlags** -Member ist eine Kopie der Nachricht **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft.
    
## <a name="remarks"></a>Bemerkungen

Die **NEWMAIL_NOTIFICATION** -Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten. Wenn das **Info** Mitglied einer **Benachrichtigung** Struktur eine **NEWMAIL_NOTIFICATION** Struktur enthält, das **UlEventType** Mitglied der **Benachrichtigung** Struktur auf festgelegt ist _FnevNewMail._
  
MAPI verwendet die **NEWMAIL_NOTIFICATION** -Struktur nur als Mitglied der **Benachrichtigung** -Struktur, die Informationen zu einem Benachrichtigungsereignis für die Advise-Empfänger enthält. 
  
Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.  <br/> |
|[Unterstützen von Ereignisbenachrichtigungen](supporting-event-notification.md) <br/> |Erläuterung der wie-Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

