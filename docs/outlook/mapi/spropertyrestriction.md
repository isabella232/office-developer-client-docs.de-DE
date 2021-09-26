---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 66ee8e34cc8c42e2ac656284d91a2f2b64c669da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629557"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Eigenschaftseinschränkung, die verwendet wird, um eine Konstante mit dem Wert einer Eigenschaft zuzuordnen.
  
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

## <a name="members"></a>Members

**relop**
  
> Relationaler Operator, der bei der Suche verwendet wird. Mögliche Werte sind:
    
  - RELOP_GE: Der Vergleich erfolgt basierend auf einem größeren oder gleichen ersten Wert.
        
  - RELOP_GT: Der Vergleich erfolgt basierend auf einem größeren ersten Wert.
        
  - RELOP_LE: Der Vergleich erfolgt basierend auf einem kleineren oder gleichen ersten Wert.
        
  - RELOP_LT: Der Vergleich basiert auf einem niedrigeren ersten Wert.
        
  - RELOP_NE: Der Vergleich erfolgt basierend auf Denkwerten.
        
  - RELOP_RE: Der Vergleich basiert auf LIKE-Werten (regulärer Ausdruck).
        
  - RELOP_EQ: Der Vergleich erfolgt basierend auf gleichen Werten.
    
**ulPropTag**
  
> Eigenschaftstag, das die zu vergleichende Eigenschaft identifiziert. 
    
**lpProp**
  
> Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die den konstanten Wert enthält, der im Vergleich verwendet wird. 
    
## <a name="remarks"></a>Bemerkungen

Es gibt zwei Eigenschaftentags in einer **SPropertyRestriction-Struktur.** Einer befindet sich im **ulPropTag-Element** und das andere befindet sich im **ulPropTag-Element** der **SPropValue-Struktur,** auf die von **lpProp** verwiesen wird. MAPI erfordert sowohl das Eigenschaftsbezeichnerfeld als auch das Eigenschaftentypfeld. Der **ulPropTag** in **SPropertyRestriction** ist die Eigenschaft, die abgeglichen werden soll, und der **lpProp-Zeiger** der **SPropertyRestriction** auf den **UlPropTag-Typ** des **SPropValue** gibt an, wie der Elementwert der **lpProp-Union** interpretiert wird. Die beiden Eigenschaftstypen müssen übereinstimmen, andernfalls wird der Fehlerwert MAPI_E_TOO_COMPLEX zurückgegeben, wenn die Einschränkung in einem Aufruf von [IMAPITable::Restrict](imapitable-restrict.md) oder [IMAPITable::FindRow](imapitable-findrow.md)verwendet wird. 
  
Die Vergleichsreihenfolge ist _(Eigenschaftswert) (relationaler Operator) (Konstantenwert)._
  
Wenn eine Eigenschaftseinschränkung an **IMAPITable::Restrict** oder **IMAPITable::FindRow** übergeben wird und die Zieleigenschaft nicht vorhanden ist, sind die Ergebnisse der Einschränkung nicht definiert. Durch Erstellen  einer AND-Einschränkung, die die Eigenschaftseinschränkung mit einer **EXIST-Einschränkung** verknüpft, kann ein Aufrufer garantiert genaue Ergebnisse erhalten. Verwenden Sie eine [SExistRestriction-Struktur,](sexistrestriction.md) um die **EXIST-Einschränkung** und eine [SAndRestriction-Struktur](sandrestriction.md) zum Definieren der **AND-Einschränkung** zu definieren. 
  
Mehrwertige Eigenschaftstags können in Eigenschaftseinschränkungen verwendet werden, wenn der Dienstanbieter, der die Tabelle implementiert, diese unterstützt. Wenn dies unterstützt wird, können mehrwertige Eigenschaftstags überall verwendet werden, wo einwertige Eigenschaftstags verwendet werden können. 
  
Mehrwertige Eigenschaftstags können in den folgenden Methoden verwendet werden:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Ein wichtiger Fall, in dem die beiden Eigenschaftentags nicht übereinstimmen, ist die Einschränkung auf eine Mehrwerteigenschaft. In diesem Fall muss Folgendes zutreffen. > Wenn der Eigenschaftstyp des **ulPropTag** von **SPropertyRestriction** das Bit-Flag für den Eigenschaftentyp mit mehreren Werten MV_FLAG (0x1000) enthält, sollte der Eigenschaftstyp des **ulPropTag** von **SPropValue** dem ersteren ohne das MV_FLAG Bit-Flag entsprechen, d. h. seine Umkehrung. > Beispielsweise würde die entsprechende **SPropertyRestriction** wie folgt angezeigt, um beispielsweise die Verwendung einer mehrwertigen benutzerdefinierten Zeichenfolgeneigenschaft wie z. B. einer Kategorie mit einem Eigenschaftstag für die Eigenschaft 0x8012101f einzuschränken, d. h. PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)). >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Beachten Sie, dass die wahrscheinliche Rückgabe MAPI_E_TOO_COMPLEX ist, wenn der Eigenschaftstyp des **ulPropTag** von **SPropValue** das MV_FLAG Bit-Flag enthält. 
  
Weitere Informationen zur **Struktur "SPropertyRestriction"** finden Sie unter ["Einschränkungen".](about-restrictions.md) 
  
## <a name="see-also"></a>Siehe auch

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [MAPI-Strukturen](mapi-structures.md)

