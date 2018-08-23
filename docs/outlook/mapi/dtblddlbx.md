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
ms.openlocfilehash: 3307bb252ca4436999a541f85657fed9878c798a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579396"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Dropdown-Listenfeld-Steuerelement, das in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet wird.
  
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
  
> Reserviert, muss NULL sein. 
    
 **ulPRDisplayProperty**
  
> Eigenschaftentag für eine Eigenschaft vom Typ PT_TSTRING. Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **UlPRTableName** -Element identifiziert. Die Werte für diese Eigenschaft sind in der Liste angezeigt. 
    
 **ulPRSetProperty**
  
> Eigenschaftentag für eine Eigenschaft eines beliebigen Typs. Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **UlPRTableName** -Element identifiziert. Wenn der Benutzer der Liste einen Eigenschaftswert für das Element **UlPRDisplayProperty** aus den Zeilen der Tabelle der Member **UlPRTableName** identifizierten auswählt, wird der entsprechende **UlPRSetProperty** Member festgelegt. 
    
 **ulPRTableName**
  
> Rufen Sie die Eigenschaftentag für ein Table-Eigenschaft vom Typ PT_OBJECT, die mithilfe einer **OpenProperty** geöffnet werden können. Die Tabelle sollte zwei Spalten: **UlPRDisplayProperty** und **UlPRSetProperty**. Die Zeilen der Tabelle sollten die Elemente in der Liste entsprechen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Struktur **DTBLDDLBX** beschreibt ein Dropdown-Listenfeld-Steuerelement, das als einzelnes Element angezeigt wird, bis der Benutzer entscheidet, um ihn zu erweitern. 
  
Die Eigenschaftentags identifizierten drei Eigenschaften arbeiten zusammen, um die Informationen in der Liste anzuzeigen, und legen Sie eine verknüpfte-Eigenschaft. Der **UlPRTableName** -Member ist ein Table-Objekt, das durch einen Aufruf von [IMAPIProp::OpenProperty](imapiprop-openproperty.md)zugegriffen wird. Die Tabelle enthält zwei Spalten: eine Spalte für die Eigenschaft durch das **UlPRDisplayProperty** -Element, und das andere für die identifizierten **UlPRSetProperty** Members-Eigenschaft identifiziert. 
  
Die **UlPRDisplayProperty** -Eigenschaft steuert die Anzeige der Browserliste. Wenn ein Benutzer einen der Werte aus der Anzeige auswählt, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) , um die entsprechende Eigenschaft festzulegen, wie durch das **UlPRSetProperty** -Element identifiziert. Dies bedeutet, dass die Eigenschaft in der gleichen Zeile wie die ausgewählten Anzeigeeigenschaft. Das **UlPRSetProperty** -Element kann nicht auf **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) festgelegt werden.
  
Anfangswert wird in der Liste angezeigt, wenn MAPI dargestellte vom **UlPRSetProperty** Member durch einen Aufruf von [IMAPIProp::GetProps](imapiprop-getprops.md) Eigenschaft abgerufen und befindet sich eine Zeile in der Tabelle mit dem Wert für den **UlPRSetProperty** Member hat. Der erste angezeigte Wert entspricht dem Inhalt der **UlPRDisplayProperty** Spalte aus dieser Zeile, die die Eigenschaft im **UlPRDisplayProperty** -Member der Struktur entspricht. Der von **GetProps** für die identifizierten **UlPRDisplayProperty** Members-Eigenschaft zurückgegebene Wert wird der erste Wert, der angezeigt wird, wenn die Liste zuerst angezeigt wird. 
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md). Informationen zu Eigenschaftstypen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[MAPI-Strukturen](mapi-structures.md)
  
[Anzeigen der Tabellenimplementierung](display-table-implementation.md)
  
[Anzeigetabellen](display-tables.md)
  
[Übersicht über Typ von MAPI-Eigenschaft](mapi-property-type-overview.md)

