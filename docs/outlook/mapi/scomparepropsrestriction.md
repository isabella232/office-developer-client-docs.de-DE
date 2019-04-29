---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440003"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Compare-Eigenschaftseinschränkung, die zwei Eigenschaften mithilfe eines relationalen Operators testet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>Members

**RelOp**
  
> Relationaler Operator, der zum Vergleichen der beiden Eigenschaften verwendet werden soll. Folgende Werte sind möglich:
    
  - RELOP_GE: der Vergleich erfolgt basierend auf einem größer oder gleich dem ersten Wert.
      
  - RELOP_GT: der Vergleich erfolgt basierend auf einem höheren ersten Wert.
      
  - RELOP_LE: der Vergleich erfolgt basierend auf einem niedrigeren oder gleichen ersten Wert.
      
  - RELOP_LT: der Vergleich erfolgt basierend auf einem niedrigeren ersten Wert.
      
  - RELOP_NE: der Vergleich erfolgt basierend auf ungleich Werten.
      
  - RELOP_RE: der Vergleich basiert auf LIKE (Regular Expression)-Werten.
      
  - RELOP_EQ: der Vergleich erfolgt basierend auf gleichen Werten.
    
**ulPropTag1**
  
> Property-Tag der ersten Eigenschaft, die verglichen werden soll. 
    
**ulPropTag2**
  
> Property-Tag der zweiten Eigenschaft, die verglichen werden soll.
    
## <a name="remarks"></a>Bemerkungen

Die Vergleichsreihenfolge ist _(Property Tag 1) (relationaler Operator) (Eigenschafts Tag 2)_. Die zu vergleichenden Eigenschaften müssen vom gleichen Typ sein. Der Versuch, Eigenschaften unterschiedlicher Typen zu vergleichen, bewirkt, dass MAPI oder der Dienstanbieter den Fehlerwert MAPI_E_TOO_COMPLEX aus der [IMAPITable](imapitableiunknown.md) -Methode zurückgibt, an die die Struktur als Parameter übergeben wird. 
  
Das Ergebnis einer Einschränkung des Compare-Eigenschaftswerts ist nicht definiert, wenn eine oder beide Eigenschaften nicht vorhanden sind. Wenn ein Client ein genau definiertes Verhalten für eine solche Einschränkung benötigt und nicht sicher ist, ob die Eigenschaft vorhanden ist (beispielsweise ist es keine erforderliche Spalte einer Tabelle), sollte es eine **und** -Einschränkung für den Join der Compare-Eigenschaftseinschränkung mit einem exist-Objekt erstellen. Einschränkung. Verwenden Sie eine [SExistRestriction](sexistrestriction.md) -Struktur, um die exist-Einschränkung und eine [SAndRestriction](sandrestriction.md) -Struktur zum Definieren der **und-** Einschränkung zu definieren. 
  
Die im **ulPropTag1** -und **ulPropTag2** -Member angegebenen Eigenschaften können mehrwertig sein, wenn der Dienstanbieter Sie unterstützt. 
  
Weitere Informationen zur **SComparePropsRestriction** -Struktur und zu Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

