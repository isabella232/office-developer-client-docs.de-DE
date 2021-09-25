---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 963563767723fbdb5e316bbd2ac8c49060b0a296
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609457"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Eigenschaftseinschränkung zum Vergleichen, bei der zwei Eigenschaften mithilfe eines relationalen Operators getestet werden. 
  
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

## <a name="members"></a>Members

**relop**
  
> Relationaler Operator zum Vergleichen der beiden Eigenschaften. Mögliche Werte sind:
    
  - RELOP_GE: Der Vergleich erfolgt basierend auf einem größeren oder gleichen ersten Wert.
      
  - RELOP_GT: Der Vergleich erfolgt basierend auf einem größeren ersten Wert.
      
  - RELOP_LE: Der Vergleich erfolgt basierend auf einem kleineren oder gleichen ersten Wert.
      
  - RELOP_LT: Der Vergleich basiert auf einem niedrigeren ersten Wert.
      
  - RELOP_NE: Der Vergleich erfolgt basierend auf Denkwerten.
      
  - RELOP_RE: Der Vergleich basiert auf LIKE-Werten (regulärer Ausdruck).
      
  - RELOP_EQ: Der Vergleich erfolgt basierend auf gleichen Werten.
    
**ulPropTag1**
  
> Eigenschaftstag der ersten Eigenschaft, die verglichen werden soll. 
    
**ulPropTag2**
  
> Eigenschaftstag der zweiten Eigenschaft, die verglichen werden soll.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Vergleichsreihenfolge ist  _(Eigenschaftstag 1) (relationaler Operator) (Eigenschaftstag 2)_. Die zu vergleichenden Eigenschaften müssen denselben Typ aufweisen. Der Versuch, Eigenschaften unterschiedlicher Typen zu vergleichen, bewirkt, dass MAPI oder der Dienstanbieter den Fehlerwert MAPI_E_TOO_COMPLEX aus der [IMAPITable-Methode](imapitableiunknown.md) zurückgibt, an die die Struktur als Parameter übergeben wird. 
  
Das Ergebnis einer Compare-Eigenschaftswerteinschränkung ist nicht definiert, wenn eine oder beide Eigenschaften nicht vorhanden sind. Wenn ein Client ein klar definiertes Verhalten für eine solche Einschränkung erfordert und nicht sicher ist, ob die Eigenschaft vorhanden ist (z. B. ist es keine erforderliche Spalte einer Tabelle), sollte er eine **AND-Einschränkung** erstellen, um die Eigenschaftseinschränkung mit einer vorhandenen Einschränkung zu verknüpfen. Verwenden Sie eine [SExistRestriction-Struktur,](sexistrestriction.md) um die vorhandene Einschränkung zu definieren, und eine [SAndRestriction-Struktur,](sandrestriction.md) um die **AND-Einschränkung** zu definieren. 
  
Die in den **Membern "ulPropTag1"** und **"ulPropTag2"** angegebenen Eigenschaften können mehrwertiger sein, wenn sie vom Dienstanbieter unterstützt werden. 
  
Weitere Informationen zur Struktur und Einschränkungen von **SComparePropsRestriction** im Allgemeinen finden Sie unter ["Informationen zu Einschränkungen".](about-restrictions.md)
  
## <a name="see-also"></a>Siehe auch

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

