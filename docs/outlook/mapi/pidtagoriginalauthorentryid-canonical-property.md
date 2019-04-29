---
title: Kanonische PidTagOriginalAuthorEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 866c28bc08f669d18487c99c9a13bc7347b605fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425589"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a>Kanonische PidTagOriginalAuthorEntryId-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID des Autors der ersten Version einer Nachricht, also der Nachricht, bevor Sie weitergeleitet oder darauf geantwortet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_AUTHOR_ENTRYID  <br/> |
|Kennung:  <br/> |0x004C  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist eine der Adresseigenschaften für den Autor einer Nachricht. Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert von **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) festlegen. Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird. 
  
Die ursprüngliche Author-Eigenschaft ermöglicht die Aufbewahrung von Informationen außerhalb der lokalen Messaging Domäne. Wenn eine Nachricht von einer anderen Messaging Domäne eingeht, beispielsweise aus dem Internet, bietet diese Eigenschaft eine Möglichkeit, um sicherzustellen, dass die ursprünglichen Informationen nicht verloren gehen.
  
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

