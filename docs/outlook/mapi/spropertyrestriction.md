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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406087"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Eigenschaftseinschränkung, die verwendet wird, um eine Konstante mit dem Wert einer Eigenschaft zu vergleichen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a>Members

**RelOp**
  
> Relationaler Operator, der bei der Suche verwendet wird. Folgende Werte sind möglich:
    
  - RELOP_GE: der Vergleich erfolgt basierend auf einem größer oder gleich dem ersten Wert.
        
  - RELOP_GT: der Vergleich erfolgt basierend auf einem höheren ersten Wert.
        
  - RELOP_LE: der Vergleich erfolgt basierend auf einem niedrigeren oder gleichen ersten Wert.
        
  - RELOP_LT: der Vergleich erfolgt basierend auf einem niedrigeren ersten Wert.
        
  - RELOP_NE: der Vergleich erfolgt basierend auf ungleich Werten.
        
  - RELOP_RE: der Vergleich basiert auf LIKE (Regular Expression)-Werten.
        
  - RELOP_EQ: der Vergleich erfolgt basierend auf gleichen Werten.
    
**ulPropTag**
  
> Property-Tag, das die zu vergleichende Eigenschaft identifiziert. 
    
**lpProp**
  
> Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die den konstanten Wert enthält, der im Vergleich verwendet wird. 
    
## <a name="remarks"></a>Bemerkungen

Es gibt zwei Property-Tags in einer **SPropertyRestriction** -Struktur. Eine befindet sich im **ulPropTag** -Element und die andere befindet sich im **ulPropTag** -Element der **SPropValue** -Struktur, auf die durch **lpProp**verwiesen wird. MAPI erfordert sowohl das Feld Eigenschafts-ID als auch das Feld Eigenschafts. Die **ulPropTag** in **SPropertyRestriction** ist die Eigenschaft, die verglichen werden soll, und der **lpProp** -Zeiger des **SPropertyRestriction** auf den **ulPropTag**-Typ des **SPropValue** gibt an, wie der Members-Wert des **lpProp** Union werden interpretiert. Die beiden Eigenschaftentypen müssen übereinstimmen, andernfalls wird der Fehlerwert MAPI_E_TOO_COMPLEX zurückgegeben, wenn die Einschränkung in einem Aufruf von [IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable:: FindRow](imapitable-findrow.md)verwendet wird. 
  
Die Vergleichsreihenfolge ist _(Eigenschaftswert) (relationaler Operator) (konstanter Wert)_.
  
Wenn eine Eigenschaftseinschränkung an **IMAPITable:: Restrict** oder **IMAPITable:: FindRow** übergeben wird und die Target-Eigenschaft nicht vorhanden ist, sind die Ergebnisse der Einschränkung nicht definiert. Durch das Erstellen einer **and** -Einschränkung, die die Eigenschaftseinschränkung mit einer **exist** -Einschränkung verknüpft, kann ein Aufrufer exakte Ergebnisse garantieren. Verwenden Sie eine [SExistRestriction](sexistrestriction.md) -Struktur, um die **exist** -Einschränkung und eine [SAndRestriction](sandrestriction.md) -Struktur zum Definieren der **und-** Einschränkung zu definieren. 
  
Mehrwertige Eigenschaftstags können in Eigenschaftseinschränkungen verwendet werden, wenn der Dienstanbieter, der die Tabelle implementiert, diese unterstützt. Wenn unterstützt, mehrwertige Eigenschaftstags können verwendet werden, wo einwertige Eigenschaftstags verwendet werden können. 
  
Mehrwertige Eigenschaftstags können in den folgenden Methoden verwendet werden:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Ein bemerkenswerter Fall, wenn die beiden Eigenschaftstags nicht übereinstimmen, ist die Beschränkung auf eine mehrwertige Eigenschaft. In diesem Fall muss Folgendes zutreffen. > wenn der Eigenschaftentyp des **ulPropTag** von **SPropertyRestriction** den mehrwertigen Eigenschaftentyp Bit Flag MV_FLAG (0x1000) enthält, muss der Eigenschaftentyp des **ulPropTag** von **SPropValue** mit dem vorherigen minus der MV_ übereinstimmen. FLAG-Bitflags, das heißt, seine Umkehrfunktion. > Wenn Sie beispielsweise eine benutzerdefinierte Zeichenfolgeneigenschaft mit mehreren Werten wie eine Kategorie mit einem Property-Tag für die Eigenschaft 0x8012101f, also PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)) einschränken möchten, wird die entsprechende **SPropertyRestriction** als folgt. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> beachten Sie, dass, wenn der Eigenschaftentyp des **ulPropTag** von **SPropValue** das MV_FLAG-Bitflags enthält, die Wahrscheinlichkeit MAPI_E_TOO_COMPLEX zurückgegeben wird. 
  
Weitere Informationen zur **SPropertyRestriction** -Struktur finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [MAPI-Strukturen](mapi-structures.md)

