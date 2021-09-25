---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 32789e57bebef3320e413fa67c6352dee43248ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614241"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Flags, die verwendet werden, um den Status von Adresseinträgen während des Namensauflösungsprozesses anzugeben.
  
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

 **Cflags**
  
> Anzahl der MAPI-definierten Flags in der Liste.
    
 **ulFlags**
  
> Ein Array von Flags, das den Status des Namensauflösungsvorgangs für einen Empfänger bereitstellt. Die folgenden Flags können festgelegt werden:
    
MAPI_AMBIGUOUS 
  
> Der Empfänger wurde aufgelöst, jedoch nicht in einen eindeutigen Eintragsbezeichner. Andere Adressbuchcontainer sollten nicht versuchen, diesen Empfänger aufzulösen. 
    
MAPI_RESOLVED 
  
> Der Empfänger wurde in einen eindeutigen Eintragsbezeichner aufgelöst. Andere Adressbuchcontainer sollten nicht versuchen, diesen Empfänger aufzulösen. 
    
MAPI_UNRESOLVED 
  
> Der Eintrag wurde nicht aufgelöst. Andere Adressbuchcontainer sollten versuchen, diesen Empfänger aufzulösen.
    
## <a name="remarks"></a>Bemerkungen

Die **FLAGLIST-Struktur** wird als Parameter für [IABContainer::ResolveNames](iabcontainer-resolvenames.md)verwendet. Jeder zu lösende Empfänger ist in einer [ADRLIST-Struktur](adrlist.md) enthalten. Wenn der Adressbuchcontainer versucht, jeden Empfänger aufzulösen, wird das entsprechende Flag im entsprechenden Eintrag in der **FLAGLIST-Struktur** festgelegt. Alle Einträge in der **FLAGLIST-Struktur** befinden sich in der gleichen Reihenfolge wie die Einträge in der **ADRLIST-Struktur.** Dies erleichtert das Zuordnen einer Kennzeichnungseinstellung zu einem Empfänger. 
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI-Strukturen](mapi-structures.md)

