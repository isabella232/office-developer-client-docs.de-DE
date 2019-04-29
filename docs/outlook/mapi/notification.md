---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432877"
---
# <a name="notification"></a>NOTIFICATION
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem aufgetretenen Ereignis und den Daten, die vom Ereignis betroffen waren.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a>Members

**ulEventType**
  
> Typ des aufgetretenen Benachrichtigungsereignisses. Der Wert des **ulEventType** -Elements entspricht der Struktur, die in der **Info** -Union enthalten ist. Das **ulEventType** -Element kann auf einen der folgenden Werte festgelegt werden: 
    
 _fnevCriticalError_
  
> Ein globaler Fehler ist aufgetreten, beispielsweise eine Sitzung wurde ausgeführt. Der **Info** -Member enthält eine [ERROR_NOTIFICATION](error_notification.md) -Struktur. 
    
 _fnevExtended_
  
> Ein internes Ereignis, das von einem bestimmten Dienstanbieter definiert wurde, ist aufgetreten. Der **Info** -Member enthält eine [EXTENDED_NOTIFICATION](extended_notification.md) -Struktur. 
    
 _Uleventmaskfnevnewmail_
  
> Eine Nachricht wurde an den entsprechenden Empfänger Ordner für die Nachrichtenklasse übermittelt und wartet auf die Verarbeitung. Der **Info** -Member enthält eine [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur. 
    
 _fnevObjectCopied_
  
> Ein MAPI-Objekt wurde kopiert. Der **Info** -Member enthält eine [OBJECT_NOTIFICATION](object_notification.md) -Struktur. 
    
 _fnevObjectCreated_
  
> Es wurde ein MAPI-Objekt erstellt. Der **Info** -Member enthält eine **OBJECT_NOTIFICATION** -Struktur. 
    
 _fnevObjectDeleted_
  
> Ein MAPI-Objekt wurde gelöscht. Der **Info** -Member enthält eine **OBJECT_NOTIFICATION** -Struktur. 
    
 _fnevObjectModified_
  
> Ein MAPI-Objekt wurde geändert. Der **Info** -Member enthält eine **OBJECT_NOTIFICATION** -Struktur. 
    
 _fnevObjectMoved_
  
> Ein Nachrichtenspeicher-oder Adressbuchobjekt wurde verschoben. Der **Info** -Member enthält eine **OBJECT_NOTIFICATION** -Struktur. 
    
 _fnevSearchComplete_
  
> Ein Suchvorgang wurde abgeschlossen, und die Ergebnisse sind verfügbar. Der **Info** -Member enthält eine **OBJECT_NOTIFICATION** -Struktur. 
    
 _fnevTableModified_
  
> Informationen in einer Tabelle wurden geändert. Der **Info** -Member enthält eine [TABLE_NOTIFICATION](table_notification.md) -Struktur. 
    
**info**
  
> Vereinigung von Benachrichtigungs Strukturen, die die betroffenen Daten für einen bestimmten Ereignistyp beschreiben. Die im **Info** -Element enthaltene Struktur hängt vom Wert des **ulEventType** -Members ab. 
    
## <a name="remarks"></a>Bemerkungen

Mindestens eine **Benachrichtigungs** Struktur wird bei jedem Aufruf der [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode einer registrierten Advise-Senke als Eingabeparameter übergeben. Die **Benachrichtigungs** Strukturen enthalten Informationen zu den bestimmten Ereignissen, die aufgetreten sind, und beschreiben die betroffenen Objekte. 
  
Bevor Clients oder Dienstanbieter, die eine Benachrichtigung erhalten, die Struktur zum Verarbeiten des Ereignisses verwenden können, müssen Sie den Ereignistyp wie im **ulEventType** -Element angegeben überprüfen. Das Codebeispiel, das hier gezeigt wird, prüft beispielsweise, ob eine neue Nachricht eingeht, und gibt die Nachrichtenklasse der Nachricht aus, wenn ein solches Ereignis ermittelt wird. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollen.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI-Strukturen](mapi-structures.md)

