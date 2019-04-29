---
title: Kanonische Pidtagoriginatorrequestedalternaterecipient (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 45cd0e8a95f908d7ef56d03b3ecab5d5df5bcae1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437861"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a>Kanonische Pidtagoriginatorrequestedalternaterecipient (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Eintrags-ID für einen vom Absender angegebenen alternativen Empfänger.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT  <br/> |
|Kennung:  <br/> |0x0C09  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird in Nachrichten mit Auto Weiterleitung verwendet. Wenn die Auto Weiterleitung nicht zulässig ist oder kein alternativer Empfänger festgelegt wurde, sollte ein Unzustellbarkeitsbericht generiert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

