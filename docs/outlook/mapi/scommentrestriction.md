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
  
Beschreibt eine Kommentareinschränkung, die zum Kommentieren einer Einschränkung verwendet wird. 
  
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

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Eigenschaftswerte im Array, auf das das **lpProp-Element verweist.** 
    
 **lpRes**
  
> Zeiger auf eine [SRestriction-Struktur.](srestriction.md) 
    
 **lpProp**
  
> Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die jeweils das Eigenschaftstag und den Wert für eine benannte Eigenschaft enthalten. 
    
## <a name="remarks"></a>Hinweise

Die **SCommentRestriction-Struktur** ordnet ein Objekt einem Satz benannter Eigenschaften zu. Kommentareinschränkungen sind im Gegensatz zu anderen Einschränkungen, da sie nicht ausgewertet werden. Das heißt, sie werden von der [IMAPITable::Restrict-Methode](imapitable-restrict.md) ignoriert. Es gibt keine Auswirkungen auf die Zeilen, die von der [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) zurückgegeben werden, nachdem ein **IMAPITable::Restrict-Aufruf** ausgeführt wurde. 
  
Die **SCommentRestriction-Struktur** kann verwendet werden, um anwendungsspezifische Informationen mit einer Einschränkung zu speichern, wenn sie auf dem Datenträger gespeichert werden. Beispielsweise kann ein Client, der den Namen einer benannten Eigenschaft, die in einer Eigenschaftseinschränkung verwendet wird, speichern, dies in einer **SCommentRestriction-Struktur** tun. Das Speichern eines Eigenschaftennamens ist in einer Eigenschaftseinschränkung nicht möglich, da die zugeordnete [SPropertyRestriction-Struktur](spropertyrestriction.md) nur das Eigenschaftstag enthält. 
  
Weitere Informationen zur Struktur und Einschränkungen **von SCommentRestriction** im Allgemeinen finden Sie unter [About Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[MAPI-Strukturen](mapi-structures.md)

