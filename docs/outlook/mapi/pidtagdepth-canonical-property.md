---
title: PidTagDepth (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 75d390edd06aaf826f6b8c2d996e4e08bf6a7334
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384213"
---
# <a name="pidtagdepth-canonical-property"></a>PidTagDepth (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine ganze Zahl, die den relativen Einzug oder Tiefe der ein Objekt in einer Hierarchietabelle darstellt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEPTH  <br/> |
|Kennung:  <br/> |0x3005  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine MAPI  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann auch die Kategorisierungsebene einer Zeile in einer Inhaltstabelle oder die Ordnerhierarchie-Tiefe in einer Hierarchietabelle angeben. Die Tiefe ist nullbasiert, wobei 0 (null) die am weitesten links Kategorie darstellt. In allen Fällen stellt Wert der Eigenschaft um einen relativen Wert statt einen absoluten Wert dar. In der Hierarchietabelle befindet sich der Wert für die Tiefe beispielsweise relativ zu den Container, von dem die Hierarchietabelle abgerufen wurde. Die Tiefe stellt eine absolute Tiefe nicht aus dem Stammcontainer dar. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Zulässige Vorgänge für die Hauptobjekte-Tabelle enthält.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagObjectType (kanonische Eigenschaft)](pidtagobjecttype-canonical-property.md)
  
[PidTagSelectable (kanonische Eigenschaft)](pidtagselectable-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

