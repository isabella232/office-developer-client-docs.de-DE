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
ms.openlocfilehash: 7177b2f0f709939b7580fa7abb87490073bb00c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588811"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wird eine eigenschaftseinschränkung vergleichen, die getestet werden zwei Eigenschaften mit einem relationalen Operator beschrieben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>Elemente

**RelOp-Element**
  
> Relationale Operator, der zum Vergleichen von zwei Eigenschaften verwendet. Mögliche Werte sind wie folgt:
    
  - RELOP_GE: Der Vergleich wird basierend auf dem ersten Wert größer oder gleich vorgenommen.
      
  - RELOP_GT: Der Vergleich wird basierend auf einen höheren Wert für die erste vorgenommen.
      
  - RELOP_LE: Der Vergleich wird basierend auf dem ersten Wert kleiner oder gleich vorgenommen.
      
  - RELOP_LT: Der Vergleich wird basierend auf einen kleineren Wert des ersten vorgenommen.
      
  - RELOP_NE: Der Vergleich basierend auf Werten mit ungleicher erfolgt.
      
  - RELOP_RE: Der Vergleich basierend auf wie Werte (reguläre Ausdrücke) erfolgt.
      
  - RELOP_EQ: Der Vergleich wird basierend auf gleich große Werte vorgenommen.
    
**ulPropTag1**
  
> Eigenschaftentag der Eigenschaft verglichen werden soll. 
    
**ulPropTag2**
  
> Eigenschaftentag der zweiten-Eigenschaft, die verglichen werden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Reihenfolge der Vergleich ist _(Eigenschafts-Tag (1) (relationalen Operator) (Eigenschaftentag 2)_. Die Eigenschaften, die verglichen werden müssen den gleichen Typ aufweisen. Bei dem Versuch, Eigenschaften mit unterschiedlichen Typen verglichen wird MAPI oder den Dienstanbieter den Fehlerwert MAPI_E_TOO_COMPLEX [IMAPITable](imapitableiunknown.md) -Methode zurückgegeben, der die Struktur als Parameter übergeben wird. 
  
Das Ergebnis der Einschränkung Wert Compare-Eigenschaft ist nicht definiert, wenn eine oder beide der Eigenschaften nicht vorhanden sind. Wenn ein Client eindeutig definiertes Verhalten für eine solche Beschränkung erfordert und sich nicht sicher ist, ob die Eigenschaft vorhanden ist (beispielsweise, es ist keine erforderliche Spalte einer Tabelle) sollten sie eine Einschränkung **und** zum Teilnehmen an der eigenschaftseinschränkung vergleichen mit einen vorhanden erstellen Einschränkung. Verwenden Sie eine [SExistRestriction](sexistrestriction.md) -Struktur, um die Einschränkung vorhanden und eine [SAndRestriction](sandrestriction.md) -Struktur so definieren Sie die Einschränkung **und** definieren. 
  
Die Member **ulPropTag1** und **ulPropTag2** angegebenen Eigenschaften können mit mehreren Werten sein, wenn der Dienstanbieter unterstützt. 
  
Weitere Informationen zu den **SComparePropsRestriction** Struktur und Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

