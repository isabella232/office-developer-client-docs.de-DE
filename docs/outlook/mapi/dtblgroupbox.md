---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ef38893c9ad44556cc9220809b5e407f86fd2642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576316"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Gruppenfeld-Steuerelement, das in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makro:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Elemente

 **ulbLpszLabel**
  
> Die Position im Speicher der Zeichenfolge, die das Gruppenfeld begleitet. Wenn angezeigt wird, wird diese auf der oberen, linken Seite des Felds angezeigt.
    
 **ulFlags**
  
> Bitmaske aus Flags verwendet, um das Format der Beschriftung festzulegen, auf die der **UlbLpszLabel** Member. Das folgende Flag kann festgelegt werden: 
    
PARAMETER MAPI_UNICODE 
  
> Die Beschriftung wird im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Struktur **DTBLGROUPBOX** beschreibt ein Gruppenfeld-Steuerelement, das verwendet wird, um andere Steuerelemente im Dialogfeld visuell zuzuordnen. Das Hervorheben Verfahren besteht im angrenzenden die andere Steuerelemente als Feld. 
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

