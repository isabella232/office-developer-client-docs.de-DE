---
title: PidLidLogDuration (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f25c1a72882f9236d56532b7259f51512734945
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336918"
---
# <a name="pidlidlogduration-canonical-property"></a>PidLidLogDuration (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt die Dauer einer Journalnachricht in Minuten dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidLogDuration  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Log  <br/> |
|Lange ID (LID):  <br/> |0x00008707  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Journal  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Dauer der Aktivität in Minuten, die der Unterschied zwischen den **Eigenschaften dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) und **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) sein muss.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Journale zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

