---
title: PidTagCorrelate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4f1b039de0d61c4adbeea25b1d85a073c1a6370b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600274"
---
# <a name="pidtagcorrelate-canonical-property"></a>PidTagCorrelate (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn der Absender einer Nachricht das Korrelationsfeature des Messagingsystems anfordert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CORRELATE  <br/> |
|Kennung:  <br/> |0x0E0C  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird verwendet, um die Korrelation eingehender Berichte mit der ursprünglichen gesendeten Nachricht anzufordern. Wenn ein Transportanbieter auf eine gesendete Nachricht **trifft, deren PR_CORRELATE** auf TRUE festgelegt ist, wird die **eigenschaft PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) auf den MTS-Bezeichner (Message Transfer System) für diese Nachricht festgelegt.
  
 **PR_CORRELATE** sollten mit Messagingsystemen verwendet werden, die Korrelation durch MTS-Bezeichner unterstützen, z. B. X.400. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

