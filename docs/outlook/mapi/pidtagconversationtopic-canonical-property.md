---
title: Kanonische Eigenschaftpidtagconversationtopic-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2e656679fcf76992ec0b648274bd5ffa673b4007
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794259"
---
# <a name="pidtagconversationtopic-canonical-property"></a>Kanonische Eigenschaftpidtagconversationtopic-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Das Thema der ersten Nachricht in einer Unterhaltung Thread enthält. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W  <br/> |
|Bezeichner:  <br/> |0x0070  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Eine Unterhaltungsthreads stellt eine Reihe von Nachrichten und Antworten. Diese Eigenschaften werden für die erste Nachricht in einem Thread, in der Regel an die **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))-Eigenschaft festgelegt. Nachfolgende Nachrichten im Thread sollte im gleiche Thema ohne Änderung verwendet werden. 
  
Die **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))-Eigenschaft gibt die Reihenfolge Beziehung zwischen nachfolgenden Nachrichten und Antworten an. Die Verwendung ist optional, auch wenn diese Eigenschaften festgelegt sind. 
  
Eine Nachricht Speicheranbieter hat die Möglichkeit der Sicherstellung der, die diese Eigenschaften immer für eingehende und ausgehende Nachrichten festgelegt werden. Wenn diese Eigenschaften sind bereits festgelegten sollten sie nicht geändert werden. Wenn dies nicht der Fall ist, können **PR_NORMALIZED_SUBJECT**festgelegt werden. Maßnahmen sollten getroffen werden, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

