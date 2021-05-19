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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425442"
---
# <a name="error_notification"></a>ERROR_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt Informationen, die sich auf einen kritischen Fehler beziehen. Dadurch wird eine Fehlerbenachrichtigung generiert. 
  
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
  
> Anzahl der Bytes in der Eintrags-ID, auf die **von lpEntryID verwiesen wird.** 
    
 **lpEntryID**
  
> Zeiger auf den Eintragsbezeichner des Objekts, das den Fehler verursacht.
    
 **scode**
  
> Fehlerwert für den kritischen Fehler. 
    
 **ulFlags**
  
> Bitmaske von Flags, die verwendet werden, um das Format des Texts zu bestimmen, auf das das **lpszError-Element** in der Struktur verweist, auf das **lpMAPIError verweist.** Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 **lpMAPIError**
  
> Zeiger auf eine [MAPIERROR-Struktur,](mapierror.md) die den Fehler beschreibt. 
    
## <a name="remarks"></a>Hinweise

Die **ERROR_NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **info-Element** der [NOTIFICATION-Struktur enthalten](notification.md) ist. Wenn das **Infom** member einer **NOTIFICATION-Struktur** eine ERROR_NOTIFICATION **enthält,** wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf _fnevCriticalError festgelegt._
  
Der Wert des **cbEntryID-Members** und des **lpEntryID-Members** kann NULL sein. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Hier erfahren Sie, wie Dienstanbieter die **IMAPISupport-Methode** zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[Benachrichtigung](notification.md)


[MAPI-Strukturen](mapi-structures.md)

