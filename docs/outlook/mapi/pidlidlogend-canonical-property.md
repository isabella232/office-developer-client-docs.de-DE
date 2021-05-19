---
title: PidLidLogEnd (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336925"
---
# <a name="pidlidlogend-canonical-property"></a>PidLidLogEnd (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt das Enddatum und die Uhrzeit für die Journalnachricht dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidLogEnd  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Log  <br/> |
|Lange ID (LID):  <br/> |0x00008708  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Journal  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Zeitpunkt, zu dem die Aktivität in Coordinated Universal Time The (UTC) endete, der gleich der **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md))-Eigenschaft und größer als oder gleich der **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md))-Eigenschaft sein muss.
  
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

