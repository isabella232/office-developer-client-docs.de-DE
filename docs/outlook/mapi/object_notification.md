---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fab2b4a20da9681db2ed29ca00beea04b6e42682
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561194"
---
# <a name="object_notification"></a>OBJECT_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Objekt, das einer Änderung unterzogen wurde, z. B. das Kopieren oder Ändern.
  
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Anzahl der Bytes im Eintragsbezeichner, auf den der **lpEntryID-Member** verweist. 
    
 **lpEntryID**
  
> Zeiger auf den Eintragsbezeichner des betroffenen Objekts.
    
 **ulObjType**
  
> Typ des betroffenen Objekts. Mögliche Typen sind:
    
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
  
> Messaging-Benutzer.
    
MAPI_ATTACH 
  
> Anhang.
    
MAPI_DISTLIST 
  
> Verteilerliste.
    
MAPI_PROFSECT 
  
> Profilabschnitt.
    
MAPI_STATUS 
  
> Status-Objekt.
    
MAPI_SESSION 
  
> Session-Objekt.
    
 **cbParentID**
  
> Anzahl der Bytes im Eintragsbezeichner, auf den der **lpParentID-Member** verweist. 
    
 **lpParentID**
  
> Zeiger auf den Eintragsbezeichner des übergeordneten Elements des betroffenen Objekts.
    
 **cbOldID**
  
> Anzahl der Bytes im Eintragsbezeichner, auf den der **lpOldID-Member** verweist. 
    
 **lpOldID**
  
> Zeiger auf den Eintragsbezeichner des ursprünglichen Objekts. Dieser Zeiger kann NULL sein, wenn für das Ereignis kein ursprüngliches Objekt erforderlich ist.
    
 **cbOldParentID**
  
> Anzahl der Bytes im Eintragsbezeichner, auf den der **lpOldParentID-Member** verweist. 
    
 **lpOldParentID**
  
> Zeiger auf den Eintragsbezeichner des übergeordneten Elements des ursprünglichen Objekts. Dieser Zeiger kann NULL sein, wenn für das Ereignis kein ursprüngliches Objekt erforderlich ist.
    
 **lpPropTagArray**
  
> Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die die Eigenschaftentags enthält, die die vom Ereignis betroffenen Eigenschaften identifizieren. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **OBJECT_NOTIFICATION** Struktur ist eines der Mitglieder der Vereinigung von Strukturen, die im **Infoelement** der [NOTIFICATION-Struktur](notification.md) enthalten sind. Wenn das **Infoelement** einer **NOTIFICATION-Struktur** eine **OBJECT_NOTIFICATION** Struktur enthält, wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf einen der folgenden Ereignistypen festgelegt: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
Das Durchsuchungsereignis, dargestellt durch den fnevSearchComplete-Ereignistyp, gibt an, dass die anfängliche Suche der Domäne nach einem Suchordner abgeschlossen wurde.
  
Die folgenden Elemente, die Informationen zum ursprünglichen Objekt enthalten, werden nur in Verschiebungs- und Kopierereignissen verwendet. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Diese Member gelten nicht für die anderen Ereignistypen.
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die [IMAPISupport-Methode](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[SPropTagArray](sproptagarray.md)


[MAPI-Strukturen](mapi-structures.md)

