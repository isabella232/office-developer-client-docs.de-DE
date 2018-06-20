---
title: Kanonische PidTagNonReceiptNotificationRequested-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 80c76242df409dbea1b60e423629b5b219e1d57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794644"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a>Kanonische PidTagNonReceiptNotificationRequested-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält True, wenn der Absender einer Nachricht nicht Eingang nach einem bestimmten Empfänger möchte.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_NON_RECEIPT_NOTIFICATION_REQUESTED  <br/> |
|Bezeichner:  <br/> |0x0C06  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft FALSE enthält und die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft TRUE enthält, der Dienstanbieter überschreiben Sie die Eigenschaft **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** und generieren kann ein Unzustellbarkeitsbericht. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

