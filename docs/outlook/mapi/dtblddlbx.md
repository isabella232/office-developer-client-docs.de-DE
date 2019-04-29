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
  
Beschreibt ein Dropdownlisten-Steuerelement, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Reserviert, muss NULL sein. 
    
 **ulPRDisplayProperty**
  
> Property-Tag für eine Eigenschaft vom Typ PT_TSTRING. Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **ulPRTableName** -Element identifiziert wird. Die Werte für diese Eigenschaft werden in der Liste angezeigt. 
    
 **ulPRSetProperty**
  
> Property-Tag für eine Eigenschaft eines beliebigen Typs. Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **ulPRTableName** -Element identifiziert wird. Wenn der Benutzer der Liste einen Eigenschaftswert für das **ulPRDisplayProperty** -Element aus den Zeilen der Tabelle auswählt, die durch das **ulPRTableName** -Element identifiziert wird, wird das entsprechende **ulPRSetProperty** -Element festgelegt. 
    
 **ulPRTableName**
  
> Property-Tag für eine Table-Eigenschaft vom Typ PT_OBJECT, die mithilfe eines **openProperty** -Aufrufs geöffnet werden kann. Die Tabelle sollte zwei Spalten aufweisen: **ulPRDisplayProperty** und **ulPRSetProperty**. Die Zeilen der Tabelle sollten den Elementen in der Liste entsprechen.
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLDDLBX** -Struktur beschreibt ein Dropdownlisten-Steuerelement, das als einzelnes Element angezeigt wird, bis der Benutzer die Erweiterung auswählt. 
  
Die drei durch die Property-Tags identifizierten Eigenschaften arbeiten zusammen, um die Informationen in der Liste anzuzeigen und eine zugehörige Eigenschaft festzulegen. Der **ulPRTableName** -Member ist ein Table-Objekt, auf das über einen Aufruf von [IMAPIProp:: OpenProperty](imapiprop-openproperty.md)zugegriffen wird. Die Tabelle enthält zwei Spalten: eine Spalte für die Eigenschaft, die vom **ulPRDisplayProperty** -Element identifiziert wird, und die andere für die Eigenschaft, die vom **ulPRSetProperty** -Element identifiziert wird. 
  
Die **ulPRDisplayProperty** -Eigenschaft steuert die Listenanzeige. Wenn ein Benutzer einen der Werte aus der Anzeige auswählt, ruft MAPI [IMAPIProp::](imapiprop-setprops.md) SetProps auf, um die entsprechende Eigenschaft festzulegen, die vom **ulPRSetProperty** -Mitglied identifiziert wird. Dies hat zur Folge, dass die Eigenschaft in derselben Zeile wie die ausgewählte Anzeigeeigenschaft angezeigt wird. Das **ulPRSetProperty** -Element kann nicht auf **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md)) festgelegt werden.
  
In der Liste wird ein Anfangswert angezeigt, wenn MAPI die vom **ulPRSetProperty** -Element dargestellte Eigenschaft durch einen Aufruf von [IMAPIProp::](imapiprop-getprops.md) GetProps abgerufen und eine Zeile in der Tabelle mit dem Wert für das **ulPRSetProperty** -Element gefunden hat. Der anfänglich angezeigte Wert ist der Inhalt der **ulPRDisplayProperty** -Spalte aus dieser Zeile, die mit der-Eigenschaft im **ulPRDisplayProperty** -Element der Struktur übereinstimmt. Der von getProps zurückgegebene Wert für die durch das **ulPRDisplayProperty** -Element angegebene Eigenschaft wird zum Anfangswert, der angezeigt wird, wenn die Liste zum ersten Mal angezeigt wird. **** 
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md). Weitere Informationen zu Eigenschaftstypen finden Sie unter [MAPI property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[MAPI-Strukturen](mapi-structures.md)
  
[Anzeigen der Tabellen Implementierung](display-table-implementation.md)
  
[Anzeige Tabellen](display-tables.md)
  
[Übersicht über die MAPI-EigenschaftsTypen](mapi-property-type-overview.md)

