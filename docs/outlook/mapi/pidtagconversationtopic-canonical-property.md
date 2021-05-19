---
title: PidTagConversationTopic (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334685"
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
   
## <a name="remarks"></a>Hinweise

Ein Unterhaltungsthread stellt eine Reihe von Nachrichten und Antworten dar. Diese Eigenschaften werden für die erste Nachricht in einem Thread festgelegt, in der Regel auf die **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) -Eigenschaft. Nachfolgende Nachrichten im Thread sollten dasselbe Thema ohne Änderung verwenden. 
  
Die **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) gibt die Reihenfolgenbeziehung zwischen nachfolgenden Nachrichten und Antworten an. Die Verwendung ist optional, auch wenn diese Eigenschaften festgelegt sind. 
  
Ein Nachrichtenspeicheranbieter kann sichergehen, dass diese Eigenschaften immer für ein- oder ausgehende Nachrichten festgelegt sind. Wenn diese Eigenschaften bereits festgelegt sind, sollten sie nicht geändert werden. Andern falls nicht, können sie auf **PR_NORMALIZED_SUBJECT.** Es sollten alle Aktionen ausgeführt werden, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

