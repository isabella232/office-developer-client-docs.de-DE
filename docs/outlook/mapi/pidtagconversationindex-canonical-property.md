---
title: PidTagConversationIndex (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334720"
---
# <a name="pidtagconversationindex-canonical-property"></a>PidTagConversationIndex (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen binären Wert, der die relative Position dieser Nachricht in einem Unterhaltungsthread angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Kennung:  <br/> |0x0071  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Unterhaltungsthread stellt eine Reihe von Nachrichten und Antworten dar. Diese Eigenschaft wird in der Regel mit verkettten Zeitstempelwerten implementiert. Die Verwendung ist optional, auch **wenn PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) festgelegt ist. 
  
MAPI bietet die [ScCreateConversationIndex-Funktion](sccreateconversationindex.md) zum Erstellen oder Aktualisieren eines Unterhaltungsindex. Die Funktion verwendet den aktuellen Indexwert als gezähltes Bytearray und gibt den Indexwert mit einem Zeitstempel zurück, der am Ende verkettt ist. Eine Nachricht, die eine Antwort auf eine andere Nachricht darstellt, sollte **ScCreateConversationIndex** verwenden, um diese Eigenschaft zu aktualisieren. 
  
Ein Nachrichtenspeicheranbieter hat die Möglichkeit,  zu PR_CONVERSATION_INDEX ein- oder ausgehenden Nachrichten immer festgelegt ist. Dazu ruft sie **ScCreateConversationIndex** auf, entweder mit dem vorhandenen Wert, wenn diese Eigenschaft festgelegt ist, oder mit NULL, falls nicht. Diese Aktion sollte ausgeführt werden, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird. 
  
Alle Nachrichten mit demselben  Wert für PR_CONVERSATION_TOPIC können für diese Eigenschaft sortiert werden, um die hierarchische Beziehung der Nachrichten zu zeigen. 
  
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

