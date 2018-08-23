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
ms.openlocfilehash: 0d427adde72c24d4ca879c7bd883af09c4ecad53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579970"
---
# <a name="notification"></a>NOTIFICATION
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen über ein Ereignis, das aufgetreten ist und die Daten, die das Ereignis betroffen ist.
  
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
  
> Typ der Benachrichtigungsereignis, das aufgetreten ist. Der Wert des Elements **UlEventType** entspricht der Struktur, die in der Union **Info** enthalten ist. Das Element **UlEventType** kann auf einen der folgenden Werte festgelegt werden: 
    
 _fnevCriticalError_
  
> Ein globaler Fehler ist aufgetreten, wie eine Sitzung Herunterfahren ausgeführt. Das **Info** -Element enthält eine [ERROR_NOTIFICATION](error_notification.md) -Struktur. 
    
 _fnevExtended_
  
> Ein internes Ereignis von einem bestimmten Dienstanbieter definierten ist aufgetreten. Das **Info** -Element enthält eine [EXTENDED_NOTIFICATION](extended_notification.md) -Struktur. 
    
 _fnevNewMail_
  
> Eine Nachricht übermittelt wurde, um den entsprechenden Ordner für die Nachrichtenklasse empfangen und wartet auf Verarbeitung. Das **Info** -Element enthält eine [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur. 
    
 _fnevObjectCopied_
  
> Ein MAPI-Objekt wurde kopiert. Das **Info** -Element enthält eine [OBJECT_NOTIFICATION](object_notification.md) -Struktur. 
    
 _fnevObjectCreated_
  
> Ein MAPI-Objekt wurde erstellt. Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur. 
    
 _fnevObjectDeleted_
  
> Ein MAPI-Objekt wurde gelöscht. Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur. 
    
 _fnevObjectModified_
  
> Ein MAPI-Objekt geändert wurde. Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur. 
    
 _fnevObjectMoved_
  
> Einen Nachrichtenspeicher oder Adresse Adressbuch-Objekt verschoben wurde. Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur. 
    
 _fnevSearchComplete_
  
> Suchvorgang beendet wurde, und die Ergebnisse verfügbar sind. Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur. 
    
 _fnevTableModified_
  
> Die Informationen in einer Tabelle wurde geändert. Das **Info** -Element enthält eine [TABLE_NOTIFICATION](table_notification.md) -Struktur. 
    
**Info**
  
> Union der Benachrichtigung Strukturen zur Beschreibung der betreffenden Daten für einen bestimmten Typ des Ereignisses. Die Struktur im **Info** -Member enthalten, hängt von den Wert des Elements **UlEventType** ab. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein oder mehrere **Benachrichtigung** Strukturen werden als Eingabeparameter mit jedem Aufruf einer registrierten Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode übergeben. Die **Benachrichtigung** Strukturen enthalten Informationen zu den bestimmte Ereignisse, die aufgetreten sind, und der betroffene Objekte beschreiben. 
  
Bevor Clients oder -Dienstanbieter erhalten eine Benachrichtigung die Struktur verwenden können Verarbeitung des Ereignisses, müssen sie den Ereignistyp überprüfen, wie im **UlEventType** -Member angegeben. Beispielsweise druckt das Codebeispiel, das hier gezeigte überprüft, ob das Eintreffen einer neuen Nachricht und beim Erkennen eines Ereignisses dieser Art, die Nachrichtenklasse der Nachricht. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.  <br/> |
|[Unterstützen von Ereignisbenachrichtigungen](supporting-event-notification.md) <br/> |Erläuterung der wie-Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI-Strukturen](mapi-structures.md)

