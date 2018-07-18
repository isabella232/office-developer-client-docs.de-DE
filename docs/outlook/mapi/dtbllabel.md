---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 28f6471f74fb0fcc4f7e2f4114f0790e1564e17e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791610"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**Betrifft**: Outlook 
  
Beschreibt eine Beschriftung, die in einem Dialogfeld verwendet werden, die aus einer Tabelle anzeigen erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makro  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Elemente

 **ulbLpszLabelName**
  
> Die Position im Speicher der Beschriftung Zeichenfolge Zeichen.
    
 **ulFlags**
  
> Bitmaske aus Flags verwendet, um das Format der Beschriftung festzulegen, auf die der **UlbLpszLabelName** Member. Das folgende Flag kann festgelegt werden: 
    
PARAMETER MAPI_UNICODE 
  
> Die Beschriftung wird im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
## <a name="remarks"></a>Bemerkungen

Eine Struktur **DTBLLABEL** beschreibt einen Text im Bezeichnungsfeld-Steuerelement, der mit einer anderen Art von Steuerelement, das das Steuerelement Bedeutung hinzugefügt angezeigt wird. Beispielsweise sind die meisten Bearbeitungssteuerelemente neben Etiketten informiert den Benutzer über den Typ der Informationen eingegeben werden positioniert. Einige Steuerelemente, wie zum Beispiel Gruppenfelder und Optionsfelder, halten Sie ihre eigenen Beschriftungen. 
  
Die Bezeichnung kann einen Windows Accelerator, als das kaufmännische und-Zeichen folgende Zeichen enthalten (&amp;). Drücken der Zugriffstaste erhält den Fokus in der ersten Nonlabel, Nonbutton Steuerelement Befolgen dieser Beschriftung in der Tabelle anzeigen.
  
Keine Unterstützung für mehrzeilige Etiketten ist vorhanden. Zeigt mehrere Zeilen erfordert mehrere Beschriftungen.
  
Es ist nicht möglich, eine Beschriftung als einen schreibgeschützten Bearbeitungssteuerelement verwenden. Der Unterschied besteht darin, dass ein Edit-Steuerelement ausgewählt und während eine Bezeichnung kann nicht kopiert werden kann. 
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

