---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 53095151ae2f378a2784cf7405955c6338d3e163
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576352"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Dropdownlistensteuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a>Elemente

 **ulFlags**
  
> Reserviert, muss Null sein. 
    
 **ulPRDisplayProperty**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_TSTRING. Diese Eigenschaft ist eine der Spalten in der Tabelle, die vom **ulPRTableName-Element** identifiziert wird. Die Werte für diese Eigenschaft werden in der Liste angezeigt. 
    
 **ulPRSetProperty**
  
> Eigenschaftstag für eine Eigenschaft eines beliebigen Typs. Diese Eigenschaft ist eine der Spalten in der Tabelle, die vom **ulPRTableName-Element** identifiziert wird. Wenn der Benutzer der Liste einen Eigenschaftswert für das **UlPRDisplayProperty-Element** aus den Zeilen der Tabelle auswählt, die vom **ulPRTableName-Element** identifiziert wird, wird das entsprechende **ulPRSetProperty-Element** festgelegt. 
    
 **ulPRTableName**
  
> Eigenschaftstag für eine Tabelleneigenschaft vom Typ PT_OBJECT, die mithilfe eines **OpenProperty-Aufrufs** geöffnet werden kann. Die Tabelle sollte zwei Spalten aufweisen: **ulPRDisplayProperty** und **ulPRSetProperty**. Die Zeilen der Tabelle sollten Elementen in der Liste entsprechen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DTBLDDLBX-Struktur** beschreibt ein Dropdownlistensteuerelement, das als einzelnes Element angezeigt wird, bis der Benutzer entscheidet, es zu erweitern. 
  
Die drei von den Eigenschaftentags identifizierten Eigenschaften arbeiten zusammen, um die Informationen in der Liste anzuzeigen und eine verwandte Eigenschaft festzulegen. Der **ulPRTableName-Member** ist ein Tabellenobjekt, auf das über einen Aufruf von [IMAPIProp::OpenProperty](imapiprop-openproperty.md)zugegriffen wird. Die Tabelle weist zwei Spalten auf: eine Spalte für die eigenschaft, die vom **ulPRDisplayProperty-Element** identifiziert wird, und die andere spalte für die eigenschaft, die vom **ulPRSetProperty-Element** identifiziert wird. 
  
Die **ulPRDisplayProperty-Eigenschaft** steuert die Listenanzeige. Wenn ein Benutzer einen der Werte aus der Anzeige auswählt, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) auf, um die entsprechende Eigenschaft wie vom **ulPRSetProperty-Element** identifiziert festzulegen. Dies bedeutet, dass sich die Eigenschaft in derselben Zeile wie die ausgewählte Anzeigeeigenschaft befindet. Das **ulPRSetProperty-Element** kann nicht auf **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) festgelegt werden.
  
Ein Anfangswert wird in der Liste angezeigt, wenn MAPI die vom **ulPRSetProperty-Element** dargestellte Eigenschaft über einen Aufruf von [IMAPIProp::GetProps](imapiprop-getprops.md) abgerufen und eine Zeile in der Tabelle mit dem Wert für das **element ulPRSetProperty** gefunden hat. Der anfänglich angezeigte Wert ist der Inhalt der **UlPRDisplayProperty-Spalte** aus dieser Zeile, die der Eigenschaft im **ulPRDisplayProperty-Element** der Struktur entspricht. Der von **GetProps** für die vom **ulPRDisplayProperty-Element** identifizierte Eigenschaft zurückgegebene Wert wird zum Anfangswert, der angezeigt wird, wenn die Liste zum ersten Mal angezeigt wird. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md) Informationen zu Eigenschaftstypen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[MAPI-Strukturen](mapi-structures.md)
  
[Implementierung von Anzeigetabellen](display-table-implementation.md)
  
[Anzeigen von Tabellen](display-tables.md)
  
[Übersicht über mapi-Eigenschaftstypen](mapi-property-type-overview.md)

