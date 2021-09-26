---
title: PidTagOriginalAuthorEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3e3daf06c5d7e7d647003774a8f284097cfcc5be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629721"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a>PidTagOriginalAuthorEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Eintragsbezeichner des Autors der ersten Version einer Nachricht, d. h. die Nachricht, bevor sie weitergeleitet oder beantwortet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_AUTHOR_ENTRYID  <br/> |
|Kennung:  <br/> |0x004C  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist eine der Adresseigenschaften für den Autor einer Nachricht. Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) festlegen. Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird. 
  
Die ursprüngliche Author-Eigenschaft ermöglicht die Aufbewahrung von Informationen von außerhalb der lokalen Messaging-Domäne. Wenn eine Nachricht von einer anderen Messagingdomäne eingeht, z. B. aus dem Internet, bietet diese Eigenschaft eine Möglichkeit, sicherzustellen, dass ursprüngliche Informationen nicht verloren gehen.
  
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

