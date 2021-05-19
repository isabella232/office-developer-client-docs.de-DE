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
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420745"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Dropdownliste, die in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
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
  
> Reserviert; muss null sein.
    
 **ulMVPropTag**
  
> Eigenschaftstag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING. Die verschiedenen Werte dieser Eigenschaft werden als unterschiedliche Einträge in der Dropdownliste angezeigt.
    
## <a name="remarks"></a>Hinweise

Eine **DTBLMVDDLBOX-Struktur** beschreibt eine mehrwertige Dropdownliste eine schreibgeschützte Liste von Elementen. Mithilfe einer mehrwertigen Dropdownliste werden Werte angezeigt, wenn ein Benutzer auf eine Bildlaufleiste klickt. 
  
Die angezeigten Daten stammen aus der Im **ulMVPropTag-Element identifizierten** Eigenschaft. Es ist nicht erforderlich, von der Eigenschaftenschnittstelle zu lesen, die der Anzeigetabelle zugeordnet ist. Da Benutzer keine Auswahl aus diesen Listenfeldern treffen können, werden daten nicht in die Eigenschaftsschnittstelle geschrieben. 
  
Für die mehrwertige Dropdownliste werden nur mehrwertige Zeichenfolgeneigenschaften unterstützt. Andere mehrwertige Eigenschaftstypen werden nicht unterstützt. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

