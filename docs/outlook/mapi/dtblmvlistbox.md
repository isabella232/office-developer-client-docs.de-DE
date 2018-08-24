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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f7c1241f2ad31dee8277f3b3b77ac02137067a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576309"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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

