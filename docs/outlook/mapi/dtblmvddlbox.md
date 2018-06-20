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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ede0a448a32565446e614fc2d14f2a72a9549dad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791613"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Betrifft**: Outlook 
  
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

## <a name="members"></a>Members

 **ulFlags**
  
> Reserviert. NULL muss sein.
    
 **ulMVPropTag**
  
> Eigenschaftentag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING. Die unterschiedlichen Werte dieser Eigenschaft werden als unterschiedliche Einträge in der Dropdown-Liste angezeigt.
    
## <a name="remarks"></a>Hinweise

Eine Struktur **DTBLMVDDLBOX** beschreibt eine mehrwertige Dropdown-Liste eine schreibgeschützte Liste von Elementen. Mithilfe ein mehrwertiges Dropdown-Listenfeld werden Werte angezeigt, wenn ein Benutzer auf eine Bildlaufleiste klickt. 
  
Die Daten, die angezeigt werden, stammt aus der Eigenschaft im **UlMVPropTag** -Member identifiziert. Es ist nicht erforderlich zum Lesen aus der Eigenschaft-Schnittstelle, die das Display-Tabelle zugeordnet ist. Darüber hinaus, da Benutzer nicht vor dieser Art von Listenfelder eine Auswahl treffen können, werden Daten nicht auf die Eigenschaft Schnittstelle geschrieben. 
  
Nur mehrwertige Zeichenfolgeneigenschaften werden für die mehrwertige Dropdown-Liste unterstützt. andere mehrwertige Eigenschaft werden nicht unterstützt. 
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

