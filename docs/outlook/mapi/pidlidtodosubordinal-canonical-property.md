---
title: Kanonische Pidlidtodosubordinal (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c4ea125a5bde89e0885be4c04e3f106f202b1e18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344919"
---
# <a name="pidlidtodosubordinal-canonical-property"></a>Kanonische Pidlidtodosubordinal (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fungiert als Tie-Breaker, wenn die **dispidToDoOrdinalDate** ([pidlidtodoordinaldate (](pidlidtodoordinaldate-canonical-property.md))-Eigenschaft Objekte und das Ergebnis in einem Unentschieden sortiert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidToDoSubOrdinal  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long-ID (Deckel):  <br/> |0x000085A1  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft verwendet wird, muss Sie lexikografisch sortiert werden. Die Komponentenzeichen der Zeichenfolge müssen nur aus den Ziffern 0 bis 9 bestehen. Diese Eigenschaft sollte anfänglich auf "5555555" festgelegt werden. Die Länge dieser Eigenschaft darf 254 Zeichen nicht überschreiten (ohne das abschließende NULL-Zeichen).
  
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



[Kanonische Pidlidtodoordinaldate (-Eigenschaft](pidlidtodoordinaldate-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

