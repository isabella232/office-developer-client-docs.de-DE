---
title: PidTagImplicitConversionProhibited (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e0983b6bcf2818699023420c4d864724db6cc9d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563455"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>PidTagImplicitConversionProhibited (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn einem Nachrichtenübertragungs-Agent (Message Transfer Agent, MTA) das Ausführen impliziter Nachrichtentextkonvertierungen untersagt ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|Kennung:  <br/> |0x0016  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Eigenschaft TRUE ist, darf das Messagingsystem keine Inhaltskonvertierung für die Nachricht ausführen, es sei denn, sie wird explizit auf Empfängerbasis mit der **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) -Eigenschaft angefordert.
  
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

