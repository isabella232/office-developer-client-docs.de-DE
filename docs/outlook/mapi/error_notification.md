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
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt Informationen zu einem wichtigen Fehler. Dadurch wird eine Fehlerbenachrichtigung generiert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Anzahl der Bytes in der Eintrags-ID, auf die von **lpEntryID**verwiesen wird. 
    
 **lpEntryID**
  
> Zeiger auf die Eintrags-ID des Objekts, das den Fehler verursacht.
    
 **SCODE**
  
> Fehlerwert für den kritischen Fehler. 
    
 **ulFlags**
  
> Bitmaske der Flags, mit denen das Format des Texts festgelegt wird, der vom **lpszError** -Element in der Struktur verweist, auf die durch **lpMAPIError**verwiesen wird. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 **lpMAPIError**
  
> Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur, die den Fehler beschreibt. 
    
## <a name="remarks"></a>Bemerkungen

Die **ERROR_NOTIFICATION** -Struktur ist ein Mitglied der Vereinigung von Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind. Wenn der **Info** -Member einer **Benachrichtigungs** Struktur eine **ERROR_NOTIFICATION** -Struktur enthält, wird das **ulEventType** -Element der **Benachrichtigungs** Struktur auf _fnevCriticalError_festgelegt.
  
Der Wert des **cbEntryID** -Elements und des **lpEntryID** -Members kann NULL sein. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollen.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[Benachrichtigung](notification.md)


[MAPI-Strukturen](mapi-structures.md)

