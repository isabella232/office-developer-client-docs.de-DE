---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 86fe4b0a1a7521c310788505b99f53bc8657de75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791643"
---
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**Betrifft**: Outlook 
  
Beschreibt die Informationen, die auf ein schwerwiegender Fehler beziehen. Daraufhin wird eine Benachrichtigung Fehler generiert werden soll. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a>Elemente

 **cbEntryID**
  
> Anzahl der Bytes in die Eintrags-ID auf **LpEntryID**zeigt. 
    
 **lpEntryID**
  
> Zeiger auf die Eintrags-ID des Objekts, das den Fehler verursacht.
    
 **SCODE**
  
> Fehlerwert für den kritischen Fehler. 
    
 **ulFlags**
  
> Bitmaske aus Flags verwendet, um das Format des Texts festzulegen, auf dem **LpszError** -Element in der Struktur auf den **LpMAPIError**zeigt. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 **lpMAPIError**
  
> Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur, die den Fehler beschreibt. 
    
## <a name="remarks"></a>Bemerkungen

Die **ERROR_NOTIFICATION** -Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten. Wenn **Info** Mitglied eine **Benachrichtigung** Struktur eine **ERROR_NOTIFICATION** -Struktur enthält, wird das **UlEventType** Mitglied der **Benachrichtigung** Struktur auf _FnevCriticalError_festgelegt.
  
Der Wert des Members **CbEntryID** und der **LpEntryID** Member kann NULL sein. 
  
Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.  <br/> |
|[Unterstützen von Ereignisbenachrichtigungen](supporting-event-notification.md) <br/> |Erläuterung der wie-Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[Benachrichtigung](notification.md)


[MAPI-Strukturen](mapi-structures.md)

