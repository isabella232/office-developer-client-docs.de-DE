---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 910f779f3463ee5dccd052655a442ef24c2cce58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570681"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Dropdown-Listenfeld, die in einem Dialogfeld verwendet werden, die aus einer Tabelle anzeigen erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>Elemente

 **ulFlags**
  
> Reserviert. NULL muss sein.
    
 **ulMVPropTag**
  
> Eigenschaftentag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING. Die unterschiedlichen Werte dieser Eigenschaft werden als unterschiedliche Einträge in der Dropdown-Liste angezeigt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Struktur **DTBLMVDDLBOX** beschreibt eine mehrwertige Dropdown-Liste eine schreibgeschützte Liste von Elementen. Mithilfe ein mehrwertiges Dropdown-Listenfeld werden Werte angezeigt, wenn ein Benutzer auf eine Bildlaufleiste klickt. 
  
Die Daten, die angezeigt werden, stammt aus der Eigenschaft im **UlMVPropTag** -Member identifiziert. Es ist nicht erforderlich zum Lesen aus der Eigenschaft-Schnittstelle, die das Display-Tabelle zugeordnet ist. Darüber hinaus, da Benutzer nicht vor dieser Art von Listenfelder eine Auswahl treffen können, werden Daten nicht auf die Eigenschaft Schnittstelle geschrieben. 
  
Nur mehrwertige Zeichenfolgeneigenschaften werden für die mehrwertige Dropdown-Liste unterstützt. andere mehrwertige Eigenschaft werden nicht unterstützt. 
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

