---
title: Kanonische Pidtagrequesteddeliverymethod (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ecfed5684ba2166c1c00c1fd07fa074b4ce9fd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434074"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a>Kanonische Pidtagrequesteddeliverymethod (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält ein binäres Array von Übermittlungsmethoden (Dienstanbieter) in der Reihenfolge, in der die Einstellung des Nachrichtenabsenders festgelegt ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REQUESTED_DELIVERY_METHOD  <br/> |
|Kennung:  <br/> |0x0C18  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das in dieser Eigenschaft enthaltene Array besteht aus ASN. 1-Bezeichnern für jeden Dienstanbieter.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

