---
title: Kanonische Pidtagoriginallyintendedrecipemailaddress (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4a0e7325618a38addefe562c8207066dfea620f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342542"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a>Kanonische Pidtagoriginallyintendedrecipemailaddress (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die e-Mail-Adresse des ursprünglich vorgesehenen Empfängers einer AutoForwarded-Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W  <br/> |
|Kennung:  <br/> |0x007C  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den ursprünglich beabsichtigten Nachrichtenempfänger. Sie müssen vom automatischen Agent festgelegt werden, der die Nachricht weitergeleitet hat.
  
Diese Eigenschaften entsprechen dem Attribut X. 400 pro Empfänger.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

