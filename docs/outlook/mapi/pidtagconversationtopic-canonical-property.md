---
title: PidTagConversationTopic (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f49bc6988ff7f7f06c22882e19d54dde6af44ce0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583512"
---
# <a name="pidtagconversationtopic-canonical-property"></a>PidTagConversationTopic (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält das Thema der ersten Nachricht in einem Unterhaltungsthread. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W  <br/> |
|Kennung:  <br/> |0x0070  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ein Unterhaltungsthread stellt eine Reihe von Nachrichten und Antworten dar. Diese Eigenschaften werden für die erste Nachricht in einem Thread festgelegt, in der Regel auf die **eigenschaft PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)). Nachfolgende Nachrichten im Thread sollten dasselbe Thema ohne Änderung verwenden. 
  
Die **eigenschaft PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) gibt die Reihenfolgenbeziehung zwischen nachfolgenden Nachrichten und Antworten an. Die Verwendung ist optional, auch wenn diese Eigenschaften festgelegt sind. 
  
Ein Nachrichtenspeicheranbieter hat die Möglichkeit, sicherzustellen, dass diese Eigenschaften immer für eingehende oder ausgehende Nachrichten festgelegt werden. Wenn diese Eigenschaften bereits festgelegt sind, sollten sie nicht geändert werden. Wenn nicht, können sie auf **PR_NORMALIZED_SUBJECT** festgelegt werden. Jede Aktion sollte ausgeführt werden, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
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

