---
title: PidTagOrdinalMost (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 31f39cfbd0e993bfc28003fd64e8af97e7e76818
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329187"
---
# <a name="pidtagordinalmost-canonical-property"></a>PidTagOrdinalMost (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine positive Zahl, deren negativer Wert kleiner oder gleich dem Wert der **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md))-Eigenschaft aller Vorgänge im Ordner ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORDINAL_MOST  <br/> |
|Kennung:  <br/> |0x36E2  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft muss aktualisiert werden, um diese Bedingung zu erhalten, wenn sich die **dispidTaskOrdinal-Eigenschaft** eines Aufgabenobjekts im Ordner so ändert, dass die Bedingung verletzt würde. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
  
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

