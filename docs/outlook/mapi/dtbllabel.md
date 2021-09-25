---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1f0bf5445404b80021350fa70c9b21c5bbbe73fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601100"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Beschriftung, die in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Members

 **ulbLpszLabelName**
  
> Position im Speicher der Zeichenfolgenbeschriftung.
    
 **ulFlags**
  
> Bitmaske mit Kennzeichen, die zum Festlegen des Formats der Bezeichnung verwendet werden, auf die der **UlbLpszLabelName-Member** verweist. Das folgende Kennzeichen kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Beschriftung hat das Unicode-Format. Wenn das MAPI_UNICODE-Kennzeichen nicht festgelegt ist, hat die Bezeichnung das ANSI-Format.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DTBLLABEL-Struktur** beschreibt einen Beschriftungssteuerelementtext, der mit einem anderen Steuerelementtyp angezeigt wird, um diesem Steuerelement Eine Bedeutung hinzuzufügen. Die meisten Bearbeitungssteuerelemente werden z. B. neben Bezeichnungen positioniert, um den Benutzer über den Typ der eingegebenen Informationen zu informieren. Einige Steuerelemente, z. B. Gruppenfelder und Optionsfelder, enthalten eigene Bezeichnungen. 
  
Die Bezeichnung kann eine Windows Zugriffstaste enthalten, die als Zeichen nach dem kaufmännischen Und-Zeichen ( ) identifiziert &amp; wird. Durch Drücken der Zugriffstaste wird der Fokus in das erste Nichtbeschriftungssteuerelement, das auf diese Bezeichnung in der Anzeigetabelle folgt, platziert.
  
Mehrzeilige Bezeichnungen werden nicht unterstützt. Das Anzeigen mehrerer Zeilen erfordert mehrere Beschriftungen.
  
Es ist nicht möglich, eine Bezeichnung als schreibgeschütztes Bearbeitungssteuerelement zu verwenden. Der Unterschied besteht darin, dass ein Bearbeitungssteuerelement ausgewählt und kopiert werden kann, während eine Bezeichnung nicht möglich ist. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

