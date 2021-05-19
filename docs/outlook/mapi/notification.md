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
  
Enthält Informationen zu einem aufgetretenen Ereignis und zu den Daten, die von dem Ereignis betroffen sind.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
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

## <a name="members"></a>Elemente

**ulEventType**
  
> Typ des aufgetretenen Benachrichtigungsereigniss. Der Wert des **ulEventType-Members** entspricht der Struktur, die in der **Info-Union enthalten** ist. Das **ulEventType-Element** kann auf einen der folgenden Werte festgelegt werden: 
    
 _fnevCriticalError_
  
> Es ist ein globaler Fehler aufgetreten, z. B. eine in Bearbeitung heruntergefahrene Sitzung. Das **Element info** enthält eine [ERROR_NOTIFICATION](error_notification.md) Struktur. 
    
 _fnevExtended_
  
> Ein internes Ereignis, das von einem bestimmten Dienstanbieter definiert wurde, ist aufgetreten. Das **Element info** enthält eine [EXTENDED_NOTIFICATION](extended_notification.md) Struktur. 
    
 _fnevNewMail_
  
> Eine Nachricht wurde an den entsprechenden Empfangsordner für die Nachrichtenklasse übermittelt und wartet auf die Verarbeitung. Das **Element info** enthält eine [NEWMAIL_NOTIFICATION](newmail_notification.md) Struktur. 
    
 _fnevObjectCopied_
  
> Ein MAPI-Objekt wurde kopiert. Das **Element info** enthält eine [OBJECT_NOTIFICATION](object_notification.md) Struktur. 
    
 _fnevObjectCreated_
  
> Ein MAPI-Objekt wurde erstellt. Das **Element info** enthält eine **OBJECT_NOTIFICATION** Struktur. 
    
 _fnevObjectDeleted_
  
> Ein MAPI-Objekt wurde gelöscht. Das **Element info** enthält eine **OBJECT_NOTIFICATION** Struktur. 
    
 _fnevObjectModified_
  
> Ein MAPI-Objekt wurde geändert. Das **Element info** enthält eine **OBJECT_NOTIFICATION** Struktur. 
    
 _fnevObjectMoved_
  
> Ein Nachrichtenspeicher oder ein Adressbuchobjekt wurde verschoben. Das **Element info** enthält eine **OBJECT_NOTIFICATION** Struktur. 
    
 _fnevSearchComplete_
  
> Ein Suchvorgang ist abgeschlossen, und die Ergebnisse sind verfügbar. Das **Element info** enthält eine **OBJECT_NOTIFICATION** Struktur. 
    
 _fnevTableModified_
  
> Die Informationen in einer Tabelle haben sich geändert. Das **Element info** enthält eine [TABLE_NOTIFICATION](table_notification.md) Struktur. 
    
**info**
  
> Union von Benachrichtigungsstrukturen, die die betroffenen Daten für einen bestimmten Ereignistyp beschreiben. Die im Element **info** enthaltene Struktur hängt vom Wert des **ulEventType-Mitglieds** ab. 
    
## <a name="remarks"></a>Hinweise

Mindestens eine **BENACHRICHTIGUNGsstruktur** wird bei jedem Aufruf der [IMAPIAdviseSink::OnNotify-Methode als Eingabeparameter an die IMAPIAdviseSink::OnNotify-Methode einer registrierten](imapiadvisesink-onnotify.md) Hinweissenke übergeben. Die **NOTIFICATION-Strukturen** enthalten Informationen zu den jeweiligen Ereignissen, die aufgetreten sind, und beschreiben die betroffenen Objekte. 
  
Bevor Clients oder Dienstanbieter, die eine Benachrichtigung erhalten, die Struktur zum Verarbeiten des Ereignisses verwenden können, müssen sie den Ereignistyp überprüfen, wie im **ulEventType-Element** angegeben. Das hier gezeigte Codebeispiel überprüft beispielsweise, ob eine neue Nachricht eintreffen kann, und gibt nach dem Erkennen eines solchen Ereignisses die Nachrichtenklasse der Nachricht aus. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Hier erfahren Sie, wie Dienstanbieter die [IMAPISupport-Methode](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI-Strukturen](mapi-structures.md)

