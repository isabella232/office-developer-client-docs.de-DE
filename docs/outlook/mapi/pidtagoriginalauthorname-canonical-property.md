---
title: Kanonische Pidtagoriginalauthorname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bb62f3a44c9f17070db969683891fb2e2d62eb5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355776"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a>Kanonische Pidtagoriginalauthorname (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Anzeigenamen des Autors der ersten Version einer Nachricht, also die Nachricht, bevor Sie weitergeleitet oder darauf geantwortet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W  <br/> |
|Kennung:  <br/> |0x004D  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |E-Mail  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Autor einer Nachricht. Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaften auf den Wert von **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) festlegen. Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.
  
Die ursprünglichen Autoren Eigenschaften ermöglichen die Aufbewahrung von Informationen außerhalb der lokalen Messaging Domäne. Wenn eine Nachricht von einer anderen Messaging Domäne eingeht, beispielsweise aus dem Internet, bieten diese Eigenschaften eine Möglichkeit, um sicherzustellen, dass die ursprünglichen Informationen nicht verloren gehen.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagDisplayName-Eigenschaft](pidtagdisplayname-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

