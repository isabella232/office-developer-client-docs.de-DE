---
title: PidTagOriginallyIntendedRecipEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7cfc47b62c9058d36a81daf24468b80c234c85ae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575001"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a>PidTagOriginallyIntendedRecipEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Eintragsbezeichner des ursprünglich vorgesehenen Empfängers einer automatisch weitergeleiteten Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_ENTRYID  <br/> |
|Kennung:  <br/> |0x1012  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist eine der Adresseigenschaften für den ursprünglich vorgesehenen Nachrichtenempfänger. Sie muss vom automatischen Agent festgelegt werden, der die Nachricht weitergeleitet hat.
  
Diese Eigenschaft entspricht dem X.400-Bericht pro Empfängerattribut.
  
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

