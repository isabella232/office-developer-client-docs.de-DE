---
title: PidTagDeliverTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6e604a385d45ed9647182ed6329ad448238569bd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613512"
---
# <a name="pidtagdelivertime-canonical-property"></a>PidTagDeliverTime (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält das Datum und die Uhrzeit der Zustellung der ursprünglichen Nachricht. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DELIVER_TIME  <br/> |
|Kennung:  <br/> |0x0010  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist eine Eigenschaft pro Empfänger in einem Übermittlungsbericht, die den Zeitpunkt angibt, zu dem die ursprüngliche Nachricht an den Nachrichtenbenutzer übermittelt wurde, für den der Übermittlungsbericht generiert wird.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

