---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cc0f0b2145b84db8e08dacb56279ef268645ef46
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624132"
---
# <a name="status_object_notification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Anzahl der Bytes im Eintragsbezeichner, auf den der **lpEntryID-Member** verweist. 
    
 **lpEntryID**
  
> Zeiger auf den Eintragsbezeichner des geänderten Statusobjekts.
    
 **cValues**
  
> Anzahl der [SPropValue-Strukturen](spropvalue.md) im Array, auf das vom **lpPropVals-Element** verwiesen wird. 
    
 **lpPropVals**
  
> Zeiger auf ein Array von **SPropValue-Strukturen,** die die Eigenschaften des geänderten Statusobjekts beschreiben. 
    
## <a name="remarks"></a>Bemerkungen

Die **STATUS_OBJECT_NOTIFICATION** Struktur ist eines der Mitglieder der Vereinigung von Strukturen, die im **Infoelement** der [NOTIFICATION-Struktur](notification.md) enthalten sind. Die **STATUS_OBJECT_NOTIFICATION** Struktur ist in einer Statusobjektbenachrichtigung für ein Ereignis vom Typ  _fnevStatusObjectModified_ enthalten. Statusobjektbenachrichtigung ist eine interne MAPI-Benachrichtigung; Clients und Dienstanbieter können sich nicht dafür registrieren, und Dienstanbieter können sie nicht generieren.
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die **IMAPISupport-Methode** zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Benachrichtigung](notification.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

