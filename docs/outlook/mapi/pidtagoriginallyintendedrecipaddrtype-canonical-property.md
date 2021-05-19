---
title: PidTagOriginallyIntendedRecipAddrtype (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipAddrtype
api_type:
- COM
ms.assetid: dcfb6bd5-bff5-4a50-aec7-4bdfdabf7631
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a826f1bdf150b42b61a61b2f53870e9f170e0777
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416090"
---
# <a name="pidtagoriginallyintendedrecipaddrtype-canonical-property"></a>PidTagOriginallyIntendedRecipAddrtype (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Adresstyp des ursprünglich beabsichtigten Empfängers einer automatisch weitergeleiteten Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE, PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_A, PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_W  <br/> |
|Kennung:  <br/> |0x007B  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften sind eine der Adresseigenschaften für den ursprünglich beabsichtigten Nachrichtenempfänger. Sie muss vom automatischen Agent festgelegt werden, der die Nachricht weitergeleitet hat.
  
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

