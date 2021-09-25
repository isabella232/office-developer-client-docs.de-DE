---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fd1f8d3f62893586f7ca3c06459a0dee149ea055
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601093"
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
  
> Reserviert; muss Null sein.
    
 **ulMVPropTag**
  
> Eigenschaftstag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DTBLMVLISTBOX-Struktur** beschreibt eine standardmäßige mehrwertige Liste mit einer schreibgeschützten Liste von Elementen. Mithilfe einer standardmäßigen mehrwertigen Liste werden die Werte sofort angezeigt. 
  
Die angezeigten Daten stammen aus der Im **ulMVPropTag-Element** identifizierten Eigenschaft. Es ist nicht erforderlich, von der Eigenschaftenschnittstelle zu lesen, die der Anzeigetabelle zugeordnet ist. Da Benutzer keine Auswahl aus diesen Listentypen treffen können, werden daten nicht in die Eigenschaftenschnittstelle geschrieben. 
  
Für die mehrwertige Liste werden nur mehrwertige Zeichenfolgeneigenschaften unterstützt. Andere mehrwertige Eigenschaftstypen werden nicht unterstützt. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

