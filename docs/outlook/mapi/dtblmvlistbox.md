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
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439702"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine mehrwertige Liste, die in einem Dialogfeld angezeigt wird, das aus einer Anzeigetabelle erstellt wird.
  
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
  
> Reserviert; muss null sein.
    
 **ulMVPropTag**
  
> Eigenschaftstag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING.
    
## <a name="remarks"></a>Hinweise

Eine **DTBLMVLISTBOX-Struktur** beschreibt eine standardmäßige mehrwertige Liste mit einer schreibgeschützten Liste von Elementen. Mithilfe einer mehrwertigen Standardliste werden die Werte sofort angezeigt. 
  
Die angezeigten Daten stammen aus der Im **ulMVPropTag-Element identifizierten** Eigenschaft. Es ist nicht erforderlich, von der Eigenschaftenschnittstelle zu lesen, die der Anzeigetabelle zugeordnet ist. Da Benutzer keine Auswahl aus diesen Listentypen treffen können, werden daten nicht in die Eigenschaftsschnittstelle geschrieben. 
  
Für die mehrwertige Liste werden nur mehrwertige Zeichenfolgeneigenschaften unterstützt. Andere mehrwertige Eigenschaftstypen werden nicht unterstützt. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

