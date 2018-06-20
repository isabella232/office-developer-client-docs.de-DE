---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2cf5ff69e8453b2da26fd5044823ddf4f99a9f45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791697"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**Betrifft**: Outlook 
  
Enthält eine Liste von Flags verwendet, um den Status von Adresseinträge während der Namensauflösungsprozess angeben.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>Members

 **cFlags**
  
> Anzahl der MAPI-defined Flags in der Liste.
    
 **ulFlags**
  
> Ein Array von Flags, die den Status des Vorgangs Lösung Namen für einen Empfänger enthält. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_AMBIGUOUS 
  
> Der Empfänger aufgelöst wurde, jedoch nicht für einen Eintrag Eindeutiger Bezeichner. Andere Address Book Container sollte nicht an diesen Empfänger zu beheben versuchen. 
    
MAPI_RESOLVED 
  
> Der Empfänger wurde in eine eindeutige ID aufgelöst. Andere Address Book Container sollte nicht an diesen Empfänger zu beheben versuchen. 
    
MAPI_UNRESOLVED 
  
> Der Eintrag wurde nicht behoben. Andere Address Book Container sollte versuchen, diese Empfänger aufzulösen.
    
## <a name="remarks"></a>Hinweise

Die Struktur **FLAGLIST** wird als Parameter für [IABContainer](iabcontainer-resolvenames.md)verwendet. Einzelnen Empfänger aufgelöst werden, ist in eine [ADRLIST](adrlist.md) -Struktur enthalten. Während der Adressbuchcontainer versucht, jeden Empfänger zu beheben, legt das entsprechende Flag in den entsprechenden Eintrag in der Struktur **FLAGLIST** fest. Alle Einträge in der Struktur **FLAGLIST** sind in der gleichen Reihenfolge als die Einträge in der **ADRLIST** -Struktur. Dies vereinfacht die eine Einstellung für die Kennzeichnung mit einem Empfänger zuordnen. 
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IABContainer](iabcontainer-resolvenames.md)


[MAPI-Strukturen](mapi-structures.md)

