---
title: PidTagEndDate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEndDate
api_type:
- HeaderDef
ms.assetid: d7ec5c79-1287-4364-b5e5-5d1d6f0ea0f1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2688e1764b6e4e31a47aeee306987caa66c709a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361061"
---
# <a name="pidtagenddate-canonical-property"></a>PidTagEndDate (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält das Enddatum und die Uhrzeit eines Termins, wie von einer Planungsanwendung verwaltet. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_END_DATE  <br/> |
|Kennung:  <br/> |0x0061  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Hinweise

Planungsanwendungen sollten sowohl die PR_START_DATE **(** [PidTagStartDate](pidtagstartdate-canonical-property.md)) als auch diese Eigenschaft beim Senden von Besprechungsanfragen festlegen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

