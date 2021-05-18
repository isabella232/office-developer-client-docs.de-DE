---
title: PidTagProviderUid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422775"
---
# <a name="pidtagprovideruid-canonical-property"></a>PidTagProviderUid (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine **MAPIUID-Struktur** des Dienstanbieters, der eine Nachricht behandeln soll. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROVIDER_UID  <br/> |
|Kennung:  <br/> |0x300C  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI allgemein  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird von allen Dienstanbietern berechnet. Sie enthält eine [MAPIUID-Struktur,](mapiuid.md) die dem Anbieter zugeordnet ist und in der Regel hart codiert wird. Sie wird in der Regel von einer Clientanwendung verwendet, die nur an den Adressbuchcontainern interessiert ist, die von einem bestimmten Anbieter bereitgestellt werden. 
  
Diese Eigenschaft wird nur als Spalteneintrag in der Anbietertabelle angezeigt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

