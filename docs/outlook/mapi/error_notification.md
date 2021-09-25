---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 775551307015ff8a36470ffcd628c7fa9df6923b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614234"
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Anzahl der Bytes im Eintragsbezeichner, auf den **lpEntryID** verweist. 
    
 **lpEntryID**
  
> Zeiger auf den Eintragsbezeichner des Objekts, das den Fehler verursacht.
    
 **scode**
  
> Fehlerwert für den kritischen Fehler. 
    
 **ulFlags**
  
> Bitmaske von Flags, die verwendet werden, um das Format des Texts festzulegen, auf den der **lpszError-Member** in der Struktur verweist, auf die **lpMAPIError** verweist. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 **lpMAPIError**
  
> Zeiger auf eine [MAPIERROR-Struktur,](mapierror.md) die den Fehler beschreibt. 
    
## <a name="remarks"></a>Bemerkungen

Die **ERROR_NOTIFICATION** Struktur ist eines der Mitglieder der Vereinigung von Strukturen, die im **Infoelement** der [NOTIFICATION-Struktur](notification.md) enthalten sind. Wenn das **Info-Element** einer **NOTIFICATION-Struktur** eine **ERROR_NOTIFICATION** Struktur enthält, wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf  _fnevCriticalError_ festgelegt.
  
Der Wert des **cbEntryID-Elements** und des **lpEntryID-Elements** kann NULL sein. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die **IMAPISupport-Methode** zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[Benachrichtigung](notification.md)


[MAPI-Strukturen](mapi-structures.md)

