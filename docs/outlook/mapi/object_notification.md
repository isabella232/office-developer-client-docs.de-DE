---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279886"
---
# <a name="objectnotification"></a>OBJECT_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Objekt, das einer Änderung unterzogen wurde, beispielsweise kopiert oder geändert wurde.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a>Elemente

 **cbEntryID**
  
> Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpEntryID** -Element verwiesen wird. 
    
 **lpEntryID**
  
> Zeiger auf die Eintrags-ID des betroffenen Objekts.
    
 **ulObjType**
  
> Typ des betroffenen Objekts. Folgende Typen sind möglich:
    
MAPI_STORE 
  
> Nachrichtenspeicher. 
    
MAPI_ADDRBOOK 
  
> Adressbuch. 
    
MAPI_FOLDER 
  
> Ordner.
    
MAPI_ABCONT 
  
> Adressbuchcontainer.
    
MAPI_MESSAGE 
  
> Nachricht.
    
MAPI_MAILUSER 
  
> Messaging Benutzer.
    
MAPI_ATTACH 
  
> Anlage.
    
MAPI_DISTLIST 
  
> Verteilerliste.
    
MAPI_PROFSECT 
  
> Profil Abschnitt.
    
MAPI_STATUS 
  
> Status-Objekt.
    
MAPI_SESSION 
  
> Session-Objekt.
    
 **cbParentID**
  
> Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpParentID** -Element verwiesen wird. 
    
 **lpParentID**
  
> Zeiger auf die Eintrags-ID des übergeordneten Elements des betroffenen Objekts.
    
 **cbOldID**
  
> Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpOldID** -Element verwiesen wird. 
    
 **lpOldID**
  
> Zeiger auf die Eintrags-ID des ursprünglichen Objekts. Dieser Zeiger kann NULL sein, wenn das Ereignis kein Originalobjekt erfordert.
    
 **cbOldParentID**
  
> Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpOldParentID** -Element verwiesen wird. 
    
 **lpOldParentID**
  
> Zeiger auf die Eintrags-ID des übergeordneten Elements des ursprünglichen Objekts. Dieser Zeiger kann NULL sein, wenn das Ereignis kein Originalobjekt erfordert.
    
 **lpPropTagArray**
  
> Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die die Eigenschaftstags enthält, die die vom Ereignis betroffenen Eigenschaften kennzeichnen. 
    
## <a name="remarks"></a>Bemerkungen

Die **OBJECT_NOTIFICATION** -Struktur ist ein Mitglied der Vereinigung von Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind. Wenn der **Info** -Member einer **Benachrichtigungs** Struktur eine **OBJECT_NOTIFICATION** -Struktur enthält, wird das **ulEventType** -Element der **Benachrichtigungs** Struktur auf einen der folgenden Ereignistypen festgelegt: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
Das durch den fnevSearchComplete-Ereignistyp dargestellte vollständige Suchereignis gibt an, dass die erste Suche der Domäne für einen Suchordner abgeschlossen wurde.
  
Die folgenden Member, die Informationen zum ursprünglichen Objekt enthalten, werden nur in Verschiebungs-und Kopier Ereignissen verwendet. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Diese Elemente gelten nicht für die anderen Ereignistypen.
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollen.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[SPropTagArray](sproptagarray.md)


[MAPI-Strukturen](mapi-structures.md)

