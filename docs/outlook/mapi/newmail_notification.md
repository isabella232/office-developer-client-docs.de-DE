---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 78fcf2e6ed088f391cf02c755b3f356464c8312e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561229"
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Anzahl der Bytes im Eintragsbezeichner, auf den der **lpEntryID-Member** verweist. 
    
 **lpEntryID**
  
> Zeiger auf den Eintragsbezeichner der neu empfangenen Nachricht.
    
 **cbParentID**
  
> Anzahl der Bytes im Eintragsbezeichner, auf den der **lpParentID-Member** verweist. 
    
 **lpParentID**
  
> Zeiger auf den Eintragsbezeichner des Empfangsordners für die neu empfangene Nachricht.
    
 **ulFlags**
  
> Bitmaske mit Flags, die verwendet werden, um das Format der zeichenfolgeneigenschaften zu beschreiben, die in der Nachricht enthalten sind. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 **lpszMessageClass**
  
> Zeiger auf die Nachrichtenklasse der neu empfangenen Nachricht. 
    
 **ulMessageFlags**
  
> Bitmaske von Flags, die den aktuellen Status der neu empfangenen Nachricht beschreibt. Der **ulMessageFlags-Member** ist eine Kopie der **eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **NEWMAIL_NOTIFICATION** Struktur ist eines der Mitglieder der Vereinigung von Strukturen, die im **Infoelement** der [NOTIFICATION-Struktur](notification.md) enthalten sind. Wenn das **Infoelement** einer **NOTIFICATION-Struktur** eine **NEWMAIL_NOTIFICATION** Struktur enthält, wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf  _fnevNewMail festgelegt._
  
MAPI verwendet die **NEWMAIL_NOTIFICATION** Struktur nur als Element der **NOTIFICATION-Struktur,** die Informationen zu einem Benachrichtigungsereignis für die Empfehlungssenke enthält. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die [IMAPISupport-Methode](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

