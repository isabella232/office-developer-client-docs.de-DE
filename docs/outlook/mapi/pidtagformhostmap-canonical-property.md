---
title: PidTagFormHostMap (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a8c7869e6bcfc926e071b386cc70f446b537ac28
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587678"
---
# <a name="pidtagformhostmap-canonical-property"></a>PidTagFormHostMap (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Hostzuordnung der verfügbaren Formulare. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_FORM_HOST_MAP  <br/> |
|Kennung:  <br/> |0x3306  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |ALLGEMEINE MAPI  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Eine Clientanwendung sollte diese Eigenschaft zusammen mit der **eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) aktualisieren, wenn die zugrunde liegende Struktur in der **IMAPIFormProp-Schnittstelle** geändert wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

