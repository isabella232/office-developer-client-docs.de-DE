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
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325760"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Dropdownliste, die in einem Dialogfeldverwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>Elemente

 **ulFlags**
  
> Reserviert muss NULL sein.
    
 **ulMVPropTag**
  
> Property-Tag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING. Die unterschiedlichen Werte dieser Eigenschaft werden in der Dropdownliste als verschiedene Einträge angezeigt.
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLMVDDLBOX** -Struktur beschreibt eine mehrwertige Dropdownliste eine schreibgeschützte Liste von Elementen. Bei Verwendung einer mehrwertigen Dropdownliste werden Werte angezeigt, wenn ein Benutzer auf eine Bildlaufleiste klickt. 
  
Die angezeigten Daten stammen aus der im **ulMVPropTag** -Element angegebenen Eigenschaft. Es ist nicht erforderlich, von der Eigenschaften Schnittstelle zu lesen, die der Anzeigetabelle zugeordnet ist. Da Benutzer keine Auswahl aus diesen Typen von Listenfeldern treffen können, werden auch keine Daten in die Eigenschaften Schnittstelle geschrieben. 
  
Nur mehrwertige Zeichenfolgeneigenschaften werden für die mehrwertige Dropdownliste unterstützt. andere mehrwertige Eigenschaftstypen werden nicht unterstützt. 
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

