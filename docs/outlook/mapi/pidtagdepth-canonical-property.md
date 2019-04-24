---
title: Kanonische Pidtagdepth (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 75d390edd06aaf826f6b8c2d996e4e08bf6a7334
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360851"
---
# <a name="pidtagdepth-canonical-property"></a>Kanonische Pidtagdepth (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine ganze Zahl, die die relative Ebene der Einrückung oder Tiefe eines Objekts in einer Hierarchietabelle darstellt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEPTH  <br/> |
|Kennung:  <br/> |0x3005  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI allgemein  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann auch die Kategorisierungs Ebene einer Zeile in einer Inhaltstabelle oder die Hierarchietiefe in einer Hierarchietabelle angeben. Die Tiefe ist nullbasiert, wobei Null die äußerste linke Kategorie darstellt. In allen Fällen stellt der Eigenschaftswert einen relativen Wert anstelle eines absoluten Werts dar. In der Hierarchietabelle ist der tiefen Wert beispielsweise relativ zu dem Container, aus dem die Hierarchietabelle abgerufen wurde. Die Tiefe stellt keine absolute Tiefe aus dem Stammcontainer dar. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Enthält zulässige Vorgänge für die Haupttabellen Objekte.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagobjecttype (-Eigenschaft](pidtagobjecttype-canonical-property.md)
  
[Kanonische Pidtagselectable (-Eigenschaft](pidtagselectable-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

