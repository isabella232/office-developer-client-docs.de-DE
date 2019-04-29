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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430609"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Kommentar Einschränkung, die zum kommentieren einer Einschränkung verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Die Anzahl der Eigenschaftswerte im Array, auf die durch das **lpProp** -Element verwiesen wird. 
    
 **lpRes**
  
> Zeiger auf eine [SRestriction](srestriction.md) -Struktur. 
    
 **lpProp**
  
> Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die jeweils das Property-Tag und den Wert für eine benannte Eigenschaft enthalten. 
    
## <a name="remarks"></a>Bemerkungen

Die **SCommentRestriction** -Struktur ordnet ein Objekt einer Gruppe benannter Eigenschaften zu. Kommentar Einschränkungen sind im Gegensatz zu anderen Einschränkungen, da Sie nicht ausgewertet werden. Das heißt, Sie werden von der [IMAPITable:: Restrict](imapitable-restrict.md) -Methode ignoriert. Es gibt keine Auswirkung auf die Zeilen, die von der [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode zurückgegeben werden, nachdem ein **IMAPITable:: Restrict** -Aufruf ausgeführt wurde. 
  
Die **SCommentRestriction** -Struktur kann verwendet werden, um anwendungsspezifische Informationen mit einer Einschränkung beizubehalten, wenn Sie auf dem Datenträger gespeichert wird. Beispielsweise kann ein Client, der den Namen einer benannten Eigenschaft speichert, die in einer Eigenschaftseinschränkung verwendet wird, dies in einer **SCommentRestriction** -Struktur tun. Das Speichern eines Eigenschaftennamens ist in einer Eigenschaftseinschränkung nicht möglich, da die zugeordnete [SPropertyRestriction](spropertyrestriction.md) -Struktur nur das Tag der Eigenschaft enthält. 
  
Weitere Informationen zur **SCommentRestriction** -Struktur und zu Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[MAPI-Strukturen](mapi-structures.md)

