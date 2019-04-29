---
title: Kanonische Pidtagoriginalauthoremailaddress (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7918c5d5b585ffb199bfbc140edfb8286b499b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436167"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a>Kanonische Pidtagoriginalauthoremailaddress (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die e-Mail-Adresse des Autors der ersten Version einer Nachricht, also die Nachricht, bevor Sie weitergeleitet oder darauf geantwortet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W  <br/> |
|Kennung:  <br/> |0x007A  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Autor einer Nachricht. Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaften auf den Wert der **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))-Eigenschaft festlegen. Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.
  
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

