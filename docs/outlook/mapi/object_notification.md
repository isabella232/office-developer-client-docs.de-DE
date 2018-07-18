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
ms.openlocfilehash: 1593152786a3345827089e5f6702454896944b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793299"
---
# <a name="objectnotification"></a>OBJECT_NOTIFICATION

  
  
**Betrifft**: Outlook 
  
Enthält Informationen zu einem Objekt, die eine Änderung unterzogen, z. B. wird kopiert oder geändert.
  
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
  
> Anzahl der Bytes in die Eintrags-ID auf den Member **LpEntryID** zeigt. 
    
 **lpEntryID**
  
> Zeiger auf die Eintrags-ID des betroffenen-Objekts.
    
 **ulObjType**
  
> Typ des Objekts betroffen. Verfügbare Typen sind wie folgt:
    
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
  
> Attachment-Objekt.
    
MAPI_DISTLIST 
  
> Verteilerliste.
    
MAPI_PROFSECT 
  
> Profilabschnitt.
    
MAPI_STATUS 
  
> Statusobjekt.
    
MAPI_SESSION 
  
> Session-Objekt.
    
 **cbParentID**
  
> Anzahl der Bytes in die Eintrags-ID auf den Member **LpParentID** zeigt. 
    
 **lpParentID**
  
> Zeiger auf die Eintrags-ID des übergeordneten Elements des betroffenen-Objekts.
    
 **cbOldID**
  
> Anzahl der Bytes in die Eintrags-ID auf den Member **LpOldID** zeigt. 
    
 **lpOldID**
  
> Zeiger auf die Eintrags-ID des ursprünglichen-Objekts. Wenn das Ereignis ursprüngliche-Objekt nicht erforderlich sind, kann dieser Zeiger NULL sein.
    
 **cbOldParentID**
  
> Anzahl der Bytes in die Eintrags-ID auf den Member **LpOldParentID** zeigt. 
    
 **lpOldParentID**
  
> Zeiger auf die Eintrags-ID des übergeordneten Elements des ursprünglichen-Objekts. Wenn das Ereignis ursprüngliche-Objekt nicht erforderlich sind, kann dieser Zeiger NULL sein.
    
 **lpPropTagArray**
  
> Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die die Eigenschaft enthält tags identifizierende Eigenschaften, die von dem Ereignis betroffen. 
    
## <a name="remarks"></a>Bemerkungen

Die **OBJECT_NOTIFICATION** -Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten. Wenn der Member **Info** eine **Benachrichtigung** Struktur eine **OBJECT_NOTIFICATION** -Struktur enthält, wird das **UlEventType** Mitglied der **Benachrichtigung** Struktur auf eine der folgenden Arten von Ereignissen festgelegt: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
Das Search-complete-Ereignis, dargestellt durch den Ereignistyp FnevSearchComplete gibt an, dass die erste Suche der Domäne für ein Suchordner abgeschlossen wurde.
  
Die folgenden Elemente, die Informationen zum ursprünglichen-Objekt enthalten sind nur in verschieben und kopieren Ereignisse verwendet. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Dieser Member gelten nicht für andere Arten von Ereignissen.
  
Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.  <br/> |
|[Unterstützen von Ereignisbenachrichtigungen](supporting-event-notification.md) <br/> |Erläuterung der wie-Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[SPropTagArray](sproptagarray.md)


[MAPI-Strukturen](mapi-structures.md)

