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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f7a236c2a7e307d278cac5ef413cbd2f600bf09f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582098"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Elemente

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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Struktur **FLAGLIST** wird als Parameter für [IABContainer](iabcontainer-resolvenames.md)verwendet. Einzelnen Empfänger aufgelöst werden, ist in eine [ADRLIST](adrlist.md) -Struktur enthalten. Während der Adressbuchcontainer versucht, jeden Empfänger zu beheben, legt das entsprechende Flag in den entsprechenden Eintrag in der Struktur **FLAGLIST** fest. Alle Einträge in der Struktur **FLAGLIST** sind in der gleichen Reihenfolge als die Einträge in der **ADRLIST** -Struktur. Dies vereinfacht die eine Einstellung für die Kennzeichnung mit einem Empfänger zuordnen. 
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI-Strukturen](mapi-structures.md)

