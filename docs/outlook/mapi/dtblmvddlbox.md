---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 384282445e6f50fac3d440e4df3a4c8e61e0c8a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551667"
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
  
> Reserviert; muss Null sein.
    
 **ulMVPropTag**
  
> Eigenschaftstag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING. Die verschiedenen Werte dieser Eigenschaft werden als unterschiedliche Einträge in der Dropdownliste angezeigt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DTBLMVDDLBOX-Struktur** beschreibt eine mehrwertige Dropdownliste, eine schreibgeschützte Liste von Elementen. Mithilfe einer mehrwertigen Dropdownliste werden Werte angezeigt, wenn ein Benutzer auf eine Bildlaufleiste klickt. 
  
Die angezeigten Daten stammen aus der Im **ulMVPropTag-Element** identifizierten Eigenschaft. Es ist nicht erforderlich, von der Eigenschaftenschnittstelle zu lesen, die der Anzeigetabelle zugeordnet ist. Da Benutzer keine Auswahl aus diesen Arten von Listenfeldern treffen können, werden die Daten nicht in die Eigenschaftenschnittstelle geschrieben. 
  
Für die mehrwertige Dropdownliste werden nur mehrwertige Zeichenfolgeneigenschaften unterstützt. Andere mehrwertige Eigenschaftstypen werden nicht unterstützt. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

