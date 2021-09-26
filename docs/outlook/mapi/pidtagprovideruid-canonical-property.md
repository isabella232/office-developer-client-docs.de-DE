---
title: Kanonische PidTagProviderUid-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 95d42bd6889ca2c8630e2240767a241142aa92d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583247"
---
# <a name="pidtagprovideruid-canonical-property"></a>Kanonische PidTagProviderUid-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine **MAPIUID-Struktur** des Dienstanbieters, der eine Nachricht verarbeitet. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROVIDER_UID  <br/> |
|Kennung:  <br/> |0x300C  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ALLGEMEINE MAPI  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird von allen Dienstanbietern berechnet. Es enthält eine [MAPIUID-Struktur,](mapiuid.md) die dem Anbieter zugeordnet und in der Regel hartcodiert ist. Es wird in der Regel von einer Clientanwendung verwendet, die nur an den von einem bestimmten Anbieter bereitgestellten Adressbuchcontainern interessiert ist. 
  
Diese Eigenschaft wird nur als Spalteneintrag in der Anbietertabelle angezeigt.
  
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

