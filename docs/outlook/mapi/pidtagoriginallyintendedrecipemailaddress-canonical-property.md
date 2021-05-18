---
title: PidTagOriginallyIntendedRecipEmailAddress (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4a0e7325618a38addefe562c8207066dfea620f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411372"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a>PidTagOriginallyIntendedRecipEmailAddress (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die E-Mail-Adresse des ursprünglich beabsichtigten Empfängers einer automatisch weitergeleiteten Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W  <br/> |
|Kennung:  <br/> |0x007C  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den ursprünglich beabsichtigten Nachrichtenempfänger. Sie müssen vom automatischen Agent festgelegt werden, der die Nachricht weitergeleitet hat.
  
Diese Eigenschaften entsprechen dem X.400-Bericht pro Empfängerattribut.
  
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

