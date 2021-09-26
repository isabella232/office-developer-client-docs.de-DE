---
title: Kanonische PidTagConversationIndex-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 496af697274a4c534335040d7ade531d5d5e05c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583485"
---
# <a name="pidtagconversationindex-canonical-property"></a>Kanonische PidTagConversationIndex-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen binären Wert, der die relative Position dieser Nachricht innerhalb eines Unterhaltungsthreads angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Kennung:  <br/> |0x0071  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ein Unterhaltungsthread stellt eine Reihe von Nachrichten und Antworten dar. Diese Eigenschaft wird in der Regel mithilfe verketteter Zeitstempelwerte implementiert. Die Verwendung ist optional, auch wenn **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) festgelegt ist. 
  
MAPI stellt die [ScCreateConversationIndex-Funktion](sccreateconversationindex.md) zum Erstellen oder Aktualisieren eines Unterhaltungsindex bereit. Die Funktion verwendet den aktuellen Indexwert als Bytearray mit Zählung und gibt den Indexwert zurück, wobei ein Zeitstempel am Ende verkettet ist. Eine Nachricht, die eine Antwort auf eine andere Nachricht darstellt, sollte **ScCreateConversationIndex** verwenden, um diese Eigenschaft zu aktualisieren. 
  
Ein Nachrichtenspeicheranbieter hat die Möglichkeit, sicherzustellen, dass **PR_CONVERSATION_INDEX** immer für ein- oder ausgehende Nachrichten festgelegt wird. Dazu kann **ScCreateConversationIndex** aufgerufen werden, entweder mit dem vorhandenen Wert, wenn diese Eigenschaft festgelegt ist, oder mit NULL, wenn dies nicht der Fall ist. Diese Aktion sollte ausgeführt werden, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird. 
  
Alle Nachrichten, die denselben Wert für **PR_CONVERSATION_TOPIC** haben, können nach dieser Eigenschaft sortiert werden, um die hierarchische Beziehung der Nachrichten anzuzeigen. 
  
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

