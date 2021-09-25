---
title: PidTagOriginatorCertificate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginatorCertificate
api_type:
- COM
ms.assetid: 65f890d8-9d25-408e-ab29-89991278b92d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 28c3c0b1f9da2c456f1d76c1471ea11d8ae85426
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574938"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a>PidTagOriginatorCertificate (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein ASN.1-Zertifikat für den Nachrichtenursprungsgeber.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINATOR_CERTIFICATE  <br/> |
|Kennung:  <br/> |0x0022  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist eine Kopie der **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) -Eigenschaft des Absenders.
  
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

