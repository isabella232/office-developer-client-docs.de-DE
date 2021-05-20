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

**relop**
  
> Relationaler Operator, der zum Vergleichen der beiden Eigenschaften verwendet werden soll. Mögliche Werte sind:
    
  - RELOP_GE: Der Vergleich basiert auf einem höheren oder gleichen ersten Wert.
      
  - RELOP_GT: Der Vergleich basiert auf einem größeren ersten Wert.
      
  - RELOP_LE: Der Vergleich basiert auf einem kleineren oder gleichen ersten Wert.
      
  - RELOP_LT: Der Vergleich basiert auf einem niedrigeren ersten Wert.
      
  - RELOP_NE: Der Vergleich basiert auf ungleichen Werten.
      
  - RELOP_RE: Der Vergleich wird basierend auf LIKE -Werten (regulärer Ausdruck) vorgenommen.
      
  - RELOP_EQ: Der Vergleich basiert auf gleichen Werten.
    
**ulPropTag1**
  
> Eigenschaftstag der ersten zu vergleichende Eigenschaft. 
    
**ulPropTag2**
  
> Eigenschaftstag der zweiten zu vergleichende Eigenschaft.
    
## <a name="remarks"></a>Hinweise

Die Vergleichsreihenfolge ist  _(Eigenschaftstag 1) (relationaler Operator) (Eigenschaftstag 2)_. Die zu vergleichenden Eigenschaften müssen vom gleichen Typ sein. Wenn Sie versuchen, Eigenschaften verschiedener Typen zu vergleichen, gibt MAPI oder der Dienstanbieter den Fehlerwert MAPI_E_TOO_COMPLEX aus der [IMAPITable-Methode](imapitableiunknown.md) zurück, an die die Struktur als Parameter übergeben wird. 
  
Das Ergebnis einer Einschränkung des Werts einer Compare-Eigenschaft ist nicht definiert, wenn eine oder beide Eigenschaften nicht vorhanden sind. Wenn ein Client ein wohldefiniertes Verhalten für eine solche Einschränkung erfordert und nicht sicher ist, ob die Eigenschaft vorhanden ist (z. B. ist es keine erforderliche Spalte einer Tabelle), sollte er eine **AND-Einschränkung** erstellen, um die Eigenschaftseinschränkung compare mit einer vorhandenen Einschränkung zu verbinden. Verwenden Sie eine [SExistRestriction-Struktur,](sexistrestriction.md) um die exist-Einschränkung und eine [SAndRestriction-Struktur](sandrestriction.md) zu definieren, um die **AND-Einschränkung zu** definieren. 
  
Die in den **Mitgliedern ulPropTag1** und **ulPropTag2** angegebenen Eigenschaften können mehrwertig sein, wenn der Dienstanbieter sie unterstützt. 
  
Weitere Informationen zur Struktur und Einschränkungen **von SComparePropsRestriction** im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

