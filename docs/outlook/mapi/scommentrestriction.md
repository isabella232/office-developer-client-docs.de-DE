---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dbc4de78db26d2e93d34feb5f5846c69a942ce5c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609432"
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

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Eigenschaftswerte im Array, auf das der **lpProp-Member** verweist. 
    
 **lpRes**
  
> Zeiger auf eine [SRestriction-Struktur.](srestriction.md) 
    
 **lpProp**
  
> Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die jeweils das Eigenschaftstag und den Wert für eine benannte Eigenschaft enthalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **SCommentRestriction-Struktur** ordnet ein Objekt einer Gruppe benannter Eigenschaften zu. Kommentareinschränkungen sind im Gegensatz zu anderen Einschränkungen, da sie nicht ausgewertet werden. Das heißt, sie werden von der [IMAPITable::Restrict-Methode](imapitable-restrict.md) ignoriert. Es gibt keine Auswirkung auf die Zeilen, die von der [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) zurückgegeben werden, nachdem ein **IMAPITable::Restrict-Aufruf** ausgeführt wurde. 
  
Die **SCommentRestriction-Struktur** kann verwendet werden, um anwendungsspezifische Informationen mit einer Einschränkung beizubehalten, wenn sie auf dem Datenträger gespeichert werden. Beispielsweise kann ein Client, der den Namen einer benannten Eigenschaft speichert, die in einer Eigenschaftseinschränkung verwendet wird, dies in einer **SCommentRestriction-Struktur** tun. Das Speichern eines Eigenschaftsnamens ist in einer Eigenschaftseinschränkung nicht möglich, da die [zugeordnete SPropertyRestriction-Struktur](spropertyrestriction.md) nur das Eigenschaftstag enthält. 
  
Weitere Informationen zur Struktur und Einschränkungen von **SCommentRestriction** im Allgemeinen finden Sie unter ["Einschränkungen".](about-restrictions.md) 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[MAPI-Strukturen](mapi-structures.md)

