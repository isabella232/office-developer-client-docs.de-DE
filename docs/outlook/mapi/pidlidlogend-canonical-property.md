---
title: Kanonische PidLidLogEnd-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3c8445e3fcec1c3fe7be91ba16ba4cd7395d526e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583779"
---
# <a name="pidlidlogend-canonical-property"></a>Kanonische PidLidLogEnd-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt das Enddatum und die Endzeit für die Journalnachricht dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidLogEnd  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Log  <br/> |
|Long ID (LID):  <br/> |0x00008708  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Journal  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Uhrzeit, zu der die Aktivität in koordinierter Weltzeit (COORDINATED Universal Time, UTC) endete, die der **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) -Eigenschaft und größer als oder gleich **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) -Eigenschaft sein muss.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Diebe zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

