---
title: PidTagRequestedDeliveryMethod (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b7ba30b299d76f3a19464d5cba1a791ad115dc7e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570889"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a>PidTagRequestedDeliveryMethod (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält ein binäres Array von Übermittlungsmethoden (Dienstanbieter) in der Reihenfolge der Einstellung eines Nachrichtensenders.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REQUESTED_DELIVERY_METHOD  <br/> |
|Kennung:  <br/> |0x0C18  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das in dieser Eigenschaft enthaltene Array besteht aus ASN.1-Bezeichnern für jeden Dienstanbieter.
  
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

