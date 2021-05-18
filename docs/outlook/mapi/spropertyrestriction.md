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
  
Beschreibt eine Eigenschaftseinschränkung, die verwendet wird, um eine Konstante mit dem Wert einer Eigenschaft zu übereinstimmen.
  
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

**relop**
  
> Relationaler Operator, der in der Suche verwendet wird. Mögliche Werte sind:
    
  - RELOP_GE: Der Vergleich basiert auf einem höheren oder gleichen ersten Wert.
        
  - RELOP_GT: Der Vergleich basiert auf einem größeren ersten Wert.
        
  - RELOP_LE: Der Vergleich basiert auf einem kleineren oder gleichen ersten Wert.
        
  - RELOP_LT: Der Vergleich basiert auf einem niedrigeren ersten Wert.
        
  - RELOP_NE: Der Vergleich basiert auf ungleichen Werten.
        
  - RELOP_RE: Der Vergleich wird basierend auf LIKE -Werten (regulärer Ausdruck) vorgenommen.
        
  - RELOP_EQ: Der Vergleich basiert auf gleichen Werten.
    
**ulPropTag**
  
> Eigenschaftstag, das die zu vergleichende Eigenschaft identifiziert. 
    
**lpProp**
  
> Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die den konstanten Wert enthält, der im Vergleich verwendet wird. 
    
## <a name="remarks"></a>Hinweise

Es gibt zwei Eigenschaftstags in einer **SPropertyRestriction-Struktur.** Einer befindet sich im **ulPropTag-Element** und das andere im **ulPropTag-Element** der **SPropValue-Struktur,** auf die **von lpProp verwiesen wird.** MAPI erfordert sowohl das Eigenschaftenbezeichnerfeld als auch das Eigenschaftentypfeld. Der **ulPropTag** in **SPropertyRestriction** ist die zu erfüllende Eigenschaft, und der **lpProp-Zeiger** der **SPropertyRestriction** auf den **UlPropTag-Typ** **des SPropValue** gibt an, wie der Memberwert der **lpProp-Union** interpretiert wird. Die beiden Eigenschaftstypen müssen übereinstimmen, sonst wird der Fehlerwert MAPI_E_TOO_COMPLEX zurückgegeben, wenn die Einschränkung in einem Aufruf von [IMAPITable::Restrict](imapitable-restrict.md) oder [IMAPITable::FindRow](imapitable-findrow.md)verwendet wird. 
  
Die Vergleichsreihenfolge  _ist (Eigenschaftswert) (relationaler Operator) (Konstantenwert)_.
  
Wenn eine Eigenschaftseinschränkung an **IMAPITable::Restrict** oder **IMAPITable::FindRow** übergeben wird und die Zieleigenschaft nicht vorhanden ist, sind die Ergebnisse der Einschränkung nicht definiert. Durch Das Erstellen einer **AND-Einschränkung,** die die Eigenschaftseinschränkung mit einer **EXIST-Einschränkung** beitritt, kann ein Anrufer genaue Ergebnisse garantiert werden. Verwenden Sie eine [SExistRestriction-Struktur,](sexistrestriction.md) um die **EXIST-Einschränkung** und eine [SAndRestriction-Struktur](sandrestriction.md) zu definieren, um die **AND-Einschränkung zu** definieren. 
  
Mehrwertige Eigenschaftstags können in Eigenschaftseinschränkungen verwendet werden, wenn der Dienstanbieter, der die Tabelle implementieren, diese unterstützt. Wenn unterstützt, können mehrwertige Eigenschaftstags überall verwendet werden, an der einwertige Eigenschaftstags verwendet werden können. 
  
Mehrwertige Eigenschaftstags können in den folgenden Methoden verwendet werden:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Ein beachtenswerter Fall, wenn die beiden Eigenschaftstags nicht übereinstimmen, ist das Einschränken auf eine mehrwertige Eigenschaft. In diesem Fall muss Folgendes zutreffen. > Wenn der Eigenschaftentyp des **ulPropTag** von **SPropertyRestriction** das > MV_FLAG (0x1000) enthält, sollte der Eigenschaftstyp des **ulPropTag** von **SPropValue** dem ersten minus dem MV_FLAG-Bit-Flag entsprechen, d. h. dem umgekehrten. > Um beispielsweise die Verwendung einer benutzerdefinierten Zeichenfolgeneigenschaft mit mehreren Wert einzuschränken, z. B. eine Kategorie mit einem Eigenschaftstag für die Eigenschaft 0x8012101f, d. h. PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), würde die entsprechende **SPropertyRestriction** wie folgt angezeigt. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Beachten Sie, dass, wenn der Eigenschaftentyp des **ulPropTag** von **SPropValue** das MV_FLAG-Bit-Flag enthält, die wahrscheinliche Rückgabe MAPI_E_TOO_COMPLEX. 
  
Weitere Informationen zur **SPropertyRestriction-Struktur** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [MAPI-Strukturen](mapi-structures.md)

