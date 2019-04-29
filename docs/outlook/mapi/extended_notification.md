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
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt Informationen, die sich auf ein Ereignis beziehen, das Dienstanbieter spezifisch ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Die Anzahl der Bytes in den ereignisspezifischen Parametern, auf die von **pbEventParameters**verwiesen wird. 
    
 **pbEventParameters**
  
> Zeiger auf ereignisspezifische Parameter. Welcher Typ von Parametern verwendet wird, hängt vom Wert des **ulEvent** -Elements ab; Diese Parameter werden vom Anbieter dokumentiert, der das Ereignis ausgelöst hat. 
    
## <a name="remarks"></a>Bemerkungen

Die **EXTENDED_NOTIFICATION** -Struktur ist ein Mitglied der Vereinigung von Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind. Wenn der **Info** -Member einer **Benachrichtigungs** Struktur eine **EXTENDED_NOTIFICATION** -Struktur enthält, wird das **ulEventType** -Element der **Benachrichtigungs** Struktur auf _fnevExtended_festgelegt.
  
Das Extended-Ereignis wird von einem Dienstanbieter definiert, der eine Art von Änderung darstellt, die von keinem der anderen vordefinierten Ereignisse abgedeckt werden kann. Nur Clients, die vor Ihrer Registrierung wissen, dass ein Dienstanbieter ein erweitertes Ereignis unterstützt, können sich für dieses Ereignis registrieren. Es ist für Clients nicht möglich, ohne Erweitertes Wissen zu ermitteln, ob ein Dienstanbieter ein Extended-Ereignis unterstützt. Wenn ein Dienstanbieter ein Extended-Ereignis unterstützt, wird gezeigt, wie ein solches Ereignis beim Empfang behandelt wird.
  
Eine erweiterte Benachrichtigung wird von der Sitzung gesendet, wenn sich ein Client abmeldet. Registrieren Sie sich für diese Benachrichtigung, indem Sie [IMAPISession:: Advise](imapisession-advise.md) aufrufen, wobei der _lpEntryID_ -Parameter auf NULL festgelegt ist und der _cbEntryID_ -Parameter auf NULL festgelegt ist. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollen.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methoden zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)


[MAPI-Strukturen](mapi-structures.md)

