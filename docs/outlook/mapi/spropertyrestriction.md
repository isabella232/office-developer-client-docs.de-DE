---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f59b0041f271010e56dda2f73d2248f133bc1325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795601"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**Betrifft**: Outlook 
  
Beschreibt eine eigenschaftseinschränkung, die verwendet wird, eine Konstante mit dem Wert einer Eigenschaft zuordnen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a>Elemente

**RelOp-Element**
  
> Relationale Operator, der in der Suche verwendet werden soll. Mögliche Werte sind wie folgt:
    
  - RELOP_GE: Der Vergleich wird basierend auf dem ersten Wert größer oder gleich vorgenommen.
        
  - RELOP_GT: Der Vergleich wird basierend auf einen höheren Wert für die erste vorgenommen.
        
  - RELOP_LE: Der Vergleich wird basierend auf dem ersten Wert kleiner oder gleich vorgenommen.
        
  - RELOP_LT: Der Vergleich wird basierend auf einen kleineren Wert des ersten vorgenommen.
        
  - RELOP_NE: Der Vergleich basierend auf Werten mit ungleicher erfolgt.
        
  - RELOP_RE: Der Vergleich basierend auf wie Werte (reguläre Ausdrücke) erfolgt.
        
  - RELOP_EQ: Der Vergleich wird basierend auf gleich große Werte vorgenommen.
    
**ulPropTag**
  
> Eigenschafts-Tag, identifiziert die Eigenschaft verglichen werden soll. 
    
**lpProp**
  
> Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die den konstanten Wert enthält, der im Vergleich verwendet werden. 
    
## <a name="remarks"></a>Bemerkungen

Es sind zwei Eigenschaftentags in eine **SPropertyRestriction** -Struktur. Eine im **UlPropTag** -Member ist und der andere im **UlPropTag** -Member der **SPropValue** Struktur auf **LpProp**zeigt. MAPI erfordert das Feld für den Bezeichner und die Eigenschaft Typ dar. Die **UlPropTag** in **SPropertyRestriction** ist der Eigenschaft abgeglichen wird und der Zeiger **LpProp** der **SPropertyRestriction** der **UlPropTag**Art der **SPropValue** gibt an, wie der Member-Wert, der die **LpProp** Union interpretiert werden. Die beiden Eigenschaftstypen müssen übereinstimmen, sonst den Fehlerwert MAPI_E_TOO_COMPLEX wird zurückgegeben, wenn die Einschränkung wieder in einem Aufruf von [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md)verwendet wird. 
  
Die Reihenfolge der Vergleich ist _(Eigenschaftswert) (relationalen Operator) (Konstantenwert)_.
  
Wenn eine eigenschaftseinschränkung **Methode IMAPITable:: Restrict** oder **IMAPITable** übergeben wird, und die Target-Eigenschaft ist nicht vorhanden, sind die Ergebnisse der Einschränkung nicht definiert. Erstellen Sie eine **AND** -Einschränkung, die die eigenschaftseinschränkung mit einer Einschränkung **vorhanden** verknüpft, kann ein Anrufer genaue Ergebnisse garantiert werden. Verwenden Sie eine [SExistRestriction](sexistrestriction.md) -Struktur, um die Einschränkung **vorhanden** und eine [SAndRestriction](sandrestriction.md) -Struktur so definieren Sie die Einschränkung **und** definieren. 
  
Mehrwertige Eigenschaftentags können in eigenschaftseinschränkungen verwendet werden, wenn der Dienstanbieter Implementieren der Tabelle, die sie unterstützt. Wenn unterstützt, können mit mehreren Werten Eigenschaftentags überall eingesetzt werden, ein einwertiges Eigenschaftentags verwendet werden können. 
  
Mehrwertige Eigenschaftentags können in den folgenden Methoden verwendet werden:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Ist ein wichtiger Fall, wenn die zwei Eigenschaftentags übereinstimmt, wird nicht durch die Beschränkung auf eine mehrwertige Eigenschaft auf. In diesem Fall muss Folgendes gelten. > Wenn der Eigenschaftstyp von der **UlPropTag** des **SPropertyRestriction** das mehrwertige Eigenschaft Typ Bitflag MV_FLAG (0 x 1000) enthält, sollte der Eigenschaftstyp von der **UlPropTag** des **SPropValue** der erste Wert minus der MV_ übereinstimmen. FLAG Bitflag, d. h., die Umkehrung. > Beispielsweise beschränken Sie die Verwendung einer mehrwertige Zeichenfolgeneigenschaft benutzerdefinierte wie eine Kategorie mit einer Eigenschaftentag für die Eigenschaft 0x8012101f, d. h., PROP_TAG (MV_FLAG | PT_UNICODE 0x8012)), als würde die entsprechende **SPropertyRestriction** angezeigt folgt. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Beachten Sie, dass der Eigenschaftstyp von der **UlPropTag** des **SPropValue** das Bitflag MV_FLAG enthält, die wahrscheinlich Rückgabe MAPI_E_TOO_COMPLEX ist. 
  
Weitere Informationen zur Struktur **SPropertyRestriction** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [MAPI-Strukturen](mapi-structures.md)

