---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eff140179865d662545d0e21ca3789a6e8c2643b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583975"
---
# <a name="notification"></a>NOTIFICATION
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Ereignis, das aufgetreten ist, und zu den Daten, die von dem Ereignis betroffen sind.
  
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

## <a name="members"></a>Members

**ulEventType**
  
> Typ des aufgetretenen Benachrichtigungsereignisses. Der Wert des **ulEventType-Elements** entspricht der Struktur, die in der **Info-Union** enthalten ist. Der **ulEventType-Member** kann auf einen der folgenden Werte festgelegt werden: 
    
 _fnevCriticalError_
  
> Es ist ein globaler Fehler aufgetreten, z. B. ein laufendes Herunterfahren einer Sitzung. Das **Info-Element** enthält eine [ERROR_NOTIFICATION](error_notification.md) Struktur. 
    
 _fnevExtended_
  
> Ein internes Ereignis, das von einem bestimmten Dienstanbieter definiert wurde, ist aufgetreten. Das **Info-Element** enthält eine [EXTENDED_NOTIFICATION](extended_notification.md) Struktur. 
    
 _fnevNewMail_
  
> Eine Nachricht wurde an den entsprechenden Empfangsordner für die Nachrichtenklasse übermittelt und wartet auf die Verarbeitung. Das **Info-Element** enthält eine [NEWMAIL_NOTIFICATION](newmail_notification.md) Struktur. 
    
 _fnevObjectCopied_
  
> Ein MAPI-Objekt wurde kopiert. Das **Info-Element** enthält eine [OBJECT_NOTIFICATION](object_notification.md) Struktur. 
    
 _fnevObjectCreated_
  
> Ein MAPI-Objekt wurde erstellt. Das **Info-Element** enthält eine **OBJECT_NOTIFICATION** Struktur. 
    
 _fnevObjectDeleted_
  
> Ein MAPI-Objekt wurde gelöscht. Das **Info-Element** enthält eine **OBJECT_NOTIFICATION** Struktur. 
    
 _fnevObjectModified_
  
> Ein MAPI-Objekt wurde geändert. Das **Info-Element** enthält eine **OBJECT_NOTIFICATION** Struktur. 
    
 _fnevObjectMoved_
  
> Ein Nachrichtenspeicher- oder Adressbuchobjekt wurde verschoben. Das **Info-Element** enthält eine **OBJECT_NOTIFICATION** Struktur. 
    
 _fnevSearchComplete_
  
> Ein Suchvorgang wurde abgeschlossen, und die Ergebnisse sind verfügbar. Das **Info-Element** enthält eine **OBJECT_NOTIFICATION** Struktur. 
    
 _fnevTableModified_
  
> Die Informationen in einer Tabelle wurden geändert. Das **Infoelement** enthält eine [TABLE_NOTIFICATION](table_notification.md) Struktur. 
    
**info**
  
> Vereinigung von Benachrichtigungsstrukturen, die die betroffenen Daten für einen bestimmten Ereignistyp beschreiben. Die im **Info-Element** enthaltene Struktur hängt vom Wert des **ulEventType-Elements** ab. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine oder mehrere **NOTIFICATION-Strukturen** werden bei jedem Aufruf der [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) einer registrierten Empfehlungssenke als Eingabeparameter übergeben. Die **NOTIFICATION-Strukturen** enthalten Informationen zu bestimmten Ereignissen, die aufgetreten sind, und beschreiben die betroffenen Objekte. 
  
Bevor Clients oder Dienstanbieter, die eine Benachrichtigung erhalten, die Struktur zum Verarbeiten des Ereignisses verwenden können, müssen sie den Ereignistyp überprüfen, wie im **ulEventType-Element** angegeben. In dem hier gezeigten Codebeispiel wird beispielsweise überprüft, ob eine neue Nachricht eintreffen soll, und wenn ein solches Ereignis erkannt wird, wird die Nachrichtenklasse der Nachricht ausgegeben. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die [IMAPISupport-Methode](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI-Strukturen](mapi-structures.md)

