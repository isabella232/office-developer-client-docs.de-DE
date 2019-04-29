---
title: Kanonische Pidtagnonreceiptnotificationrequested (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0c6b56a786ea794587e140c9555cc88cd862b489
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419751"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a>Kanonische Pidtagnonreceiptnotificationrequested (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Nachrichtenabsender eine Benachrichtigung über den nicht Empfang eines bestimmten Empfängers wünscht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NON_RECEIPT_NOTIFICATION_REQUESTED  <br/> |
|Kennung:  <br/> |0x0C06  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft FALSE enthält und die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft true enthält, kann der Dienstanbieter die **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** -Eigenschaft überschreiben und eine Unzustellbarkeitsbericht. 
  
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

