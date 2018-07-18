---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0de5bf5d5bb4d8c5606e97bdbc6e70493609a05f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791611"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Betrifft**: Outlook 
  
Beschreibt eine mehrwertige Liste, die in einem Dialogfeld angezeigt werden, die aus einer Tabelle anzeigen erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Elemente

 **ulFlags**
  
> Reserviert. NULL muss sein.
    
 **ulMVPropTag**
  
> Eigenschaftentag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING.
    
## <a name="remarks"></a>Bemerkungen

Eine Struktur **DTBLMVLISTBOX** beschreibt eine standard mehrwertige Liste, die eine schreibgeschützte Liste der Elemente verfügt. Eine mehrwertige Liste verwenden, werden die Werte sofort angezeigt. 
  
Die Daten, die angezeigt werden, stammt aus der Eigenschaft im **UlMVPropTag** -Member identifiziert. Es ist nicht erforderlich zum Lesen aus der Eigenschaft-Schnittstelle, die das Display-Tabelle zugeordnet ist. Darüber hinaus, da der Benutzer eine Auswahl aus Risiko dieser Arten von Listen nicht können, werden Daten nicht auf die Eigenschaft Schnittstelle geschrieben. 
  
Nur mehrwertige Zeichenfolgeneigenschaften werden für die Liste mit mehreren Werten unterstützt. andere mehrwertige Eigenschaft werden nicht unterstützt. 
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

