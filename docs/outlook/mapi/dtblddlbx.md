---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438848"
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
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_TSTRING. Diese Eigenschaft ist eine der Spalten in der Vom **ulPRTableName-Element** identifizierten Tabelle. Die Werte für diese Eigenschaft werden in der Liste angezeigt. 
    
 **ulPRSetProperty**
  
> Eigenschaftstag für eine Eigenschaft eines beliebigen Typs. Diese Eigenschaft ist eine der Spalten in der Vom **ulPRTableName-Element** identifizierten Tabelle. Wenn der Benutzer der Liste einen Eigenschaftswert für das **ulPRDisplayProperty-Element** aus den Zeilen der Tabelle auswählt, die vom **ulPRTableName-Element** identifiziert werden, wird das entsprechende **ulPRSetProperty-Element** festgelegt. 
    
 **ulPRTableName**
  
> Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call. Die Tabelle sollte zwei Spalten enthalten: **ulPRDisplayProperty** und **ulPRSetProperty**. Die Zeilen der Tabelle sollten den Elementen in der Liste entsprechen.
    
## <a name="remarks"></a>Hinweise

Eine **DTBLDDLBX-Struktur** beschreibt ein Dropdownlistensteuerelement, das als einzelnes Element angezeigt wird, bis der Benutzer es erweitert. 
  
Die drei von den Eigenschaftstags identifizierten Eigenschaften arbeiten zusammen, um die Informationen in der Liste anzeigen und eine zugehörige Eigenschaft festlegen. Das **ulPRTableName-Element** ist ein Tabellenobjekt, auf das über einen Aufruf von [IMAPIProp::OpenProperty zugegriffen wird.](imapiprop-openproperty.md) Die Tabelle verfügt über zwei Spalten: eine Spalte für die eigenschaft, die vom **ulPRDisplayProperty-Element** identifiziert wird, und die andere für die Eigenschaft, die vom **ulPRSetProperty-Element** identifiziert wird. 
  
Die **ulPRDisplayProperty-Eigenschaft** steuert die Listenanzeige. Wenn ein Benutzer einen der Werte aus der Anzeige auswählt, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) auf, um die entsprechende Eigenschaft wie vom **ulPRSetProperty-Element** identifiziert zu festlegen. Dies bedeutet, dass die Eigenschaft in derselben Zeile wie die ausgewählte Anzeigeeigenschaft ist. Das **ulPRSetProperty-Element** kann nicht auf PR_NULL **(** [PidTagNull](pidtagnull-canonical-property.md)) festgelegt werden.
  
Ein Anfangswert wird in der Liste angezeigt, wenn MAPI die eigenschaft abgerufen hat, die durch das **ulPRSetProperty-Element** durch einen Aufruf von [IMAPIProp::GetProps](imapiprop-getprops.md) dargestellt wurde und eine Zeile in der Tabelle mit dem Wert für das **ulPRSetProperty-Element** gespeichert wurde. Der anfängliche angezeigte Wert ist der Inhalt der **ulPRDisplayProperty-Spalte** aus dieser Zeile, die der Eigenschaft im **ulPRDisplayProperty-Element** der Struktur entspricht. Der von **GetProps** zurückgegebene Wert für die vom **ulPRDisplayProperty-Element** identifizierte Eigenschaft wird zum Anfänglichen Wert, der angezeigt wird, wenn die Liste zum ersten Mal angezeigt wird. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md). Informationen zu Eigenschaftstypen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[MAPI-Strukturen](mapi-structures.md)
  
[Implementierung der Anzeigetabelle](display-table-implementation.md)
  
[Anzeigen von Tabellen](display-tables.md)
  
[Übersicht über den MAPI-Eigenschaftstyp](mapi-property-type-overview.md)

