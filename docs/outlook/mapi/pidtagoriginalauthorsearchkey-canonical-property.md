---
title: PidTagOriginalAuthorSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 09331e1201b6f6e45bb9e26e618ee59e67efbf8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409580"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a>PidTagOriginalAuthorSearchKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Suchschlüssel des Autors der ersten Version einer Nachricht, d. h. die Nachricht, bevor sie weitergeleitet oder beantwortet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_AUTHOR_SEARCH_KEY  <br/> |
|Kennung:  <br/> |0x0056  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist eine der Adresseigenschaften für den Autor einer Nachricht. Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert der **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey-Eigenschaft](pidtagsendersearchkey-canonical-property.md) festlegen. Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird. 
  
Die ursprünglichen Autoreneigenschaften ermöglichen die Aufbewahrung von Informationen außerhalb der lokalen Messagingdomäne. Wenn eine Nachricht von einer anderen Messagingdomäne, z. B. aus dem Internet, eintrifft, stellen diese Eigenschaften eine Möglichkeit zur Verfügung, um sicherzustellen, dass ursprüngliche Informationen nicht verloren gehen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

