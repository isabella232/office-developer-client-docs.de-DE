---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 71e0a08436c925f0d68d63111722cc01bd73cc5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795648"
---
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Betrifft**: Outlook 
  
Beschreibt ein Statusobjekt, das von einer Änderung betroffen ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a>Elemente

 **cbEntryID**
  
> Anzahl der Bytes in die Eintrags-ID auf den Member **LpEntryID** zeigt. 
    
 **lpEntryID**
  
> Zeiger auf die Eintrags-ID des geänderten Status-Objekts.
    
 **cValues**
  
> Anzahl der [SPropValue](spropvalue.md) Strukturen im Array auf der Member **LpPropVals** zeigt. 
    
 **lpPropVals**
  
> Zeiger auf ein Array von **SPropValue** -Strukturen, die die Eigenschaften des geänderten Status-Objekts zu beschreiben. 
    
## <a name="remarks"></a>Bemerkungen

Die **STATUS_OBJECT_NOTIFICATION** -Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten. Die Struktur **STATUS_OBJECT_NOTIFICATION** ist eine Benachrichtigung zum Status-Objekt für ein Ereignis des Typs _FnevStatusObjectModified_enthalten. Benachrichtigung über den-Objekt ist eine interne MAPI-Benachrichtigung an. Clients und -Dienstanbieter können nicht für sie registrieren und Dienstanbieter können es nicht generiert.
  
Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.  <br/> |
|[Unterstützen von Ereignisbenachrichtigungen](supporting-event-notification.md) <br/> |Erläuterung der wie-Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

