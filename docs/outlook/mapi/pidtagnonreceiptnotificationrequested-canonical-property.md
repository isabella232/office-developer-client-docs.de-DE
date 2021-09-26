---
title: PidTagNonReceiptNotificationRequested (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1c355489d927920d5d1e058f2e8b96c2915830dd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629722"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a>PidTagNonReceiptNotificationRequested (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Nachrichtensender eine Benachrichtigung über den Nicht-Empfang für einen angegebenen Empfänger erhalten möchte.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NON_RECEIPT_NOTIFICATION_REQUESTED  <br/> |
|Kennung:  <br/> |0x0C06  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft FALSE enthält und die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) -Eigenschaft TRUE enthält, kann der Dienstanbieter die **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** Eigenschaft überschreiben und einen Unzustellbarkeitsbericht generieren. 
  
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

