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
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338276"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Liste mit mehreren Werten, die in einem Dialogfeld angezeigt wird, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Elemente

 **ulFlags**
  
> Reserviert muss NULL sein.
    
 **ulMVPropTag**
  
> Property-Tag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING.
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLMVLISTBOX** -Struktur beschreibt eine standardmäßige mehrwertige Liste mit einer schreibgeschützten Liste von Elementen. Bei Verwendung einer standardmäßigen mehrwertigen Liste werden die Werte sofort angezeigt. 
  
Die angezeigten Daten stammen aus der im **ulMVPropTag** -Element angegebenen Eigenschaft. Es ist nicht erforderlich, von der Eigenschaften Schnittstelle zu lesen, die der Anzeigetabelle zugeordnet ist. Da Benutzer keine Auswahl aus diesen Listentypen treffen können, werden auch keine Daten in die Eigenschaften Schnittstelle geschrieben. 
  
Nur mehrwertige Zeichenfolgeneigenschaften werden für die mehrwertige Liste unterstützt. andere mehrwertige Eigenschaftstypen werden nicht unterstützt. 
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

