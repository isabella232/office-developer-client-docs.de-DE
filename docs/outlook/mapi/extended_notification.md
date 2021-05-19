---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415719"
---
# <a name="extended_notification"></a>EXTENDED_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt Informationen, die sich auf ein ereignis beziehen, das Dienstanbieterspezifisch ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a>Elemente

 **ulEvent**
  
> Erweiterter Ereigniscode, der vom Anbieter definiert wird.
    
 **cb**
  
> Anzahl der Bytes in den ereignisspezifischen Parametern, auf die von **pbEventParameters verwiesen wird.** 
    
 **pbEventParameters**
  
> Zeiger auf ereignisspezifische Parameter. Der Typ der verwendeten Parameter hängt vom Wert des **ulEvent-Mitglieds** ab. Diese Parameter werden vom Anbieter dokumentiert, der das Ereignis ausgegeben hat. 
    
## <a name="remarks"></a>Hinweise

Die **EXTENDED_NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **info-Element** der [NOTIFICATION-Struktur enthalten](notification.md) ist. Wenn das **Infom** member einer **NOTIFICATION-Struktur** eine EXTENDED_NOTIFICATION **enthält,** wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf _fnevExtended festgelegt._
  
Das erweiterte Ereignis wird von einem Dienstanbieter definiert, um einen Änderungstyp zu repräsentieren, der von keinem der anderen vordefinierten Ereignisse abgedeckt werden kann. Nur Clients, die vor der Registrierung wissen, dass ein Dienstanbieter ein erweitertes Ereignis unterstützt, können sich für dieses Ereignis registrieren. Clients können ohne erweiterte Kenntnisse nicht ermitteln, ob ein Dienstanbieter ein erweitertes Ereignis unterstützt. Wenn ein Dienstanbieter ein erweitertes Ereignis unterstützt, wird gezeigt, wie ein solches Ereignis beim Empfangen behandeln wird.
  
Eine erweiterte Benachrichtigung wird von der Sitzung gesendet, wenn sich ein Client abmeldet. Registrieren Sie sich für diese Benachrichtigung, indem [Sie IMAPISession::Advise](imapisession-advise.md) aufrufen, wenn  _der lpEntryID-Parameter_ auf NULL und  _der cbEntryID-Parameter_ auf Null festgelegt ist. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Hier erfahren Sie, wie Dienstanbieter die [IMAPISupport-Methoden](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)


[MAPI-Strukturen](mapi-structures.md)

