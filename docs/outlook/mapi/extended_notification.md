---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 814bd8866863794740aafd553047c6443f192b04
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614220"
---
# <a name="extended_notification"></a>EXTENDED_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt Informationen, die sich auf ein Ereignis beziehen, das dienstanbieterspezifisch ist. 
  
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

## <a name="members"></a>Members

 **ulEvent**
  
> Erweiterter Ereigniscode, der vom Anbieter definiert wird.
    
 **cb**
  
> Anzahl der Bytes in den ereignisspezifischen Parametern, auf die durch **pbEventParameters** verwiesen wird. 
    
 **pbEventParameters**
  
> Zeiger auf ereignisspezifische Parameter. Der Typ der verwendeten Parameter hängt vom Wert des **ulEvent-Elements** ab. Diese Parameter werden vom Anbieter dokumentiert, der das Ereignis ausgestellt hat. 
    
## <a name="remarks"></a>Bemerkungen

Die **EXTENDED_NOTIFICATION** Struktur ist eines der Mitglieder der Vereinigung von Strukturen, die im **Infoelement** der [NOTIFICATION-Struktur](notification.md) enthalten sind. Wenn das **Infoelement** einer **NOTIFICATION-Struktur** eine **EXTENDED_NOTIFICATION** Struktur enthält, wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf  _fnevExtended_ festgelegt.
  
Das erweiterte Ereignis wird von einem Dienstanbieter definiert, um eine Art von Änderung darzustellen, die von keinem der anderen vordefinierten Ereignisse abgedeckt werden kann. Nur Clients, die vor der Registrierung wissen, dass ein Dienstanbieter ein erweitertes Ereignis unterstützt, können sich für dieses Ereignis registrieren. Clients können ohne erweiterte Kenntnisse nicht ermitteln, ob ein Dienstanbieter ein erweitertes Ereignis unterstützt. Wenn ein Dienstanbieter ein erweitertes Ereignis unterstützt, wird gezeigt, wie ein solches Ereignis beim Empfang behandelt wird.
  
Eine erweiterte Benachrichtigung wird von der Sitzung gesendet, wenn sich ein Client abmeldet. Registrieren Sie sich für diese Benachrichtigung, indem [Sie IMAPISession::Advise](imapisession-advise.md) aufrufen, wobei der  _parameter lpEntryID_ auf NULL und der  _cbEntryID-Parameter_ auf Null festgelegt ist. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die [IMAPISupport-Methoden](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)


[MAPI-Strukturen](mapi-structures.md)

