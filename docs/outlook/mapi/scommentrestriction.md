---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2185b059f2b831a14b90bad3a3c286ed72f8234d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795449"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**Betrifft**: Outlook 
  
Beschreibt eine Einschränkung Kommentar, der verwendet wird, um eine Einschränkung kommentieren. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a>Members

 **cValues**
  
> Anzahl-Eigenschaftswerte im Array auf den Member **LpProp** zeigt. 
    
 **lpRes**
  
> Zeiger auf eine [SRestriction](srestriction.md) -Struktur. 
    
 **lpProp**
  
> Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, mit der Eigenschafts-Tag und der Wert für eine benannte Eigenschaft. 
    
## <a name="remarks"></a>Hinweise

Die Struktur **SCommentRestriction** ordnet ein Objekt zusammen mit einer Gruppe von benannten Eigenschaften. Kommentar Einschränkungen sind im Gegensatz zu anderen Einschränkungen, da sie nicht ausgewertet werden. D. h., werden sie von der [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode ignoriert. Es ist keine Auswirkung auf die Zeilen, die von [der QueryRows](imapitable-queryrows.md) zurückgegeben wird, nachdem eine **Methode IMAPITable:: Restrict** aufgerufen wurde. 
  
Anwendungsspezifische Informationen mit einer Einschränkung beibehalten, wenn es auf dem Datenträger gespeichert wird, kann die **SCommentRestriction** -Struktur verwendet werden. Beispielsweise kann ein Client, speichern den Namen einer benannten Eigenschaft in einer eigenschaftseinschränkung verwendet dazu eine **SCommentRestriction** -Struktur. Speichern einen Eigenschaftennamen ist nicht möglich, in einer eigenschaftseinschränkung, da die zugeordnete [SPropertyRestriction](spropertyrestriction.md) Struktur das Eigenschafts-Tag enthält. 
  
Weitere Informationen zu den **SCommentRestriction** Struktur und Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[MAPI-Strukturen](mapi-structures.md)

