---
title: Kanonische Pidlidtodoordinaldate (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345276"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Kanonische Pidlidtodoordinaldate (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Sortierreihenfolge von Objekten in einer konsolidierten Aufgabenliste.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidToDoOrdinalDate  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long-ID (Deckel):  <br/> |0x000085A0  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn ein Objekt gekennzeichnet wird, sollte diese Eigenschaft auf die aktuelle Uhrzeit in koordinierter weltZeit (UTC) festgelegt werden. 
  
Wenn der Client es einem Benutzer ermöglicht, Vorgänge innerhalb der konsolidierten Aufgabenliste per Drag & Drop neu anordnen zu können, kann er einen beliebigen geeigneten Algorithmus verwenden, um den neuen Wert dieser Eigenschaft zu bestimmen, sodass die Aufgabe an der richtigen Stelle angezeigt wird, wenn diese Eigenschaft als Sor verwendet wird. Ting-Feld.
  
Wenn diese Eigenschaft verwendet wird, um Objekte und die Sortierergebnisse in einem tie zu sortieren, wird die **dispidToDoSubOrdinal** ([pidlidtodosubordinal (](pidlidtodosubordinal-canonical-property.md))-Eigenschaft als Tie-Breaker verwendet.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidlidtodosubordinal (-Eigenschaft](pidlidtodosubordinal-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

