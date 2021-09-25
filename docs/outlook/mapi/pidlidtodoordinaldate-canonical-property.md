---
title: Kanonische PidLidToDoOrdinalDate-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f91759f10909190a88a35b8841ee51950cf4c44e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620289"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Kanonische PidLidToDoOrdinalDate-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Sortierreihenfolge von Objekten in einer konsolidierten Aufgabenliste.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidToDoOrdinalDate  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085A0  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Vorgang  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn ein Objekt gekennzeichnet ist, sollte diese Eigenschaft auf die aktuelle Uhrzeit in koordinierter Weltzeit (COORDINATED Universal Time, UTC) festgelegt werden. 
  
Wenn der Client einem Benutzer ermöglicht, Aufgaben innerhalb der konsolidierten Aufgabenliste durch Ziehen oder andere Mechanismen neu anzuordnen, kann er einen geeigneten Algorithmus verwenden, um den neuen Wert dieser Eigenschaft zu bestimmen, sodass die Aufgabe an der richtigen Stelle angezeigt wird, wenn diese Eigenschaft als Sortierfeld verwendet wird.
  
Wenn diese Eigenschaft zum Sortieren von Objekten verwendet wird und die Sortierung zu einer Gleichung führt, wird die **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) -Eigenschaft als Tie breaker verwendet.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[PidLidToDoSubOrdinal (kanonische Eigenschaft)](pidlidtodosubordinal-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

