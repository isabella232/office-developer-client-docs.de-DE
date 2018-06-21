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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5e23d9b829a941e3add8b8d8e137c73052b08aa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19791658"
---
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**Betrifft**: Outlook 
  
Beschreibt die Informationen, die auf ein Ereignis bezieht, die anbieterspezifische-Dienst ist. 
  
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
  
> Erweiterte Ereigniscode, die vom Anbieter definiert ist.
    
 **cb**
  
> Anzahl der Bytes in der Ereignis-spezifischen Parametern auf **PbEventParameters**zeigt. 
    
 **pbEventParameters**
  
> Zeiger auf Ereignis-spezifischen Parametern. Der Typ von Parametern, die verwendet werden, hängt von den Wert des Elements **UlEvent** ab. Diese Parameter sind vom Anbieter dokumentiert, die das Ereignis ausgegeben. 
    
## <a name="remarks"></a>Hinweise

Die **EXTENDED_NOTIFICATION** -Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten. Wenn **Info** Mitglied eine **Benachrichtigung** Struktur eine **EXTENDED_NOTIFICATION** -Struktur enthält, wird das **UlEventType** Mitglied der **Benachrichtigung** Struktur auf _FnevExtended_festgelegt.
  
Das erweiterte-Ereignis wird durch einen Dienstanbieter, eine Art der Änderung darstellen, die von keiner anderen vordefinierten Ereignisse behandelt werden kann nicht definiert. Für dieses Ereignis können nur Clients, die wissen, bevor sie registrieren, dass es sich bei ein Dienstanbieter ein erweiterte Ereignis unterstützt registrieren. Es ist nicht möglich für Clients ohne guten Kenntnissen zu bestimmen, ob es sich bei ein Dienstanbieter ein erweiterte Ereignis unterstützt. Wenn ein Dienstanbieter ein erweiterte Ereignis unterstützt, wird gezeigt, wie ein Ereignis beim Empfang zu behandeln.
  
Wenn ein Client abmeldet eine erweiterte Benachrichtigung von der Sitzung gesendet. Registrieren Sie für diese Benachrichtigung durch Aufrufen von [IMAPISession::Advise](imapisession-advise.md) mit der _LpEntryID_ -Parameter auf NULL und der _CbEntryID_ -Parameter auf 0 (null) festgelegt. 
  
Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.  <br/> |
|[Benachrichtigung bei unterstützenden](supporting-event-notification.md) <br/> |Erläuterung der wie-Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methoden verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)


[MAPI-Strukturen](mapi-structures.md)

