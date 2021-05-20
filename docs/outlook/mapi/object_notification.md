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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430168"
---
# <a name="object_notification"></a>OBJECT_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Objekt, das einer Änderung unterzogen wurde, z. B. kopiert oder geändert.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
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
  
> Anzahl der Bytes in der Eintrags-ID, auf die das **lpEntryID-Element** verweist. 
    
 **lpEntryID**
  
> Zeiger auf den Eintragsbezeichner des betroffenen Objekts.
    
 **ulObjType**
  
> Typ des betroffenen Objekts. Folgende Typen sind möglich:
    
MAPI_STORE 
  
> Nachrichtenspeicher. 
    
MAPI_ADDRBOOK 
  
> Adressbuch. 
    
MAPI_FOLDER 
  
> Folder.
    
MAPI_ABCONT 
  
> Adressbuchcontainer.
    
MAPI_MESSAGE 
  
> Nachricht.
    
MAPI_MAILUSER 
  
> Messagingbenutzer.
    
MAPI_ATTACH 
  
> Anlage.
    
MAPI_DISTLIST 
  
> Verteilerliste.
    
MAPI_PROFSECT 
  
> Abschnitt "Profil".
    
MAPI_STATUS 
  
> Status-Objekt.
    
MAPI_SESSION 
  
> Session-Objekt.
    
 **cbParentID**
  
> Anzahl der Bytes in der Eintrags-ID, auf die das **lpParentID-Element** verweist. 
    
 **lpParentID**
  
> Zeiger auf den Eintragsbezeichner des übergeordneten Objekts des betroffenen Objekts.
    
 **cbOldID**
  
> Anzahl der Bytes in der Eintrags-ID, auf die das **lpOldID-Element** verweist. 
    
 **lpOldID**
  
> Zeiger auf den Eintragsbezeichner des ursprünglichen Objekts. Dieser Zeiger kann NULL sein, wenn für das Ereignis kein ursprüngliches Objekt erforderlich ist.
    
 **cbOldParentID**
  
> Anzahl der Bytes in der Eintrags-ID, auf die das **lpOldParentID-Element** verweist. 
    
 **lpOldParentID**
  
> Zeiger auf den Eintragsbezeichner des übergeordneten Objekts des ursprünglichen Objekts. Dieser Zeiger kann NULL sein, wenn für das Ereignis kein ursprüngliches Objekt erforderlich ist.
    
 **lpPropTagArray**
  
> Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die die Eigenschaftstags enthält, die eigenschaften identifizieren, die vom Ereignis betroffen sind. 
    
## <a name="remarks"></a>Hinweise

Die **OBJECT_NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **info-Element** der [NOTIFICATION-Struktur enthalten](notification.md) ist. Wenn das **Infom** member einer **NOTIFICATION-Struktur** eine OBJECT_NOTIFICATION **enthält,** wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf einen der folgenden Ereignistypen festgelegt: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
Das vollständige Suchereignis, dargestellt durch den fnevSearchComplete-Ereignistyp, gibt an, dass die anfängliche Suche der Domäne nach einem Suchordner abgeschlossen ist.
  
Die folgenden Elemente, die Informationen zum ursprünglichen Objekt enthalten, werden nur in Move- und Copy-Ereignissen verwendet. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Diese Elemente gelten nicht für die anderen Ereignistypen.
  
Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Hier erfahren Sie, wie Dienstanbieter die [IMAPISupport-Methode](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[SPropTagArray](sproptagarray.md)


[MAPI-Strukturen](mapi-structures.md)

