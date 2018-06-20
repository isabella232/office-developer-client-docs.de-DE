---
title: Kanonische PidLidToDoOrdinalDate-Eigenschaft
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
ms.openlocfilehash: d708424ccb15be15746fe8a33eea73a8e0f99323
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793876"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Kanonische PidLidToDoOrdinalDate-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Bestimmt die Sortierreihenfolge der Objekte in einer konsolidierten Aufgabenliste.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidToDoOrdinalDate  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x000085A0  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn ein Objekt gekennzeichnet ist, muss diese Eigenschaft auf die aktuelle Zeit in koordinierter Weltzeit (UTC) festgelegt werden. 
  
Wenn der Client Benutzern das Neuanordnen von Aufgaben in der konsolidierten Aufgabenliste ermöglicht durch Ziehen oder andere Mechanismen, können sie alle geeigneten Algorithmus Sie den neuen Wert dieser Eigenschaft ermitteln, damit die Aufgabe an der richtigen Stelle angezeigt wird, wenn diese Eigenschaft als ein Sor verwendet wird Ting dar.
  
Wenn diese Eigenschaft sortiert Objekte und die Ergebnisse in einer Gleichwertigkeit Sortieren verwendet wird, wird die Eigenschaft **DispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) als eine Tie wörtertrennung verwendet.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidLidToDoSubOrdinal-Eigenschaft](pidlidtodosubordinal-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

