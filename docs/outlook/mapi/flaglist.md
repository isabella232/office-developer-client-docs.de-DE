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
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336939"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Flags, die zum Anzeigen des Status von Adresseinträgen während des Namensauflösungsvorgangs verwendet werden.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>Elemente

 **cFlags**
  
> Die Anzahl der MAPI-definierten Flags in der Liste.
    
 **ulFlags**
  
> Ein Array von Flags, das den Status des Vorgangs zur Namensauflösung für einen Empfänger bereitstellt. Die folgenden Flags können festgelegt werden:
    
MAPI_AMBIGUOUS 
  
> Der Empfänger wurde aufgelöst, jedoch nicht zu einer eindeutigen Eintrags-ID. Andere Adressbuchcontainer sollten nicht versuchen, diesen Empfänger aufzulösen. 
    
MAPI_RESOLVED 
  
> Der Empfänger wurde in eine eindeutige Eintrags-ID aufgelöst. Andere Adressbuchcontainer sollten nicht versuchen, diesen Empfänger aufzulösen. 
    
MAPI_UNRESOLVED 
  
> Der Eintrag wurde nicht aufgelöst. Andere Adressbuchcontainer sollten versuchen, diesen Empfänger aufzulösen.
    
## <a name="remarks"></a>Bemerkungen

Die **flaglist** -Struktur wird als Parameter für [IABContainer:: ResolveNames](iabcontainer-resolvenames.md)verwendet. Jeder der zu lösenden Empfänger ist in einer [ADRLIST](adrlist.md) -Struktur enthalten. Während der Adressbuchcontainer versucht, jeden Empfänger aufzulösen, wird das entsprechende Flag im entsprechenden Eintrag in der **flaglist** -Struktur festgelegt. Alle Einträge in der Flaglist **** -Struktur haben dieselbe Reihenfolge wie die Einträge in der **ADRLIST** -Struktur. Dies erleichtert das Zuordnen einer Flag-Einstellung zu einem Empfänger. 
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI-Strukturen](mapi-structures.md)

