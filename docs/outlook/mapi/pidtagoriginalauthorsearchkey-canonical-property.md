---
title: Kanonische Pidtagoriginalauthorsearchkey (-Eigenschaft
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
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a>Kanonische Pidtagoriginalauthorsearchkey (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Suchschlüssel des Autors der ersten Version einer Nachricht, also die Nachricht, bevor Sie weitergeleitet oder darauf geantwortet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_AUTHOR_SEARCH_KEY  <br/> |
|Kennung:  <br/> |0x0056  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist eine der Adresseigenschaften für den Autor einer Nachricht. Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert der **PR_SENDER_SEARCH_KEY**-[pidtagsendersearchkey (](pidtagsendersearchkey-canonical-property.md) -Eigenschaft festlegen. Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird. 
  
Die ursprünglichen Autoren Eigenschaften ermöglichen die Aufbewahrung von Informationen außerhalb der lokalen Messaging Domäne. Wenn eine Nachricht von einer anderen Messaging Domäne eingeht, beispielsweise aus dem Internet, bieten diese Eigenschaften eine Möglichkeit, um sicherzustellen, dass die ursprünglichen Informationen nicht verloren gehen.
  
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

