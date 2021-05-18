---
title: PidTagCorrelate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea217808a163c7f16bbaa3c5a959fd32c8cbe10c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405219"
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
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird zum Anfordern der Korrelation eingehender Berichte mit der ursprünglich gesendeten Nachricht verwendet. Wenn ein Transportanbieter auf eine übermittelte Nachricht mit **PR_CORRELATE** true trifft, legt er die **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) -Eigenschaft auf den #A0 (Message Transfer System) für diese Nachricht fest.
  
 **PR_CORRELATE** sollten mit Messagingsystemen verwendet werden, die die Korrelation durch den MTS-Bezeichner unterstützen, z. B. X.400. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

